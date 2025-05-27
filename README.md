🎟️ e-Ticket
Um sistema simples de compra de ingressos desenvolvido com HTML, CSS e JavaScript.

📋 Descrição
Este projeto simula uma plataforma online de vendas de ingressos, onde os usuários podem:

✅ Selecionar o tipo de ingresso (Inferior, Superior ou Pista)
✅ Informar a quantidade desejada (até 10)
✅ Comprar ingressos e reduzir o estoque disponível em tempo real
✅ Visualizar as quantidades atualizadas de ingressos disponíveis
✅ Receber alertas de confirmação ou erro conforme a disponibilidade do estoque

O foco principal do projeto é praticar manipulação do DOM, eventos e lógica condicional com JavaScript.

🖼️ Prévia do Projeto
<img src="./assets/PNG/Logo e-tricket.png" alt="Logo e-Ticket" width="200"/>
🛠️ Tecnologias Utilizadas
HTML5 — Estrutura da página

CSS3 — Estilos visuais e layout

JavaScript (ES6) — Lógica para compra e controle de estoque

Google Fonts — Fontes Chakra Petch e Inter

🚀 Funcionalidades
🏷️ Seleção do tipo de ingresso via dropdown

🔢 Campo de input para informar a quantidade

⚠️ Verificação de estoque com atualização em tempo real

✅ Confirmação de compra com alertas

❌ Alerta para estoque insuficiente

📁 Estrutura do Projeto
pgsql
Copiar
Editar
e-ticket/
├── assets/
│   ├── PNG/
│   │   └── Logo e-tricket.png
│   ├── SVG/
│   │   └── Hachuras.svg
│   └── Ingresso.svg
├── js/
│   └── app.js
├── styles/
│   ├── _reset.css
│   └── style.css
├── index.html
└── README.md
🧑‍💻 Como Funciona
HTML
Define a estrutura com:

Cabeçalho: Logo

Conteúdo Principal: Formulário com opções de ingresso, campo para quantidade e botão de compra

Seção: Exibe as quantidades disponíveis para cada tipo de ingresso

JavaScript
Implementa a lógica principal:

javascript
Copiar
Editar
function comprar() {
    let tipo = document.getElementById('tipo-ingresso')
    let qtd = parseInt(document.getElementById('qtd').value)

    if(tipo.value == 'pista') {
        comprarPista(qtd)
    } else if (tipo.value == 'superior') {
        comprarSuperior(qtd)
    } else {
        comprarInferior(qtd)
    }
}
Cada tipo de ingresso possui sua própria função de verificação e atualização. Por exemplo:

javascript
Copiar
Editar
function comprarPista(qtd) {
    let qtdPista = parseInt(document.getElementById('qtd-pista').textContent)
    if (qtd > qtdPista) {
        alert("Quantidade indisponível para tipo de pista")
    } else {
        qtdPista -= qtd
        document.getElementById('qtd-pista').textContent = qtdPista
        alert("Compra realizada com sucesso")
    }
}
O mesmo se aplica para os ingressos Superior e Inferior.

⚙️ Como Executar o Projeto
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seu-usuario/e-ticket.git
Navegue até a pasta do projeto:

bash
Copiar
Editar
cd e-ticket
Abra o arquivo index.html no seu navegador preferido.

✅ Não é necessário servidor ou instalação de pacotes!

🎯 Principais Aprendizados
Manipulação do DOM com getElementById e textContent

Lógica condicional para validar estoque e compras

Programação orientada a eventos com onclick

Organização limpa com separação de HTML, CSS e JavaScript

🚫 Limitações
❌ Não possui persistência de dados: o estoque é reiniciado ao atualizar a página

❌ Sem integração com backend ou sistema de pagamento

❌ Sem validação de entrada além dos atributos HTML min e max

🤝 Contribuições
Contribuições, melhorias e sugestões são bem-vindas!
Sinta-se à vontade para forkar o projeto, criar uma nova branch e enviar um pull request.

📄 Licença
Licença MIT.

✨ Autor
Desenvolvido por Vinnícius Yuri 🚀

=======================================================================================================
ENGLISH

e-Ticket
A simple ticket purchasing system developed with HTML, CSS, and JavaScript.

📋 Description
This project simulates an online ticket sales platform where users can:

✅ Select the type of ticket (Inferior, Superior, or Pista)
✅ Enter the desired quantity (up to 10)
✅ Buy tickets and reduce the available stock in real-time
✅ View updated quantities of tickets available
✅ Receive confirmation or error alerts based on stock availability

The project focuses on practicing DOM manipulation, event handling, and conditional logic with JavaScript.

🖼️ Project Preview
<img src="./assets/PNG/Logo e-tricket.png" alt="e-Ticket Logo" width="200"/>
🛠️ Technologies Used
HTML5 — Page structure

CSS3 — Visual styles and layout

JavaScript (ES6) — Business logic for ticket purchasing and stock management

Google Fonts — Chakra Petch and Inter for typography

🚀 Features
🏷️ Ticket selection via dropdown

🔢 Input for selecting quantity

⚠️ Stock verification with real-time updates

✅ Purchase confirmation with alerts

❌ Alert for insufficient stock

📁 Project Structure
pgsql
Copiar
Editar
e-ticket/
├── assets/
│   ├── PNG/
│   │   └── Logo e-tricket.png
│   ├── SVG/
│   │   └── Hachuras.svg
│   └── Ingresso.svg
├── js/
│   └── app.js
├── styles/
│   ├── _reset.css
│   └── style.css
├── index.html
└── README.md
🧑‍💻 How It Works
HTML
Defines the structure with:

Header: Logo

Main: Form with ticket options, quantity input, and purchase button

Section: Displays available quantities for each ticket type

JavaScript
Implements the core logic:

javascript
Copiar
Editar
function comprar() {
    let tipo = document.getElementById('tipo-ingresso')
    let qtd = parseInt(document.getElementById('qtd').value)

    if(tipo.value == 'pista') {
        comprarPista(qtd)
    } else if (tipo.value == 'superior') {
        comprarSuperior(qtd)
    } else {
        comprarInferior(qtd)
    }
}
Each ticket type has its own purchase verification and update function. For example:

javascript
Copiar
Editar
function comprarPista(qtd) {
    let qtdPista = parseInt(document.getElementById('qtd-pista').textContent)
    if (qtd > qtdPista) {
        alert("Quantidade indisponível para tipo de pista")
    } else {
        qtdPista -= qtd
        document.getElementById('qtd-pista').textContent = qtdPista
        alert("Compra realizada com sucesso")
    }
}
Similar logic applies to Superior and Inferior tickets.

⚙️ How to Run the Project
Clone the repository:

bash
Copiar
Editar
git clone https://github.com/your-username/e-ticket.git
Navigate to the project folder:

bash
Copiar
Editar
cd e-ticket
Open index.html in your preferred browser.

✅ No need for servers or package installations!

🎯 Key Learnings
DOM manipulation with getElementById and textContent

Conditional logic for validating stock and purchases

Event-driven programming with onclick

Clean structuring with separation of HTML, CSS, and JavaScript

🚫 Limitations
❌ No persistence: stock resets upon page refresh

❌ No backend integration or payment system

❌ No input sanitization beyond min/max HTML attributes

🤝 Contributions
Contributions, improvements, and suggestions are welcome!
Feel free to fork the project, open a new branch, and submit a pull request.

📄 License
MIT License.

✨ Author
Developed by Vinnícius Yuri 🚀
