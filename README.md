## Instalação

Clonar o repositório

```bash
  git clone [repositório](https://github.com/Leokrindges/API_lista_de_recados/)
```

Instalar as depêndencias do projeto

```bash
  yarn install | npm install
```

Iniciar o projeto

```bash
  yarn run dev | yarn dev | npm run dev
```

## Documentação da API

Esta API foi desenvolvida para gerenciar informações sobre recados. Ela oferece funcionalidades para criar, ler, atualizar e excluir recados.
Além de criar e fazer o login de usuários.


#### Retorna uma lista de todos os usuários e seus recados cadastrados.

```http
  GET /usuario
```


#### Retorna todos os detalhes de um usuario e recado específico com base no ID fornecido na URL.

```http
  GET recados/
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
| `id` | `String` | **Obrigatório**. id do usuario para filtragem




#### Criar um recado

```http
  POST /usuario/recados/
```

| Parâmetro   | Tipo               | Descrição                                   |
| :---------- | :----------------- | :------------------------------------------ |
| `Access token`        | `string`           | **Obrigatório**. token do usuario |
| `Titulo`       | `String`           | **Obrigatório**. titulo do recado |
| `Descrição `      | `string`           | **Obrigatório**. descrição do recado |




#### Atualiza recado existente com base no ID do usuario e ID do recado fornecido na URL.

```http
  PUT /usuario/recados/:idRecado
```

| Parâmetro   | Tipo               | Descrição                                   |
| :---------- | :----------------- | :------------------------------------------ |
| `Access token`        | `string`           | **Obrigatório**. token do usuario |
| `id`        | `string`           | **Obrigatório**. id do recado |
| `Recados`   | `Array de objetos` | **Obrigatório**. lista de com recados |
| `Titulo`       | `String`           | **Obrigatório**. titulo do recado |
| `Descrição `      | `string`           | **Obrigatório**. descrição do recado |



### Exclui um recado com base no ID do recado fornecido na URL.
```http
  DELETE /usuario/recados/:idRecado
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `Access token`        | `string`           | **Obrigatório**. token do usuario |
| `idRecado`      | `String` | **Obrigatório**. id do recado |



### Cria um usuario
```http
  POST /usuario
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `id`      | `String` | **Obrigatório**. id do usuario |
| `Nome`      | `String` | **Obrigatório**. Nome do usuário |
| `E-mail`      | `String` | **Obrigatório**. E-mail do usuário |
| `Senha`      | `String` | **Obrigatório**. Senha do usuário |


### Login
```http
  POST /usuario/login
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `E-mail`      | `String` | **Obrigatório**. E-mail do usuário |
| `Senha`      | `String` | **Obrigatório**. Senha do usuário |




