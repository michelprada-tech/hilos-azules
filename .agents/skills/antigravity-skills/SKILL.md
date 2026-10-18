---
name: antigravity-skills
description: "Transforms static HTML into cinematic, web-ready experiences using Draupnir's spectral powers (GSAP + ScrollTrigger + Lenis)."
---

# 🌌 ANTIGRAVITY SKILLS — UNIFIED MEGA EDITION

> **Aurora Effects Library** + **Cinematographer Mode** + **Code-Ready Templates**
> 
> Versão: 3.0 MEGA | Stack: GSAP + ScrollTrigger + Lenis

---

## 🎯 MISSÃO

Transformar Claude em um **CINEMATÓGRAFO DE CÓDIGO WEB** capaz de:

1. **CRIAR** websites Awwwards-tier do zero com efeitos cinematográficos
2. **CINEMATOGRAFAR** HTML existente sem modificar o design
3. **APLICAR** efeitos proprietários (Black Hole, Spiral Vortex, Magnetic, Parallax)

---

## 📦 O QUE ESTA SKILL INCLUI

| Componente | Descrição |
|------------|-----------|
| **Aurora Effects Library** | Efeitos proprietários com código testado |
| **Cinematographer Mode** | Sistema para dar vida a HTML estático |
| **Scene Architecture** | Mental model Composition → Scenes → Components |
| **Templates HTML** | Código pronto para copiar/colar |
| **Prompts Otimizados** | Instruções para diferentes cenários |

---

## 🔥 EFEITOS DISPONÍVEIS

### TIER S — ASSINATURA AURORA

| Efeito | Complexidade | Scroll? | Descrição |
|--------|--------------|---------|-----------|
| **Black Hole Reveal** | ⭐⭐⭐ | ✅ | Hero "sugado" revelando conteúdo |
| **Black Hole Spiral** | ⭐⭐⭐⭐ | ✅ | Variação com rotação |
| **Black Hole Shatter** | ⭐⭐⭐⭐ | ✅ | Múltiplos buracos (vidro quebrado) |
| **Spiral Vortex Menu** | ⭐⭐⭐⭐⭐ | ❌ | Menu 3D em espiral |
| **Parallax Depth Stack** | ⭐⭐ | ✅ | Camadas com velocidades diferentes |
| **Magnetic Interactions** | ⭐⭐ | ❌ | Cursor + elementos magnéticos |

### TIER A — ESSENCIAIS

| Efeito | Uso |
|--------|-----|
| Split Text Reveal | Headlines cinematográficos |
| Staggered Cards | Entrada em cascata |
| Floating Elements | Decorações animadas |
| Scroll Progress | Barra de progresso |
| Grain Overlay | Textura cinematográfica |

---

## 🎬 CINEMATOGRAPHER MODE

### ATIVAÇÃO

```
CINEMATOGRAPHER MODE ATIVADO.
Receba HTML estático e adicione VIDA sem modificar o design.
```

### REGRAS INVIOLÁVEIS

```
┌─────────────────────────────────────────────────────────────────┐
│  🚫 PROIBIDO:                                                   │
│  - Redesenhar QUALQUER elemento visual                          │
│  - Mudar cores, fontes, espaçamentos                            │
│  - Alterar estrutura HTML (exceto wrappers para 3D)             │
│  - Remover classes CSS existentes                               │
│                                                                  │
│  ✅ PERMITIDO:                                                   │
│  - Adicionar scripts JavaScript                                 │
│  - Adicionar data-attributes para controle                      │
│  - Criar wrappers necessários para efeitos 3D                   │
│  - Inserir canvas WebGL como background layer                   │
└─────────────────────────────────────────────────────────────────┘
```

### WORKFLOW

```
1. INVENTÁRIO → Analise elementos animáveis (NÃO MODIFIQUE)
2. PLANO → Defina timeline de animações
3. INJEÇÃO → CDNs no <head>
4. IMPLEMENTAÇÃO → Scripts no final do <body>
5. VALIDAÇÃO → HTML original 100% intacto
```

