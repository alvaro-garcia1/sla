<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#10131f">
  <title>Calculadora</title>
  <style>
    :root {
      color-scheme: dark;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: #10131f;
      color: #f5f6fb;
    }

    * {
      box-sizing: border-box;
    }

    body {
      min-height: 100vh;
      margin: 0;
      display: grid;
      place-items: center;
      padding: 24px;
      background:
        radial-gradient(ellipse at 20% 15%, rgb(91 72 191 / 24%), transparent 42%),
        radial-gradient(ellipse at 85% 90%, rgb(38 132 157 / 18%), transparent 38%),
        #10131f;
    }

    .calculator {
      width: min(100%, 360px);
      padding: 24px;
      border: 1px solid rgb(255 255 255 / 9%);
      border-radius: 28px;
      background: rgb(26 30 45 / 92%);
      box-shadow: 0 24px 80px rgb(0 0 0 / 38%);
    }

    .heading {
      margin: 0 0 22px;
      color: #aeb5ca;
      font-size: 0.8rem;
      font-weight: 650;
      letter-spacing: 0.16em;
      text-align: center;
      text-transform: uppercase;
    }

    .display {
      min-height: 112px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: flex-end;
      overflow: hidden;
      padding: 14px 4px 20px;
    }

    .expression {
      min-height: 24px;
      color: #929ab2;
      font-size: 0.95rem;
    }

    .result {
      width: 100%;
      overflow: hidden;
      color: #fff;
      font-size: clamp(2.4rem, 12vw, 3.5rem);
      font-variant-numeric: tabular-nums;
      font-weight: 350;
      letter-spacing: -0.06em;
      text-align: right;
      text-overflow: ellipsis;
      white-space: nowrap;
    }

    .keys {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }

    button {
      min-width: 0;
      aspect-ratio: 1;
      border: 0;
      border-radius: 18px;
      background: #2b3043;
      color: #f5f6fb;
      cursor: pointer;
      font: inherit;
      font-size: 1.25rem;
      transition: background 140ms ease, transform 140ms ease;
      -webkit-tap-highlight-color: transparent;
    }

    button:hover {
      background: #383e54;
    }

    button:active {
      transform: scale(0.95);
    }

    button:focus-visible {
      outline: 2px solid #a998ff;
      outline-offset: 2px;
    }

    .utility {
      background: #3a4055;
      color: #d2d6e4;
    }

    .operator {
      background: #34304f;
      color: #c3b8ff;
      font-size: 1.45rem;
    }

    .operator:hover {
      background: #453e68;
    }

    .equals {
      background: #8068ef;
      color: white;
      font-size: 1.5rem;
    }

    .equals:hover {
      background: #927df5;
    }

    .zero {
      grid-column: span 2;
      aspect-ratio: auto;
      text-align: left;
      padding-left: 28px;
    }

    @media (max-width: 380px) {
      .calculator {
        padding: 18px;
      }

      .keys {
        gap: 8px;
      }

      button {
        border-radius: 15px;
      }
    }
  </style>
