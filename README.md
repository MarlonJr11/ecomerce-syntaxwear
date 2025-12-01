# SyntaxWear — Ecommerce de Tênis e Sneakers

Projeto front-end estático de um e‑commerce de calçados (protótipo/portfólio) criado para demonstrar layout, componentes e organização de estilos.

**Status:** Em desenvolvimento — HTML + CSS puro

**Última atualização:** 30 de novembro de 2025

**Resumo:**
- **Objetivo:** Apresentar uma loja online de tênis/sneakers com foco em visual, experiência de navegação e componentes reutilizáveis.
- **Tecnologias:** HTML5, CSS3 (reset + variáveis + componentes). Sem build tools — site estático.

**Como abrir (localmente)**
- Abra o arquivo `index.html` no seu navegador (duplo clique ou via servidor local).
- Para servir com um servidor simples (PowerShell):

```powershell
# A partir da pasta do projeto
python -m http.server 3000; Start-Process "http://localhost:3000"
```

Observação: caso não tenha Python, pode usar extensões do editor (ex.: Live Server) ou outro servidor estático.

**Estrutura do projeto**

- `index.html` — página principal com header (logo, navegação central e menu direito), hero, categorias/destaques, grade de produtos e footer.
- `css/` — estilos do projeto
	- `reset.css` — reset baseado no Andy Bell (normalize moderno e preferências de movimento)
	- `variables.css` — variáveis CSS (cores, tipografia, espaçamentos)
	- `base.css` — tipografia base e regras globais
	- `layout.css` — grid e layout geral
	- `components/` — estilos por componente
		- `header.css`, `hero.css`, `product-category.css`, `product-grid.css`, `footer.css`
- `images/` — ativos de imagem
	- `logo/`, `icons/`, `products/`, `banners/`, `favicons/`
- `README.md` — este arquivo

**Pontos importantes (visão técnica)**
- A navegação principal está dividida em duas áreas: `nav-center` (categorias) e `nav-right` (menu de acesso rápido: Nossas Lojas, Sobre, Perfil, Dúvidas, Carrinho). Use essas classes para posicionamento via CSS.
- O projeto usa classes BEM-light (ex.: `hero__title`, `produto__card`) para tornar o CSS previsível e modular.
- Ícones vetoriais e imagens estão em `images/icons` e `images/logo` — prefira SVG para ícones quando possível.

**Acessibilidade**
- Use atributos `alt` descritivos em todas as imagens (já aplicados no HTML onde possível).
- `aria-label` foi aplicado em elementos de navegação importantes; revise e adicione `aria-current` quando implementar rotas/estados.
- Forneça foco visível (`:focus`) nos links e controles ao estilizar os componentes.

**Como estilizar / onde editar**
- Alterações globais: `css/variables.css` (cores, tipografia). Modifique variáveis para aplicar tema rápido.
- Reset global: `css/reset.css` — não remova; ele garante consistência entre navegadores.
- Componentes: edite os arquivos dentro de `css/components/` para atualizar o header, hero, cards e footer.

**Checklist / Próximos passos sugeridos**
- [ ] Adicionar responsividade móvel completa (menu mobile e grid responsivo).
- [ ] Conectar um sistema de build (PostCSS/Autoprefixer) se for necessário suporte antigo.
- [ ] Converter componentes repetidos para templates ou incluir framework JS se quiser interatividade (carrinho, filtros, busca).
- [ ] Otimizar imagens e gerar `srcset`/`picture` para loading responsivo.