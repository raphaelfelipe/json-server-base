Endpoints

URL base : https://api-atividade-11.herokuapp.com

Cadastro de usuário

POST /register - FORMATO DA REQUISIÇÃO

{
"email": "macedo@teste.com",
"password": "123456",
"name": "Raphael",
}
Caso dê tudo certo, a resposta será assim:

POST /register - FORMATO DA RESPOSTA - STATUS 201

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6Im1hY2VkbzFAdGVzdGUuY29tIiwiaWF0IjoxNjQ3MjIxMjE0LCJleHAiOjE2NDcyMjQ4MTQsInN1YiI6IjIifQ.9vntsCbzTiox2QMHdM6eZ58n4-iLJwk3v7Z-2Nipomg",
"user": {
"email": "macedo@teste.com",
"name": "Raphael",
"id": 1
}
}

POST /login - FORMATO DA RESPOSTA - STATUS 201

{

Login

POST /login - FORMATO DA REQUISIÇÃO

{
"email": "macedo@teste.com",
"password": "123456"
}
Caso dê tudo certo, a resposta será assim:

POST /login - FORMATO DA RESPOSTA - STATUS 201

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6Im1hY2Vkb0B0ZXN0ZS5jb20iLCJpYXQiOjE2NDcyMjE3MjIsImV4cCI6MTY0NzIyNTMyMiwic3ViIjoiMSJ9.EzpyRUebEG728lvIWeaQoE-KK4fAUelOP8yipMLAcE0",
"user": {
"email": "macedo@teste.com",
"name": "Raphael",
"id": 1
}
}

Lista histórias

GET /history - FORMATO DA RESPOSTA - STATUS 200

[
{
"genre": "horror",
"title": "Drácula, o vampíro da noite",
"sinapse": "Uma história de terror de vampíros",
"userId": 1,
"id": 1
}
]

Para verificar qual usuário possui história, usar o endpoint: GET /history/{id}?\_expand=user

Caso dê tudo certo, a resposta será assim:

{
"genre": "horror",
"title": "Drácula, o vampíro da noite",
"sinapse": "Uma história de terror de vampíros",
"userId": 1,
"id": 1,
"user": {
"email": "macedo@teste.com",
"password": "$2a$10$Ms.U9A6QrC/FHKPJlbbmie2dLHYD3qLugXraDdTeq4TTXh9Zga1v.",
"name": "Raphael",
"id": 1
}
}

Listar cursos

GET /courses - FORMATO DA RESPOSTA - STATUS 200

[
{
"course": "Development",
"status": "Advensed",
"userId": 1,
"id": 1
}
]

Precisar estar autentificado

Adicionar história

POST /history - FORMATO DA REQUISIÇÂO - STATUS 201

{
"genre": "horror",
"title": "Jason",
"sinapse": "sexta-feira 13",
"userId": 1,
}

POST /history - FORMATO DA RESPOSTA - STATUS 201

{
"genre": "horror",
"title": "Jason",
"sinapse": "sexta-feira 13",
"userId": 1,
"id": 2
}

Adicionar Cursos

POST /courses - FORMATO DA REQUISIÇÂO - STATUS 201

{
"course": "Development",
"status": "Advensed",
"userId": 1
}

POST /courses - FORMATO DA RESPOSTA - STATUS 201

{
"course": "Development",
"status": "Advensed",
"userId": 1,
"id": 1
}
