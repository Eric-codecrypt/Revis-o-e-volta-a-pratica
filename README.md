# ✅ Revisão Pós-Férias
**Curso:** Técnico em Desenvolvimento de Sistemas  
**Formato:** Respostas resolvidas em Markdown

---

## 📌 PHP

```php
// 1. Olá, mundo!
echo "Olá, mundo!";

// 2. Soma via $_GET
$soma = $_GET['a'] + $_GET['b'];
echo "Soma: $soma";

// 3. Par ou ímpar
$num = 5;
if ($num % 2 == 0) {
  echo "Par";
} else {
  echo "Ímpar";
}

// 4. For de 1 a 10
for ($i = 1; $i <= 10; $i++) {
  echo "$i<br>";
}

// 5. Foreach com nomes
$nomes = ["Ana", "João", "Lucas", "Beatriz", "Clara"];
foreach ($nomes as $nome) {
  echo $nome . "<br>";
}

// 6. Conexão PDO
try {
  $pdo = new PDO("mysql:host=localhost;dbname=escola", "root", "");
  echo "Conectado!";
} catch (PDOException $e) {
  echo "Erro: " . $e->getMessage();
}

// 7. Formulário + PDO (HTML + PHP)
<form method="post">
  <input name="nome">
  <input name="idade" type="number">
  <input name="turma">
  <button type="submit">Enviar</button>
</form>

<?php
if ($_POST) {
  $stmt = $pdo->prepare("INSERT INTO alunos (nome, idade, turma) VALUES (?, ?, ?)");
  $stmt->execute([$_POST['nome'], $_POST['idade'], $_POST['turma']]);
}
?>

// 8. Função com nome
function boasVindas($nome) {
  return "Bem-vindo, $nome!";
}
echo boasVindas("Eric");

// 9. MVC (estrutura de pastas)
/mvc
├── controller/
│   └── AlunoController.php
├── model/
│   └── AlunoModel.php
├── view/
│   └── alunoView.php
├── config.php
└── index.php

// 10. CRUD
├── view/
│   ├── registrar.php
│   ├── alunoView.php
│   ├── editar.php
│   └── deletar.php
├── config.php
└── index.php
```
#


## 🎨 CSS

```css
/* 1. Botão azul arredondado */
.botao {
  background: blue;
  color: white;
  border-radius: 10px;
  padding: 10px;
}

/* 2. Título h1 vermelho centralizado */
h1 {
  color: red;
  text-align: center;
}

/* 3. Cor de fundo ao hover */
div:hover {
  background-color: #eee;
}

/* 4. Flexbox horizontal */
.container {
  display: flex;
}

/* 5. Cartão com sombra e borda */
.cartao {
  border: 1px solid #ccc;
  box-shadow: 0px 0px 10px #aaa;
  padding: 10px;
}

/* 6. Media query para telas pequenas */
@media (max-width: 600px) {
  body {
    background: lightgray;
  }
}

/* 7. Formulário com padding, margin e borda */
form {
  padding: 20px;
  margin: 10px;
  border: 1px solid black;
}

/* 8. Botão no canto com position absolute */
.botao {
  position: absolute;
  top: 0;
  right: 0;
}

/* 9. Fonte personalizada */
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}

/* 10. Navbar com menu hambúrguer */
@media (max-width: 600px) {
  .navbar {
    display: none;
  }
  .menu-hamburguer {
    display: block;
  }
}

```
#


## 🌐 HTML

```html
<!-- 1. Título, parágrafo e imagem -->
<h1>Bem-vindo</h1>
<p>Este é um parágrafo</p>
<img src="imagem.jpg" alt="Imagem">

<!-- 2. Formulário com input, textarea e select -->
<form>
  <input type="text" name="nome">
  <textarea name="mensagem"></textarea>
  <select name="opcao">
    <option>Opção 1</option>
    <option>Opção 2</option>
  </select>
</form>

<!-- 3. Tabela com 3 colunas e 4 linhas -->
<table border="1">
  <tr><th>Nome</th><th>Idade</th><th>Turma</th></tr>
  <tr><td>Ana</td><td>16</td><td>A</td></tr>
  <tr><td>João</td><td>17</td><td>B</td></tr>
  <tr><td>Clara</td><td>16</td><td>A</td></tr>
</table>

<!-- 4. Link -->
<a href="https://www.google.com" target="_blank">Ir para Google</a>

<!-- 5. Tags semânticas -->
<header>Topo</header>
<main>Conteúdo</main>
<footer>Rodapé</footer>

<!-- 6. Lista ordenada -->
<ol>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
  <li>Item 4</li>
  <li>Item 5</li>
</ol>

<!-- 7. Campo de e-mail -->
<input type="email" placeholder="Digite seu e-mail">

<!-- 8. Botão visual -->
<button>Não faz nada</button>

<!-- 9. Vídeo do YouTube -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/ID_DO_VIDEO" frameborder="0" allowfullscreen></iframe>

<!-- 10. Formulário completo -->
<form>
  <input type="text" placeholder="Nome">
  <input type="email" placeholder="Email">
  <input type="password" placeholder="Senha">
  <button type="submit">Cadastrar</button>
</form>

```
#


