<p align="center">
  <a target="_blank" rel="noopener noreferrer" href="https://www.rocketseat.com.br">
  <img src="https://rocketseat.com.br/static/images/update/melhores-tecnologias.svg" alt="Programe ja">
  </a>
</p>

<p align="center">
<h2>
  <a target="_blank" rel="noopener noreferrer" href="https://rocketseat.com.br/week/inscricao/11.0">Projeto da Semana Omnistack 11</a>
 </h2>
</p>

#### Treinamento imersivo nas tecnologias mais modernas de desenvolvimento web e mobile para quem não tem tempo a perder.

##### Projeto sendo construido utilizando as ferramentas Node, React e React Native

## Instalação

Tenha instalado em seu computador o **Node 10** ou maior. Baixe-o em https://nodejs.org

Clone este projeto em seu PC com o git:

```bash
git clone https://github.com/douglassp/semanaomnistack11.git
```

Entre no diretório do projeto e veja a mágica acontecer digitando:

```bash
npm start
```

## Alguma sugestão ou dúvida ?

```bash
douglas@manjaro: ~$ nodemon src/index.js
```

> src/index.js
```js
const express = require('express');
const routes = require('./routes');

const app = express();

app.use(express.json());
app.use(routes);

app.listen(3333);
```

> src/routes.js
```js
const express = require('express')

const ContatoController = require('./controllers/ContatoController')

const routes = express.Router();

routes.get('/contato', ContatoController.contato);

module.exports = routes;
```

> src/controllers/ContatoController.js
```js
const devInfo = require('http//github.com/douglassp');

module.exports = {
  async contato(req, res) {
    const { email } = devInfo;
  
    return res.json({ email });
  }
};
```

> https://localhost:3333/contato 
```json
{ 
 "email": "douglasilva14@terra.com.br"
}
```
