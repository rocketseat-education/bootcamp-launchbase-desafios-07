<h1 align="center">
    <img alt="Launchbase" src="https://storage.googleapis.com/golden-wind/bootcamp-launchbase/logo.png" width="400px" />
</h1>

<h3 align="center">
  Desafio 7: Envio de imagens Foodfy
</h3>

<blockquote align="center">“Quanto mais você estuda, mais aprende e se aproxima de realizar seu sonhos!”</blockquote>

<p align="center">

  <a href="https://rocketseat.com.br">
    <img alt="Made by Rocketseat" src="https://img.shields.io/badge/made%20by-Rocketseat-%23F8952D">
  </a>

  <a href="LICENSE" >
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23F8952D">
  </a>

</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Entrega</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Você irá criar um sistema de envio de imagem, conforme as especificações abaixo.

Veja também as especificações do layout, abrindo o arquivo que está em [layouts/index.html](../layouts/index.html) no seu navegador Google Chrome. 

**Download dos arquivos:** https://github.com/Rocketseat/bootcamp-launchbase-desafios-07/archive/master.zip

### Tabelas

Crie uma tabela de nome `files` com os campos

- `id SERIAL PRIMARY KEY`
- `name TEXT`
- `path TEXT NOT NULL`

Essa tabela acima irá receber todas as imagens do sistema.

Crie uma tabela de nome `recipe_files` com os campos

- `id SERIAL PRIMARY KEY`
- `recipe_id INTEGER REFERENCES recipes(id)`
- `file_id INTEGER REFERENCES files(id)`

Você vai precisar buscar as imagens de uma receita, criando um 
relacionamento entre as tabelas `recipe_files` com a tabela `files`

### Receitas

Adicionar imagens às receitas.

- No banco de dados, remova o campo `image`, pois não será mais necessário.
- Crie um campo de upload de imagens
- Coloque um limite de 5 imagens
- A receita deve ter pelo menos uma imagem

**Criação de uma receita**
![Imagem da Página de Criação de Receitas](../layouts/preview/desafio-07-receita-criação.png)

**Edição de uma receitas**
![Imagem Página de Edição de Receitas](../layouts/preview/desafio-07-receita-edição.png)

### Chefs

Adicionar a imagem de avatar para o chef

- Remova o campo `avatar_url` da tabela de chefs
- Adicione o campo `file_id INTEGER REFERENCES files(id)`

Você vai precisar criar um relacionamento entre `chefs` e `files`

Dica: Use `ALTER TABLE` para fazer as alterações da tabela de chefs.

**Criação de um chef**
![Imagem da Página de Criação de Chef](../layouts/preview/desafio-07-chef-criação.png)

**Edição de um chef**
![Imagem Página de Edição de Chef](../layouts/preview/desafio-07-chef-edição.png)

### Apresentação

Mostrar as novas imagens de receitas e chefs que estarão cadastradas no banco de dados.

Na página de detalhe de uma receita, criar uma funcionalidade de troca de imagens conforme imagem abaixo.
![Imagem da Página de Detalhes de uma Receita](../layouts/preview/desafio-07-receita-detalhe.png)

**Não haverá alterações** visuais para os chefs.

### Novos conceitos

Aplique os conceitos de `async/await` e de `try/catch` que você aprendeu nas aulas.

## :calendar: Entrega

Esse desafio **não precisa ser entregue** e não receberá correção. Após concluí-lo, adicionar esse código ao seu Github é uma boa forma de demonstrar seus conhecimentos para oportunidades futuras.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](../LICENSE) para mais detalhes.

---

Feito com :purple_heart: by [Rocketseat](https://rocketseat.com.br) :wave: [Entre na nossa comunidade!](https://discordapp.com/invite/gCRAFhc)
