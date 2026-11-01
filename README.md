# 💐 Buquê de Lírios em ASCII
 
Um buquê de **13 lírios em 3D** que brotam de um morrinho de grama, desabrocham um a um e balançam com a brisa, tudo desenhado com **letras e símbolos** sobre um céu estrelado.
 
Um arquivo só, sem instalar nada. É só abrir no navegador.
 
> 🔗 **Demo ao vivo:** `https://g0rda0.github.io/Buque-de-Lirios-em-ASCII/`
 
---
 
## ✨ O que tem na animação
 
- 🌷 **13 lírios** de cores diferentes (vermelho, rosa, amarelo, branco, pêssego...), cada um com 6 pétalas curvas e dobradas
- 🌱 Caules, folhas e um **morrinho de terra com grama** que sobe do chão
- 🌬️ **Vento** que balança as flores e a grama
- ⭐ Céu com **estrelinhas que piscam**, **estrelas cadentes** e brilhos de 4 pontas
- 🔤 Tudo "traduzido" em **caracteres ASCII coloridos**, com um leve efeito de cintilação
---
 
## 🎮 Como interagir
 
| Ação | O que acontece |
|---|---|
| Arrastar o mouse / dedo | Sopra uma brisa que balança o buquê |
| Clicar / tocar na tela | **Replanta** o buquê (reinicia a animação) |
| Tecla `Espaço` ou `R` | Também reinicia |
 
Funciona no computador e no celular.
 
---
 
## ▶️ Como usar
 
**Abrir direto**
1. Baixe o arquivo `index.html` (ou `Flores.html`).
2. Dê dois cliques nele. Ele abre no seu navegador.

---
 
## 🧠 Como funciona
 
Esta é a parte curiosa do projeto. A ideia é uma "máquina de duas etapas":
 
1. **Desenha as flores em 3D num canvas escondido.** A cada quadro, o código calcula a posição de cada pétala, folha e caule, projeta tudo na tela e pinta de trás para frente (algoritmo do pintor) com iluminação e névoa de profundidade.
2. **Converte a imagem em ASCII.** Um *shader* (programa que roda na placa de vídeo) divide a imagem em uma grade de células. Para cada célula, ele calcula o brilho e a cor médios e escolhe o caractere que melhor representa aquele brilho, de `.` (escuro) até `@` (claro).
Se o navegador não tiver WebGL ou o PixiJS não carregar, entra um **plano B em Canvas 2D** que faz a mesma conversão.
 
**Tecnologias:** HTML, CSS, JavaScript puro, Canvas 2D e [PixiJS 7](https://pixijs.com/) (WebGL).
 
---
 
## 🛠️ Personalize
 
Tudo fica no próprio arquivo, perto do começo do `<script>`:
 
- **`LILIES`**: posição, tamanho e cor de cada flor. Troque as cores ou o número de flores.
- **`PAL`**: paleta de cores dos lírios.
- **`RAMP`**: a sequência de caracteres usada no efeito ASCII (do mais apagado ao mais forte).
- **`windAt`**: a força e o ritmo do vento.
---
 
## ⚠️ Observações
 
- O PixiJS é carregado de um CDN, então na primeira vez é preciso estar **online**. Sem internet, a animação funciona no plano B (Canvas 2D).
- Em celulares mais antigos, o modo WebGL costuma ser mais fluido do que o Canvas 2D.
---
 
## 📄 Licença
 
Distribuído sob a licença **MIT**. Sinta-se livre para usar e adaptar, mantendo o crédito.
 
Feito por **gordaoprojetos** · [Instagram](https://www.instagram.com/gordaoprojetos/)