</head>
<body>
  <main class="calculator" aria-label="Calculadora">
    <h1 class="heading">Calculadora</h1>
    <section class="display" aria-live="polite" aria-atomic="true">
      <div class="expression" id="expression"></div>
      <div class="result" id="result">0</div>
    </section>
    <section class="keys" aria-label="Teclas da calculadora">
      <button class="utility" type="button" data-action="clear" aria-label="Limpar">AC</button>
      <button class="utility" type="button" data-action="sign" aria-label="Trocar sinal">+/−</button>
      <button class="utility" type="button" data-action="percent" aria-label="Porcentagem">%</button>
      <button class="operator" type="button" data-operator="/" aria-label="Dividir">÷</button>

      <button type="button" data-digit="7">7</button>
      <button type="button" data-digit="8">8</button>
      <button type="button" data-digit="9">9</button>
      <button class="operator" type="button" data-operator="*" aria-label="Multiplicar">×</button>

      <button type="button" data-digit="4">4</button>
      <button type="button" data-digit="5">5</button>
      <button type="button" data-digit="6">6</button>
      <button class="operator" type="button" data-operator="-" aria-label="Subtrair">−</button>

      <button type="button" data-digit="1">1</button>
      <button type="button" data-digit="2">2</button>
      <button type="button" data-digit="3">3</button>
      <button class="operator" type="button" data-operator="+" aria-label="Somar">+</button>

      <button class="zero" type="button" data-digit="0">0</button>
      <button type="button" data-action="decimal" aria-label="Vírgula decimal">,</button>
      <button class="equals" type="button" data-action="equals" aria-label="Igual">=</button>
    </section>
  </main>

  <script>
    const resultDisplay = document.querySelector("#result");
    const expressionDisplay = document.querySelector("#expression");
    const keys = document.querySelector(".keys");
    const numberFormat = new Intl.NumberFormat("pt-BR", {
      maximumFractionDigits: 10,
    });

    let currentInput = "0";
    let previousInput = null;
    let operator = null;
    let shouldResetInput = false;
    let hasError = false;

    function formatValue(value) {
      const number = Number(value);
      return Number.isFinite(number) ? numberFormat.format(number) : "Erro";
    }

    function render() {
      resultDisplay.textContent = hasError ? "Erro" : formatValue(currentInput);
      expressionDisplay.textContent = operator && previousInput !== null
        ? `${formatValue(previousInput)} ${operator === "*" ? "×" : operator === "/" ? "÷" : operator}`
        : "";
    }

    function clear() {
      currentInput = "0";
      previousInput = null;
      operator = null;
      shouldResetInput = false;
      hasError = false;
      render();
    }

    function inputDigit(digit) {
      if (hasError) clear();
      if (shouldResetInput) {
        currentInput = digit;
        shouldResetInput = false;
      } else if (currentInput === "0") {
        currentInput = digit;
      } else if (currentInput.replace("-", "").length < 15) {
        currentInput += digit;
      }
      render();
    }

    function inputDecimal() {
      if (hasError) clear();
      if (shouldResetInput) {
        currentInput = "0.";
        shouldResetInput = false;
      } else if (!currentInput.includes(".")) {
        currentInput += ".";
      }
      render();
    }

    function calculate() {
      if (operator === null || previousInput === null) return;

      const first = Number(previousInput);
      const second = Number(currentInput);
      let answer;

      switch (operator) {
        case "+":
          answer = first + second;
          break;
        case "-":
          answer = first - second;
          break;
        case "*":
          answer = first * second;
          break;
        case "/":
          if (second === 0) {
            hasError = true;
            currentInput = "0";
            previousInput = null;
            operator = null;
            shouldResetInput = true;
            render();
            return;
          }
          answer = first / second;
          break;
        default:
          return;
      }

      currentInput = String(Number(answer.toPrecision(12)));
      previousInput = null;
      operator = null;
      shouldResetInput = true;
      render();
    }

    function chooseOperator(nextOperator) {
      if (hasError) clear();
      if (operator !== null && !shouldResetInput) calculate();
      previousInput = currentInput;
      operator = nextOperator;
      shouldResetInput = true;
      render();
    }

    function performAction(action) {
      if (action === "clear") {
        clear();
      } else if (action === "equals") {
        calculate();
      } else if (action === "decimal") {
        inputDecimal();
      } else if (action === "sign" && !hasError) {
        currentInput = String(Number(currentInput) * -1);
        render();
      } else if (action === "percent" && !hasError) {
        currentInput = String(Number(currentInput) / 100);
        render();
      }
    }

    keys.addEventListener("click", (event) => {
      const button = event.target.closest("button");
      if (!button) return;

      if (button.dataset.digit !== undefined) {
        inputDigit(button.dataset.digit);
      } else if (button.dataset.operator) {
        chooseOperator(button.dataset.operator);
      } else if (button.dataset.action) {
        performAction(button.dataset.action);
      }
    });

    document.addEventListener("keydown", (event) => {
      if (/^\d$/.test(event.key)) {
        inputDigit(event.key);
      } else if (event.key === "." || event.key === ",") {
        inputDecimal();
      } else if (["+", "-", "*", "/"].includes(event.key)) {
        chooseOperator(event.key);
      } else if (event.key === "Enter" || event.key === "=") {
        event.preventDefault();
        calculate();
      } else if (event.key === "Escape") {
        clear();
      } else if (event.key === "Backspace" && !hasError) {
        currentInput = shouldResetInput ? "0" : currentInput.slice(0, -1);
        if (currentInput === "" || currentInput === "-") currentInput = "0";
        shouldResetInput = false;
        render();
      }
    });

    render();
  </script>
</body>
</html>
