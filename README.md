# Brasil: Século XX (1888–1985) — Linha do Tempo Histórica
# Brazil Timebound

Aplicação web educacional desenvolvida como projeto final de Desenvolvimento Web, dedicada a documentar e apresentar de forma interativa os principais marcos políticos, sociais e culturais da História do Brasil ao longo do século XX.

## Sobre o Projeto

O portal foi concebido para unir rigor historiográfico (embasado em fontes primárias e acervos de universidades como USP e UnB) a boas práticas modernas de engenharia de interfaces. A navegação segue uma abordagem **Mobile-First**, com arquitetura modular leve e conformidade com os critérios de acessibilidade da **WCAG 2.1**.

## Funcionalidades Implementadas

* **Linha do Tempo Interativa:** Exibição cronológica dos eventos históricos em grid responsivo (1 coluna no mobile, 2 no tablet e 3 no desktop).
* **Filtragem Dinâmica por Período:** Botões interativos com suporte a atributos ARIA (`aria-pressed`) para filtrar marcos por recortes históricos (República Velha, Era Vargas, Período Democrático, Regime Militar e Redemocratização).
* **Leitura Aprofundada (Modal):** Janela modal dinâmica que exibe detalhes completos e contexto histórico ao selecionar qualquer evento.
* **Barra de Acessibilidade:** Controles em JavaScript para alternância entre Modo Claro (pergaminho) e Modo Escuro, além de redimensionamento do tamanho base das fontes (`A+` / `A-`).
* **Carrossel de Imagens Históricas:** Galeria rotativa com fotografias de arquivo e descrições textuais alternativas (`alt`).
* **Área de Login:** Formulário de autenticação para colaboradores com validação nativa em HTML5.

## Identidade Visual e Acessibilidade (WCAG 2.1)

A paleta segue a proporção **60-30-10** com estética editorial de papel e tinta, validada no *Adobe Express Color Contrast Checker*:

| Token CSS | Cor | Aplicação | Contraste |
| :--- | :--- | :--- | :--- |
| `--bg-parchment` | `#F7F1E4` | Fundo principal (60%) | Base |
| `--text-primary` | `#1E1B18` | Textos corridos (30%) | **AAA** (~13:1) |
| `--accent-crimson` | `#C21A00` | Títulos, datas e botões (10%) | **AA** (5.42:1) |

## Tecnologias Utilizadas

* **HTML5 Semântico:** Estruturação acessível com `<header>`, `<nav>`, `<main>`, `<section>` e `<footer>`.
* **CSS3 Customizado:** Tokens de cores, carregamento local de tipografia (`@font-face`) e sobrescrita controlada de variáveis.
* **Bootstrap 5.3:** Sistema de grid responsivo, barra de navegação retrátil, carrossel e modal.
* **JavaScript Vanilla (ES6+):** Separação entre camada de dados (`data.js`) e manipulação do DOM (`app.js`).

## Estrutura de Pastas

```text
/
├── index.html          # Estrutura semântica principal, carrossel, modal e login
├── css/
│   └── styles.css      # Tokens de cor, regras @font-face e estilos de modo escuro
├── fonts/
│   └── ...             # Arquivos locais de tipografia editorial (WOFF2/TTF)
├── js/
│   ├── data.js         # Acervo estruturado dos eventos históricos (Array de Objetos)
│   └── app.js          # Renderização dos cards, filtros e controles de acessibilidade
└── README.md           # Documentação do projeto
