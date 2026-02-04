
💡 Interruptor por Gestos com IA
Este projeto é uma aplicação web experimental que utiliza Inteligência Artificial para controlar o ambiente (neste caso, a cor do fundo da página) através de gestos manuais capturados pela webcam.

🚀 Como funciona?
A aplicação utiliza um modelo de Visão Computacional treinado no Google Teachable Machine. O código monitora o vídeo da webcam em tempo real e, quando detecta um gesto específico com mais de 90% de confiança, executa uma ação:

Sinal de Positivo (👍): Ativa a classe "Ligado", tornando o fundo da tela branco.

Sinal de Negativo (👎): Ativa a classe "Desligado", tornando o fundo da tela preto.

🛠️ Tecnologias Utilizadas
HTML5 & CSS3: Para a estrutura e transições suaves de cores.

JavaScript (ES6): Para a lógica de manipulação do DOM.

TensorFlow.js: Biblioteca utilizada para carregar e rodar o modelo de aprendizado de máquina diretamente no navegador.

Teachable Machine: Ferramenta utilizada para treinar o modelo de classificação de imagem.

📦 Como rodar o projeto

Clone ou copie o código do arquivo index.html.

Abra o arquivo em qualquer navegador moderno (Chrome, Edge, Firefox).

Clique no botão "Ativar Monitor de Gestos".

Autorize o acesso à câmera quando o navegador solicitar.

Faça os gestos:

Mostre o polegar para cima (👍) para "ligar a luz".

Mostre o polegar para baixo (👎) para "apagar a luz".

🔍 Detalhes Técnicos do Modelo
O modelo está hospedado em:
https://teachablemachine.withgoogle.com/models/dyhTt2Eiw/

A lógica principal reside na função predict(), que lê os labels (etiquetas) vindos da IA e altera o estilo CSS do body do HTML:

JavaScript

if (pName === "Ligado" && pValue > 0.90) {
    document.body.style.backgroundColor = "#ffffff"; // Branco
} else if (pName === "Desligado" && pValue > 0.90) {
    document.body.style.backgroundColor = "#121212"; // Preto
}