### OUTPUT CORRETO

```html
<!-- HTML ORIGINAL 100% INTACTO -->
<section class="hero">
  <h1>TITLE</h1>
</section>

<!-- SCRIPTS ADICIONADOS -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
<script src="https://unpkg.com/lenis@1.1.13/dist/lenis.min.js"></script>
<script>
// CINEMATOGRAPHER RUNTIME
gsap.from('.hero h1', {y: 100, opacity: 0, duration: 1});
</script>
```

---

## 🕳️ BLACK HOLE REVEAL — CÓDIGO COMPLETO

### Conceito
Hero fixo é "sugado" para um buraco negro central, revelando conteúdo abaixo.

### HTML Necessário

```html
<!-- Hero Layer (fixo) -->
<div class="hero-layer" id="heroLayer">
    <div class="hero-content">
        <div class="hero-bg-grid"></div>
        <div class="hero-bg-glow"></div>
        <div class="event-horizon-ring"></div>
        
        <div class="hero-badge">
            <span>◆</span>
            <span>Your Badge</span>
        </div>
        
        <h1 class="hero-title">YOUR TITLE</h1>
        <p class="hero-subtitle">Your Subtitle</p>
        <button class="hero-cta">Call to Action</button>
        
        <div class="scroll-indicator">
            <span>Scroll to Enter</span>
            <div class="arrow"></div>
        </div>
    </div>
</div>

<!-- Conteúdo revelado -->
<div class="content-below">
    <div class="scroll-spacer"></div>
    <section class="revealed-section">
        <!-- Seu conteúdo aqui -->
    </section>
</div>
```

### CSS Essencial

```css
:root {
    --gold: #D4AF37;
    --gold-light: #F8F1D2;
    --gold-dim: #8a7122;
    --void: #050505;
}

/* Hero Layer - Fixo com mask */
.hero-layer {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    z-index: 100;
    pointer-events: none;
    
    -webkit-mask-image: radial-gradient(
        circle at 50% 50%,
        transparent 0%,
        black 0%
    );
    mask-image: radial-gradient(
        circle at 50% 50%,
        transparent 0%,
        black 0%
    );
}

.hero-content {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: var(--void);
    position: relative;
    overflow: hidden;
    pointer-events: auto;
}

/* Background Grid */
.hero-bg-grid {
    position: absolute;
    inset: 0;
    background-image: 
        linear-gradient(to right, rgba(212, 175, 55, 0.03) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(212, 175, 55, 0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
}

/* Glow Center */
.hero-bg-glow {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 800px;
    height: 800px;
    background: radial-gradient(circle, rgba(212, 175, 55, 0.15) 0%, transparent 70%);
    pointer-events: none;
}

/* Event Horizon Ring */
.event-horizon-ring {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 500px;
    height: 500px;
    border-radius: 50%;
    border: 1px solid rgba(212, 175, 55, 0.2);
    box-shadow: 
        0 0 60px rgba(212, 175, 55, 0.1),
        inset 0 0 60px rgba(212, 175, 55, 0.05);
    pointer-events: none;
}

.event-horizon-ring::before {
    content: '';
    position: absolute;
    inset: -20px;
    border-radius: 50%;
    border: 1px solid rgba(212, 175, 55, 0.1);
}

.event-horizon-ring::after {
    content: '';
    position: absolute;
    inset: 20px;
    border-radius: 50%;
    border: 1px solid rgba(212, 175, 55, 0.15);
}

/* Typography */
.hero-badge {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 8px 16px;
    background: rgba(212, 175, 55, 0.1);
    border: 1px solid rgba(212, 175, 55, 0.3);
    margin-bottom: 40px;
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: 0.3em;
    color: var(--gold);
}

.hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 10vw, 8rem);
    font-weight: 400;
    font-style: italic;
    background: linear-gradient(180deg, var(--gold) 0%, var(--gold-light) 50%, var(--gold-dim) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-align: center;
    line-height: 1.1;
}

.hero-subtitle {
    font-size: clamp(1rem, 3vw, 1.5rem);
    font-weight: 300;
    letter-spacing: 0.5em;
    text-transform: uppercase;
    color: rgba(255, 255, 255, 0.6);
    margin-top: 20px;
}

.hero-cta {
    margin-top: 60px;
    padding: 20px 50px;
    background: var(--gold);
    color: #000;
    border: none;
    font-family: 'Space Grotesk', sans-serif;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all 0.4s ease;
}

.hero-cta:hover {
    background: #fff;
    box-shadow: 0 0 40px rgba(212, 175, 55, 0.5);
}

/* Scroll Indicator */
.scroll-indicator {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    color: rgba(255, 255, 255, 0.4);
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
}

.scroll-indicator .arrow {
    width: 20px;
    height: 20px;
    border-right: 1px solid rgba(212, 175, 55, 0.5);
    border-bottom: 1px solid rgba(212, 175, 55, 0.5);
    transform: rotate(45deg);
    animation: bounce 2s infinite;
}

@keyframes bounce {
    0%, 100% { transform: rotate(45deg) translateY(0); }
    50% { transform: rotate(45deg) translateY(10px); }
}

/* Content Below */
.content-below {
    position: relative;
    z-index: 1;
}

.scroll-spacer {
    height: 100vh;
    pointer-events: none;
}
```

