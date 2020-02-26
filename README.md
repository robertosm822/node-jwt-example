# node-jwt-example
## Instalar dependências
```
    npm install
```

## Gerando certificados

O algorítmo de encriptação do token usa o conteúdo de arquivos de certificados que contém as chaves pública e privada. Para gerar estes arquivos, execute o arquivo:

```
$ ./generateKeys.sh
```
A senha solicitada pelo comando pode ficar em branco. Os arquivos **_private.key_** e **_public.key_** serão gerados na pasta **_src_**.

## Iniciar o servidor
Para iniciar o servidor Express, use o comando:

```
   npm start
```

## Rotas de Testes
- Login para gerar o TOKEN de autenticação usando o Postman:
```
  username: admin / password: 123456
  POST: localhost:3000/login
```

- Rota para gerar o desbloqueio da session:
```
  GET: localhost:3000/protected
  Passar na aba 'Headers' => "Authorization"
  Adicionar no value "Bearer TOKEN_GERADO"
```