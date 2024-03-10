<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Контроль Доходов и Расходов</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: black;
            color: white;
            margin: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        h1 {
            margin-bottom: 10px;
        }
        .form-container {
            display: flex;
            width: 100%;
            max-width: 300px; /* Уменьшили ширину для мобильных устройств */
            margin-bottom: 10px;
        }
        .form {
            flex: 1;
            margin-right: 5px;
        }
        .input-field {
            width: calc(100% - 10px);
            padding: 5px;
            font-size: 14px; /* Уменьшили размер шрифта */
            margin-bottom: 5px;
            border: 1px solid green;
            border-radius: 3px;
            background-color: black;
            color: white;
        }
        .button {
            width: calc(100% - 10px);
            padding: 8px;
            font-size: 14px; /* Уменьшили размер шрифта */
            background-color: green;
            color: white;
            border: none;
            border-radius: 3px;
            cursor: pointer;
        }
        .result {
            font-size: 16px; /* Уменьшили размер шрифта */
            font-weight: bold;
            color: green;
            margin-bottom: 5px;
        }
        .list-container {
            display: flex;
            flex-direction: column; /* Изменили направление для мобильных устройств */
            align-items: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 300px; /* Уменьшили ширину для мобильных устройств */
        }
        .transaction-list {
            width: 100%;
            list-style: none;
            padding: 0;
            text-align: center;
            margin-bottom: 10px;
        }
        .transaction-item {
            font-size: 14px; /* Уменьшили размер шрифта */
            margin-bottom: 3px;
            color: green;
            display: flex;
            justify-content: space-between;
        }
        .transaction-item button {
            background-color: red;
            color: white;
            border: none;
            padding: 3px;
            margin-left: 5px;
            cursor: pointer;
        }
        .total-container {
            width: 100%;
            max-width: 300px; /* Уменьшили ширину для мобильных устройств */
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        .total {
            font-size: 16px; /* Уменьшили размер шрифта */
            font-weight: bold;
            color: green;
            text-align: center;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <h1>Контроль Доходов и Расходов</h1>
    <div class="form-container">
        <div class="form">
            <label for="incomeInput">Доход: </label>
            <input type="number" id="incomeInput" class="input-field" placeholder="Сумма" oninput="calculatePercentage('income')">
            <button class="button" onclick="addTransaction('income')">Добавить</button>
            <div class="result income-result">Доход в процентах: 0%</div>
        </div>

        <div class="form">
            <label for="expenseInput">Расход: </label>
            <input type="number" id="expenseInput" class="input-field" placeholder="Сумма" oninput="calculatePercentage('expense')">
            <button class="button" onclick="addTransaction('expense')">Добавить</button>
            <div class="result expense-result">Расход в процентах: 0%</div>
        </div>
    </div>

    <div class="list-container">
        <ul id="incomeList" class="transaction-list"></ul>
        <ul id="expenseList" class="transaction-list"></ul>
    </div>

    <div class="total-container">
        <div id="total" class="total">Баланс: 0 KZT</div>
    </div>

    <script>
        // Ваш JavaScript код остается без изменений
    </script>
</body>
</html>
