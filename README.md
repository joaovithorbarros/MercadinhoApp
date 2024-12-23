# MercadinhoApp

## Pré-requisitos

Antes de começar, certifique-se de que você tenha os seguintes requisitos instalados:

- **Java 23**
- **Maven 3.8+ -> 4.0.0**.
- **DB PostgreSQL**

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/JIgorSilva/MercadinhoApp.git
   ```
2. Configure as variáveis de ambiente:
   - No arquivo `application.properties`:
     ```properties
     spring.datasource.url=jdbc:postgresql://localhost:5432/seu-banco
     spring.datasource.username=usuario
     spring.datasource.password=senha
     spring.jpa.hibernate.ddl-auto=update
     ```

3. Instale as dependências:
   ```bash / zsh / shell
   mvn clean 
   mvn install
   ```

4. Inicie o banco de dados:
   - Se necessário, execute um script SQL inicial (ex.: `src/main/resources/db/V1__Create_produtos_table.sql`).
   - Dentro da sua interface BD ou via terminal no diretorio da aplicação.

5. Inicie a aplicação:
   ```bash / zsh / shell
   mvn spring-boot:run ou via interface IDE
   ```

## Endpoints Principais

### `GET /api/produtos`
Retorna a lista de todos os produtos.

### `POST /api/produtos`
Cria um novo produto. Exemplo de payload:
```json
{
  {
  "id": 1, "id -> campo auto incrementavel não precisa ser enviado no request "
  "nome": "Mucilon Multi",
  "descricao": "Mucilon multi fibras 400g",
  "preco": 17.46,
  "quantidade": 372
  }
}
```

## Testes


## Docker (Opcional)

Se preferir rodar com Docker:
1. Construa a imagem:
   ```bash / zsh / shell
   docker build -t sua-api .
   ```

2. Rode o container:
   ```bash / zsh / shell
   docker run -p 8080:8080 sua-api
   ```

## Contribuindo

1. Faça um fork do repositório.
```bash / zsh / shell
   MercadinhoApp
   ```
2.Branch Main
```bash / zsh / shell
  git checkout main 
   ```
3. Crie uma Branch a parit da main
   ```bash / zsh / shell
  Ex: git checkout -b nome-da-nova-branch ex:"(api-METODO(Produto)-LOCAL(Repository))-NUMERO APOS A ULTIMA TASK(TASK-0numero)"
   ```
4. Faça commit das suas mudanças:
   ```bash / zsh / shell
   git commit -m "Criação de clasee para exception personalizadas..."
   ```
4. Envie seu branch:
   ```bash / zsh / shell
   git push origin minha-feature
   ```
5. Abra um Pull Request.

## Bugs

```bash / zsh / shell
   ```
1. Branch Main (efetue o pull)

```bash / zsh / shell
   git checkout main
   git pull
   ```
2. Checkout Branch criada

```bash / zsh / shell
 git checkout -b nome-da-nova-branch com o prefixo FIX seguindo o mesmo nome da branch que esta sendo corrigido o erro ex:" fix(api-produto-controller-getId-TASK-0-ultimo numero da branch criada).
   ```
4. Faça commit das suas mudanças:

```bash / zsh / shell
 git commit -m "Criação de clasee para exception personalizadas..."
   ```
4. Envie seu branch:
   
   git push origin minha-feature

5. Abra um Pull Request."
   
