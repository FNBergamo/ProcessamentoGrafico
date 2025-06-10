# Resposta ao Desafio – Módulo 5

## 🎯 Controle e Animação de Sprites

Este projeto implementa um personagem central (o Vampirão) que permanece fixo no centro da janela enquanto o **fundo se move**, criando a ilusão de deslocamento. A classe `Sprite` suporta animações usando spritesheets, e o controle é feito via teclado (WASD e setas) para as 4 direções.

---

## ✅ Funcionalidades Implementadas

- [x] **Animação por spritesheet** para os estados _walk_ e _idle_
- [x] **Controle de direção** por teclado: movimenta o fundo conforme W, A, S, D ou setas
- [x] **Loop contínuo de animação** com taxa de \~12 FPS
- [x] **Fundo deslocável**, simulando movimento enquanto o vampirão permanece centrado

---

## 🛠 Tecnologias Utilizadas

- C++
- OpenGL
- GLFW
- GLAD
- GLM
- STB_IMAGE

---

## 🎮 Controles no Teclado

| Tecla         | Ação                                                           |
| ------------- | -------------------------------------------------------------- |
| W ou ↑        | Animação de caminhada para o norte                             |
| S ou ↓        | Animação de caminhada para o sul                               |
| A ou ←        | Move fundo para a esquerda; Animação de caminhada para o oeste |
| D ou →        | Move fundo para a direita; Animação de caminhada para o leste  |
| Nenhuma tecla | Vampirão entra em modo idle                                    |

---

## ℹ️ Estrutura e Funcionamento

- **`Sprite vamp`**: personagem central com animações de caminhada (_walk_) e parada (_idle_).
- **`Sprite bg`**: fundo que se desloca sobre tecla pressionada para simular movimento.
- A lógica de input define `dir`, animação e atualiza `vamp.texID`, `vamp.nFrames`, `vamp.ds`, `vamp.dt`.
- Quando `isMoving == true`, o fundo se desloca proporcional ao vetor `dir`, sem mover o vampirão.

---

## 🚀 Possíveis Evoluções

- Inserir colisões com objetos/parallax

---

## 📝 Observações Finais

Este projeto atende aos requisitos de:

- Suporte a spritesheet & animação
- Controle direcional via teclado
- Ilusão de movimento por deslocamento do plano de fundo
