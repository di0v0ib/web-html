<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7的20以内加减乘除练习</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            background-color: #f5f5f5;
        }
        .container {
            width: 100%;
            max-width: 400px;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .setting {
            margin-bottom: 20px;
        }
        .setting label {
            font-size: 16px;
            margin-right: 10px;
        }
        .setting input {
            width: 60px;
            padding: 5px;
            font-size: 16px;
            text-align: center;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .setting button {
            padding: 6px 15px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-left: 10px;
        }
        .setting button:hover {
            background-color: #45a049;
        }
        .timer {
            font-size: 20px;
            margin-bottom: 20px;
            font-weight: bold;
        }
        .question {
            font-size: 24px;
            margin-bottom: 15px;
            text-align: center;
        }
        .answer-area {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-bottom: 20px;
        }
        #answer-input {
            width: 100px;
            height: 40px;
            font-size: 20px;
            text-align: center;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
        #submit-btn {
            margin-left: 10px;
            padding: 8px 15px;
            background-color: #2196F3;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        #submit-btn:hover {
            background-color: #0b7dda;
        }
        .num-keyboard {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            width: 100%;
        }
        .num-btn {
            padding: 15px;
            font-size: 20px;
            border: none;
            border-radius: 5px;
            background-color: #e0e0e0;
            cursor: pointer;
        }
        .num-btn:hover {
            background-color: #d0d0d0;
        }
        .del-btn {
            background-color: #ff9800;
            color: white;
        }
        .del-btn:hover {
            background-color: #f57c00;
        }
        .result-area {
            margin-top: 20px;
            font-size: 18px;
        }
        .wrong {
            color: red;
            margin-left: 5px;
        }
        .finished {
            margin-top: 10px;
            color: #4CAF50;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="setting">
            <label for="question-count">出题数量：</label>
            <input type="number" id="question-count" min="1" max="50" value="10">
            <button id="start-btn">开始练习</button>
        </div>
        <div class="timer">用时：<span id="time">00:00:00</span></div>
        <div class="question" id="question-area">请点击开始练习</div>
        <div class="answer-area">
            <input type="text" id="answer-input" readonly placeholder="输入答案">
            <button id="submit-btn" disabled>提交</button>
        </div>
        <div class="num-keyboard">
            <button class="num-btn">1</button>
            <button class="num-btn">2</button>
            <button class="num-btn">3</button>
            <button class="num-btn">4</button>
            <button class="num-btn">5</button>
            <button class="num-btn">6</button>
            <button class="num-btn">7</button>
            <button class="num-btn">8</button>
            <button class="num-btn">9</button>
            <button class="num-btn">0</button>
            <button class="num-btn del-btn">删除</button>
        </div>
        <div class="result-area" id="result-area"></div>
    </div>

    <script>
        let timer = null;
        let startTime = 0;
        let currentQuestion = null;
        let questionList = [];
        let currentIndex = 0;
        let wrongCount = 0;
        let isRunning = false;

        // DOM元素
        const startBtn = document.getElementById('start-btn');
        const questionCountInput = document.getElementById('question-count');
        const timeSpan = document.getElementById('time');
        const questionArea = document.getElementById('question-area');
        const answerInput = document.getElementById('answer-input');
        const submitBtn = document.getElementById('submit-btn');
        const numBtns = document.querySelectorAll('.num-btn');
        const delBtn = document.querySelector('.del-btn');
        const resultArea = document.getElementById('result-area');

        // 生成7的20以内加减乘除题目
        function generateQuestions(count) {
            const ops = ['+', '-', '*'];
            const questions = [];
            while (questions.length < count) {
                const op = ops[Math.floor(Math.random() * ops.length)];
                let a, b, result;
                switch (op) {
                    case '+':
                        a = 7;
                        b = Math.floor(Math.random() * 14); 
                        result = a + b;
                        break;
                    case '-':
                        a = Math.floor(Math.random() * 14) + 7; 
                        b = 7;
                        result = a - b;
                        break;
                    case '*':
                        a = 7;
                        b = Math.floor(Math.random() * 3) + 1; 
                        result = a * b;
                        break;
                }
                if (result >= 0 && result <= 20) {
                    // 显示时替换为×，方便阅读
                    const showOp = op === '*' ? '×' : op;
                    questions.push({ expr: `${a} ${showOp} ${b} = ?`, answer: result });
                }
            }
            return questions;
        }

        // 计时函数
        function updateTime() {
            const now = Date.now();
            const diff = now - startTime;
            const hours = Math.floor(diff / 3600000).toString().padStart(2, '0');
            const minutes = Math.floor((diff % 3600000) / 60000).toString().padStart(2, '0');
            const seconds = Math.floor((diff % 60000) / 1000).toString().padStart(2, '0');
            timeSpan.textContent = `${hours}:${minutes}:${seconds}`;
        }

        // 开始练习
        startBtn.addEventListener('click', () => {
            const count = parseInt(questionCountInput.value.trim());
            if (isNaN(count) || count < 1 || count > 50) {
                alert('请输入1-50之间的有效数字');
                return;
            }
            // 重置所有状态
            clearInterval(timer);
            questionList = [];
            currentIndex = 0;
            wrongCount = 0;
            isRunning = true;
            resultArea.innerHTML = '';
            answerInput.value = '';
            // 生成题目
            questionList = generateQuestions(count);
            // 开始计时
            startTime = Date.now();
            timer = setInterval(updateTime, 1000);
            // 显示第一题
            currentQuestion = questionList[currentIndex];
            questionArea.textContent = currentQuestion.expr;
            submitBtn.disabled = false;
        });

        // 数字键盘事件绑定
        numBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                if (!isRunning) return;
                if (btn.classList.contains('del-btn')) {
                    answerInput.value = answerInput.value.slice(0, -1);
                    return;
                }
                answerInput.value += btn.textContent;
            });
        });

        // 提交答案
        submitBtn.addEventListener('click', () => {
            if (!isRunning || answerInput.value.trim() === '') return;
            const userAnswer = parseInt(answerInput.value.trim());
            const correctAnswer = currentQuestion.answer;
            const isCorrect = userAnswer === correctAnswer;

            const resultItem = document.createElement('div');
            resultItem.textContent = currentQuestion.expr.replace('?', userAnswer);
            if (!isCorrect) {
                wrongCount++;
                resultItem.innerHTML += `<span class="wrong">❌ 正确答案：${correctAnswer}</span>`;
            }
            resultArea.appendChild(resultItem);

            // 滚动到最新结果
            resultArea.scrollTop = resultArea.scrollHeight;

            // 下一题
            currentIndex++;
            answerInput.value = '';
            if (currentIndex < questionList.length) {
                currentQuestion = questionList[currentIndex];
                questionArea.textContent = currentQuestion.expr;
            } else {
                // 练习结束
                clearInterval(timer);
                isRunning = false;
                submitBtn.disabled = true;
                questionArea.textContent = '练习完成！';
                const finishedItem = document.createElement('div');
                finishedItem.className = 'finished';
                finishedItem.textContent = `共${questionList.length}题，错误${wrongCount}题，总用时：${timeSpan.textContent}`;
                resultArea.appendChild(finishedItem);
            }
        });

        // 防止重复点击
        startBtn.addEventListener('mousedown', (e) => {
            e.preventDefault();
        });
    </script>
</body>
</html>
