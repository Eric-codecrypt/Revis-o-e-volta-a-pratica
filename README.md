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

// 9. Mini MVC (estrutura de pastas)
/mvc
├── controller/
│   └── AlunoController.php
├── model/
│   └── Aluno.php
├── view/
│   └── alunoView.php
└── index.php

```css

## 🎨 CSS
