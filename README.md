# Ignite Conceitos Do Nodejs

[![Node.js CI](https://github.com/AugustoSavi/IgniteConceitosDoNodejs/actions/workflows/node.js.yml/badge.svg)](https://github.com/AugustoSavi/IgniteConceitosDoNodejs/actions/workflows/node.js.yml)

<h2 align="center"> Endpoints </h2>

- Create User

```
curl --request POST \
  --url http://localhost:3333/users \
  --header 'Content-Type: application/json' \
  --data '{
	"name": "Danilo Vieira",
	"username": "danilo"
}'
```

- Get User

```
curl --request GET \
  --url http://localhost:3333/user \
  --header 'username: danilo'
```

- Create Todo

```
curl --request POST \
  --url http://localhost:3333/todos \
  --header 'Content-Type: application/json' \
  --header 'username: danilo' \
  --data '{
	"title": "Nome da tarefa2",
	"deadline": "2021-12-14"
}'
```

- Get Todos

```
curl --request GET \
  --url http://localhost:3333/todos \
  --header 'username: danilo'
```

- Update Todo

```
curl --request PUT \
  --url http://localhost:3333/todos/6b3136ae-a6e8-4ed5-98b0-939f94a811fa \
  --header 'Content-Type: application/json' \
  --header 'username: danilo' \
  --data '{
	"title": "Nome alterado",
	"deadline": "2021-12-15"
}'
```

- Mark Todo as Done


```
curl --request PATCH \
  --url http://localhost:3333/todos/6b3136ae-a6e8-4ed5-98b0-939f94a811fa/done \
  --header 'Content-Type: application/json' \
  --header 'username: danilo' \
  --data '{
	"title": "Nome alterado",
	"deadline": "2021-12-15"
}'
```