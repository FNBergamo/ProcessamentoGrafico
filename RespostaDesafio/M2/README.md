# Exercícios com OpenGL 3.3+

## 🎯 Objetivo

Este projeto tem como objetivo praticar a criação e manipulação de geometria básica com OpenGL moderno (versão 3.3+), com foco em VAOs, buffers e uso opcional de matrizes de transformação via GLM.

Os exercícios foram desenvolvidos com base no material da disciplina e no repositório de exemplos fornecido.

--- 

## 🧩 Estrutura da Solução

### 📌 Parte 1 – Sem Matriz de Transformação

#### ✅ Exercício 1
- Implementada a função:
  ```cpp
  GLuint createTriangle(float x0, float y0, float x1, float y1, float x2, float y2);

* Cria um triângulo com os vértices passados por parâmetro e retorna o identificador do VAO correspondente.

#### ✅ Exercício 2

* Utilização da função `createTriangle` para criar **5 triângulos**.
* Os VAOs criados foram armazenados em um `std::vector<GLuint>`.
* Durante a renderização, o programa **itera sobre o vetor** para desenhar todos os triângulos.

---

### 📌 Parte 2 – Com Matriz de Transformação

#### ✅ Exercício 3

* Criada a estrutura `Triangle` contendo:

  * A **posição** (x, y) do triângulo.
  * A **cor** (RGB).
* Utilizado um **único VAO fixo** para representar um triângulo padrão.
* As posições e cores dos triângulos são armazenadas em um `std::vector<Triangle>`.
* A cada clique do mouse, um novo triângulo é adicionado com:

  * Transformação aplicada com **GLM** para posicionamento.
  * Cor **aleatória**, gerada dinamicamente.

---

## 🛠️ Tecnologias Utilizadas

* C++
* OpenGL 3.3+
* GLFW
* GLAD
* GLM

---

## 📝 Observações

* A resolução da janela é de **800x600**, com projeção ortográfica.
* Cada triângulo criado a partir do clique do mouse é transformado via **GLM** para sua respectiva posição.
* Este projeto segue os padrões propostos em aula e utiliza boas práticas de organização e reaproveitamento de VAOs e estruturas.
