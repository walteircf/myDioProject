# 🛒 Projeto SwagLabsShopping - Sistema de Gerenciamento e Autenticação

## 📌 Descrição

O **SwagLabsShopping** é um projeto de loja virtual com foco em **autenticação de usuários**, incluindo funcionalidades de login, cadastro e redefinição de senha. O projeto segue práticas de **Desenvolvimento Guiado por Comportamento (BDD)**, com testes manuais documentados no Zephyr/Jira, garantindo rastreabilidade e validação dos requisitos.

---

## 🧭 Fluxo de Trabalho

O fluxo de desenvolvimento das tarefas segue um ciclo estruturado para garantir organização e rastreamento:

1. **COMECAR**  
   Criação da tarefa → vai para **TO DO**

2. **TO DO (A Fazer)**  
   Aguardando início  
   - Iniciar sprint → **IN PROGRESS**  
   - Não será trabalhado → **CLOSED**  
   - Refatoração → permanece em TO DO

3. **IN PROGRESS (Em Progresso)**  
   Em desenvolvimento  
   - Enviar para QA → **READY FOR QA**  
   - Reanálise após erro → permanece em IN PROGRESS

4. **READY FOR QA (Pronto para QA)**  
   Pronto para validação de qualidade  
   - QA inicia validação → **IN REVIEW**

5. **IN REVIEW (Em Revisão)**  
   QA revisa a tarefa  
   - Aprovado → **RESOLVED**  
   - Reprovado → **REOPENED**

6. **REOPENED (Reaberto)**  
   Correção necessária → volta para **IN PROGRESS**

7. **RESOLVED (Resolvido)**  
   Pronto para produção → **DONE**

8. **DONE (Concluído)**  
   Finalizado com sucesso

9. **CLOSED (Encerrado)**  
   Tarefa abandonada ou descartada

---

## 🧪 Testes Realizados

Os testes foram conduzidos manualmente com base em BDD, registrados no Zephyr para Jira.

### ✔️ Cenários testados

#### 🧾 Teste SWAG-T1 - Login sem cadastro
- **Ação:** Tentar login com usuário não cadastrado  
- **Resultado esperado:** Acesso negado  
- **Status:** ✅ Sucesso

#### 🧾 Teste SWAG-T2 - Cadastro de novo cliente
- **Ação:** Clicar em "Realizar cadastro" e preencher dados  
- **Resultado esperado:** Cadastro efetuado com sucesso  
- **Status:** ✅ Sucesso

> Execuções feitas por **Walteir Coelho** com tempo de execução entre 13s e 34s.

---

## 💡 Metodologia BDD

Utilizamos o **BDD (Behavior Driven Development)** para escrever testes orientados a comportamento. Exemplo de cenário:

```
Cenário: Cliente sem cadastro deseja criar uma conta
Dado que o cliente esteja na tela de login
E não esteja cadastrado no sistema
Quando clicar em ‘criar conta’
Então será redirecionado para uma tela de criação de nova conta
```

## 📚 User Stories

### 📄 SWAG-2: Login com opções de cadastro e redefinição

**Como** cliente  
**Quero** acessar a página de login  
**Para** visualizar opções de login, cadastro e redefinição de senha

**Critérios de aceite:**
- Formulário de login visível
- Botões para cadastro e "esqueci minha senha"

---

### 📄 SWAG-4: Recuperação de senha

**Como** cliente  
**Quero** informar meu e-mail cadastrado  
**Para** receber instruções de redefinição de senha

**Critérios de aceite:**
- Campo de e-mail
- Validação do e-mail
- Envio do link/token por e-mail

---

## 🔧 Requisitos Técnicos

- Criação de **API RESTful**
- Interface **Web / Web Mobile**
- Integração com serviço de e-mail
- Banco de dados para autenticação

**Ambientes:**
- Desenvolvimento
- Homologação de usuários
- QA
- Produção

---

## 🧑‍💻 Desenvolvedor Responsável

| Nome           | Função                 |
|----------------|------------------------|
| Walteir Coelho | Testador e Relator QA  |

---

## 📂 Estrutura Recomendada

```bash
📁 src/
 ┣ 📂 backend/
 ┃ ┗ 📄 auth-api.js
 ┣ 📂 frontend/
 ┃ ┗ 📄 login.html
 ┣ 📂 tests/
 ┃ ┗ 📄 login.feature
📄 README.md
