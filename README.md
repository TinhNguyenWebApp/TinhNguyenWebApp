##  ✨ TinhNguyenWebApp👋

<!--
**TinhNguyenWebApp/TinhNguyenWebApp** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<?xml version="1.0" encoding="utf-8"?>
<!--
  Animated space banner SVG
  - Save as assets/banner.svg in your repo
  - Edit the text lines below (line with id="title" and id="subtitle")
-->
<svg xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink"
     viewBox="0 0 1200 420"
     preserveAspectRatio="xMidYMid slice"
     role="img"
     aria-label="Space banner with animated stars and planet">
  <defs>
    <!-- background gradient -->
    <linearGradient id="bg" x1="0" x2="0" y1="0" y2="1">
      <stop offset="0%" stop-color="#061026"/>
      <stop offset="55%" stop-color="#041022"/>
      <stop offset="100%" stop-color="#020314"/>
    </linearGradient>

    <!-- radial soft glow for planet -->
    <radialGradient id="planetGlow" cx="35%" cy="50%" r="75%">
      <stop offset="0%" stop-color="#fff7d4" stop-opacity="0.8"/>
      <stop offset="40%" stop-color="#ffd28b" stop-opacity="0.25"/>
      <stop offset="100%" stop-color="#ff8a3d" stop-opacity="0"/>
    </radialGradient>

    <!-- planet surface pattern -->
    <radialGradient id="planetSurface" cx="40%" cy="35%">
      <stop offset="0%" stop-color="#9fd3ff"/>
      <stop offset="50%" stop-color="#2a98ff"/>
      <stop offset="100%" stop-color="#164b7a"/>
    </radialGradient>

    <filter id="softShadow" x="-50%" y="-50%" width="200%" height="200%">
      <feDropShadow dx="0" dy="8" stdDeviation="18" flood-color="#000" flood-opacity="0.6"/>
    </filter>

    <!-- reusable star circle -->
    <circle id="star" r="1.8" fill="#ffffff" />
  </defs>

  <!-- Background -->
  <rect width="100%" height="100%" fill="url(#bg)"/>

  <!-- distant faint nebula -->
  <g opacity="0.12">
    <ellipse cx="900" cy="120" rx="320" ry="140" fill="#2b3b66"/>
    <ellipse cx="280" cy="290" rx="220" ry="90" fill="#1f2a44"/>
  </g>

  <!-- animated starfield (cloned stars with different positions/animation) -->
  <g id="stars">
    <!-- We create multiple stars with different positions and animate opacity (twinkle) -->
    <!-- A handful to keep SVG size reasonable; add more if desired -->
    <use xlink:href="#star" x="80"  y="40"  opacity="0.8">
      <animate attributeName="opacity" values="0.1;0.9;0.2" dur="3.8s" repeatCount="indefinite" begin="0s"/>
    </use>
    <use xlink:href="#star" x="140" y="120" opacity="0.9">
      <animate attributeName="opacity" values="0.2;1;0.3" dur="4.6s" repeatCount="indefinite" begin="0.4s"/>
    </use>
    <use xlink:href="#star" x="210" y="60" opacity="0.7">
      <animate attributeName="opacity" values="0.05;0.8;0.1" dur="5.2s" repeatCount="indefinite" begin="0.8s"/>
    </use>
    <use xlink:href="#star" x="320" y="32" opacity="0.7">
      <animate attributeName="opacity" values="0.1;0.7;0.15" dur="4.2s" repeatCount="indefinite" begin="0.9s"/>
    </use>
    <use xlink:href="#star" x="480" y="110" opacity="0.6">
      <animate attributeName="opacity" values="0.05;0.85;0.2" dur="6.1s" repeatCount="indefinite" begin="0.2s"/>
    </use>
    <use xlink:href="#star" x="560" y="50" opacity="0.9">
      <animate attributeName="opacity" values="0.15;1;0.25" dur="3.6s" repeatCount="indefinite" begin="0.3s"/>
    </use>
    <use xlink:href="#star" x="700" y="90" opacity="0.7">
      <animate attributeName="opacity" values="0.05;0.8;0.15" dur="5.6s" repeatCount="indefinite" begin="0.7s"/>
    </use>
    <use xlink:href="#star" x="860" y="40" opacity="0.9">
      <animate attributeName="opacity" values="0.1;0.95;0.2" dur="4.0s" repeatCount="indefinite" begin="0.25s"/>
    </use>
    <use xlink:href="#star" x="1020" y="140" opacity="0.65">
      <animate attributeName="opacity" values="0.05;0.75;0.12" dur="6.3s" repeatCount="indefinite" begin="0.6s"/>
    </use>
    <use xlink:href="#star" x="1150" y="60" opacity="0.8">
      <animate attributeName="opacity" values="0.08;0.85;0.18" dur="4.8s" repeatCount="indefinite" begin="1s"/>
    </use>
    <!-- few smaller pinpoints -->
    <circle cx="920" cy="210" r="0.9" fill="#fff">
      <animate attributeName="opacity" values="0.05;0.9;0.05" dur="3.2s" repeatCount="indefinite" begin="0.2s"/>
    </circle>
    <circle cx="460" cy="240" r="0.8" fill="#fff">
      <animate attributeName="opacity" values="0.02;0.8;0.02" dur="5.1s" repeatCount="indefinite" begin="0.5s"/>
    </circle>
  </g>

  <!-- planet group positioned right -->
  <g id="planetWrap" transform="translate(980,210)">
    <!-- glow -->
    <circle cx="0" cy="0" r="90" fill="url(#planetGlow)" opacity="0.65" />
    <!-- orbit ring -->
    <ellipse cx="0" cy="0" rx="140" ry="60" fill="none" stroke="rgba(255,255,255,0.02)" stroke-width="1" />
    <!-- the planet itself -->
    <g id="planet" filter="url(#softShadow)">
      <!-- main sphere -->
      <circle cx="0" cy="0" r="48" fill="url(#planetSurface)"/>
      <!-- lighter land-ish shapes (simple) -->
      <path d="M-16,-6 C-4,-20 12,-18 22,-6 C18,6 2,14 -10,12 C-20,10 -26,-2 -16,-6 Z"
            fill="#1f7f5a" opacity="0.9"/>
      <path d="M-8,18 C4,26 20,24 26,14 C20,10 6,8 -6,12 C-8,14 -12,16 -8,18 Z"
            fill="#155f44" opacity="0.75"/>
      <!-- subtle shiny highlight -->
      <ellipse cx="-14" cy="-18" rx="9" ry="4" fill="rgba(255,255,255,0.3)"/>
    </g>

    <!-- rotation animation for planet group (spin effect) -->
    <animateTransform xlink:href="#planet" attributeName="transform"
                      type="rotate" from="0 0 0" to="360 0 0" dur="18s" repeatCount="indefinite" />

    <!-- small moon orbiting -->
    <g id="moonWrap">
      <circle cx="110" cy="-20" r="5" fill="#d7d7d7" opacity="0.95" />
      <animateTransform xlink:href="#moonWrap" attributeName="transform"
                        type="rotate" from="0 0 0" to="-360 0 0" dur="9s" repeatCount="indefinite" />
    </g>
  </g>

  <!-- center-left decorative faint comet streaming -->
  <g opacity="0.7" transform="translate(260,200) rotate(-12)">
    <ellipse cx="0" cy="0" rx="140" ry="10" fill="rgba(255,255,255,0.02)"/>
    <rect x="-220" y="-6" width="300" height="12" rx="6" fill="url(#bg)" opacity="0.03">
      <animate attributeName="x" from="-220" to="260" dur="9s" repeatCount="indefinite" />
    </rect>
  </g>

  <!-- Main text block (center-left) -->
  <g transform="translate(120,170)" font-family="Inter, Arial, Helvetica, sans-serif">
    <!-- Title -->
    <text id="title" x="0" y="0" font-size="38" fill="#ffffff" font-weight="700" letter-spacing="0.6">
      <tspan>Hi there! I'm</tspan>
      <tspan x="0" dy="46" fill="#9be7ff" font-size="44" font-weight="800">TinhNguyenWebApp</tspan>
    </text>

    <!-- Subtitle -->
    <text id="subtitle" x="0" y="120" font-size="18" fill="#c8d9ee" opacity="0.95">
      <tspan>Web/App Designer • Landing Page • Internal Software</tspan>
    </text>

    <!-- small tech icons (simple circles as placeholders; you can replace with inline SVG icons if want) -->
    <g transform="translate(0,160)">
      <rect x="0" y="-8" rx="8" ry="8" width="520" height="42" fill="rgba(255,255,255,0.02)"/>
      <!-- example circular icons -->
      <g transform="translate(12,12)">
        <circle cx="16" cy="6" r="12" fill="#f7df1e"/> <!-- js-like -->
        <text x="16" y="11" font-size="10" text-anchor="middle" fill="#111" font-weight="700">JS</text>
      </g>
      <g transform="translate(62,12)">
        <circle cx="16" cy="6" r="12" fill="#61dafb"/>
        <text x="16" y="11" font-size="10" text-anchor="middle" fill="#012">R</text>
      </g>
      <g transform="translate(112,12)">
        <circle cx="16" cy="6" r="12" fill="#3fb27f"/>
        <text x="16" y="11" font-size="10" text-anchor="middle" fill="#022">V</text>
      </g>
      <g transform="translate(162,12)">
        <circle cx="16" cy="6" r="12" fill="#0d1117"/>
        <text x="16" y="11" font-size="10" text-anchor="middle" fill="#fff">GH</text>
      </g>
      <g transform="translate(212,12)">
        <circle cx="16" cy="6" r="12" fill="#2563eb"/>
        <text x="16" y="11" font-size="10" text-anchor="middle" fill="#fff">VS</text>
      </g>
    </g>
  </g>

  <!-- subtle bottom vignette -->
  <rect y="320" width="1200" height="140" fill="black" opacity="0.06"/>
</svg>




