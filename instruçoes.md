Aqui está uma proposta de enunciado detalhado para o desafio final:

---

## **Desafio Final de Web Front-End Básico: Landing Page com API de Clima**

### **Descrição**
Crie uma Landing Page funcional e interativa que exiba informações climáticas em tempo real utilizando HTML, CSS e JavaScript puro (sem bibliotecas/frameworks). O objetivo é praticar os conceitos aprendidos em aula e demonstrar suas habilidades de desenvolvimento web básico.

---

### **Requisitos Obrigatórios**
1. **Estrutura HTML**:
   - Deve conter ao menos as seguintes seções:
     - Um cabeçalho com o nome do site e um menu de navegação simples.
     - Um campo de busca para digitar o nome de uma cidade.
     - Um botão para consultar o clima.
     - Uma área para exibir as informações climáticas, incluindo:
       - Nome da cidade.
       - Temperatura atual.
       - Descrição do clima (ex.: ensolarado, nublado, etc.).
       - Ícone representando o clima.
   - Um rodapé com informações fictícias ou links externos.

2. **Estilização CSS**:
   - Utilize um layout responsivo (adaptável a diferentes tamanhos de tela).
   - Adicione pelo menos **uma animação CSS** (ex.: fade-in, slide, ou animação no botão de busca).
   - Inclua estilos visuais que tornem a página atrativa (cores, fontes, margens, etc.).

3. **Funcionalidade com JavaScript Puro**:
   - Realizar uma **requisição a uma API de clima** para obter os dados da cidade pesquisada.
   - Atualizar o conteúdo da página dinamicamente com as informações retornadas pela API.
   - Tratar erros (ex.: exibir uma mensagem amigável se a cidade não for encontrada).

4. **API Utilizada**:
   - Use a API gratuita do [OpenWeatherMap](https://openweathermap.org/api). Escolha o tipo "Current Weather Data".
   - Você precisará criar uma conta e obter uma chave de API (API Key).

---

### **Etapas de Desenvolvimento (Dicas Detalhadas)**

#### **1. Planejamento e Estrutura HTML**
- Comece criando o layout básico no HTML. Utilize as tags principais como `<header>`, `<main>`, `<footer>`, `<form>`, `<input>`, `<button>`, `<section>` e `<div>`.
- Planeje onde as informações climáticas serão exibidas. Use `<h2>`, `<p>` e uma tag de imagem `<img>` para o ícone do clima.

---

#### **2. Estilização CSS**
- Crie um arquivo CSS separado e importe no HTML.
- Use seletores para estilizar as áreas do cabeçalho, formulário e exibição dos resultados.
- Dicas para responsividade:
  - Utilize media queries para ajustar o layout para dispositivos móveis.
  - Experimente usar unidades relativas como `%`, `em`, `rem`, ou `vh/vw`.

- **Animação**:
  - Escolha uma animação simples, como um botão que muda de cor ao passar o mouse, ou um fade-in para exibir os resultados.
  - Utilize `@keyframes` para definir a animação.

---

#### **3. Integração com JavaScript**
- Crie um arquivo `script.js` e importe no HTML.
- Adicione um evento `click` ao botão de busca.
- Use o método `fetch()` para consumir a API do OpenWeatherMap.
  - URL da API: `https://api.openweathermap.org/data/2.5/weather?q={CITY_NAME}&appid={API_KEY}&units=metric`
  - Substitua `{CITY_NAME}` pelo nome da cidade digitada e `{API_KEY}` pela sua chave da API.
- Faça o tratamento da resposta JSON da API para obter:
  - Nome da cidade (`data.name`)
  - Temperatura (`data.main.temp`)
  - Descrição do clima (`data.weather[0].description`)
  - Ícone (`data.weather[0].icon` → `http://openweathermap.org/img/wn/{ICON}.png`)
- Atualize os elementos HTML com as informações retornadas.

---

#### **4. Tratamento de Erros**
- Adicione verificações para:
  - Se o usuário não digitou nada, exibir uma mensagem de erro.
  - Se a API retornar um erro (ex.: cidade não encontrada), exibir um alerta ou mensagem amigável.
- Dica: Use o método `.catch()` para capturar erros na requisição `fetch()`.

---

### **Extra (Para Quem Quiser Ir Além)**
- Adicione um **background dinâmico** que muda com base no clima (ex.: imagens diferentes para clima ensolarado, chuvoso, etc.).
- Implemente uma funcionalidade para salvar as últimas cidades pesquisadas no localStorage.
- Adicione suporte para idiomas (traduza as descrições do clima para português).

---

### **Entrega**
- Envie o código em um arquivo ZIP ou faça upload para um repositório no GitHub.
- Inclua um README.md explicando:
  - Como configurar e executar o projeto.
  - As funcionalidades implementadas.

---

Boa sorte e divirta-se desenvolvendo! 🎉