## 🛢️ MySQL (PHPMyAdmin)

```mysql
-- 1. Criar base de dados
CREATE DATABASE escola;

-- 2. Tabela alunos
CREATE TABLE alunos (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(50),
  idade INT,
  turma VARCHAR(10)
);

-- 3. Inserir registros
INSERT INTO alunos (nome, idade, turma) VALUES ('Ana', 16, 'A');
INSERT INTO alunos (nome, idade, turma) VALUES ('João', 17, 'B');
INSERT INTO alunos (nome, idade, turma) VALUES ('Clara', 16, 'A');

-- 4. Mostrar todos
SELECT * FROM alunos;

-- 5. Atualizar idade
UPDATE alunos SET idade = 18 WHERE nome = 'João';

-- 6. Deletar aluno
DELETE FROM alunos WHERE nome = 'Ana';

-- 7. LIKE (nome começa com A)
SELECT * FROM alunos WHERE nome LIKE 'A%';

-- 8. Ordernar por idade decrescente
SELECT * FROM alunos ORDER BY idade DESC;

-- 9. Tabela professores e relacionamento
CREATE TABLE professores (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(50)
);
ALTER TABLE alunos ADD COLUMN professor_id INT;
ALTER TABLE alunos ADD FOREIGN KEY (professor_id) REFERENCES professores(id);


```
#


## 💡 Arduino

```arduino
// 1. Circuito com LEDs: vermelho = pino 2, amarelo = 3, verde = 4
// 2, 3, 4, 5 - Código completo
int vermelho = 2;
int amarelo = 3;
int verde = 4;

void setup() {
  pinMode(vermelho, OUTPUT);
  pinMode(amarelo, OUTPUT);
  pinMode(verde, OUTPUT);
}

void loop() {
  digitalWrite(vermelho, HIGH);
  delay(5000);
  digitalWrite(vermelho, LOW);

  digitalWrite(amarelo, HIGH);
  delay(2000);
  digitalWrite(amarelo, LOW);

  digitalWrite(verde, HIGH);
  delay(4000);
  digitalWrite(verde, LOW);

  delay(10000); // Apagar tudo após 10s
}

// 6. Botão de pedestre (pino 5)
int botao = 5;

void loop() {
  if (digitalRead(botao) == HIGH) {
    // repete ciclo do semáforo
  }
}

// 7. Sem pinMode: os pinos não funcionam corretamente — LEDs não acendem.

```
#


## 🔧 Tinkercad


![Circuito do Semáforo no Tinkercad](https://github.com/Eric-codecrypt/Revis-o-e-volta-a-pratica/blob/main/428ceb47-4a3a-410e-8480-0f36c13c50da.png)




#


## 🧠 Projetos – Scrum e Documentação

```projetos
1. Scrum é um framework ágil para desenvolvimento rápido de software. Ele usa sprints curtas e entregas incrementais.

2. Papéis:
- Product Owner: responsável pelo backlog e visão do produto.
- Scrum Master: garante que o time siga o Scrum corretamente.
- Dev Team: equipe que desenvolve o produto.

3. Backlog:
- Criar login
- Fazer tela de tarefas
- Salvar tarefas no banco

4. Sprint de 1 semana

| Dia       | Tarefa                |
|-----------|-----------------------|
| Segunda   | Planejamento Sprint   |
| Terça     | Desenvolvimento Login |
| Quarta    | Tela de tarefas       |
| Quinta    | Testes e ajustes      |
| Sexta     | Revisão e entrega     |

5. Cronograma de Projeto

| Semana | Atividade          |
|--------|--------------------|
| 1      | Levantamento       |
| 2      | Protótipo          |
| 3      | Desenvolvimento    |
| 4      | Testes e entrega   |

6. Documento de Requisitos:
- Objetivo do sistema
- Funcionalidades
- Regras de negócio
- Interface esperada

7. User Story:
"Como usuário, quero adicionar tarefas para acompanhar meus compromissos."

8. Fluxograma:
[Login] → [Verificar Usuário] → [Acesso liberado] / [Erro]

9. Kanban:

| A Fazer | Em Andamento | Concluído |
|---------|--------------|-----------|
| Login   | Tela de tarefas | -     |
|         | Banco de dados  | -     |

10. Boas práticas:
- Comentários claros
- Padrões de codificação
- Documentação atualizada


```
#


## 🧮 Lógica de Programação

```logica
# 1. Positivo ou negativo
num = int(input("Digite um número: "))
if num >= 0:
    print("Positivo")
else:
    print("Negativo")

# 2. Maior valor
a = int(input("A: "))
b = int(input("B: "))
print("Maior:", a if a > b else b)

# 3. Tabuada do 7
for i in range(1, 11):
    print(f"7 x {i} = {7*i}")

# 4. Contar 1 a 100 e dizer se par
for i in range(1, 101):
    if i % 2 == 0:
        print(f"{i} é par")

# 5. Média de 3 notas
n1 = float(input("Nota 1: "))
n2 = float(input("Nota 2: "))
n3 = float(input("Nota 3: "))
media = (n1 + n2 + n3) / 3
print("Aprovado" if media >= 7 else "Reprovado")

```
#

