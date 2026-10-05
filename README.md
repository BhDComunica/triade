# Tríade Hospedagem Boutique

Código-fonte da versão publicada no ChatGPT Sites.

- Site: https://triade-hospedagem-boutique.bhd-comunica-2376.chatgpt.site
- Projeto Sites: `appgprj_6ab5b1050fe08191a43094f7fbc703ae`
- Estrutura: `build.py` gera as páginas estáticas em `dist/`; os arquivos em `dist/` são publicados pelo Sites.

Este repositório é uma cópia do código. Alterações no GitHub não são implantadas automaticamente no Sites.

## Estrutura

- `build.py`: geração das oito páginas HTML, do sitemap e do arquivo robots.txt, com a biblioteca padrão do Python.
- `dist/`: versão estática pronta para servir.
- `dist/style.css` e `dist/app.js`: estilos e interações do site.
- `dist/assets/`: fotos, logotipos, ícone e vídeo, incluindo as variantes de imagens responsivas.

## Executar localmente

Requer Python 3. Na raiz do repositório:

```sh
python3 -m http.server 8000 --directory dist
```

Abra http://localhost:8000. Não abra os arquivos HTML diretamente: o site usa caminhos relativos à raiz do servidor.

## Gerar as páginas novamente

```sh
python3 build.py
```

O script regenera o HTML, o sitemap e o robots.txt. Os estilos, o JavaScript e os arquivos de mídia em `dist/` são mantidos separadamente e devem ser preservados.

## Hospedagem

Use `dist/` como diretório público na raiz do domínio. O site não exige Node.js, dependências Python adicionais ou servidor de aplicação. Fontes são carregadas pelo Google Fonts; a consulta de reserva abre uma conversa no WhatsApp, sem armazenar dados no repositório.

Esta importação não configura publicação automática, GitHub Pages ou alteração de domínio. Os URLs canônicos e o sitemap foram preservados conforme a versão original (`https://triadehospedagem.com.br/`). Para hospedagem em um subdiretório, os caminhos absolutos precisam ser adaptados.

## Origem

Importação da versão 4 do projeto Sites, no commit de origem `ccba74d5d080173af7a517441a328b733749c707`. Os arquivos do site são preservados sem alteração de conteúdo ou identidade visual.
