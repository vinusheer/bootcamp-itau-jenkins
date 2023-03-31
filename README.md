# Vamos fazer nosso primeiro deploy com o Jenkins?

### Siga estes passos
1. Configure as credenciais do seu repositório do GitHub no Jenkins;
2. Crie um projeto do tipo Multibranch Pipeline e associe-o com seu repositório;
3. Crie uma pipeline com Jenkinsfile que, ao perceber uma mudança na branch *main*, execute dois estágios: 
   - Estágio 1: Listar os arquivos do repositório;
   - Estágio 2: Fazaer o upload do arquivo **index.html** via *CURL* no endpoint do nosso servidor:
```sh
Método: PUT
URL: https://ktxdfuuszshdwe2fpi6niua45e0pduww.lambda-url.us-east-1.on.aws/
Cabeçalhos obrigatórios:
  myToken: BNUhVeITc3kgQM4g07rat62XKmiMYf
  myPath: <verificar seu path no arquivo paths-permitidos.txt>  
# exemplo
$ curl -H 'authToken: BNUhVeITc3kgQM4g07rat62XKmiMYf' -H 'myPath: <seu-path>' -T index.html https://ktxdfuuszshdwe2fpi6niua45e0pduww.lambda-url.us-east-1.on.aws/
 ```
Se tudo for feito corretamente, ao acessar a URL `http://bootcamp-itau.s3-website-us-east-1.amazonaws.com/<seu-path>/index.html` no seu browser, você verá uma página web indicando o sucesso do seu deploy.
