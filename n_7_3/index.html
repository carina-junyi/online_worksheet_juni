<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>N-7-3 負數與數的四則運算互動講義</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- KaTeX for Beautiful Math -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"></script>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;500;700&display=swap');
        body { font-family: 'Noto Sans TC', sans-serif; background-color: #f8fafc; }
        .number-line-cell { transition: all 0.3s ease; position: relative; }
        .marker { transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275); }
        .math-fact { background-color: #fef3c7; color: #92400e; padding: 2px 6px; border-radius: 4px; font-weight: bold; font-family: sans-serif; }
        .hidden { display: none; }
        /* Smooth Math Transitions */
        .katex { font-size: 1.1em; }
    </style>
</head>
<body class="p-4 md:p-8">
    <div class="max-w-4xl mx-auto">
        <!-- Header -->
        <header class="text-center mb-8">
            <h1 class="text-3xl md:text-4xl font-bold text-slate-800 mb-2">📘 負數與數的四則混合運算</h1>
            <p class="text-slate-600">N-7-3 互動式學習講義</p>
        </header>

        <!-- Learning Objectives -->
        <section class="bg-white rounded-xl shadow-sm p-6 mb-6 border-l-4 border-indigo-500">
            <h2 class="text-xl font-bold text-indigo-700 mb-3">🎯 學習目標</h2>
            <ul class="list-disc list-inside text-slate-700 space-y-1 text-sm md:text-base">
                <li>認識「負數」是比 $0$ 小的數。</li>
                <li>用正、負數表示生活中性質相反的量。</li>
                <li>理解並找出一個數的「相反數」。</li>
                <li>正確進行正負數的加、減運算（數線法）。</li>
                <li>破解「負負得正」與「負號意義」的常見迷思。</li>
            </ul>
        </section>

        <!-- Concept Cards -->
        <div class="grid md:grid-cols-3 gap-4 mb-8">
            <div class="bg-blue-50 p-5 rounded-lg border border-blue-200 shadow-sm">
                <h3 class="font-bold text-blue-700 text-lg mb-2">1️⃣ 負數是什麼？</h3>
                <p class="text-sm text-blue-800">比 $0$ 小的數，符號為「 $-$ 」。</p>
                <div class="mt-3 text-xs space-y-1 text-blue-600">
                    <p>• 虧損 $100$ 元：$-100$</p>
                    <p>• 零下 $5$ 度：$-5$</p>
                </div>
            </div>
            <div class="bg-emerald-50 p-5 rounded-lg border border-emerald-200 shadow-sm">
                <h3 class="font-bold text-emerald-700 text-lg mb-2">2️⃣ 相反數</h3>
                <p class="text-sm text-emerald-800">兩數相加等於 $0$，則互為相反數。</p>
                <div class="mt-3 text-xs space-y-1 text-emerald-600">
                    <p>• $5$ 的相反數是 $-5$</p>
                    <p>• $-3$ 的相反數是 $3$</p>
                </div>
            </div>
            <div class="bg-slate-100 p-5 rounded-lg border border-slate-200 shadow-sm">
                <h3 class="font-bold text-slate-700 text-lg mb-2">3️⃣ 大小比較</h3>
                <p class="text-sm text-slate-800">在數線上越右邊越大。</p>
                <p class="mt-3 text-xs font-bold text-slate-500">
                    注意：$-3 > -10$
                </p>
            </div>
        </div>

        <!-- Interactive Number Line -->
        <section class="bg-white rounded-xl shadow-md p-6 mb-8 overflow-hidden">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold text-slate-800">📏 互動數線模擬</h2>
                <button onclick="resetMarker()" class="px-4 py-2 bg-slate-200 hover:bg-slate-300 rounded-md text-sm font-medium">重置位置</button>
            </div>
            
            <p class="text-slate-600 mb-8 text-sm">點擊按鈕來移動數線上的小點，觀察加法與減法的方向！</p>

            <div class="relative py-12 mb-8 border-b border-t border-slate-100 bg-slate-50/50 rounded-lg">
                <div class="absolute left-0 right-0 h-1 bg-slate-400 top-1/2 -translate-y-1/2"></div>
                <div class="relative flex justify-between px-4" id="number-line"></div>
                <div id="pointer" class="marker absolute top-1/2 -translate-y-1/2 w-8 h-8 bg-indigo-600 rounded-full border-4 border-white shadow-lg flex items-center justify-center text-white text-[10px] font-bold z-20" style="left: 50%;">0</div>
            </div>

            <div class="flex flex-wrap gap-3 justify-center">
                <div class="flex items-center gap-2 mr-4">
                    <span class="text-sm font-bold text-slate-700">當前位置：</span>
                    <span id="current-val" class="text-2xl font-black text-indigo-600">0</span>
                </div>
                <div class="h-8 w-px bg-slate-300 mx-2"></div>
                <button onclick="moveMarker(1)" class="px-4 py-2 bg-green-500 hover:bg-green-600 text-white rounded-lg shadow-sm font-bold">$+ 1$</button>
                <button onclick="moveMarker(-1)" class="px-4 py-2 bg-red-500 hover:bg-red-600 text-white rounded-lg shadow-sm font-bold">$- 1$</button>
                <button onclick="moveMarker(5)" class="px-4 py-2 bg-green-700 hover:bg-green-800 text-white rounded-lg shadow-sm font-bold">$+ 5$</button>
                <button onclick="moveMarker(-5)" class="px-4 py-2 bg-red-700 hover:bg-red-800 text-white rounded-lg shadow-sm font-bold">$- 5$</button>
            </div>
        </section>

        <!-- Dynamic Multi-Question Quiz -->
        <section class="bg-amber-50 rounded-xl shadow-sm p-6 mb-8 border border-amber-200">
            <div class="flex justify-between items-center mb-4">
                <h2 class="text-xl font-bold text-amber-800" id="quiz-title">🔍 引導練習</h2>
                <span id="quiz-progress" class="text-sm font-bold bg-amber-200 text-amber-800 px-3 py-1 rounded-full">第 1 / 3 題</span>
            </div>
            
            <div id="quiz-content" class="space-y-6">
                <!-- Question steps will be injected here -->
            </div>

            <div id="quiz-feedback" class="hidden mt-6 p-4 rounded-lg font-bold text-center"></div>
            
            <div id="next-question-container" class="hidden mt-6 text-center">
                <button onclick="nextQuestion()" class="px-8 py-3 bg-amber-600 hover:bg-amber-700 text-white rounded-xl shadow-lg font-bold transition">下一題 ➔</button>
            </div>
        </section>

        <!-- Application & Challenge Section -->
        <section class="bg-indigo-50 rounded-xl shadow-md p-6 mb-8 border border-indigo-200">
            <div class="flex items-center gap-2 mb-4">
                <span class="text-2xl">🚀</span>
                <h2 class="text-xl font-bold text-indigo-800">五、應用題／挑戰題</h2>
            </div>
            
            <div class="bg-white rounded-lg p-5 shadow-sm mb-6 border border-indigo-100">
                <h3 class="font-bold text-slate-800 mb-3 text-lg">💰 生活應用題：小明的帳戶</h3>
                <p class="text-slate-700 leading-relaxed mb-4">
                    小明某天的帳戶變化如下：
                    <br>• 早上 <span class="text-green-600 font-bold underline">存入 $500$ 元</span>
                    <br>• 下午 <span class="text-red-600 font-bold underline">支出 $1200$ 元</span>
                </p>
                <div class="bg-indigo-50 p-4 rounded-lg">
                    <p class="text-sm font-bold text-indigo-700 mb-2">💡 引導列式：</p>
                    <p class="text-2xl font-mono text-center py-4 bg-white rounded border border-indigo-200" id="math-formula">
                        $+500 + (-1200) = ?$
                    </p>
                </div>
            </div>

            <!-- Challenge Interaction -->
            <div class="text-center">
                <p class="text-slate-800 font-medium mb-3">請問最後的餘額是多少元？代表什麼意義？</p>
                <div class="flex flex-col sm:flex-row gap-3 justify-center items-center">
                    <input type="number" id="challenge-answer" placeholder="輸入數字..." class="px-4 py-2 border-2 border-indigo-300 rounded-lg focus:outline-none focus:border-indigo-600 w-32 text-center font-bold">
                    <button onclick="checkChallenge()" class="px-6 py-2 bg-indigo-600 text-white rounded-lg font-bold hover:bg-indigo-700 transition">檢查答案</button>
                </div>
                <div id="challenge-feedback" class="hidden mt-4 p-4 rounded-lg font-bold"></div>
            </div>
        </section>

        <!-- Misconceptions & Reflection -->
        <footer class="grid md:grid-cols-2 gap-6">
            <div class="bg-white p-6 rounded-xl shadow-sm border border-slate-200">
                <h3 class="font-bold text-slate-800 mb-4 border-b pb-2">⚠️ 常見迷思（小心陷阱）</h3>
                <ul class="text-sm space-y-4 text-slate-600">
                    <li class="flex items-start gap-2">
                        <span class="text-red-500 font-bold">❌</span> 
                        <div>
                            <span class="font-bold text-slate-800">負號就是減號？</span>
                            <p class="text-xs text-slate-500 mt-1">不是喔！「負號」代表性質，「減號」代表運算。例如：$(-5) - 3$。</p>
                        </div>
                    </li>
                    <li class="flex items-start gap-2">
                        <span class="text-red-500 font-bold">❌</span> 
                        <div>
                            <span class="font-bold text-slate-800">$-a$ 一定是負數？</span>
                            <p class="text-xs text-slate-500 mt-1">錯！如果 $a = -2$，那 $-a = -(-2) = 2$，會變成正數！</p>
                        </div>
                    </li>
                </ul>
            </div>
            <div class="bg-slate-800 text-slate-100 p-6 rounded-xl shadow-sm">
                <h3 class="font-bold mb-3 border-b border-slate-600 pb-2">🤔 反思與討論</h3>
                <p class="text-sm leading-relaxed mb-4 italic text-slate-400">
                    「想像你正在還債，當你的負債（負數）減少時，你的總財產反而是增加了嗎？」
                </p>
            </div>
        </footer>
    </div>

    <script>
        // Number Line Logic
        const range = 10;
        let currentPos = 0;
        const lineContainer = document.getElementById('number-line');
        const pointer = document.getElementById('pointer');
        const currentValDisplay = document.getElementById('current-val');

        function initNumberLine() {
            lineContainer.innerHTML = '';
            for (let i = -range; i <= range; i++) {
                const tick = document.createElement('div');
                tick.className = 'flex flex-col items-center z-10';
                const line = document.createElement('div');
                line.className = `w-0.5 ${i === 0 ? 'h-4 bg-slate-800' : 'h-2 bg-slate-400'}`;
                const label = document.createElement('span');
                label.className = `text-[10px] mt-1 font-bold ${i < 0 ? 'text-red-500' : i > 0 ? 'text-green-600' : 'text-slate-800'}`;
                label.innerText = i;
                tick.appendChild(line);
                tick.appendChild(label);
                lineContainer.appendChild(tick);
            }
            updatePointer();
        }

        function updatePointer() {
            const percentage = ((currentPos + range) / (range * 2)) * 100;
            pointer.style.left = `calc(${percentage}% - 16px)`;
            pointer.innerText = currentPos;
            currentValDisplay.innerText = currentPos;
            if (currentPos > 0) pointer.className = "marker absolute top-1/2 -translate-y-1/2 w-8 h-8 bg-green-600 rounded-full border-4 border-white shadow-lg flex items-center justify-center text-white text-xs font-bold z-20";
            else if (currentPos < 0) pointer.className = "marker absolute top-1/2 -translate-y-1/2 w-8 h-8 bg-red-600 rounded-full border-4 border-white shadow-lg flex items-center justify-center text-white text-xs font-bold z-20";
            else pointer.className = "marker absolute top-1/2 -translate-y-1/2 w-8 h-8 bg-indigo-600 rounded-full border-4 border-white shadow-lg flex items-center justify-center text-white text-xs font-bold z-20";
        }

        function moveMarker(step) {
            const next = currentPos + step;
            if (next >= -range && next <= range) {
                currentPos = next;
                updatePointer();
            }
        }

        function resetMarker() {
            currentPos = 0;
            updatePointer();
        }

        // Quiz Logic
        const quizData = [
            {
                title: "題目一：計算 $(-3) - 5$",
                steps: [
                    {
                        question: "1️⃣ 算式從「 $-3$ 」出發，它在數線的哪一邊？",
                        options: [
                            { text: "$0$ 的左邊三格", correct: true, feedback: "✅ 正確！負數在 $0$ 的左邊。" },
                            { text: "$0$ 的右邊三格", correct: false, feedback: "❌ 不對喔，正數才在右邊。" }
                        ]
                    },
                    {
                        question: "2️⃣ 題目是「減 $5$」，代表我們要往哪個方向移動？",
                        options: [
                            { text: "往左移動 $5$ 格", correct: true, feedback: "✅ 沒錯！「減法」就是往左（變小）走。" },
                            { text: "往右移動 $5$ 格", correct: false, feedback: "❌ 往右走是加法喔！" }
                        ]
                    },
                    {
                        question: "3️⃣ 最後會停在哪個數字上？",
                        options: [
                            { text: "$2$", correct: false, feedback: "❌ 不對，這是在 $0$ 的左邊喔。" },
                            { text: "$-8$", correct: true, feedback: "🎉 太棒了！ $(-3)$ 往左走 $5$ 格就是 $-8$。" },
                            { text: "$-2$", correct: false, feedback: "❌ 算算看：$-3, -4, -5, -6, -7$... 再一格是？" }
                        ]
                    }
                ]
            },
            {
                title: "題目二：計算 $2 + (-6)$",
                steps: [
                    {
                        question: "1️⃣ 算式的起點是「 $2$ 」，代表它在？",
                        options: [
                            { text: "$0$ 的右邊兩格", correct: true, feedback: "✅ 正確！正數在 $0$ 的右邊。" },
                            { text: "$0$ 的左邊兩格", correct: false, feedback: "❌ 這是正數 $2$ 喔，再看一次位置。" }
                        ]
                    },
                    {
                        question: "2️⃣ 加上一個負數「 $+ (-6)$ 」，在數線上等於？",
                        options: [
                            { text: "往右走 $6$ 格", correct: false, feedback: "❌ 加上負數代表變小，方向應該反轉。" },
                            { text: "往左走 $6$ 格", correct: true, feedback: "✅ 聰明！加上負數就跟「減法」一樣往左走。" }
                        ]
                    },
                    {
                        question: "3️⃣ 從 $2$ 往左走 $6$ 格，最後停在哪？",
                        options: [
                            { text: "$8$", correct: false, feedback: "❌ 這是往右走的結果。" },
                            { text: "$-4$", correct: true, feedback: "🎉 沒錯！經過了 $0$ 之後，再往左走到 $-4$。" },
                            { text: "$-8$", correct: false, feedback: "❌ 走太多了。" }
                        ]
                    }
                ]
            },
            {
                title: "題目三：計算 $(-4) + 9$",
                steps: [
                    {
                        question: "1️⃣ 先找到起點「 $-4$ 」，並進行「 $+ 9$ 」，這代表？",
                        options: [
                            { text: "往右移動 $9$ 格", correct: true, feedback: "✅ 正確！加法代表變大，往右移動。" },
                            { text: "往左移動 $9$ 格", correct: false, feedback: "❌ 加法是往右喔！" }
                        ]
                    },
                    {
                        question: "2️⃣ 從 $-4$ 往右移動 $4$ 格後，會到達哪裡？",
                        options: [
                            { text: "$-8$", correct: false, feedback: "❌ 往右移動，負值應該會增加。" },
                            { text: "$0$", correct: true, feedback: "✅ 沒錯！ $-4 + 4 = 0$。" }
                        ]
                    },
                    {
                        question: "3️⃣ 既然要往右移動 $9$ 格，剛到 $0$ (走了4格)，還要再往右走幾格？",
                        options: [
                            { text: "再走 $5$ 格，停在 $5$", correct: true, feedback: "🎉 答對了！ $(-4) + 9 = 5$。" },
                            { text: "再走 $9$ 格，停在 $9$", correct: false, feedback: "❌ 別忘了我們已經先從 $-4$ 走到 $0$ 囉。" }
                        ]
                    }
                ]
            }
        ];

        let currentQuestionIndex = 0;
        let currentStepIndex = 0;

        const quizContent = document.getElementById('quiz-content');
        const quizFeedback = document.getElementById('quiz-feedback');
        const nextBtnContainer = document.getElementById('next-question-container');
        const progressDisplay = document.getElementById('quiz-progress');
        const quizTitle = document.getElementById('quiz-title');

        function renderStep() {
            const question = quizData[currentQuestionIndex];
            const step = question.steps[currentStepIndex];
            
            quizTitle.innerText = question.title;
            progressDisplay.innerText = `第 ${currentQuestionIndex + 1} / ${quizData.length} 題`;

            let html = `
                <div class="animate-in fade-in duration-500">
                    <p class="text-slate-800 mb-4 font-bold text-lg">${step.question}</p>
                    <div class="flex flex-wrap gap-3">
            `;

            step.options.forEach((opt, i) => {
                html += `
                    <button onclick="handleAnswer(${opt.correct}, '${opt.feedback.replace(/'/g, "\\'")}')" 
                            class="px-5 py-3 bg-white border-2 border-amber-200 rounded-xl hover:border-amber-500 hover:bg-amber-100 transition shadow-sm font-medium">
                        ${opt.text}
                    </button>
                `;
            });

            html += `</div></div>`;
            quizContent.innerHTML = html;
            // Re-render math in the injected content
            renderMathInElement(quizContent, {
                delimiters: [
                    {left: '$', right: '$', display: false},
                    {left: '$$', right: '$$', display: true}
                ]
            });
        }

        function handleAnswer(isCorrect, fbText) {
            quizFeedback.classList.remove('hidden');
            quizFeedback.innerHTML = fbText;
            renderMathInElement(quizFeedback);

            if (isCorrect) {
                quizFeedback.className = "mt-6 p-4 rounded-lg font-bold text-center bg-green-100 text-green-800 border-2 border-green-200";
                setTimeout(() => {
                    quizFeedback.classList.add('hidden');
                    if (currentStepIndex < quizData[currentQuestionIndex].steps.length - 1) {
                        currentStepIndex++;
                        renderStep();
                    } else {
                        showQuestionComplete();
                    }
                }, 1800);
            } else {
                quizFeedback.className = "mt-6 p-4 rounded-lg font-bold text-center bg-red-100 text-red-800 border-2 border-red-200";
            }
        }

        function showQuestionComplete() {
            quizContent.innerHTML = `
                <div class="text-center py-8">
                    <div class="text-5xl mb-4">🏆</div>
                    <h3 class="text-2xl font-black text-amber-800 mb-2">挑戰成功！</h3>
                    <p class="text-slate-600">你已經完全掌握了這題的邏輯。</p>
                </div>
            `;
            if (currentQuestionIndex < quizData.length - 1) {
                nextBtnContainer.classList.remove('hidden');
            } else {
                quizContent.innerHTML += `<p class="mt-4 font-bold text-indigo-600 text-center w-full">恭喜你完成了所有引導練習！🎉</p>`;
            }
        }

        function nextQuestion() {
            currentQuestionIndex++;
            currentStepIndex = 0;
            nextBtnContainer.classList.add('hidden');
            renderStep();
        }

        // Challenge Logic
        function checkChallenge() {
            const val = document.getElementById('challenge-answer').value;
            const fb = document.getElementById('challenge-feedback');
            fb.classList.remove('hidden');
            
            if (val === "-700") {
                fb.innerHTML = `✅ 完全正確！最後餘額為 $-700$ 元。<br>這代表帳戶處於「透支」狀態，比 $0$ 元還少了 $700$ 元！`;
                fb.className = "mt-4 p-4 rounded-lg font-bold bg-green-100 text-green-800 border-2 border-green-200";
            } else if (val === "700") {
                fb.innerHTML = `❌ 數字對了，但符號不對喔！<br>支出比存入多，餘額應該是正還是負？`;
                fb.className = "mt-4 p-4 rounded-lg font-bold bg-red-100 text-red-800 border-2 border-red-200";
            } else {
                fb.innerHTML = `❌ 算算看：$500 - 1200$ 是多少？<br>從 $500$ 往左走 $1200$ 步。`;
                fb.className = "mt-4 p-4 rounded-lg font-bold bg-red-100 text-red-800 border-2 border-red-200";
            }
            renderMathInElement(fb);
        }

        window.onload = () => {
            initNumberLine();
            renderStep();
            // Initial Math Render
            renderMathInElement(document.body, {
                delimiters: [
                    {left: '$', right: '$', display: false},
                    {left: '$$', right: '$$', display: true}
                ]
            });
        };
    </script>
</body>
</html>
