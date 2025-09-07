# Mathfiep Template

Um template Typst moderno e elegante para documentos matemáticos, exercícios e notas de estudo.

## Características

- **Temas**: Modo escuro e claro
- **Componentes**: Problemas, definições, teoremas, info boxes
- **Matemática**: Suporte completo para LaTeX math
- **Visual**: Design moderno com tipografia clara

## Instalação

### Manual (Atual)
1. Clone/baixe este repositório
2. Use como template local

### Via Typst Universe (Futuro)
```bash
typst init @preview/mathfiep
```

## Uso Básico

```typst
#import "src/lib.typ": *

#show: mathfiep.with(
  title: "Matemática",
  subtitle: "Lista de Exercícios",
  author: "Seu Nome",
  theme: "dark" // ou "light"
)

= Exercícios

#mathfiep-problem(
  title: "Integral Básica",
  difficulty: "easy"
)[
  Calcule: $ integral x^2 dif x $
][
  $ integral x^2 dif x = x^3/3 + C $
]
```

## Componentes Disponíveis

- `mathfiep-problem()` - Problemas com solução e níveis de dificuldade
- `mathfiep-definition()` - Definições matemáticas  
- `mathfiep-theorem()` - Teoremas numerados
- `mathfiep-info()` - Caixas de informação (info, warning, error, success)
- `mathfiep-steps()` - Passos de solução organizados
- `mathfiep-final()` - Resposta final destacada
- `mathfiep-code()` - Blocos de código

## Exemplos

- `template/main.typ` - Exemplo completo com todos os componentes

## Compilação

```bash
# Compilação única
./typst-local compile --root . template/main.typ documento.pdf

# Modo watch (recompila automaticamente)  
./typst-local watch --root . template/main.typ documento.pdf
```

## Temas

### Tema Escuro (padrão)
- Fundo: `#0f1419`
- Texto: `#bfbdb6`
- Destaque: `#39bae6`

### Tema Claro
- Fundo: `#fafafa`
- Texto: `#575279`
- Destaque: `#286983`

## Licença

MIT License - veja [LICENSE](LICENSE) para detalhes.

## Contribuição

Contribuições são bem-vindas! Este template foi aprimorado com novas funcionalidades e design moderno.
