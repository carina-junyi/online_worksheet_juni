import React, { useState, useEffect } from 'react';
import { CheckCircle, HelpCircle, ArrowRight, RefreshCw, BookOpen, Star, AlertCircle, Info, ChevronRight, Rocket, Send } from 'lucide-react';

const App = () => {
  // 練習 1 的題目狀態
  const [q1Index, setQ1Index] = useState(0);
  const [practiceStep, setPracticeStep] = useState(1);
  const [userInput, setUserInput] = useState("");
  const [feedback, setFeedback] = useState({ show: false, message: '', type: '' });

  // 練習 2 的題目狀態（隨機順序）
  const [shuffledPairs, setShuffledPairs] = useState([]);
  const [matchingAnswers, setMatchingAnswers] = useState({});

  // 實戰挑戰狀態
  const [challengeAnswers, setChallengeAnswers] = useState({ a: "", b: "", c: "" });
  const [challengeFeedback, setChallengeFeedback] = useState(null);

  const questions1 = [
    {
      num: 48,
      steps: [2, 2, 2, 2],
      results: [24, 12, 6, 3],
      final: "2⁴ × 3"
    },
    {
      num: 60,
      steps: [2, 2, 3],
      results: [30, 15, 5],
      final: "2² × 3 × 5"
    },
    {
      num: 90,
      steps: [2, 3, 3],
      results: [45, 15, 5],
      final: "2 × 3² × 5"
    }
  ];

  const matchingPairs = [
    { num: 36, formula: '2² × 3²', label: 'A' },
    { num: 45, formula: '3² × 5', label: 'B' },
    { num: 50, formula: '2 × 5²', label: 'C' },
    { num: 84, formula: '2² × 3 × 7', label: 'D' }
  ];

  useEffect(() => {
    shuffleMatching();
  }, []);

  const shuffleMatching = () => {
    const shuffled = [...matchingPairs].sort(() => Math.random() - 0.5);
    setShuffledPairs(shuffled);
    setMatchingAnswers({});
  };

  const handlePractice1 = (val) => {
    const input = parseInt(val);
    const currentQ = questions1[q1Index];
    const targetDivisor = currentQ.steps[practiceStep - 1];

    if (input === targetDivisor) {
      const nextResult = currentQ.results[practiceStep - 1];
      setFeedback({ 
        show: true, 
        message: `✅ 正確！除以 ${input} 得到 ${nextResult}。`, 
        type: 'success' 
      });
      setPracticeStep(practiceStep + 1);
    } else {
      setFeedback({ 
        show: true, 
        message: `❌ 再想一下，建議從最小的質因數開始除喔！`, 
        type: 'error' 
      });
    }
    setUserInput("");
  };

  const nextQuestion1 = () => {
    if (q1Index < questions1.length - 1) {
      setQ1Index(q1Index + 1);
      setPracticeStep(1);
      setFeedback({ show: false, message: '', type: '' });
    }
  };

  const handleMatch = (num, option) => {
    setMatchingAnswers(prev => ({ ...prev, [num]: option }));
  };

  // 實戰挑戰檢查
  const checkChallenge = () => {
    const { a, b, c } = challengeAnswers;
    if (parseInt(a) === 2 && parseInt(b) === 2 && parseInt(c) === 1) {
      setChallengeFeedback({ type: 'success', text: "太厲害了！252 = 2² × 3² × 7¹，你完全掌握了標準分解式！" });
    } else {
      setChallengeFeedback({ type: 'error', text: "答案不完全正確喔。試著先對 252 進行短除法分解。 (提示：252 = 4 × 63)" });
    }
  };

  return (
    <div className="min-h-screen bg-slate-50 p-4 md:p-8 font-sans text-slate-900">
      <div className="max-w-4xl mx-auto">
        <header className="text-center mb-8">
          <h1 className="text-3xl md:text-4xl font-bold text-slate-800 mb-2">📘 質因數分解的標準分解式</h1>
          <p className="text-slate-600">N-7-2 互動式學習講義</p>
        </header>

        {/* 學習目標 */}
        <section className="bg-white rounded-xl shadow-sm p-6 mb-6 border-l-4 border-blue-500">
          <h2 className="text-xl font-bold text-blue-700 mb-3 flex items-center gap-2">
            <BookOpen className="w-5 h-5" /> 🎯 學習目標
          </h2>
          <ul className="list-disc list-inside text-slate-700 space-y-1 text-sm md:text-base">
            <li>說出什麼是「質因數」。</li>
            <li>學會將一個合數分解成質因數相乘。</li>
            <li>使用「指數」正確寫出標準分解式。</li>
            <li>理解分解式底數必須「從小排到大」。</li>
          </ul>
        </section>

        {/* 概念說明 */}
        <div className="grid md:grid-cols-3 gap-4 mb-8 text-sm md:text-base">
          <div className="bg-green-50 p-5 rounded-lg border border-green-200 shadow-sm">
            <h3 className="font-bold text-green-700 text-lg mb-2">1️⃣ 質因數</h3>
            <p className="text-green-800 text-sm">因數中同時也是「質數」的數字。</p>
            <p className="mt-2 font-mono text-xs text-green-600 bg-white/50 p-1 rounded">例：12 的質因數是 2, 3</p>
          </div>
          <div className="bg-slate-100 p-5 rounded-lg border border-slate-200 shadow-sm">
            <h3 className="font-bold text-slate-700 text-lg mb-2">2️⃣ 質因數分解</h3>
            <p className="text-slate-800 text-sm">把合數寫成「質數相乘」的過程。</p>
            <p className="mt-2 font-mono text-xs text-slate-500 bg-white/50 p-1 rounded">例：12 = 2 × 2 × 3</p>
          </div>
          <div className="bg-blue-50 p-5 rounded-lg border border-blue-200 shadow-sm">
            <h3 className="font-bold text-blue-700 text-lg mb-2">3️⃣ 標準分解式</h3>
            <p className="text-blue-800 font-bold text-sm">使用指數表示重複的質因數。</p>
            <p className="mt-2 font-mono text-xs text-blue-600 underline bg-white/50 p-1 rounded">例：12 = 2² × 3</p>
          </div>
        </div>

        {/* 互動練習 1 */}
        <section className="bg-amber-50 rounded-xl shadow-md p-6 mb-8 border border-amber-200">
          <div className="flex justify-between items-center mb-6">
            <h2 className="text-xl font-bold text-amber-800 flex items-center gap-2">
              <RefreshCw className="w-5 h-5" /> 🧮 互動練習 1：步步分解
            </h2>
            <span className="text-xs bg-amber-200 text-amber-800 px-2 py-1 rounded-full font-bold">進度：{q1Index + 1}/{questions1.length}</span>
          </div>
          
          <div className="bg-white p-8 rounded-xl border border-amber-200 mb-4 text-center shadow-inner relative overflow-hidden">
            {practiceStep <= questions1[q1Index].steps.length ? (
              <div className="space-y-6">
                <div className="text-5xl font-black text-slate-200 tracking-widest animate-pulse">
                  {practiceStep === 1 ? questions1[q1Index].num : questions1[q1Index].results[practiceStep - 2]}
                </div>
                <div className="text-amber-900 font-medium text-sm md:text-base">
                  這個數可以用哪個<b>最小質數</b>來除？
                </div>
                <div className="flex gap-2 justify-center mt-4">
                  <input
                    type="number"
                    value={userInput}
                    onChange={(e) => setUserInput(e.target.value)}
                    className="w-20 border-2 border-amber-300 rounded-lg px-2 py-2 text-center text-xl font-bold focus:ring-4 focus:ring-amber-200 outline-none"
                    placeholder="?"
                  />
                  <button onClick={() => handlePractice1(userInput)} className="bg-amber-600 text-white px-4 py-2 rounded-lg font-bold hover:bg-amber-700">檢查</button>
                </div>
              </div>
            ) : (
              <div className="space-y-4 animate-fadeIn">
                <p className="text-2xl font-bold text-green-800">🎉 完成！</p>
                <div className="bg-slate-50 p-4 rounded-xl border border-slate-200 inline-block font-mono text-xl shadow-sm">
                  {questions1[q1Index].num} = <span className="text-blue-600 font-bold">{questions1[q1Index].final}</span>
                </div>
                <div className="mt-4">
                  {q1Index < questions1.length - 1 && (
                    <button onClick={nextQuestion1} className="bg-blue-600 text-white px-6 py-2 rounded-full font-bold hover:bg-blue-700 flex items-center gap-2 mx-auto">下一題 <ChevronRight className="w-4 h-4" /></button>
                  )}
                </div>
              </div>
            )}
          </div>
          {feedback.show && practiceStep <= questions1[q1Index].steps.length && (
            <div className={`p-4 rounded-lg font-bold text-center text-sm ${feedback.type === 'success' ? 'bg-green-100 text-green-800' : 'bg-red-100 text-red-800'}`}>
              {feedback.message}
            </div>
          )}
        </section>

        {/* 互動練習 2 */}
        <section className="bg-white rounded-xl shadow-md p-6 mb-8 border border-slate-200">
          <div className="flex justify-between items-center mb-6">
            <h2 className="text-xl font-bold text-slate-800 flex items-center gap-2">
              <CheckCircle className="w-5 h-5 text-green-500" /> 🧩 互動練習 2：配對挑戰
            </h2>
            <button onClick={shuffleMatching} className="text-xs bg-slate-100 text-slate-600 px-3 py-1.5 rounded-lg flex items-center gap-1">
              <RefreshCw className="w-3 h-3" /> 重新隨機
            </button>
          </div>
          <div className="grid gap-3 mb-6">
            {shuffledPairs.map((pair) => (
              <div key={pair.num} className="flex items-center justify-between p-4 bg-slate-50 rounded-xl border border-slate-100">
                <div className="text-2xl font-black text-slate-700 w-16">{pair.num}</div>
                <ArrowRight className="text-slate-300 w-6 h-6" />
                <div className="flex gap-2">
                  {['A', 'B', 'C', 'D'].map((opt) => (
                    <button key={opt} onClick={() => handleMatch(pair.num, opt)} className={`w-10 h-10 rounded-full border-2 font-bold transition-all ${matchingAnswers[pair.num] === opt ? (opt === pair.label ? 'bg-green-500 border-green-600 text-white' : 'bg-red-500 border-red-600 text-white') : 'bg-white border-slate-200 text-slate-400 hover:border-blue-400'}`}>
                      {opt}
                    </button>
                  ))}
                </div>
              </div>
            ))}
          </div>
          <div className="bg-slate-900 text-slate-300 p-4 rounded-xl text-sm grid grid-cols-2 md:grid-cols-4 gap-2">
            <p><b>(A)</b> 2² × 3²</p><p><b>(B)</b> 3² × 5</p><p><b>(C)</b> 2 × 5²</p><p><b>(D)</b> 2² × 3 × 7</p>
          </div>
        </section>

        {/* 實戰挑戰 - 新增部分 */}
        <section className="bg-gradient-to-br from-indigo-50 to-white rounded-xl shadow-lg p-6 mb-8 border-2 border-indigo-200 relative overflow-hidden">
          <div className="absolute top-0 right-0 p-4 opacity-10"><Rocket className="w-24 h-24 text-indigo-900" /></div>
          <h2 className="text-2xl font-bold text-indigo-900 mb-4 flex items-center gap-2">
            <Rocket className="w-6 h-6" /> 🚀 實戰挑戰：綜合填空練習
          </h2>
          <div className="bg-white p-6 rounded-xl border border-indigo-100 shadow-sm">
            <p className="text-slate-800 mb-4 leading-relaxed">
              已知數字 <span className="font-black text-indigo-600 underline">252</span> 的標準分解式可以寫成：
              <span className="block text-2xl font-serif text-center my-4 py-2 bg-slate-50 rounded-lg border-2 border-dashed border-indigo-100">
                2<sup>a</sup> × 3<sup>b</sup> × 7<sup>c</sup>
              </span>
              請動手分解看看，並找出指數 <span className="font-bold">a, b, c</span> 分別是多少？
            </p>
            
            <div className="flex flex-wrap items-center justify-center gap-6 mt-6">
              <div className="flex flex-col items-center">
                <label className="text-xs font-bold text-slate-400 mb-1 uppercase">指數 a</label>
                <input 
                  type="number" 
                  value={challengeAnswers.a} 
                  onChange={(e) => setChallengeAnswers({...challengeAnswers, a: e.target.value})}
                  className="w-16 h-12 border-2 border-slate-200 rounded-lg text-center text-xl font-bold focus:border-indigo-500 outline-none"
                  placeholder="?"
                />
              </div>
              <div className="flex flex-col items-center">
                <label className="text-xs font-bold text-slate-400 mb-1 uppercase">指數 b</label>
                <input 
                  type="number" 
                  value={challengeAnswers.b} 
                  onChange={(e) => setChallengeAnswers({...challengeAnswers, b: e.target.value})}
                  className="w-16 h-12 border-2 border-slate-200 rounded-lg text-center text-xl font-bold focus:border-indigo-500 outline-none"
                  placeholder="?"
                />
              </div>
              <div className="flex flex-col items-center">
                <label className="text-xs font-bold text-slate-400 mb-1 uppercase">指數 c</label>
                <input 
                  type="number" 
                  value={challengeAnswers.c} 
                  onChange={(e) => setChallengeAnswers({...challengeAnswers, c: e.target.value})}
                  className="w-16 h-12 border-2 border-slate-200 rounded-lg text-center text-xl font-bold focus:border-indigo-500 outline-none"
                  placeholder="?"
                />
              </div>
              <button 
                onClick={checkChallenge}
                className="mt-5 md:mt-0 bg-indigo-600 text-white px-8 py-3 rounded-lg font-bold hover:bg-indigo-700 flex items-center gap-2 shadow-md transition-all active:scale-95"
              >
                <Send className="w-4 h-4" /> 提交答案
              </button>
            </div>

            {challengeFeedback && (
              <div className={`mt-6 p-4 rounded-lg flex items-start gap-3 animate-fadeIn ${challengeFeedback.type === 'success' ? 'bg-green-50 text-green-800 border border-green-200' : 'bg-red-50 text-red-800 border border-red-200'}`}>
                {challengeFeedback.type === 'success' ? <CheckCircle className="w-5 h-5 mt-0.5 shrink-0" /> : <AlertCircle className="w-5 h-5 mt-0.5 shrink-0" />}
                <p className="text-sm font-medium">{challengeFeedback.text}</p>
              </div>
            )}
          </div>
        </section>

        {/* Footer */}
        <footer className="grid md:grid-cols-2 gap-6">
          <div className="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
            <h3 className="font-bold text-slate-800 mb-3 border-b pb-2 flex items-center gap-2">
              <AlertCircle className="text-red-500 w-5 h-5" /> ⚠️ 常見迷思
            </h3>
            <ul className="text-sm space-y-3 text-slate-600">
              <li className="flex items-start gap-2 italic">「指數為 1 時，通常省略不寫。」</li>
              <li className="flex items-start gap-2 italic">「底數請務必從小到大排列。」</li>
              <li className="flex items-start gap-2 italic">「分解式中不可以出現 4、6、9 等合數。」</li>
            </ul>
          </div>
          <div className="bg-indigo-900 text-indigo-50 p-6 rounded-xl shadow-sm">
            <h3 className="font-bold mb-3 border-b border-indigo-700 pb-2 flex items-center gap-2">
              <Info className="w-5 h-5" /> 🤔 思考題
            </h3>
            <p className="text-sm italic leading-relaxed">
              如果一個數的分解式是 2³ × 5，那麼這個數是多少？<br/><br/>
              如果把這個數再乘以 2，分解式會變成什麼樣子？
            </p>
          </div>
        </footer>

        <div className="mt-12 text-center text-slate-400 text-xs pb-8">
          依據 108 課綱數學領域課程手冊編製 · N-7-2 學習單元
        </div>
      </div>
      
      <style>{`
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        .animate-fadeIn { animation: fadeIn 0.4s ease-out forwards; }
      `}</style>
    </div>
  );
};

export default App;
