# Portfólio de Tarcisio Marcos

Site estático de dados, Business Intelligence e inteligência de mercado. Versão bilíngue PT/EN, com temas claro/escuro e cinco dashboards públicos do Power BI.

## Arquivos

- `index.html`: estrutura, páginas e textos estáticos.
- `assets/css/style.css`: estilos e ajustes para celular.
- `assets/js/app.js`: projetos, traduções, navegação, interações e links dos dashboards.
- `assets/images/`: seis imagens WebP usadas pelo site.
- `.nojekyll`: permite servir o site estático sem processamento Jekyll.
- `.gitignore`: exclui arquivos locais do sistema operacional.

Não há instalação de pacotes, compilação ou servidor de aplicação. Todas as imagens usadas pelo site estão incluídas.

## Publicar no GitHub Pages

1. Extraia o ZIP no computador.
2. Abra o repositório de destino no GitHub. Se já houver um site, use uma branch separada e revise as mudanças antes de incorporá-las.
3. Envie o conteúdo desta pasta para a raiz da branch escolhida. O arquivo `index.html` deve ficar na raiz, ao lado da pasta `assets`. Não envie somente o ZIP nem crie uma pasta extra envolvendo o site.
4. Abra **Settings > Pages**.
5. Em **Build and deployment > Source**, escolha **Deploy from a branch**.
6. Selecione a branch que contém os arquivos (por exemplo, `main`) e a pasta **/(root)**. Salve.
7. Acompanhe o endereço e o status da publicação em **Settings > Pages**.

Em um repositório comum da conta TaMarcos, o endereço terá o formato `https://tamarcos.github.io/NOME-DO-REPOSITORIO/`. O endereço efetivo aparece nas configurações do Pages.

Documentação oficial: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Abrir e editar

Abra `index.html` no navegador com a pasta `assets` ao lado. Para servir localmente, execute `python3 -m http.server 8000` nesta pasta e abra `http://localhost:8000`.

- **Projetos e descrição dos cases:** procure `projects` e `caseDossiers` em `assets/js/app.js`.
- **Traduções:** procure `englishText` no mesmo arquivo. Ao mudar um texto português, atualize a tradução correspondente.
- **Links do Power BI:** procure `dashboardUrls`.
- **Textos institucionais e contato:** edite `index.html` e as respectivas traduções.
- **Identidade visual:** edite `assets/css/style.css`.
- **Capas:** substitua os WebP mantendo os nomes, ou atualize `imageAssets` no JavaScript.

A navegação usa rotas com hash, como `#/projetos/f1`, compatíveis com a estrutura deste site estático. Os caminhos dos recursos são relativos para funcionar também em um repositório de projeto.

## Dependências e comportamento

- As fontes são solicitadas ao Google Fonts; existem fontes de fallback.
- Os dashboards são carregados do Power BI quando o visitante solicita a visualização. Exigem internet e disponibilidade do relatório original. Há um link alternativo para abrir em outra aba.
- O seletor PT/EN traduz o portfólio. O idioma dos relatórios incorporados é definido no Power BI.
- Tema e idioma são guardados no armazenamento local do navegador, quando permitido.
- E-mail, WhatsApp e LinkedIn usam links diretos. Não há formulário com backend ou serviço de envio.
- As capas são ilustrações conceituais geradas para o portfólio.

## Validação desta entrega

Verificadas a sintaxe do JavaScript, a integridade das imagens, a presença dos recursos locais e a correspondência do conteúdo com a versão bilíngue. A revisão visual completa em navegador e o carregamento dos relatórios do Power BI ainda devem ser conferidos após a publicação.
