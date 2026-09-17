# Registros de Testes de Validação Nativa - Atividade Prática 04

## Formulário de Contato (`#form-contato`)

### Teste 1: Submissão do formulário vazio

- **Ação realizada:** Clique no botão "Enviar mensagem" sem preencher nenhum campo.
- **Campo que bloqueou:** `Seu nome` (`#nome`).
- **Mensagem exibida:** "Preencha este campo."

### Teste 2: Nome com menos de 3 caracteres (`minlength`)

- **Ação realizada:** Digitei "Oi" no campo `Seu nome` e cliquei em submeter.
- **Campo que bloqueou:** `Seu nome` (`#nome`).
- **Mensagem exibida:** "Aumente o texto para 3 caracteres ou mais (você está usando 2 caracteres)."

### Teste 3: Formato de e-mail inválido

- **Ação realizada:** Preenchi o nome ("Heitor") e digitei "heitor.souza" no campo de e-mail.
- **Campo que bloqueou:** `Seu e-mail` (`#email`).
- **Mensagem exibida:** "Inclua um "@" no endereço de e-mail. "heitor.souza" está sem um "@"."

### Teste 4: Mensagem com menos de 10 caracteres (`minlength`)

- **Ação realizada:** Preenchi nome e e-mail válidos, e digitei "Olá" na mensagem.
- **Campo que bloqueou:** `Mensagem` (`#mensagem`).
- **Mensagem exibida:** "Aumente o texto para 10 caracteres ou mais (você está usando 3 caracteres)."

---

## Formulário Temático (`#form-solicitacao-oficina`)

### Teste 1: Submissão sem selecionar o turno (`select` obrigatório)

- **Ação realizada:** Preenchi o nome, e-mail e data, mantendo o select no valor inicial vacilante ("-- Selecione o turno --") e cliquei em submeter.
- **Campo que bloqueou:** `Turno de preferência` (`#turma-horario`).
- **Mensagem exibida:** "Selecione um item da lista."

### Teste 2: Submissão sem selecionar o nível de conhecimento (`radio` obrigatório)

- **Ação realizada:** Preenchi todos os campos superiores e o select, mas deixei os rádio buttons desmarcados.
- **Campo que bloqueou:** `Nível de conhecimento prévio dos alunos` (`#nivel-iniciante`).
- **Mensagem exibida:** "Selecione uma destas opções."

### Teste 3: Valor abaixo do limite mínimo (`min`)

- **Ação realizada:** Digitei "2" no campo de quantidade de alunos beneficiados (cujo limite `min="5"`).
- **Campo que bloqueou:** `Quantidade estimada de alunos beneficiados` (`#qtd-alunos`).
- **Mensagem exibida:** "O valor deve ser maior ou igual a 5."
