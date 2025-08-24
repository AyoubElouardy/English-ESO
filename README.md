# English-ESO
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Aprende inglés para secundaria (ESO) en España con 100 ejercicios progresivos de gramática, vocabulario y comprensión (A2-B1). Inicia sesión con Gmail y sigue tu progreso.">
    <meta name="keywords" content="aprender inglés ESO, inglés secundaria España, ejercicios inglés A2 B1, gramática inglesa, vocabulario ESO, ejercicios progresivos inglés">
    <meta name="author" content="English ESO Learning">
    <title>English ESO Learning: 100 Ejercicios Progresivos</title>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://accounts.google.com/gsi/client" async defer></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background: linear-gradient(to bottom, #f0f4f8, #d9e2ec);
            min-height: 100vh;
            color: #333;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        #container {
            width: 900px;
            max-width: 95%;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        header {
            background: #007bff;
            color: #fff;
            text-align: center;
            padding: 20px;
        }

        header h1 {
            font-size: 32px;
            margin-bottom: 10px;
        }

        nav {
            display: flex;
            justify-content: center;
            background: #f8f9fa;
            padding: 15px;
            border-bottom: 1px solid #ddd;
        }

        nav a {
            color: #007bff;
            text-decoration: none;
            font-size: 18px;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 5px;
            transition: background 0.3s;
        }

        nav a:hover {
            background: #e9ecef;
        }

        .content {
            padding: 30px;
        }

        .lesson, .quiz, .progress {
            margin-bottom: 40px;
        }

        h2 {
            font-size: 26px;
            color: #007bff;
            margin-bottom: 15px;
        }

        p {
            font-size: 16px;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .quiz-question {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
            border: 1px solid #ddd;
        }

        .quiz-question label {
            display: block;
            margin: 10px 0;
            font-size: 16px;
            cursor: pointer;
        }

        .quiz-question input[type="radio"] {
            margin-right: 10px;
        }

        button {
            background: #28a745;
            color: #fff;
            border: none;
            padding: 12px 24px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }

        button:hover {
            background: #218838;
        }

        #quiz-result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
            color: #333;
        }

        #progress-chart {
            max-width: 100%;
            margin-top: 20px;
            background: #fff;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .progress-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }

        .progress-table th, .progress-table td {
            border: 1px solid #ddd;
            padding: 10px;
            text-align: left;
        }

        .progress-table th {
            background: #007bff;
            color: #fff;
        }

        .social-share {
            margin-top: 20px;
            text-align: center;
        }

        .social-share a {
            color: #007bff;
            text-decoration: none;
            margin: 0 10px;
            font-size: 16px;
        }

        #login-section {
            text-align: center;
            padding: 40px;
        }

        #logout-button {
            background: #dc3545;
            margin-top: 20px;
        }

        #logout-button:hover {
            background: #c82333;
        }

        #exercise-list {
            display: none;
        }

        .exercise-item {
            background: #f8f9fa;
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .exercise-item:hover {
            background: #e9ecef;
        }

        #current-exercise {
            display: none;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 24px;
            }

            nav {
                flex-direction: column;
                gap: 10px;
            }

            nav a {
                padding: 8px;
                font-size: 16px;
            }

            .content {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div id="container">
        <header>
            <h1>English ESO Learning: 100 Ejercicios Progresivos</h1>
            <p>Ejercicios para estudiantes de ESO (A2-B1)</p>
        </header>
        <nav>
            <a href="#lessons">Lecciones</a>
            <a href="#exercises">Ejercicios</a>
            <a href="#progress">Progreso</a>
            <a href="#resources">Recursos</a>
        </nav>
        <div class="content">
            <section id="login-section">
                <h2>Inicia Sesión con Gmail</h2>
                <div id="g_id_onload"
                     data-client_id="YOUR_CLIENT_ID.apps.googleusercontent.com"
                     data-callback="handleCredentialResponse"
                     data-use_fedcm_for_prompt="true">
                </div>
                <div class="g_id_signin"
                     data-type="standard"
                     data-size="large"
                     data-theme="outline"
                     data-text="sign_in_with"
                     data-shape="rectangular"
                     data-logo_alignment="left">
                </div>
                <p>Reemplaza YOUR_CLIENT_ID con tu Client ID de Google Cloud Console.</p>
            </section>
            <section id="lessons" class="lesson" style="display: none;">
                <h2>Lecciones de Inglés para ESO</h2>
                <p>Accede a 100 ejercicios progresivos, desde nivel A2 hasta B1, diseñados para el currículo de ESO.</p>
                <p>Los ejercicios cubren gramática, vocabulario y comprensión, empezando con temas básicos como Present Simple y avanzando hacia estructuras más complejas como condicionales.</p>
            </section>
            <section id="exercises" style="display: none;">
                <h2>Ejercicios Progresivos</h2>
                <div id="exercise-list"></div>
                <div id="current-exercise">
                    <h3 id="exercise-title"></h3>
                    <p id="exercise-question"></p>
                    <div id="exercise-options"></div>
                    <button onclick="finalizeExercise()">Finalizar Ejercicio</button>
                    <div id="exercise-result"></div>
                </div>
            </section>
            <section id="progress" class="progress" style="display: none;">
                <h2>Tu Progreso</h2>
                <p>Consulta tu progreso en los 100 ejercicios.</p>
                <canvas id="progress-chart" width="600" height="300"></canvas>
                <table class="progress-table">
                    <tr>
                        <th>Ejercicio</th>
                        <th>Estado</th>
                    </tr>
                    <!-- Filas generadas dinámicamente -->
                </table>
            </section>
            <section id="resources" class="resources" style="display: none;">
                <h2>Recursos Adicionales</h2>
                <p>Explora más herramientas para mejorar tu inglés:</p>
                <ul>
                    <li><a href="https://www.bbc.co.uk/learningenglish/" target="_blank">BBC Learning English</a></li>
                    <li><a href="https://www.duolingo.com/" target="_blank">Duolingo</a></li>
                    <li><a href="https://www.cambridgeenglish.org/" target="_blank">Cambridge English</a></li>
                </ul>
            </section>
            <button id="logout-button" onclick="logout()" style="display: none;">Cerrar Sesión</button>
            <div class="social-share">
                <p>¡Comparte esta página!</p>
                <a href="https://x.com/share?url=https://english-eso-learning.com&text=¡Aprende inglés para ESO con 100 ejercicios progresivos!" target="_blank">Compartir en X</a>
            </div>
        </div>
    </div>

    <script>
        // Generar 100 ejercicios progresivos
        const exercises = Array.from({length: 100}, (_, i) => {
            const level = Math.floor(i / 20); // Divide en 5 niveles de dificultad
            const topics = [
                // Nivel 1 (1-20): Present Simple (A2, fácil)
                () => ({
                    title: `Ejercicio ${i+1}: Present Simple`,
                    question: `Complete: I ___ to school every day.`,
                    options: ['go', 'goes', 'going'],
                    correct: 0
                }),
                // Nivel 2 (21-40): Present Continuous (A2, medio)
                () => ({
                    title: `Ejercicio ${i+1}: Present Continuous`,
                    question: `Complete: They ___ football now.`,
                    options: ['play', 'are playing', 'plays'],
                    correct: 1
                }),
                // Nivel 3 (41-60): Past Simple (A2-B1, medio)
                () => ({
                    title: `Ejercicio ${i+1}: Past Simple`,
                    question: `Complete: She ___ to the park yesterday.`,
                    options: ['go', 'went', 'gone'],
                    correct: 1
                }),
                // Nivel 4 (61-80): Future Tenses (B1, medio-avanzado)
                () => ({
                    title: `Ejercicio ${i+1}: Future Tense`,
                    question: `Complete: We ___ to London next week.`,
                    options: ['will go', 'go', 'going'],
                    correct: 0
                }),
                // Nivel 5 (81-100): Second Conditional (B1, avanzado)
                () => ({
                    title: `Ejercicio ${i+1}: Second Conditional`,
                    question: `Complete: If I ___ rich, I ___ travel the world.`,
                    options: ['am / will', 'were / would', 'was / will'],
                    correct: 1
                })
            ];
            return topics[Math.min(level, topics.length - 1)]();
        });

        let userEmail = null;
        let progress = Array(100).fill(false); // true si completado correctamente
        let currentExerciseIndex = -1;

        // Manejar respuesta de Google
        function handleCredentialResponse(response) {
            const responsePayload = JSON.parse(atob(response.credential.split('.')[1]));
            userEmail = responsePayload.email;
            document.getElementById('login-section').style.display = 'none';
            document.querySelectorAll('.content section').forEach(sec => sec.style.display = 'block');
            document.getElementById('logout-button').style.display = 'block';
            loadProgress();
            loadExerciseList();
        }

        // Cerrar sesión
        function logout() {
            google.accounts.id.disableAutoSelect();
            userEmail = null;
            document.getElementById('login-section').style.display = 'block';
            document.querySelectorAll('.content section').forEach(sec => sec.style.display = 'none');
            document.getElementById('logout-button').style.display = 'none';
            document.getElementById('current-exercise').style.display = 'none';
            document.getElementById('exercise-list').innerHTML = '';
        }

        // Cargar progreso de localStorage
        function loadProgress() {
            const savedProgress = localStorage.getItem(`progress_${userEmail}`);
            if (savedProgress) {
                progress = JSON.parse(savedProgress);
            }
            updateProgressChart();
            updateProgressTable();
        }

        // Guardar progreso
        function saveProgress() {
            localStorage.setItem(`progress_${userEmail}`, JSON.stringify(progress));
        }

        // Cargar lista de ejercicios
        function loadExerciseList() {
            const list = document.getElementById('exercise-list');
            list.style.display = 'block';
            list.innerHTML = '';
            exercises.forEach((ex, index) => {
                const item = document.createElement('div');
                item.className = 'exercise-item';
                item.textContent = `${ex.title} ${progress[index] ? '(Completado)' : ''}`;
                item.onclick = () => loadExercise(index);
                list.appendChild(item);
            });
        }

        // Cargar ejercicio actual
        function loadExercise(index) {
            currentExerciseIndex = index;
            const ex = exercises[index];
            document.getElementById('exercise-title').textContent = ex.title;
            document.getElementById('exercise-question').textContent = ex.question;
            const optionsDiv = document.getElementById('exercise-options');
            optionsDiv.innerHTML = '';
            ex.options.forEach((opt, optIndex) => {
                const label = document.createElement('label');
                const radio = document.createElement('input');
                radio.type = 'radio';
                radio.name = 'exercise-option';
                radio.value = optIndex;
                label.appendChild(radio);
                label.appendChild(document.createTextNode(opt));
                optionsDiv.appendChild(label);
            });
            document.getElementById('exercise-result').textContent = '';
            document.getElementById('current-exercise').style.display = 'block';
        }

        // Finalizar ejercicio
        function finalizeExercise() {
            const selected = document.querySelector('input[name="exercise-option"]:checked');
            if (!selected) {
                alert('Selecciona una opción');
                return;
            }
            const selectedIndex = parseInt(selected.value);
            const ex = exercises[currentExerciseIndex];
            const isCorrect = selectedIndex === ex.correct;
            document.getElementById('exercise-result').textContent = isCorrect ? '¡Correcto!' : 'Incorrecto. Intenta de nuevo.';
            document.getElementById('exercise-result').style.color = isCorrect ? '#28a745' : '#dc3545';
            if (isCorrect) {
                progress[currentExerciseIndex] = true;
                saveProgress();
                loadExerciseList();
                updateProgressChart();
                updateProgressTable();
            }
        }

        // Inicializar gráfico de Chart.js
        const chartCtx = document.getElementById('progress-chart').getContext('2d');
        const progressChart = new Chart(chartCtx, {
            type: 'bar',
            data: {
                labels: exercises.map((_, i) => `Ej ${i+1}`),
                datasets: [{
                    label: 'Completado',
                    data: progress.map(p => p ? 100 : 0),
                    backgroundColor: progress.map(p => p ? '#28a745' : '#dc3545')
                }]
            },
            options: {
                scales: {
                    y: { beginAtZero: true, max: 100 },
                    x: { title: { display: true, text: 'Ejercicios' } }
                },
                plugins: {
                    title: { display: true, text: 'Progreso en Ejercicios' }
                }
            }
        });

        // Actualizar gráfico
        function updateProgressChart() {
            progressChart.data.datasets[0].data = progress.map(p => p ? 100 : 0);
            progressChart.data.datasets[0].backgroundColor = progress.map(p => p ? '#28a745' : '#dc3545');
            progressChart.update();
        }

        // Actualizar tabla de progreso
        function updateProgressTable() {
            const table = document.querySelector('.progress-table');
            table.innerHTML = '<tr><th>Ejercicio</th><th>Estado</th></tr>';
            progress.forEach((p, i) => {
                const row = document.createElement('tr');
                row.innerHTML = `<td>Ejercicio ${i+1}</td><td>${p ? 'Completado' : 'Pendiente'}</td>`;
                table.appendChild(row);
            });
        }

        // Actualizar tabla inicialmente
        updateProgressTable();
    </script>
</body>
</html>
