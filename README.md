<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>学生信息查询</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        input[type="text"] {
            padding: 10px;
            margin: 10px 0;
            width: 80%;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .result {
            margin-top: 20px;
            font-size: 1.2em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>学生信息查询</h1>
        <input type="text" id="nameInput" placeholder="请输入中文姓名">
        <button onclick="searchStudent()">查询</button>
        <div class="result" id="result"></div>
    </div>

    <script>
        // 学生数据
        const students = {
            "卞俊涵": {账号: "PD2023B01", 密码: "832392"},
            "黄语恩": {账号: "PD2023B03", 密码: "903205"},
            "蒋澜若": {账号: "PD2023B04", 密码: "188562"},
            "李姵谊": {账号: "PD2023B05", 密码: "334343"},
            "王曦紫": {账号: "PD2023B06", 密码: "442337"},
            "汪行之": {账号: "PD2023B07", 密码: "846291"},
            "杨颜溪": {账号: "PD2023B09", 密码: "915105"},
            "余佳玥": {账号: "PD2023B10", 密码: "625478"},
            "邹芊羽": {账号: "PD2023B11", 密码: "154129"},
            "李泯德": {账号: "PD2023B14", 密码: "747743"},
            "李浚霆": {账号: "PD2023B16", 密码: "142737"},
            "罗兆然": {账号: "PD2023B17", 密码: "784177"},
            "吕以泽": {账号: "PD2023B18", 密码: "682071"},
            "茅书禾": {账号: "PD2023B19", 密码: "429184"},
            "汪轾源": {账号: "PD2023B20", 密码: "198312"},
            "许天佑": {账号: "PD2023B21", 密码: "736191"},
            "许若恩": {账号: "PD2023B22", 密码: "471423"},
            "周之安": {账号: "PD2023B25", 密码: "694581"},
            "王雅靖": {账号: "PD2023B27", 密码: "887799"},
            "刘宇轩": {账号: "PD2023B28", 密码: "453623"},
            "袁寄书": {账号: "PD2023B29", 密码: "639221"},
            "孙鸣阳": {账号: "PD2023B30", 密码: "912332"},
            "王嘉辉": {账号: "PD2023B31", 密码: "854130"},
            "陈嘉泽": {账号: "PD2023B32", 密码: "681247"},
            "刘逸楷": {账号: "PD2023B33", 密码: "325217"}
        };

        function searchStudent() {
            const name = document.getElementById("nameInput").value;
            const resultDiv = document.getElementById("result");
            if (students[name]) {
                resultDiv.innerHTML = `账号: ${students[name].账号}<br>密码: ${students[name].密码}`;
            } else {
                resultDiv.innerHTML = "未找到该学生信息";
            }
        }
    </script>
</body>
</html>
