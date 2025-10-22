# DasLoto - CSS Modular Structure

## 📁 Estrutura dos Arquivos CSS

```
assets/css/
├── main-style.css     # Estilos principais do site (NOVO)
└── dark-theme.css     # Tema escuro base (existente)
```

## 🔗 Como Implementar em Outras Páginas

Para aplicar o novo design moderno em outras páginas do projeto, siga estes passos:

### 1. Inclusão dos Arquivos CSS

Adicione as seguintes linhas no `<head>` de cada página HTML:

```html
<!-- Fonts & Libs -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">

<!-- Tema base -->
<link href="./assets/css/dark-theme.css" rel="stylesheet" />

<!-- Main Styles -->
<link href="./assets/css/main-style.css" rel="stylesheet" />
```

### 2. Scripts Necessários

Adicione antes do fechamento do `</body>`:

```html
<!-- Scripts -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>
<script>
  // Initialize AOS
  AOS.init({
    duration: 800,
    once: true,
    offset: 100
  });

  // Update year
  document.getElementById('year').textContent = new Date().getFullYear();
</script>
```

## 🎨 Classes CSS Disponíveis

### Layout Geral
- `.navbar` - Navegação fixa moderna
- `.hero-section` - Seção principal com gradientes
- `.section-title` - Títulos de seções
- `.section-subtitle` - Subtítulos de seções

### Componentes
- `.btn-primary` - Botão principal com gradiente
- `.btn-secondary` - Botão secundário transparente
- `.btn-download` - Botão de download específico

### Cards e Containers
- `.feature-card` - Cards de recursos com glassmorphism
- `.tool-card` - Cards de ferramentas
- `.testimonial-card` - Cards de depoimentos
- `.faq-item` - Itens de perguntas frequentes
- `.legal-card` - Card da seção legal

### Footer
- `.footer` - Rodapé moderno
- `.footer-brand` - Marca no rodapé
- `.footer-links` - Links do rodapé
- `.download-btn` - Botões de download no rodapé

## 🎯 Variáveis CSS Customizáveis

O arquivo `main-style.css` utiliza variáveis CSS que podem ser personalizadas:

```css
:root {
  --primary-color: #4f46e5;
  --secondary-color: #7c3aed;
  --success-color: #10b981;
  --warning-color: #f59e0b;
  --dark-bg: #0f172a;
  --dark-surface: #1e293b;
  --dark-border: #334155;
  --text-light: #f8fafc;
  --text-muted: #94a3b8;
  --gradient-primary: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  --gradient-secondary: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}
```

## 📱 Responsividade

O CSS inclui breakpoints responsivos:
- **Desktop**: Layout completo
- **Tablet**: Adaptação de grid e espaçamentos
- **Mobile** (< 768px): Layout otimizado para touch

## 🎭 Animações Incluídas

- **AOS (Animate On Scroll)**: Animações suaves de entrada
- **Hover Effects**: Efeitos de hover em todos os componentes
- **Smooth Transitions**: Transições fluidas

## 🔧 Exemplo de Implementação

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DasLoto - Página</title>
  
  <!-- CSS Links aqui -->
  
</head>
<body>
  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg">
    <!-- Conteúdo da navegação -->
  </nav>

  <!-- Hero Section -->
  <section class="hero-section">
    <!-- Conteúdo hero -->
  </section>

  <!-- Footer -->
  <footer class="footer">
    <!-- Conteúdo do footer -->
  </footer>

  <!-- Scripts aqui -->
</body>
</html>
```

## 🚀 Benefícios da Modularização

1. **Reutilização**: CSS pode ser usado em todas as páginas
2. **Manutenção**: Alterações centralizadas em um arquivo
3. **Performance**: Cache do CSS pelo navegador
4. **Consistência**: Design uniforme em todo o projeto
5. **Escalabilidade**: Fácil adição de novos componentes

## 📋 Lista de Páginas para Atualizar

- [ ] `projects/about.html`
- [ ] `projects/delete-account.html` 
- [ ] `projects/manutenance.html`
- [ ] `projects/plans.html`
- [ ] `projects/policies.html`

## 🎨 Próximos Passos

1. Aplicar o CSS modular nas páginas listadas acima
2. Testar responsividade em diferentes dispositivos
3. Validar animações AOS funcionando corretamente
4. Verificar carregamento das fontes e ícones