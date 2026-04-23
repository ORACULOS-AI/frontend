# ORACULOS Landing Page - Modular

Landing page da ORACULOS com estética street/urban reconstruída do zero.

## 📁 Estrutura de Arquivos

```
landing-page/
├── index.html              ← Arquivo principal (com CSS e JS inline)
├── styles.css              ← CSS standalone (para manutenção)
├── scripts.js              ← JavaScript standalone (para manutenção)
├── README.md               ← Este arquivo
├── scripts/
│   ├── assemble.py         ← Script para montar HTML modular
│   └── recover.py          ← Script para recuperar CSS/JS de backup
├── sections/               ← Seções modulares (HTML fragments)
│   ├── hero.html           ← Seção hero principal
│   ├── manifesto.html      ← "Quem Somos" - Manifesto
│   ├── capabilities.html   ← "Capacidades" - 6 cards
│   ├── marquee.html        ← Ticker animado
│   ├── opensource.html     ← ORACULOS OS + Terminal
│   ├── team.html           ← Grid de membros do time
│   ├── videos.html         ← Embed Instagram + CTA
│   └── footer.html         ← Footer completo
└── components/             ← Componentes reutilizáveis
    ├── navbar.html         ← Navbar + menu mobile
    ├── loading-screen.html ← Tela de carregamento
    └── back-to-top.html    ← Botão voltar ao topo
```

## 🎨 Estética

- **Cores base:** Preto (#000) e Branco (#FFF) dominantes
- **Acentos street:** Neon blue (#00D4FF), Neon pink (#FF2D7B), Acid green (#BFFF00)
- **Tipografia:** 
  - Display: Space Grotesk (bold)
  - Body: Inter
  - Mono: JetBrains Mono
  - Hero: Bebas Neue
- **Elementos visuais:** Wireframe grid, spray paint blobs, starburst, color blocks, lightning doodles, halftone, asphalt texture, scanlines, noise overlay
- **Efeitos:** Glitch animation, scroll reveal, typewriter terminal, custom cursor, parallax

## 🚀 Como Usar

### Desenvolvimento
Abra diretamente `index.html` no navegador. O CSS e JS estão inline para performance.

### Manutenção por Seção
1. Edite o arquivo em `sections/` ou `components/` conforme necessário
2. Copie o conteúdo para o `index.html` na posição correspondente
3. Ou use o script de assembly: `python scripts/assemble.py`

### Build
```bash
cd landing-page
python scripts/assemble.py
# Gera index.complete.html com todas as seções montadas
```

## ✨ Seções da Página

| Seção | Arquivo | Descrição |
|-------|---------|-----------|
| Loading Screen | `components/loading-screen.html` | Animação de boot tipo terminal |
| Navbar | `components/navbar.html` | Navegação fixa com menu mobile |
| Hero | `sections/hero.html` | Título principal + CTAs |
| Manifesto | `sections/manifesto.html` | "Quem Somos" + stats |
| Capabilities | `sections/capabilities.html` | 6 cards de capacidades técnicas |
| Marquee | `sections/marquee.html` | Ticker infinito com keywords |
| Open Source | `sections/opensource.html` | ORACULOS OS + terminal animado |
| Team | `sections/team.html` | Grid com 13 membros |
| Videos | `sections/videos.html` | Embed Instagram |
| Footer | `sections/footer.html` | CTAs + links + mapa |

## 🎯 Interactions

- **Loading screen:** Sequência de boot com terminal animado
- **Custom cursor:** Círculo + trail que reage a hover
- **Glitch effect:** No hero title e capability cards
- **Scroll reveal:** Elementos aparecem ao entrar na viewport
- **Typewriter:** Terminal ORACULOS OS com efeito de digitação
- **Navbar:** Background escuro ao scrollar
- **Back to top:** Botão aparece após 500px de scroll
- **Parallax:** Grid do hero se move com scroll
- **Counters:** Animação de contagem nos stats

## 📱 Responsivo

- Desktop: 3 colunas nos cards, 4 colunas no team
- Tablet: 2 colunas
- Mobile: 1 coluna, menu hamburger

## 🔧 Cores (CSS Variables)

```css
--black: #000000
--black-soft: #111111
--white: #FFFFFF
--gray-mid: #888888
--gray-dark: #333333
--neon-blue: #00D4FF
--neon-pink: #FF2D7B
--acid-green: #BFFF00
--spray-orange: #FF6B2B
```

## 📝 Notas

- CSS e JS estão inline no `index.html` para performance (single file deploy)
- Arquivos `styles.css` e `scripts.js` são para referência/manutenção
- Seções em `sections/` e `components/` facilitam edição modular
- Google Fonts carregadas via preconnect para performance

---

Feito na rua · UFC Russas · Apache 2.0 · 2025–2026