### JavaScript Completo

```javascript
(function() {
    'use strict';
    
    // ═══════════════════════════════════════════════════════════
    // SMOOTH SCROLL (LENIS)
    // ═══════════════════════════════════════════════════════════
    
    const lenis = new Lenis({
        duration: 1.4,
        easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)),
        smoothWheel: true,
    });

    function raf(time) {
        lenis.raf(time);
        requestAnimationFrame(raf);
    }
    requestAnimationFrame(raf);

    gsap.registerPlugin(ScrollTrigger);
    gsap.ticker.add((time) => lenis.raf(time * 1000));
    gsap.ticker.lagSmoothing(0);

    // ═══════════════════════════════════════════════════════════
    // BLACK HOLE CONFIG
    // ═══════════════════════════════════════════════════════════
    
    const config = {
        startHoleSize: 0,
        endHoleSize: 150,
        edgeSoftness: 5,
    };
    
    const heroLayer = document.getElementById('heroLayer');
    const heroContent = heroLayer.querySelector('.hero-content');
    
    // ═══════════════════════════════════════════════════════════
    // BLACK HOLE SCROLL EFFECT
    // ═══════════════════════════════════════════════════════════
    
    ScrollTrigger.create({
        trigger: '.scroll-spacer',
        start: 'top top',
        end: 'bottom top',
        scrub: 1,
        onUpdate: (self) => {
            const progress = self.progress;
            const easedProgress = progress * progress; // easeInQuad
            const holeSize = config.startHoleSize + (easedProgress * config.endHoleSize);
            const edgeEnd = holeSize + config.edgeSoftness;
            
            // Update mask
            heroLayer.style.maskImage = `radial-gradient(
                circle at 50% 50%,
                transparent ${holeSize}%,
                black ${edgeEnd}%
            )`;
            heroLayer.style.webkitMaskImage = heroLayer.style.maskImage;
            
            // Pull effect
            const pullScale = 1 + (easedProgress * 0.1);
            const pullOpacity = 1 - (easedProgress * 0.5);
            heroContent.style.transform = `scale(${pullScale})`;
            heroContent.style.opacity = pullOpacity;
            
            // Pointer events
            heroLayer.style.pointerEvents = holeSize > 50 ? 'none' : 'auto';
        }
    });

    // ═══════════════════════════════════════════════════════════
    // EVENT HORIZON RING ANIMATION
    // ═══════════════════════════════════════════════════════════
    
    const eventHorizon = document.querySelector('.event-horizon-ring');
    if (eventHorizon) {
        ScrollTrigger.create({
            trigger: '.scroll-spacer',
            start: 'top top',
            end: 'bottom top',
            scrub: 0.5,
            onUpdate: (self) => {
                const rotation = self.progress * 180;
                const scale = 1 - (self.progress * 0.3);
                eventHorizon.style.transform = 
                    `translate(-50%, -50%) rotate(${rotation}deg) scale(${scale})`;
            }
        });
    }

    // ═══════════════════════════════════════════════════════════
    // REVEALED CONTENT ANIMATIONS
    // ═══════════════════════════════════════════════════════════
    
    gsap.from('.revealed-section .section-title', {
        y: 40,
        opacity: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
            trigger: '.revealed-section',
            start: 'top 60%',
        }
    });

    gsap.from('.card', {
        y: 60,
        opacity: 0,
        duration: 0.8,
        stagger: 0.15,
        ease: 'power3.out',
        scrollTrigger: {
            trigger: '.cards-grid',
            start: 'top 80%',
        }
    });

    console.log('🕳️ Black Hole Effect Initialized');
})();
```

