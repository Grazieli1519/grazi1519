# grazi1519
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo de Aventura</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="game-container">
        <h1>Aventura Interativa</h1>
        <p id="story">Você acorda em uma floresta desconhecida. O que você faz?</p>
        <div id="choices">
            <button onclick="chooseOption(1)">Explorar a floresta</button>
            <button onclick="chooseOption(2)">Gritar por ajuda</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #e0f7fa;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

#game-container {
    background-color: #ffffff;
    border: 2px solid #00897b;
    border-radius: 10px;
    padding: 20px;
    text-align: center;
    width: 300px;
}

button {
    margin: 10px;
    padding: 10px;
    background-color: #00796b;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #004d40;
}
function chooseOption(option) {
    const storyElement = document.getElementById('story');
    const choicesElement = document.getElementById('choices');

    if (option === 1) {
        storyElement.textContent = 'Você encontra um caminho que leva a uma pequena vila.';
        choicesElement.innerHTML = `
            <button onclick="chooseOption(3)">Ir para a vila</button>
            <button onclick="chooseOption(4)">Voltar para a floresta</button>
        `;
    } else if (option === 2) {
        storyElement.textContent = 'Seu grito atraiu uma criatura misteriosa!';
        choicesElement.innerHTML = `
            <button onclick="chooseOption(5)">Enfrentar a criatura</button>
            <button onclick="chooseOption(6)">Fugir</button>
        `;
    } else if (option === 3) {
        storyElement.textContent = 'Na vila, você encontra um mercador amigável que oferece ajuda.';
        choicesElement.innerHTML = `<button onclick="chooseOption(7)">Conversar com o mercador</button>`;
    }
    // Continue a expandir a lógica para outras opções...
}
