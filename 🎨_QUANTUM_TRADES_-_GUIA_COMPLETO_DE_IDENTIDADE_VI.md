# 🎨 QUANTUM TRADES - GUIA COMPLETO DE IDENTIDADE VISUAL
## Design System Oficial - Versão Final

---

## 📋 **ÍNDICE**

1. [Cores Oficiais](#cores-oficiais)
2. [Logo e Marca](#logo-e-marca)
3. [Tipografia](#tipografia)
4. [Componentes](#componentes)
5. [Layout e Grid](#layout-e-grid)
6. [Responsividade](#responsividade)
7. [Código CSS Completo](#código-css-completo)

---

## 🎨 **CORES OFICIAIS**

### **Paleta Principal**
```css
/* Azuis Quantum (Base) */
--primary-blue: #1a1a2e;           /* Cor principal - fundo escuro */
--secondary-blue: #16213e;         /* Cor secundária - elementos */
--accent-blue: #0f3460;            /* Cor de destaque - detalhes */

/* Dourados Quantum (Destaque) */
--quantum-gold: #ffd700;           /* Dourado principal - CTA e destaques */
--gold-light: #ffed4e;             /* Dourado claro - hover states */
--gold-dark: #b8860b;              /* Dourado escuro - bordas */
```

### **Gradientes Oficiais**
```css
/* Gradiente Principal (Background) */
--gradient-main: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);

/* Gradiente Dourado (Botões) */
--gradient-gold: linear-gradient(135deg, #ffd700, #ffed4e);

/* Gradiente Cards */
--gradient-card: linear-gradient(135deg, rgba(26, 26, 46, 0.95) 0%, rgba(22, 33, 62, 0.95) 100%);
```

### **Cores de Estado**
```css
--success-color: #4CAF50;          /* Verde - sucesso */
--warning-color: #FF9800;          /* Laranja - aviso */
--error-color: #F44336;            /* Vermelho - erro */
--info-color: #2196F3;             /* Azul - informação */
```

### **Cores de Texto**
```css
--text-primary: #ffffff;           /* Texto principal */
--text-secondary: #b0b0b0;         /* Texto secundário */
--text-muted: #808080;             /* Texto esmaecido */
--text-gold: #ffd700;              /* Texto dourado */
```

---

## 🏷️ **LOGO E MARCA**

### **Logo Principal**
- **Arquivo:** `quantum_trades_logo.png`
- **Formato:** PNG com transparência
- **Cores:** Dourado (#FFD700) com efeitos de sombra

### **Tamanhos Padrão**
```css
/* Logo Pequeno (Header) */
.quantum-logo--small .quantum-logo-image {
    width: 32px;
    height: 32px;
}

/* Logo Médio (Padrão) */
.quantum-logo-image {
    width: 40px;
    height: 40px;
}

/* Logo Grande (Destaque) */
.quantum-logo--large .quantum-logo-image {
    width: 60px;
    height: 60px;
}

/* Logo Login (Tela de Login) */
.quantum-logo--login .quantum-logo-image {
    width: 125px;
    height: 125px;
}
```

### **Uso do Logo**
```html
<!-- Logo Padrão -->
<div class="quantum-logo">
    <img src="quantum_trades_logo.png" alt="Quantum Trades" class="quantum-logo-image">
    <span>Quantum Trades</span>
</div>

<!-- Logo Login -->
<div class="quantum-logo quantum-logo--login">
    <img src="quantum_trades_logo.png" alt="Quantum Trades" class="quantum-logo-image">
</div>
```

### **Regras de Uso**
- ✅ **SEMPRE** usar o logo oficial
- ✅ **MANTER** proporções originais
- ✅ **APLICAR** efeito drop-shadow
- ❌ **NUNCA** alterar cores
- ❌ **NUNCA** distorcer proporções
- ❌ **NUNCA** usar versões não oficiais

---

## 📝 **TIPOGRAFIA**

### **Fonte Principal**
```css
--font-family-primary: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

### **Hierarquia de Títulos**
```css
h1 {
    font-size: 2.25rem;        /* 36px */
    color: #ffd700;            /* Dourado */
    font-weight: 700;          /* Bold */
}

h2 {
    font-size: 1.875rem;       /* 30px */
    color: #ffd700;            /* Dourado */
    font-weight: 700;          /* Bold */
}

h3 {
    font-size: 1.5rem;         /* 24px */
    color: #ffffff;            /* Branco */
    font-weight: 700;          /* Bold */
}

h4 {
    font-size: 1.25rem;        /* 20px */
    color: #ffffff;            /* Branco */
    font-weight: 600;          /* Semibold */
}

h5 {
    font-size: 1.125rem;       /* 18px */
    color: #ffffff;            /* Branco */
    font-weight: 500;          /* Medium */
}

h6 {
    font-size: 1rem;           /* 16px */
    color: #ffffff;            /* Branco */
    font-weight: 500;          /* Medium */
}
```

### **Tamanhos de Fonte**
```css
--font-size-xs: 0.75rem;      /* 12px */
--font-size-sm: 0.875rem;     /* 14px */
--font-size-base: 1rem;       /* 16px - padrão */
--font-size-lg: 1.125rem;     /* 18px */
--font-size-xl: 1.25rem;      /* 20px */
--font-size-2xl: 1.5rem;      /* 24px */
--font-size-3xl: 1.875rem;    /* 30px */
--font-size-4xl: 2.25rem;     /* 36px */
```

### **Pesos de Fonte**
```css
--font-weight-light: 300;     /* Light */
--font-weight-normal: 400;    /* Normal */
--font-weight-medium: 500;    /* Medium */
--font-weight-semibold: 600;  /* Semibold */
--font-weight-bold: 700;      /* Bold */
--font-weight-extrabold: 800; /* Extra Bold */
```

---

## 🔘 **COMPONENTES**

### **Botões**

#### **Botão Primário (Dourado)**
```css
.btn-primary {
    background: linear-gradient(135deg, #ffd700, #ffed4e);
    color: #1a1a2e;
    border: 2px solid transparent;
    padding: 0.5rem 1rem;
    border-radius: 8px;
    font-weight: 500;
    transition: all 0.3s ease;
}

.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(255, 215, 0, 0.4);
}
```

#### **Botão Secundário (Outline)**
```css
.btn-secondary {
    background: transparent;
    color: #ffd700;
    border: 2px solid #ffd700;
    padding: 0.5rem 1rem;
    border-radius: 8px;
    font-weight: 500;
    transition: all 0.3s ease;
}

.btn-secondary:hover {
    background: #ffd700;
    color: #1a1a2e;
    transform: translateY(-2px);
}
```

### **Cards**
```css
.quantum-card {
    background: linear-gradient(135deg, rgba(26, 26, 46, 0.95) 0%, rgba(22, 33, 62, 0.95) 100%);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    border: 1px solid rgba(255, 215, 0, 0.1);
    padding: 2rem;
    transition: all 0.3s ease;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
}

.quantum-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 20px 25px rgba(0, 0, 0, 0.15);
    border-color: rgba(255, 215, 0, 0.3);
}
```

### **Header Fixo**
```css
.quantum-header {
    background: rgba(26, 26, 46, 0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(255, 215, 0, 0.2);
    padding: 1rem 2rem;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 1030;
    transition: all 0.3s ease;
}
```

### **Formulários**
```css
.form-input {
    width: 100%;
    padding: 0.75rem 1rem;
    border: 2px solid rgba(255, 215, 0, 0.3);
    border-radius: 8px;
    background: rgba(26, 26, 46, 0.95);
    color: #ffffff;
    font-size: 1rem;
    transition: all 0.3s ease;
}

.form-input:focus {
    outline: none;
    border-color: #ffd700;
    box-shadow: 0 0 10px rgba(255, 215, 0, 0.3);
}
```

---

## 📐 **LAYOUT E GRID**

### **Container Principal**
```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 2rem;
}
```

### **Grid System**
```css
.dashboard-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
    margin-bottom: 2rem;
}
```

### **Espaçamentos Padrão**
```css
--spacing-xs: 0.25rem;    /* 4px */
--spacing-sm: 0.5rem;     /* 8px */
--spacing-md: 1rem;       /* 16px */
--spacing-lg: 1.5rem;     /* 24px */
--spacing-xl: 2rem;       /* 32px */
--spacing-2xl: 3rem;      /* 48px */
--spacing-3xl: 4rem;      /* 64px */
```

---

## 📱 **RESPONSIVIDADE**

### **Breakpoints**
```css
/* Desktop Large */
@media (min-width: 1200px) { }

/* Desktop */
@media (max-width: 1199px) { }

/* Tablet */
@media (max-width: 768px) {
    .container {
        padding: 0 1rem;
    }
    
    .quantum-header {
        padding: 1rem;
    }
}

/* Mobile */
@media (max-width: 480px) {
    .container {
        padding: 0 0.5rem;
    }
    
    .quantum-card {
        padding: 1.5rem;
    }
}
```

### **Menu Hambúrguer (Mobile)**
```css
.hamburger-menu {
    display: none;
    flex-direction: column;
    cursor: pointer;
    padding: 0.5rem;
    gap: 4px;
}

.hamburger-line {
    width: 25px;
    height: 3px;
    background: #ffd700;
    transition: all 0.3s ease;
    border-radius: 2px;
}

@media (max-width: 768px) {
    .hamburger-menu {
        display: flex;
    }
}
```

---

## 🎯 **INDICADORES DE STATUS**

### **Status Online/Offline**
```css
.status-indicator {
    display: inline-block;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    margin-right: 0.5rem;
}

.status-online {
    background: #4CAF50;
    box-shadow: 0 0 10px rgba(76, 175, 80, 0.5);
}

.status-offline {
    background: #F44336;
    box-shadow: 0 0 10px rgba(244, 67, 54, 0.5);
}
```

---

## ⚡ **ANIMAÇÕES E TRANSIÇÕES**

### **Transições Padrão**
```css
--transition-fast: 0.15s ease;
--transition-normal: 0.3s ease;
--transition-slow: 0.5s ease;
```

### **Animações Específicas**
```css
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.fade-in {
    animation: fadeIn 0.6s ease-out;
}
```

---

## 🔧 **IMPLEMENTAÇÃO**

### **1. Incluir CSS Principal**
```html
<link rel="stylesheet" href="quantum_trades_identidade_visual_completa.css">
```

### **2. Estrutura HTML Base**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quantum Trades</title>
    <link rel="stylesheet" href="quantum_trades_identidade_visual_completa.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Header -->
    <header class="quantum-header">
        <div class="header-content">
            <div class="quantum-logo">
                <img src="quantum_trades_logo.png" alt="Quantum Trades" class="quantum-logo-image">
                <span>Quantum Trades</span>
            </div>
            <div class="header-actions">
                <button class="btn btn-primary">Dashboard</button>
                <button class="btn btn-secondary">Sair</button>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="dashboard-page">
        <div class="container">
            <!-- Conteúdo aqui -->
        </div>
    </main>
</body>
</html>
```

### **3. Exemplo de Card**
```html
<div class="quantum-card">
    <div class="card-header">
        <i class="fas fa-chart-line"></i>
        <span>Título do Card</span>
    </div>
    <div class="card-body">
        <p>Conteúdo do card aqui...</p>
    </div>
</div>
```

---

## ✅ **CHECKLIST DE IMPLEMENTAÇÃO**

### **Cores e Visual**
- [ ] Gradiente principal aplicado no background
- [ ] Cores douradas (#FFD700) nos destaques
- [ ] Azuis escuros (#1a1a2e) nos containers
- [ ] Transparências e blur effects nos cards

### **Logo e Marca**
- [ ] Logo oficial (quantum_trades_logo.png) implementado
- [ ] Tamanhos corretos aplicados
- [ ] Efeitos de sombra configurados
- [ ] Hover effects funcionando

### **Tipografia**
- [ ] Fonte Inter carregada
- [ ] Hierarquia de títulos aplicada
- [ ] Cores de texto corretas
- [ ] Tamanhos responsivos

### **Componentes**
- [ ] Botões com gradiente dourado
- [ ] Cards com backdrop-filter
- [ ] Header fixo funcionando
- [ ] Formulários estilizados

### **Responsividade**
- [ ] Breakpoints configurados
- [ ] Menu hambúrguer no mobile
- [ ] Grid responsivo
- [ ] Espaçamentos adaptativos

---

## 🎨 **EXEMPLOS DE USO**

### **Página de Login**
```html
<div class="login-page">
    <div class="login-card">
        <div class="quantum-logo quantum-logo--login">
            <img src="quantum_trades_logo.png" alt="Quantum Trades" class="quantum-logo-image">
        </div>
        <h2>Bem-vindo ao Quantum Trades</h2>
        <!-- Formulário de login -->
    </div>
</div>
```

### **Dashboard Principal**
```html
<div class="dashboard-page">
    <div class="container">
        <div class="dashboard-grid">
            <div class="quantum-card">
                <div class="card-header">
                    <i class="fas fa-dollar-sign"></i>
                    <span>Saldo Total</span>
                </div>
                <div class="card-body">
                    <div class="price-value">R$ 125.430,50</div>
                    <div class="price-change positive">+2.5%</div>
                </div>
            </div>
            <!-- Mais cards... -->
        </div>
    </div>
</div>
```

---

**🎨 Identidade Visual Quantum Trades - Versão Final**  
*Design System Completo e Padronizado*  
*Criado em 06/08/2025*

