<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Artist Draw!</title>
    <style>
        body {
            margin: 0;
            font-family: 'Poppins', sans-serif;
            display: flex;
            flex-direction: column;
            height: 100vh;
            background: #f4f4f4;
            overflow: hidden;
        }
        .header {
            background: #005BAC;
            color: white;
            padding: 15px;
            text-align: center;
            font-size: 1.8rem;
            font-weight: bold;
        }
        .toolbar {
            display: flex;
            justify-content: center;
            align-items: center;
            background: white;
            padding: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            gap: 15px;
            width: 100%; /* Ensure toolbar spans full width */
            box-sizing: border-box; /* Include padding in width calculation */
        }
        .toolbar input, .toolbar button {
            padding: 10px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        input[type="color"] {
            width: 50px;
            height: 50px;
            border: none;
            cursor: pointer;
        }
        input[type="range"] {
            width: 150px; /* Ensure width is adequate for user interaction */
        }
        button {
            background-color: #00c897;
            color: white;
            font-weight: bold;
        }
        button#eraserButton {
            background-color: #ff4757;
        }
        .canvas-container {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            background: white;
        }
        canvas {
            background-color: white;
            cursor: crosshair;
            border-radius: 10px;
            box-shadow: 0px 6px 15px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body>
    <div class="header">Artist Draw!</div>
    <div class="toolbar">
        <input type="color" id="colorPicker" value="#000000">
        <input type="range" id="brushSize" min="1" max="50" value="5">
        <button onclick="clearCanvas()">Clear</button>
        <button onclick="toggleEraser()" id="eraserButton">Eraser</button>
    </div>
    <div class="canvas-container">
        <canvas id="drawingCanvas"></canvas>
    </div>
    <script>
        const canvas = document.getElementById("drawingCanvas");
        const ctx = canvas.getContext("2d");

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight - document.querySelector('.header').offsetHeight - document.querySelector('.toolbar').offsetHeight;
            clearCanvas();
        }

        let drawing = false;
        let erasing = false;
        let brushColor = document.getElementById("colorPicker").value;
        let brushSize = document.getElementById("brushSize").value; // Initialize brush size

        canvas.addEventListener("mousedown", (event) => {
            drawing = true;
            ctx.beginPath();
            draw(event);
        });

        canvas.addEventListener("mouseup", () => {
            drawing = false;
        });

        canvas.addEventListener("mousemove", draw);

        document.getElementById("colorPicker").addEventListener("input", (event) => {
            brushColor = event.target.value;
        });

        document.getElementById("brushSize").addEventListener("input", (event) => {
            brushSize = event.target.value; // Update brush size when slider changes
        });

        function draw(event) {
            if (!drawing) return;

            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;

            ctx.lineWidth = brushSize; // Use updated brush size
            ctx.lineCap = "round";
            ctx.strokeStyle = erasing ? "white" : brushColor;

            ctx.lineTo(x, y);
            ctx.stroke();
            ctx.beginPath();
            ctx.moveTo(x, y);
        }

        function clearCanvas() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
        }

        function toggleEraser() {
            erasing = !erasing;
            document.getElementById("eraserButton").innerText = erasing ? "Draw" : "Eraser";
        }

        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
    </script>
</body>
</html>
