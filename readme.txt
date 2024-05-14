E se precisarmos utilizar imagem em nossas perguntas?

Primeiramente devemos adicionar a pergunta no arquivo "script.js", criando a variavel 'img' e passando
o caminho da imagem (img: 'img/imagem.png'), logo após devemos acessar o arquivo 'app.js' e localizarmos
a 'function getNewQuestion' e adicionarmos este código:
if(currentQuestion.hasOwnProperty("img")){
    const img = document.createElement("img");
    img.src = currentQuestion.img;
    questionText.appendChild(img);
}
Logo após devemos acessarmos o nosso código CSS e adicionarmos este código:
.quiz-box .question-text img{
    max-width: 100%;
    display: block;
    margin-top: 15px;
}

E se tivermos um total de 30 ou mais perguntas e desejarmos adicionar apenas 10?

No arquivo 'app.js' criamos uma const (const questionLimit = 10) e alteramos todas as variaveis chamada
'quiz.length'.