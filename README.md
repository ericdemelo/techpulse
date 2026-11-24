# TechPulse | Portal de Notícias de Tecnologia

Primeira versão funcional da página inicial do TechPulse, construída com HTML5 semântico e CSS externo, responsiva para computadores e celulares.

## Estrutura do projeto

```
techpulse/
├── index.html
├── css/
│   └── style.css
├── images/
│   └── banner-techpulse.svg
└── README.md
```

Estrutura e estilo ficam em arquivos separados: o `index.html` cuida do conteúdo e o `css/style.css` cuida do visual, vinculado por `<link rel="stylesheet">`.

## Especificações técnicas

| Item | Decisão |
|---|---|
| Linguagens | HTML5 e CSS3 (sem frameworks) |
| Tags semânticas | `<header>`, `<nav>`, `<main>`, `<article>`, `<footer>` |
| Conteúdo | `<h1>`, `<h2>`, `<h3>`, `<p>` com `<strong>` e `<em>`, `<ul>`, `<img>` com `alt`, `<a>` |
| Seletores CSS | Tag (`body`, `p`, `h2`...), classe `.botao` (reutilizável) e ID `#cabecalho-principal` (exclusivo) |
| Box Model | `padding`, `border` e `margin` aplicados no cabeçalho, cartão, botão, lista e rodapé |
| Responsividade | `<meta name="viewport">` e Media Query `@media (max-width: 600px)` |

## Justificativas de design

### Cores (Hexadecimal e RGBA)
- **Azul profundo `#0B1F3A`**: cabeçalho, rodapé e títulos. Transmite seriedade e confiança, adequadas a um portal de notícias.
- **Ciano `#00C2FF`**: destaques, bordas e botão de ação. Remete ao "pulso" digital e chama a atenção para o que é clicável.
- **Fundo claro `#F4F7FB`** e **branco `#FFFFFF`**: conforto de leitura e contraste com o cartão de conteúdo.
- **Texto `#1B2733`**: contraste alto sobre fundo claro, bom para leitura prolongada.
- **RGBA** `rgba(0, 194, 255, 0.12)` na lista de tecnologias e `rgba(0, 194, 255, 0.5)` nas bordas do menu: transparência para suavizar os blocos sem criar novas cores.

### Tipografia
- Fonte `"Segoe UI", Roboto, Arial, sans-serif`: sem serifa, limpa e legível em telas, com alternativas para cada sistema.
- Tamanho base de 18px (16px no celular) e `line-height: 1.6` para leitura confortável.
- Alinhamento: títulos e cabeçalho centralizados; parágrafos justificados no desktop e alinhados à esquerda no celular, onde a justificação cria espaços irregulares.

### Espaços (Box Model)
- **padding**: afasta o texto das bordas (botão `14px 28px`, cartão `30px`, lista, menu).
- **border**: define contornos (borda lateral ciano do cartão, linha ciano sob o cabeçalho, contorno do botão e da imagem).
- **margin**: separa blocos vizinhos (títulos, parágrafos, imagem, botão) e centraliza o `<main>` com largura máxima de 800px.

### Tecnologias e serviços
- **HTML5 + CSS3 puros**: leves, rápidos e compatíveis com qualquer navegador.
- **Imagem em SVG**: vetorial, nítida em qualquer tela e de arquivo pequeno.
- **Git/GitHub**: versionamento e publicação do repositório.
- Sem JavaScript nesta versão, pois o escopo é estrutura e estilo.

## Sitemap Visual

```
Página Inicial (Home)
│
├── Inteligência Artificial
│   ├── IA Generativa
│   ├── Machine Learning
│   └── Ética e Regulação
│
├── Cloud
│   ├── Computação em Nuvem
│   ├── DevOps e Infraestrutura
│   └── Serviços e Plataformas
│
├── Cibersegurança
│   ├── Ameaças e Vulnerabilidades
│   ├── Privacidade e LGPD
│   └── Boas Práticas
│
└── Institucional
    ├── Sobre o TechPulse
    └── Contato
```

### Hierarquia de conteúdo
- **Nível 1**: Página Inicial, o ponto de entrada.
- **Nível 2**: seções temáticas, que correspondem aos itens do menu (`<nav>`).
- **Nível 3**: subcategorias, onde ficam as reportagens (`<article>`).
- Profundidade máxima de 3 níveis, para que qualquer notícia seja alcançada em até 3 cliques.

### Taxonomia
- **Taxonomia fechada**: as 3 seções e suas subcategorias são fixas e controladas pela equipe editorial. Cada notícia pertence a uma única subcategoria principal, o que evita ambiguidade e facilita a navegação e o SEO.
- **Tags complementares** (por exemplo: "OpenAI", "nuvem híbrida", "ransomware") podem ser adicionadas depois em uma taxonomia aberta, para cruzar temas entre seções.
- O mesmo vocabulário de seções é usado no menu, no Sitemap Visual e, futuramente, no `sitemap.xml` para os buscadores.

## Como executar
Abra o arquivo `index.html` em qualquer navegador. Para testar a versão mobile, reduza a largura da janela ou use o modo responsivo das ferramentas do desenvolvedor (F12).
