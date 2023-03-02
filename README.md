# api-recruiters-place

# <h1 align="center">Rodar API Localmente</h1>

<p>Abra o terminal:</p>

```
npm run server

# ou

node server.js
```

<h2>Funcionando</h2>

```
$ npm run server

> server
> node server.js

Server is running on port: 3001

# ou

$ node server.js
Server is running on port: 3001
```

# <h1 align="center">Rotas que não precisam de autenticação</h1>

# <h1 align="center">Register</h1>

```
POST /register FORMATO DA REQUISIÇÃO - STATUS 200
```

```
Para Desenvolvedor:
```

```
{
	"name": "Pablo",
	"email": "pablo5@mail.com",
	"password": "123456789",
	"isRecruiter": true,
	"city": "SP",
	"schooling": "Superior",
	"vacancy": "Front-end",
	"isWork": true,
	"linkedin": "http://linkedin.com",
	"github": "http://linkedin.com",
	"portfolio": "http://linkedin.com",
	"tech":{
		"html": true,
		"css": true,
		"js": true,
		"react": true,
		"ts": true,
		"angular": true,
		"vuejs": true,
		"php": true,
		"c": true
	}
}
```

```
Para Recrutador:
```

```
{
	"name": "Pablo",
	"email": "pablo5@mail.com",
	"password": "123456789",
	"isRecruiter": true,

}
```

```
POST /register FORMATO DA RESPOSTA - STATUS 200
```

```
Para Desenvolvedor:
```

```
{
	{
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InBhYmxvNTZAbWFpbC5jb20iLCJpYXQiOjE2Njc0ODIxNDQsImV4cCI6MTY2NzQ4NTc0NCwic3ViIjoiNyJ9.oQQ5Em8Z-0DptiXBl0A3kjcxlk7bpH6Ew_vu5jedYEY",
	"user": {
		"email": "pablo56@mail.com",
		"name": "Pablo",
		"isRecruiter": true,
		"city": "SP",
		"schooling": "Superior",
		"vacancy": "Front-end",
		"isWork": true,
		"linkedin": "http://linkedin.com",
		"github": "http://linkedin.com",
		"portfolio": "http://linkedin.com",
		"tech": {
			"html": true,
			"css": true,
			"js": true,
			"react": true,
			"ts": true,
			"angular": true,
			"vuejs": true,
			"php": true,
			"c": true
		},
		"id": 7
	}
}
}
```

```

Para Recrutador:

```

```
{
	{
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InBhYmxvNTZAbWFpbC5jb20iLCJpYXQiOjE2Njc0ODIxNDQsImV4cCI6MTY2NzQ4NTc0NCwic3ViIjoiNyJ9.oQQ5Em8Z-0DptiXBl0A3kjcxlk7bpH6Ew_vu5jedYEY",
	"user": {
		"email": "pablo56@mail.com",
		"name": "Pablo",
		"isRecruiter": true,
		}
	}
}
```

# <h1 align="center">Login</h1>

```
POST /login FORMATO DA REQUISIÇÃO - STATUS 200
```

```
{
	"email": "pablo@mail.com",
	"password": "123456"
}
```

```
POST /login FORMATO DA RESPOSTA - STATUS 200
```

```
 {
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InBhYmxvQG1haWwuY29tIiwiaWF0IjoxNjY3MzE0ODAyLCJleHAiOjE2NjczMTg0MDIsInN1YiI6IjEifQ.qq8dCsGE0lq-Wh-5ZSfgyKi7yPOjL1KhroZZkwF_WQA",
	"user": {
		"email": "pablo@mail.com",
		"name": "Pablo",
		"age": "31",
		"id": 1
		...
	}
}
```

# <h1 align="center">Rotas que precisam de autenticação</h1>

```
 Authorization

 Authorization: Bearer {accessToken}
```

# <h1 align="center">Mostrar todos usuários</h1>

```
GET /users FORMATO DA RESPOSTA - STATUS 200
```

```
[
	{
		"email": "pablo3@mail.com",
		"password": "$2a$10$m78xwTXufrGUSF8tFmVO3uqe4ymnd2MVDURg3iZW3iTQ0uB7dIVIW",
		"name": "Pablo",
		"schooling": "Ensino Superior",
		"vacancy": "Front-end",
		"id": 3
	},
	{
		"email": "pablo4@mail.com",
		"password": "$2a$10$rG7D/CBrm27xaTosFZsn7ewOe8ZUy1fbxfx3Q7zMBFOc5ev9Ux/4q",
		"name": "Pablo",
		"schooling": "Ensino Superior",
		"vacancy": "Front-end",
		"id": 4
	}
]
```

# <h1 align="center">Mostrar usuário logado</h1>

```
GET /users/id FORMATO DA RESPOSTA - STATUS 200
```

```
{
	"email": "pablo2@mail.com",
	"password": "$2a$10$DTyyNXOCyhYCrzhwT6FkYeQNRGQqIlC308viCKbj7hACFu/Yf//0y",
	"name": "Pablo",
	"age": "31",
	"id": 2
	...
}
```

# <h1 align="center">Editar usuário logado</h1>

```
PATCH /users/id FORMATO DA REQUISIÇÃO - STATUS 200
```

```
{
	"email": "pablo2@mail.com",
	"password": "$2a$10$DTyyNXOCyhYCrzhwT6FkYeQNRGQqIlC308viCKbj7hACFu/Yf//0y",
	"name": "Pablo",
	"age": "37",
	"id": 2
	"city": "Rio de Janeiro"
}
```

```
PATCH /users/id FORMATO DA RESPOSTA - STATUS 200
```

```
{
	"email": "pablo2@mail.com",
	"password": "$2a$10$DTyyNXOCyhYCrzhwT6FkYeQNRGQqIlC308viCKbj7hACFu/Yf//0y",
	"name": "Pablo",
	"age": "37",
	"id": 2
	"city": "Rio de Janeiro"
}
```

# <h1 align="center">Postar comentário</h1>

```
POST /coments FORMATO DA REQUISIÇÃO - STATUS 200
```

```
{
	"idFrom": "8",
	"idTo": "5",
	"from": "Pablin",
	"to": "Pablo",
	"coments": "olá vamos codar ?"
}
```

```
POST /coments FORMATO DA RESPOSTA - STATUS 200
```

```
{
	"idFrom": "8",
	"idTo": "5",
	"from": "Pablin",
	"to": "Pablo",
	"coments": "olá vamos codar ?",
	"id": 3
}
```

# <h1 align="center">Enviar mensagem</h1>

```
POST /chat FORMATO DA REQUISIÇÃO - STATUS 200
```

```
{
	"chat":"Ok, vamos marcar bonitão.",
 	"from": "Pablo",
	"idFrom": "8",
	"isRead": false,
	"idTo": "12",
	"to": "Pablin"
}
```

```
POST /chat FORMATO DA RESPOSTA - STATUS 200
```

```
{
	"chat": "Ok, vamos marcar bonitão.",
	"from": "Pablo",
	"idFrom": "8",
	"isRead": false,
	"idTo": "12",
	"to": "Pablin",
	"id": 13
}
```
