# Login Seguro

Sistema de cadastro, login e controle de acesso desenvolvido com Java 21, Spring Boot, Spring Security, Thymeleaf e MongoDB Atlas. O projeto foi organizado para facilitar a adaptação a diferentes temas de Projeto Final de Curso.

## Funcionalidades

- Cadastro de usuários com validação de nome, e-mail e senha.
- Login e logout gerenciados pelo Spring Security.
- Senhas protegidas com hash BCrypt.
- Controle de acesso por três perfis: `USER`, `MODERATOR` e `ADMIN`.
- Armazenamento de usuários e sessões no MongoDB Atlas.
- Temas visuais selecionáveis por configuração: `padrao` e `noite`.
- Proteção CSRF, renovação do identificador de sessão após o login e cookies configuráveis para HTTPS.

## Tecnologias

- Java 21
- Spring Boot
- Spring Security
- Spring Data MongoDB
- Spring Session Data MongoDB
- Thymeleaf
- Maven

## Requisitos

- JDK 21 ou superior
- Maven 3.9 ou superior
- Conta e cluster MongoDB Atlas
- Visual Studio Code com as extensões Java e Spring Boot (opcional)

## Configuração do MongoDB Atlas

1. Crie um cluster no MongoDB Atlas.
2. Crie um usuário de banco com permissão `readWrite` para o banco `login_seguro`.
3. Em **Network Access**, permita o IP da máquina onde o sistema será executado.
4. Copie a URI de conexão em **Connect → Drivers**.
5. Configure as variáveis de ambiente no terminal do VS Code:

   ```powershell
   $env:MONGODB_URI="mongodb+srv://USUARIO:SENHA@SEU-CLUSTER.mongodb.net/login_seguro?retryWrites=true&w=majority"
   $env:MONGODB_DATABASE="login_seguro"
   $env:APP_THEME="padrao"
   $env:COOKIE_SECURE="false"