### Variações

```javascript
// SPIRAL VORTEX — Conteúdo gira enquanto é sugado
onUpdate: (self) => {
    const progress = self.progress;
    const easedProgress = progress * progress;
    const holeSize = easedProgress * 150;
    const rotation = progress * 720;
    const scale = 1 - (easedProgress * 0.3);
    
    heroLayer.style.maskImage = `radial-gradient(
        circle at 50% 50%,
        transparent ${holeSize}%,
        black ${holeSize + 8}%
    )`;
    heroContent.style.transform = `scale(${scale}) rotate(${rotation}deg)`;
    heroContent.style.opacity = 1 - easedProgress;
}

// IMPLODE — Efeito 3D
onUpdate: (self) => {
    const progress = self.progress;
    const easedProgress = Math.pow(progress, 1.5);
    const holeSize = easedProgress * 160;
    const scale = 1 - (easedProgress * 0.6);
    const rotateX = easedProgress * 20;
    const translateZ = -easedProgress * 500;
    
    heroLayer.style.maskImage = `radial-gradient(
        circle at 50% 50%,
        transparent ${holeSize}%,
        black ${holeSize + 3}%
    )`;
    heroContent.style.perspective = '1000px';
    heroContent.style.transform = `scale(${scale}) rotateX(${rotateX}deg) translateZ(${translateZ}px)`;
}

// SHATTER — Múltiplos buracos
onUpdate: (self) => {
    const progress = self.progress;
    const easedProgress = progress * progress;
    
    const hole1 = easedProgress * 100;
    const hole2 = Math.max(0, (progress - 0.2) * 1.25) * 60;
    const hole3 = Math.max(0, (progress - 0.3) * 1.43) * 50;
    const hole4 = Math.max(0, (progress - 0.4) * 1.67) * 40;
    
    heroLayer.style.maskImage = `
        radial-gradient(circle at 50% 50%, transparent ${hole1}%, black ${hole1 + 5}%),
        radial-gradient(circle at 30% 30%, transparent ${hole2}%, black ${hole2 + 3}%),
        radial-gradient(circle at 70% 70%, transparent ${hole3}%, black ${hole3 + 3}%),
        radial-gradient(circle at 70% 30%, transparent ${hole4}%, black ${hole4 + 3}%)
    `;
    heroLayer.style.maskComposite = 'intersect';
    
    const shake = Math.sin(progress * 50) * (1 - progress) * 3;
    heroContent.style.transform = `translateX(${shake}px)`;
}
```

---

## 🌀 SPIRAL VORTEX MENU — CÓDIGO COMPLETO

### Conceito
Menu fullscreen com itens orbitando uma singularidade central.

### Config

```javascript
const config = {
    baseRadius: 250,
    radiusIncrement: 30,
    startAngle: -90,
    angleIncrement: 45,
    rotationPerScroll: 15,
    spiralInDuration: 0.8,
    spiralOutDuration: 0.5,
};
```

### HTML

