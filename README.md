# api-recruiters-place

## Rotas que não precisam de autenticação

# <h1 align="center">Login</h1>

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
	}
}
```

# <h1 align="center">Register</h1>

```
POST /register FORMATO DA RESPOSTA - STATUS 200
```

```
{
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InBhYmxvNEBtYWlsLmNvbSIsImlhdCI6MTY2NzMxMzI4NSwiZXhwIjoxNjY3MzE2ODg1LCJzdWIiOiI0In0.rjj_nsCafkdGQrbN1Qq8E_U_cpsc6aOEeSkAid9Pm-k",
	"user": {
		"email": "pablo4@mail.com",
		"name": "Pablo",
		"escolaridade": "Ensino Superior",
		"Vaga": "Front-end",
		"id": 4
	}
}
```

## Rotas que precisam de autenticação

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
		"escolaridade": "Ensino Superior",
		"Vaga": "Front-end",
		"id": 3
	},
	{
		"email": "pablo4@mail.com",
		"password": "$2a$10$rG7D/CBrm27xaTosFZsn7ewOe8ZUy1fbxfx3Q7zMBFOc5ev9Ux/4q",
		"name": "Pablo",
		"escolaridade": "Ensino Superior",
		"Vaga": "Front-end",
		"id": 4
	}
]
```

# <h1 align="center">Mostrar todos usuários</h1>

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
}
```
