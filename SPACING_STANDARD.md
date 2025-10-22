# Padrão de Espaçamento - DasLoto Plans

## 📐 Variáveis de Espaçamento Definidas

```css
:root {
  --spacing-section: 4rem;           /* Espaçamento entre seções (desktop) */
  --spacing-between-elements: 2rem;  /* Espaçamento entre elementos */
  --spacing-card-padding: 2rem;      /* Padding interno dos cards */
  --spacing-hero-padding: 4rem 2rem; /* Padding específico do hero */
}
```

## 📱 Responsividade (Mobile - max-width: 768px)

```css
:root {
  --spacing-section: 2.5rem;           /* Reduzido para mobile */
  --spacing-between-elements: 1.5rem;  /* Reduzido para mobile */
  --spacing-card-padding: 1.5rem;      /* Reduzido para mobile */
  --spacing-hero-padding: 2.5rem 1rem 2rem; /* Reduzido para mobile */
}
```

## 🎯 Elementos Que Usam Este Padrão

### Seções Principais
- `.pricing-hero` → Usa `--spacing-hero-padding` e `--spacing-section`
- `.plan-comparison` → Usa `--spacing-card-padding` e `--spacing-section`
- `.social-proof` → Usa `--spacing-card-padding` e `--spacing-section`
- `.guarantee-section` → Usa `--spacing-section`
- `.feature-highlight` → Usa `--spacing-card-padding` e `--spacing-section`
- `.value-proposition` → Usa `--spacing-section`

### Seções de Conteúdo
- `.testimonials-section` → Padding e margin padronizados
- `.faq-section` → Padding e margin padronizados
- `.legal-section` → Padding e margin padronizados
- `.hero-section` → Padding e margin padronizados

### Classes Bootstrap
- `.py-5` → Agora usa `--spacing-section`
- `.my-5` → Agora usa `--spacing-between-elements`

## 📊 Hierarquia de Espaçamento

```
Espaçamento Maior (4rem/2.5rem)
├─ Entre seções principais
├─ Margin dos containers grandes
└─ Padding das seções hero

Espaçamento Médio (2rem/1.5rem)
├─ Entre elementos dentro de seção
├─ Padding dos cards
└─ Margin entre grupos de elementos

Espaçamento Pequeno (1rem e menos)
├─ Dentro dos componentes
├─ Entre linhas de texto
└─ Margin dos elementos filhos
```

## ✅ Benefícios da Padronização

1. **Consistência Visual** - Toda página segue o mesmo padrão
2. **Responsividade** - Ajustes automáticos em mobile
3. **Manutenção Fácil** - Alterar espaçamento em um só lugar
4. **Performance** - Uso de CSS variables
5. **Escalabilidade** - Fácil aplicar em outras páginas

## 🔄 Como Usar em Novas Seções

```html
<!-- Exemplo de nova seção com espaçamento padronizado -->
<section class="minha-secao py-5">
  <div class="container">
    <h2>Título</h2>
    <!-- conteúdo -->
  </div>
</section>
```

```css
.minha-secao {
  padding: var(--spacing-section) 0;
  margin: var(--spacing-section) 0;
}

.minha-secao .card {
  padding: var(--spacing-card-padding);
  margin-bottom: var(--spacing-between-elements);
}

@media (max-width: 768px) {
  .minha-secao {
    padding: var(--spacing-between-elements) 0;
    margin: var(--spacing-between-elements) 0;
  }
}
```

## 🎨 Breakpoints

- **Desktop**: Sem media query (padrão)
- **Tablet/Mobile**: `@media (max-width: 768px)`
  - Espaçamento reduzido por fator de ~0.625x
  - Mantém proporção visual

## 📝 Checklist de Implementação

- [x] Seção Hero/Pricing definida
- [x] Cards de planos padronizados
- [x] Tabela de comparação padronizada
- [x] Social proof padronizado
- [x] Value propositions padronizado
- [x] Guarantee section padronizada
- [x] Testimonials section padronizada
- [x] FAQ section padronizada
- [x] Legal notice padronizada
- [x] Final CTA padronizada
- [x] Footer padronizado
- [x] Media queries para mobile
- [x] Bootstrap classes (.py-5, .my-5) integradas