```html
<button class="menu-trigger" id="menuTrigger">
    <span class="menu-trigger-text">Menu</span>
    <span class="menu-trigger-icon">
        <span></span><span></span><span></span>
    </span>
</button>

<div class="spiral-menu" id="spiralMenu">
    <div class="spiral-bg">
        <div class="spiral-bg-grid"></div>
        <div class="spiral-bg-glow"></div>
        <div class="vortex-ring"></div>
        <div class="vortex-ring"></div>
        <div class="vortex-ring"></div>
        <div class="vortex-ring"></div>
        <div class="vortex-ring"></div>
    </div>
    
    <div class="singularity" id="singularity"></div>
    
    <div class="spiral-items" id="spiralItems">
        <a href="#" class="spiral-item">
            <span class="spiral-item-number">01</span>
            <span class="spiral-item-text">Home</span>
        </a>
        <a href="#" class="spiral-item">
            <span class="spiral-item-number">02</span>
            <span class="spiral-item-text">About</span>
        </a>
        <a href="#" class="spiral-item">
            <span class="spiral-item-number">03</span>
            <span class="spiral-item-text">Work</span>
        </a>
        <a href="#" class="spiral-item">
            <span class="spiral-item-number">04</span>
            <span class="spiral-item-text">Services</span>
        </a>
        <a href="#" class="spiral-item">
            <span class="spiral-item-number">05</span>
            <span class="spiral-item-text">Contact</span>
        </a>
    </div>
</div>
```

### JavaScript Core

```javascript
(function() {
    const config = {
        baseRadius: 250,
        radiusIncrement: 30,
        startAngle: -90,
        angleIncrement: 45,
        rotationPerScroll: 15,
    };
    
    const menuTrigger = document.getElementById('menuTrigger');
    const spiralMenu = document.getElementById('spiralMenu');
    const singularity = document.getElementById('singularity');
    const spiralItems = document.querySelectorAll('.spiral-item');
    const vortexRings = document.querySelectorAll('.vortex-ring');
    
    let isOpen = false;
    let currentRotation = 0;
    
    function positionItems(rotation) {
        spiralItems.forEach((item, index) => {
            const angle = config.startAngle + (index * config.angleIncrement) + rotation;
            const radius = config.baseRadius + (index * config.radiusIncrement);
            const radians = angle * (Math.PI / 180);
            
            const x = Math.cos(radians) * radius;
            const y = Math.sin(radians) * radius;
            
            const normalizedY = (y / radius + 1) / 2;
            const scale = 1.2 - (normalizedY * 0.5);
            const opacity = 1 - (normalizedY * 0.5);
            
            gsap.to(item, {
                x, y, scale, opacity,
                duration: 0.5,
                ease: 'power2.out',
            });
            
            item.style.zIndex = Math.round((1 - normalizedY) * 100);
        });
    }
    
    function openMenu() {
        isOpen = true;
        spiralMenu.classList.add('active');
        document.body.classList.add('menu-open');
        
        gsap.fromTo(singularity, 
            { scale: 0 },
            { scale: 1, duration: 0.6, ease: 'back.out(2)' }
        );
        
        gsap.fromTo(vortexRings,
            { scale: 0, opacity: 0 },
            { scale: 1, opacity: 1, duration: 0.8, stagger: 0.1, ease: 'power2.out' }
        );
        
        spiralItems.forEach((item, index) => {
            const angle = config.startAngle + (index * config.angleIncrement);
            const radius = config.baseRadius + (index * config.radiusIncrement);
            const radians = angle * (Math.PI / 180);
            
            gsap.fromTo(item,
                { x: 0, y: 0, scale: 0, rotation: -180, opacity: 0 },
                {
                    x: Math.cos(radians) * radius,
                    y: Math.sin(radians) * radius,
                    scale: 1, rotation: 0, opacity: 1,
                    duration: 0.8,
                    delay: 0.2 + index * 0.08,
                    ease: 'back.out(1.2)',
                }
            );
        });
    }
    
    function closeMenu() {
        isOpen = false;
        document.body.classList.remove('menu-open');
        
        spiralItems.forEach((item, index) => {
            gsap.to(item, {
                x: 0, y: 0, scale: 0, rotation: 180, opacity: 0,
                duration: 0.5,
                delay: index * 0.05,
                ease: 'power2.in',
            });
        });
        
        gsap.to(singularity, { scale: 0, duration: 0.4, delay: 0.3 });
        gsap.to(vortexRings, { scale: 0, opacity: 0, duration: 0.5, stagger: 0.05 });
        
        setTimeout(() => {
            spiralMenu.classList.remove('active');
            currentRotation = 0;
        }, 800);
    }
    
    menuTrigger.addEventListener('click', () => isOpen ? closeMenu() : openMenu());
    
    window.addEventListener('wheel', (e) => {
        if (!isOpen) return;
        e.preventDefault();
        currentRotation += (e.deltaY > 0 ? 1 : -1) * config.rotationPerScroll;
        positionItems(currentRotation);
    }, { passive: false });
    
    window.addEventListener('keydown', (e) => {
        if (e.key === 'Escape' && isOpen) closeMenu();
    });
    
    // Vortex rings rotation
    vortexRings.forEach((ring, i) => {
        gsap.to(ring, {
            rotation: i % 2 === 0 ? 360 : -360,
            duration: 60 + i * 10,
            repeat: -1,
            ease: 'none',
        });
    });
})();
```

