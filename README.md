# alexandre
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Quiz de Informática</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(120deg, #e3f2fd, #c8e6c9);
            margin: 0;
            padding: 30px;
            display: flex;
            justify-content: center;
            align-items: start;
            min-height: 100vh;
        }

        .container {
            background-color: #ffffff;
            border-radius: 12px;
            padding: 30px 40px;
            max-width: 900px;
            width: 100%;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            animation: fadeIn 0.5s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 30px;
            font-size: 32px;
        }

        .questão {
            margin-bottom: 35px;
            padding-bottom: 20px;
            border-bottom: 1px solid #ccc;
        }

        .questão img {
            width: 100%;
            max-width: 600px;
            height: auto;
            display: block;
            margin: 0 auto 15px;
            border-radius: 10px;
        }

        .questão p {
            font-size: 20px;
            font-weight: 600;
            color: #444;
            margin-bottom: 12px;
        }

        ul {
            list-style: none;
            padding-left: 0;
        }

        li label {
            display: block;
            background: #f0f4f8;
            margin: 8px 0;
            padding: 12px;
            border-radius: 6px;
            transition: 0.3s;
            cursor: pointer;
        }

        li label:hover {
            background-color: #dcedc8;
        }

        input[type="radio"] {
            margin-right: 10px;
        }

        button {
            background-color: #4caf50;
            color: white;
            font-size: 16px;
            padding: 12px 24px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 20px;
            transition: background 0.3s;
        }

        button:hover {
            background-color: #388e3c;
        }

        #result {
            text-align: center;
            font-size: 22px;
            font-weight: bold;
            margin-top: 30px;
            color: #2e7d32;
            transition: 0.4s;
        }

        .erro {
            color: rgb(206, 5, 5);
            text-align: center;
            font-weight: bold;
            margin-top: 15px;
        }

        .ação {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        @media (max-width: 600px) {
            .questão p {
                font-size: 18px;
            }

            button {
                width: 100%;
            }

            .ação {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Quiz de Informática</h1>

    <form id="quizForm">
        <!-- As 12 questões completas foram incluídas -->
        <div class="questão">
            <img src="https://i.imgur.com/QJXlpRW.jpg" alt="Atalhos do Windows">
            <p>1. Qual é o atalho para copiar um texto no Windows?</p>
            <ul>
                <li><label><input type="radio" name="q1" value="a"> Ctrl + X</label></li>
                <li><label><input type="radio" name="q1" value="b"> Ctrl + C</label></li>
                <li><label><input type="radio" name="q1" value="c"> Ctrl + V</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/zv0KVVt.png" alt="Hardware e Software">
            <p>2. A imagem representa a diferença entre hardware e software. Qual é a definição correta de software?</p>
            <ul>
                <li><label><input type="radio" name="q2" value="a"> A parte física do computador</label></li>
                <li><label><input type="radio" name="q2" value="b"> Os programas e sistemas operacionais</label></li>
                <li><label><input type="radio" name="q2" value="c"> Os cabos de energia</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/70eYrEJ.png" alt="Dispositivos de Entrada">
            <p>3. Qual dos seguintes é um dispositivo de entrada de dados?</p>
            <ul>
                <li><label><input type="radio" name="q3" value="a"> Monitor</label></li>
                <li><label><input type="radio" name="q3" value="b"> Impressora</label></li>
                <li><label><input type="radio" name="q3" value="c"> Teclado</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/SUtSRM4.png" alt="Ícones de Navegadores">
            <p>4. Qual desses é um navegador de internet?</p>
            <ul>
                <li><label><input type="radio" name="q4" value="a"> Microsoft Word</label></li>
                <li><label><input type="radio" name="q4" value="b"> Google Chrome</label></li>
                <li><label><input type="radio" name="q4" value="c"> Windows Explorer</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/dvCQdbp.png" alt="Tipos de Arquivos">
            <p>5. O que significa um arquivo com a extensão .jpg?</p>
            <ul>
                <li><label><input type="radio" name="q5" value="a"> Documento de texto</label></li>
                <li><label><input type="radio" name="q5" value="b"> Imagem</label></li>
                <li><label><input type="radio" name="q5" value="c"> Planilha eletrônica</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/7LzfqGb.png" alt="Disco Rígido">
            <p>6. O que é HD (disco rígido)?</p>
            <ul>
                <li><label><input type="radio" name="q6" value="a"> Memória RAM</label></li>
                <li><label><input type="radio" name="q6" value="b"> Unidade de processamento gráfico</label></li>
                <li><label><input type="radio" name="q6" value="c"> Dispositivo de armazenamento de dados</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/ZFFfFGx.png" alt="Atualização do Windows">
            <p>7. Por que é importante manter o sistema operacional atualizado?</p>
            <ul>
                <li><label><input type="radio" name="q7" value="a"> Para consumir mais memória</label></li>
                <li><label><input type="radio" name="q7" value="b"> Para corrigir falhas e aumentar a segurança</label></li>
                <li><label><input type="radio" name="q7" value="c"> Para deixar o computador mais lento</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/Bn5hN4q.png" alt="CPU">
            <p>8. O que significa a sigla CPU?</p>
            <ul>
                <li><label><input type="radio" name="q8" value="a"> Unidade Central de Processamento</label></li>
                <li><label><input type="radio" name="q8" value="b"> Controle de Periféricos Universais</label></li>
                <li><label><input type="radio" name="q8" value="c"> Unidade de Energia Principal</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/LMRy8qY.png" alt="Nuvem">
            <p>9. O que é computação em nuvem?</p>
            <ul>
                <li><label><input type="radio" name="q9" value="a"> Tipo de cabo de rede</label></li>
                <li><label><input type="radio" name="q9" value="b"> Armazenamento e acesso a dados pela internet</label></li>
                <li><label><input type="radio" name="q9" value="c"> Método de refrigeração</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/C1XTXc3.png" alt="Tecla F5">
            <p>10. O que acontece ao pressionar F5 no navegador?</p>
            <ul>
                <li><label><input type="radio" name="q10" value="a"> Atualiza a página</label></li>
                <li><label><input type="radio" name="q10" value="b"> Fecha o navegador</label></li>
                <li><label><input type="radio" name="q10" value="c"> Abre o gerenciador de tarefas</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/M0zKkKe.png" alt="Android">
            <p>11. Qual destes é um sistema operacional para celulares?</p>
            <ul>
                <li><label><input type="radio" name="q11" value="a"> Android</label></li>
                <li><label><input type="radio" name="q11" value="b"> Linux Mint</label></li>
                <li><label><input type="radio" name="q11" value="c"> Windows 10</label></li>
            </ul>
        </div>

        <div class="questão">
            <img src="https://i.imgur.com/7szFGLx.png" alt="Phishing">
            <p>12. O que é phishing?</p>
            <ul>
                <li><label><input type="radio" name="q12" value="a"> Ataque físico ao computador</label></li>
                <li><label><input type="radio" name="q12" value="b"> Tipo de software de antivírus</label></li>
                <li><label><input type="radio" name="q12" value="c"> Tentativa de enganar o usuário para obter dados</label></li>
            </ul>
        </div>

        <div class="ação">
            <button type="button" onclick="verificarRespostas()">Enviar</button>
            <button type="button" onclick="reiniciarQuiz()">Reiniciar</button>
        </div>
    </form>

    <div id="result"></div>
    <div id="error" class="erro"></div>
</div>

<script>
    function verificarRespostas() {
        const respostasCorretas = {
            q1: "b", q2: "b", q3: "c", q4: "b", q5: "b",
            q6: "c", q7: "b", q8: "a", q9: "b", q10: "a",
            q11: "a", q12: "c"
        };

        let pontuacao = 0;
        let total = Object.keys(respostasCorretas).length;
        let todasRespondidas = true;

        for (let q in respostasCorretas) {
            const resposta = document.querySelector(input[name="${q}"]:checked);
            if (!resposta) {
                todasRespondidas = false;
                break;
            }
        }

        const result = document.getElementById("result");
        const error = document.getElementById("error");

        if (!todasRespondidas) {
            error.innerText = "Por favor, responda todas as perguntas antes de enviar.";
            result.innerText = "";
            window.scrollTo({ top: 0, behavior: 'smooth' });
            return;
        }

        error.innerText = "";

        for (let q in respostasCorretas) {
            const respostaSelecionada = document.querySelector(input[name="${q}"]:checked);
            if (respostaSelecionada.value === respostasCorretas[q]) {
                pontuacao++;
            }
        }

        result.innerText = 🎉 Você acertou ${pontuacao} de ${total} perguntas!;
        result.style.transform = "scale(1.1)";
        setTimeout(() => result.style.transform = "scale(1)", 200);
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    function reiniciarQuiz() {
        document.getElementById("quizForm").reset();
        document.getElementById("result").innerText = "";
        document.getElementById("error").innerText = "";
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }
</script>

</body>
</html>
 
