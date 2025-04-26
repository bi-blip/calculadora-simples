<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Calculadora Simples</title>
    <link rel="stylesheet" href="style.css">
    
</head>
<body>

<div class="calculator">
    <input type="text" id="display" disabled>
    <div class="buttons">
        <button onclick="clearDisplay()">C</button>
        <button onclick="appendValue('7')">7</button>
        <button onclick="appendValue('8')">8</button>
        <button onclick="appendValue('9')">9</button>
        <button onclick="appendValue('/')">/</button>

        <button onclick="appendValue('4')">4</button>
        <button onclick="appendValue('5')">5</button>
        <button onclick="appendValue('6')">6</button>
        <button onclick="appendValue('')"></button>

        <button onclick="appendValue('1')">1</button>
        <button onclick="appendValue('2')">2</button>
        <button onclick="appendValue('3')">3</button>
        <button onclick="appendValue('-')">-</button>

        <button onclick="appendValue('0')">0</button>
        <button onclick="appendValue('.')">.</button>
        <button onclick="calculateResult()">=</button>
        <button onclick="appendValue('+')">+</button>
    </div>
</div>
<style>
      body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #35033a;
    margin: 0;
}

.calculator {
    background: #4e0323;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(0,0,0,0.1);
}

#display {
    width: 100%;
    height: 50px;
    font-size: 24px;
    text-align: right;
    margin-bottom: 10px;
    padding: 5px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

button {
    height: 50px;
    font-size: 20px;
    border: none;
    border-radius: 5px;
    background: #e0e0e0;
    cursor: pointer;
    transition: background 0.3s;
}

button:hover {
    background: #d0d0d0;
}
</style>

<script>
        function appendValue(value) {
    document.getElementById('display').value += value;
}

function clearDisplay() {
    document.getElementById('display').value = '';
}

function calculateResult() {
    try {
        document.getElementById('display').value = eval(document.getElementById('display').value);
    } catch (error) {
        alert('Erro na expressão');
    }
}


</script>


</body>
</html>