---

## 🧲 MAGNETIC INTERACTIONS — CÓDIGO COMPLETO

### Custom Cursor

```javascript
const cursor = document.getElementById('cursor');
let mouseX = 0, mouseY = 0, cursorX = 0, cursorY = 0;

document.addEventListener('mousemove', (e) => {
    mouseX = e.clientX;
    mouseY = e.clientY;
});

function updateCursor() {
    cursorX += (mouseX - cursorX) * 0.15;
    cursorY += (mouseY - cursorY) * 0.15;
    gsap.set(cursor, { x: cursorX, y: cursorY });
    requestAnimationFrame(updateCursor);
}
updateCursor();
```

### Magnetic Elements

```javascript
document.querySelectorAll('[data-magnetic]').forEach(el => {
    const strength = parseFloat(el.dataset.magnetic) || 0.3;
    
    el.addEventListener('mouseenter', () => cursor.classList.add('hover'));
    el.addEventListener('mouseleave', () => {
        cursor.classList.remove('hover');
        gsap.to(el, { x: 0, y: 0, duration: 0.6, ease: 'elastic.out(1, 0.4)' });
    });
    
    el.addEventListener('mousemove', (e) => {
        const rect = el.getBoundingClientRect();
        const centerX = rect.left + rect.width / 2;
        const centerY = rect.top + rect.height / 2;
        gsap.to(el, {
            x: (e.clientX - centerX) * strength,
            y: (e.clientY - centerY) * strength,
            duration: 0.3,
            ease: 'power2.out',
        });
    });
});
```

### CSS

```css
* { cursor: none; }

.cursor {
    position: fixed;
    top: 0;
    left: 0;
    pointer-events: none;
    z-index: 99999;
    mix-blend-mode: difference;
}

.cursor-dot {
    position: absolute;
    top: -4px;
    left: -4px;
    width: 8px;
    height: 8px;
    background: #fff;
    border-radius: 50%;
}

.cursor-ring {
    position: absolute;
    top: -20px;
    left: -20px;
    width: 40px;
    height: 40px;
    border: 1px solid rgba(255, 255, 255, 0.5);
    border-radius: 50%;
    transition: transform 0.15s, border-color 0.3s;
}

.cursor.hover .cursor-ring {
    transform: scale(1.5);
    border-color: var(--gold);
    background: rgba(212, 175, 55, 0.1);
}
```

---

## 📐 PARALLAX DEPTH STACK — CÓDIGO COMPLETO

### HTML

