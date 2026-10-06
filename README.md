# Livraria API - Segurança

## Rodar no VS Code

1. Abra esta pasta no VS Code.
2. Abra **Terminal > New Terminal**.
3. Execute:

```bash
npm install
npm start
```

4. Quando aparecer:

```text
Livraria API rodando em http://localhost:3000
```

abra no navegador:

```text
http://localhost:3000
```

## Credenciais

**ADMIN**
- E-mail: `admin@livraria.com`
- Senha: `admin123`

**USER / Leitor**
- E-mail: `leitor@gmail.com`
- Senha: `leitor123`

## O que testar

- Sem login: listar livros funciona.
- ADMIN: pode cadastrar livro e autor.
- USER: pode comentar, mas não pode cadastrar livro/autor.
- Sem token: comentário retorna 401.
- USER tentando rota ADMIN: retorna 403.

## Rotas pedidas

- `GET /api/v1/livros` - público
- `GET /api/v1/livros/:id` - público
- `POST /api/v1/auth/register` - público
- `POST /api/v1/auth/login` - público
- `POST /api/v1/livros/:id/comentarios` - USER ou ADMIN autenticado
- `POST /api/v1/autores` - ADMIN
- `POST /api/v1/livros` - ADMIN
