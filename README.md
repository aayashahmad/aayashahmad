<svg viewBox="0 0 1180 610" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
  <defs>
    <!-- Light Mode Gradients -->
    <linearGradient id="accentGradLight" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#2563EB;stop-opacity:1">
        <animate attributeName="offset" from="0%" to="100%" dur="8s" repeatCount="indefinite" />
      </stop>
      <stop offset="50%" style="stop-color:#06B6D4;stop-opacity:1">
        <animate attributeName="offset" from="50%" to="150%" dur="8s" repeatCount="indefinite" />
      </stop>
      <stop offset="100%" style="stop-color:#10B981;stop-opacity:1">
        <animate attributeName="offset" from="100%" to="200%" dur="8s" repeatCount="indefinite" />
      </stop>
    </linearGradient>

    <radialGradient id="bgGlowLight" cx="50%" cy="50%" r="50%">
      <stop offset="0%" style="stop-color:#2563EB;stop-opacity:0.08" />
      <stop offset="100%" style="stop-color:#06B6D4;stop-opacity:0.02" />
    </radialGradient>

    <linearGradient id="asciiGradLight" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#06B6D4;stop-opacity:1" />
      <stop offset="50%" style="stop-color:#2563EB;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#06B6D4;stop-opacity:1" />
      <animate attributeName="y1" from="0%" to="100%" dur="6s" repeatCount="indefinite" />
      <animate attributeName="y2" from="100%" to="200%" dur="6s" repeatCount="indefinite" />
    </linearGradient>

    <!-- Glow Filter -->
    <filter id="glowLight">
      <feGaussianBlur stdDeviation="2.5" result="coloredBlur" />
      <feMerge>
        <feMergeNode in="coloredBlur" />
        <feMergeNode in="SourceGraphic" />
      </feMerge>
    </filter>

    <!-- Scanline Filter -->
    <pattern id="scanlinesLight" x="0" y="0" width="100%" height="4" patternUnits="userSpaceOnUse">
      <line x1="0" y1="0" x2="100%" y2="0" stroke="rgba(15,23,42,0.01)" stroke-width="2" />
    </pattern>

    <!-- Noise Pattern -->
    <filter id="noiseLight">
      <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="4" />
      <feDisplacementMap in="SourceGraphic" scale="0.5" />
    </filter>
  </defs>

  <!-- Background -->
  <rect width="1180" height="610" fill="#FFFFFF" />

  <!-- Background Glow -->
  <ellipse cx="200" cy="100" rx="400" ry="300" fill="url(#bgGlowLight)">
    <animate attributeCx="from" by="50" dur="8s" repeatCount="indefinite" />
  </ellipse>
  <ellipse cx="1000" cy="500" rx="350" ry="250" fill="url(#bgGlowLight)" opacity="0.5">
    <animate attributeCx="from" by="-40" dur="10s" repeatCount="indefinite" />
  </ellipse>

  <!-- Main Container -->
  <g>
    <!-- Left Section - ASCII Art -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.5s" fill="freeze" />
      
      <!-- Floating Animation -->
      <g>
        <animateTransform attributeName="transform" type="translate" 
          from="0 0" to="0 -8" dur="4s" 
          values="0 0; 0 -8; 0 0" repeatCount="indefinite" />
        
        <!-- ASCII Portrait -->
        <g filter="url(#glowLight)">
          <text x="140" y="120" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ░░░░░░░░░░░░
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0s" fill="freeze" />
          </text>
          <text x="140" y="135" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ▓▓░░░░░░░░▓▓
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.1s" fill="freeze" />
          </text>
          <text x="140" y="150" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ██░░██░░░░██
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.2s" fill="freeze" />
          </text>
          <text x="140" y="165" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ██░░██░░░░██
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.3s" fill="freeze" />
          </text>
          <text x="140" y="180" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ██░░██░░░░██
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.4s" fill="freeze" />
          </text>
          <text x="140" y="195" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ██░░░░░░░░██
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.5s" fill="freeze" />
          </text>
          <text x="140" y="210" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ▓▓░░░░░░░░▓▓
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.6s" fill="freeze" />
          </text>
          <text x="140" y="225" font-family="'Courier New', monospace" font-size="10" fill="url(#asciiGradLight)" letter-spacing="2" opacity="0">
            ░░░░░░░░░░░░
            <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="0.7s" fill="freeze" />
          </text>
        </g>
      </g>
    </g>

    <!-- Right Section - Terminal Content -->
    <rect x="450" y="40" width="700" height="530" rx="12" fill="#F8FAFC" stroke="rgba(15,23,42,0.08)" stroke-width="1" opacity="0.9" filter="url(#noiseLight)" />
    
    <!-- Scanlines Overlay -->
    <rect x="450" y="40" width="700" height="530" rx="12" fill="url(#scanlinesLight)" opacity="0.02" />

    <!-- Terminal Header -->
    <rect x="450" y="40" width="700" height="40" rx="12" rx="12" fill="rgba(248,250,252,0.5)" stroke="rgba(15,23,42,0.08)" stroke-width="1" />
    
    <!-- Terminal Dots -->
    <circle cx="475" cy="60" r="3" fill="#DC2626" opacity="0.6" />
    <circle cx="495" cy="60" r="3" fill="#F59E0B" opacity="0.6" />
    <circle cx="515" cy="60" r="3" fill="#10B981" opacity="0.6" />
    
    <!-- Terminal Text -->
    <text x="470" y="63" font-family="'Courier New', monospace" font-size="12" fill="#64748B">~ aayashahmad</text>

    <!-- Greeting Section -->
    <text x="480" y="110" font-family="'Courier New', monospace" font-size="14" fill="#06B6D4" opacity="0">
      $ hi 👋
      <animate attributeName="opacity" from="0" to="1" dur="0.4s" begin="1s" fill="freeze" />
    </text>

    <!-- Main Heading -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.5s" begin="1.5s" fill="freeze" />
      <text x="480" y="145" font-family="'Courier New', monospace" font-size="28" font-weight="bold" fill="#0F172A">
        I'm Aayash Ahmad
      </text>
    </g>

    <!-- Typing Text Animation -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="2s" fill="freeze" />
      <text x="480" y="180" font-family="'Courier New', monospace" font-size="14" fill="url(#accentGradLight)">
        $ Full-Stack Developer
        <animate attributeName="visibility" from="hidden" to="visible" dur="1.5s" begin="2s" repeatCount="indefinite" />
      </text>
    </g>

    <!-- Info Items -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="3s" fill="freeze" />
      <text x="480" y="220" font-family="'Courier New', monospace" font-size="12" fill="#475569">📍 Pulwama, Kashmir</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="3.3s" fill="freeze" />
      <text x="480" y="245" font-family="'Courier New', monospace" font-size="12" fill="#475569">🎓 MCA Graduate • IUST</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="3.6s" fill="freeze" />
      <text x="480" y="270" font-family="'Courier New', monospace" font-size="12" fill="#475569">💡 React • Node.js • Go • AI Explorer</text>
    </g>

    <!-- Skills Section -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="4s" fill="freeze" />
      <text x="480" y="310" font-family="'Courier New', monospace" font-size="12" font-weight="bold" fill="#0F172A">→ Skills</text>
    </g>

    <!-- Skill Pills -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="4.3s" fill="freeze" />
      <!-- React -->
      <rect x="480" y="325" width="70" height="28" rx="14" fill="rgba(6,182,212,0.1)" stroke="rgba(6,182,212,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="515" y="345" font-family="'Courier New', monospace" font-size="11" fill="#06B6D4" text-anchor="middle">React</text>
      
      <!-- Node.js -->
      <rect x="565" y="325" width="80" height="28" rx="14" fill="rgba(16,185,129,0.1)" stroke="rgba(16,185,129,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="605" y="345" font-family="'Courier New', monospace" font-size="11" fill="#10B981" text-anchor="middle">Node.js</text>
      
      <!-- Python -->
      <rect x="660" y="325" width="75" height="28" rx="14" fill="rgba(37,99,235,0.1)" stroke="rgba(37,99,235,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="698" y="345" font-family="'Courier New', monospace" font-size="11" fill="#2563EB" text-anchor="middle">Python</text>
      
      <!-- Go -->
      <rect x="750" y="325" width="60" height="28" rx="14" fill="rgba(59,130,246,0.1)" stroke="rgba(59,130,246,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="780" y="345" font-family="'Courier New', monospace" font-size="11" fill="#3B82F6" text-anchor="middle">Go</text>
    </g>

    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="4.6s" fill="freeze" />
      <!-- TypeScript -->
      <rect x="480" y="365" width="85" height="28" rx="14" fill="rgba(59,130,246,0.1)" stroke="rgba(59,130,246,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="523" y="385" font-family="'Courier New', monospace" font-size="11" fill="#3B82F6" text-anchor="middle">TypeScript</text>
      
      <!-- MongoDB -->
      <rect x="580" y="365" width="85" height="28" rx="14" fill="rgba(34,197,94,0.1)" stroke="rgba(34,197,94,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="623" y="385" font-family="'Courier New', monospace" font-size="11" fill="#22C55E" text-anchor="middle">MongoDB</text>
      
      <!-- Express -->
      <rect x="680" y="365" width="75" height="28" rx="14" fill="rgba(71,85,105,0.1)" stroke="rgba(71,85,105,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="718" y="385" font-family="'Courier New', monospace" font-size="11" fill="#475569" text-anchor="middle">Express</text>
    </g>

    <!-- Social Section -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="5s" fill="freeze" />
      <text x="480" y="435" font-family="'Courier New', monospace" font-size="12" font-weight="bold" fill="#0F172A">→ Connect</text>
    </g>

    <!-- Social Icons -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="5.3s" fill="freeze" />
      
      <!-- GitHub Icon -->
      <circle cx="500" cy="460" r="18" fill="rgba(15,23,42,0.05)" stroke="rgba(6,182,212,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="500" y="467" font-family="Arial" font-size="18" fill="#06B6D4" text-anchor="middle">𝘨</text>
      
      <!-- LinkedIn Icon -->
      <circle cx="540" cy="460" r="18" fill="rgba(15,23,42,0.05)" stroke="rgba(37,99,235,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="540" y="467" font-family="Arial" font-size="18" fill="#2563EB" text-anchor="middle">in</text>
      
      <!-- Email Icon -->
      <circle cx="580" cy="460" r="18" fill="rgba(15,23,42,0.05)" stroke="rgba(99,102,241,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="580" y="467" font-family="Arial" font-size="14" fill="#6366F1" text-anchor="middle">✉</text>
      
      <!-- Portfolio Icon -->
      <circle cx="620" cy="460" r="18" fill="rgba(15,23,42,0.05)" stroke="rgba(16,185,129,0.4)" stroke-width="1" filter="url(#glowLight)" />
      <text x="620" y="467" font-family="Arial" font-size="16" fill="#10B981" text-anchor="middle">🌐</text>
    </g>

    <!-- Contact Email -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="5.6s" fill="freeze" />
      <text x="480" y="510" font-family="'Courier New', monospace" font-size="11" fill="#64748B">
        📧 bhatashu666@gmail.com
      </text>
    </g>

    <!-- Footer Quote -->
    <g opacity="0">
      <animate attributeName="opacity" from="0" to="1" dur="0.3s" begin="6s" fill="freeze" />
      <text x="480" y="545" font-family="'Courier New', monospace" font-size="10" fill="#94A3B8" font-style="italic">
        $ Code, Create, Innovate – that's the journey I follow
      </text>
    </g>
  </g>

  <!-- Glowing Border Shimmer -->
  <rect x="450" y="40" width="700" height="530" rx="12" fill="none" stroke="url(#accentGradLight)" stroke-width="1.5" opacity="0.2">
    <animate attributeName="stroke-dashoffset" from="0" to="100" dur="3s" repeatCount="indefinite" />
  </rect>
</svg>
