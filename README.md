# 🌀 Como Criar um Bloco Giratório 3D com HTML e CSS

Veja o projeto completo:  
👉 [https://blocogiratorio.netlify.app/](https://blocogiratorio.netlify.app/)

---

## 📦 Estrutura HTML

```html
<div class="cube-container">
  <div class="cube">
    <div class="face front"></div>
    <div class="face back"></div>
    <div class="face left"></div>
    <div class="face right"></div>
    <div class="face top"></div>
    <div class="face bottom"></div>
  </div>
</div>


---

🎨 Estilização CSS

body {
  margin: 0;
  background: #101820;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
}

.cube-container {
  perspective: 1000px;
  width: 150px;
  height: 150px;
}

.cube {
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  animation: spin 6s infinite linear;
  position: relative;
}

.face {
  position: absolute;
  width: 150px;
  height: 150px;
  background: #007BFF;
  opacity: 0.9;
  border: 2px solid #fff;
}

.front  { transform: translateZ(75px); }
.back   { transform: rotateY(180deg) translateZ(75px); }
.left   { transform: rotateY(-90deg) translateZ(75px); }
.right  { transform: rotateY(90deg) translateZ(75px); }
.top    { transform: rotateX(90deg) translateZ(75px); }
.bottom { transform: rotateX(-90deg) translateZ(75px); }

@keyframes spin {
  from { transform: rotateX(0) rotateY(0); }
  to   { transform: rotateX(360deg) rotateY(360deg); }
}


---

🧠 Interatividade com JS (opcional)

document.querySelector('.cube').addEventListener('click', () => {
  const sounds = ["click1.mp3", "click2.mp3"];
  const audio = new Audio(sounds[Math.floor(Math.random() * sounds.length)]);
  audio.play();
});


---

📘 Créditos

Projeto criado por um autor anônimo.
Acesse o site completo e interativo:
🔗 https://blocogiratorio.netlify.app/
