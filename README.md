#

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>ماشین حساب</title>

    <style>
        body {
            font-family: sans-serif;
            text-align: center;
            margin-top: 40px;
        }

        input {
            width: 250px;
            height: 35px;
            font-size: 18px;
            margin: 10px;
            padding: 5px;
            border: 1px solid #aaa;
            border-radius: 5px;
        }

        button {
            width: 50px;
            height: 40px;
            margin: 5px;
            font-size: 20px;
            background: #e0e0e0;   /* رنگ خیلی ساده */
            border: 1px solid #777;
            border-radius: 5px;
            cursor: pointer;
        }

        button:hover {
            background: #c7c7c7;
        }

        #result {
            margin-top: 20px;
            font-size: 22px;
            padding: 10px;
            border: 1px solid #ddd;
            width: 250px;
            margin-left: auto;
            margin-right: auto;
            border-radius: 5px;
            background: #fafafa;
        }
    </style>
</head>
<body>

    <input type="number" id="num1" placeholder="num1"><br>
    <input type="number" id="num2" placeholder="num2"><br>

    <button onclick="calc('+')">+</button>
    <button onclick="calc('-')">-</button>
    <button onclick="calc('*')">*</button>
    <button onclick="calc('/')">/</button>
    <button onclick="calc('%')">%</button>

    <div id="result">نتیجه</div>

    <script>
        function calc(op) {
            var n1 = Number(document.getElementById("num1").value);
            var n2 = Number(document.getElementById("num2").value);
            var res = 0;

            if (op === "+") res = n1 + n2;
            else if (op === "-") res = n1 - n2;
            else if (op === "*") res = n1 * n2;
            else if (op === "/") {
                if (n2 === 0) res = "خطا";
                else res = n1 / n2;
            }
            else if (op === "%") res = n1 % n2;

            document.getElementById("result").innerHTML = res;
        }
    </script>

</body>
</html>

 -