```html
<section class="hero">
    <div class="hero-bg" data-speed="0.2"></div>
    <div class="hero-grid" data-speed="0.3"></div>
    <div class="decoration" data-speed="0.4"></div>
    <div class="decoration" data-speed="0.5"></div>
    <div class="hero-content" data-speed="0.6">
        <h1>Title</h1>
    </div>
    <div class="foreground-line" data-speed="0.9"></div>
</section>
```

### JavaScript

```javascript
document.querySelectorAll('[data-speed]').forEach(el => {
    const speed = parseFloat(el.dataset.speed);
    const movement = (1 - speed) * 100;
    
    gsap.to(el, {
        yPercent: -movement,
        ease: 'none',
        scrollTrigger: {
            trigger: el.closest('section'),
            start: 'top bottom',
            end: 'bottom top',
            scrub: true,
        }
    });
});
```

### Guia de Velocidades

```
Layer       Speed    Movimento
───────────────────────────────
Background  0.2      -80%
Grid        0.3      -70%
Decorations 0.4-0.5  -60% a -50%
Content     0.6      -40%
Foreground  0.8-0.9  -20% a -10%
```

---

## 📦 CDN DEPENDENCIES

```html
<!-- OBRIGATÓRIO -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
<script src="https://unpkg.com/lenis@1.1.13/dist/lenis.min.js"></script>

<!-- FONTES RECOMENDADAS -->
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
```

---

## 🎨 STYLE PRESETS

### Swiss Private Banking
```css
:root {
    --gold: #D4AF37;
    --gold-light: #F8F1D2;
    --gold-dim: #8a7122;
    --void: #050505;
    --cream: #FAFAF8;
}
/* Animações lentas (1s+), power2.out, muito whitespace */
```

### Tech Brutal
```css
:root {
    --accent: #FF0000;
    --bg: #000000;
    --text: #FFFFFF;
}
/* Animações rápidas (0.3s), linear, high contrast */
```

### Organic Luxury
```css
:root {
    --accent: #8B7355;
    --bg: #F5F0EB;
    --text: #2C2416;
}
/* Animações fluidas, elastic.out */
```

---

## ✅ CHECKLIST DE QUALIDADE

```
VISUAL
□ Tipografia distintiva (não Inter/Roboto)
□ Palette cohesiva
□ Zero elementos genéricos

ANIMAÇÃO
□ Load sequence cronometrada
□ Scroll animations 60fps
□ Stagger timing natural (0.1-0.15s)
□ Easing consistente (power3.out)

TÉCNICO
□ GSAP registrado
□ ScrollTrigger cleanup (React)
□ Lenis conectado ao GSAP ticker
□ Mobile: reduced-motion

CINEMATOGRAPHER
□ HTML original 100% intacto
□ Apenas scripts adicionados
□ Nenhum redesign
```

---

## 🚀 QUICK PROMPTS

### Criar site com Black Hole
```
Use Antigravity Skills MEGA.
Crie landing page estilo Swiss Banking com:
- Hero usando BLACK HOLE REVEAL
- Features com parallax depth stack
- CTA com magnetic buttons
- Smooth scroll Lenis
```

### Cinematografar código existente
```
CINEMATOGRAPHER MODE ATIVADO.
Adicione VIDA ao HTML abaixo sem modificar o design:
- Smooth scroll
- Hero entrance
- Parallax backgrounds
- Magnetic buttons

REGRA: HTML 100% INTACTO. Apenas adicione <script>.

[HTML AQUI]
```

### Aplicar efeito específico
```
Aplique SPIRAL VORTEX MENU.
Items: Home, About, Work, Services, Contact
Estilo: Gold accent, void background
```

---

## 📚 REFERÊNCIAS

### Sites Tier S
- **Studio Dialect** - studiodialect.com
- **Exoape** - exoape.com
- **Fantasy** - fantasy.co
- **Talhaaclark** - talhaaclark.com.au

---

*Antigravity Skills MEGA v3.0 — Aurora Gold Pipeline*
*"Make websites that move people."*
