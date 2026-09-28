# divulgacao/ — cards e textos para as redes

| Arquivo | Uso |
|---|---|
| `linkedin.png` | Imagem quadrada (1080×1080) para o post no feed do LinkedIn |
| `github-social-preview.png` | Imagem 2:1 (1280×640) para a prévia social do repositório (GitHub › Settings › Social preview) e para posts com link |
| `card-linkedin.tex`, `card-github.tex`, `card-comum.tex` | Fontes das imagens, na marca da for_code (Lexend e os logos de `docs/assets/`) |
| `textos-linkedin.md` | Texto do post e texto para a seção **Projetos** do perfil |

Para regerar as imagens (XeLaTeX):

```bash
latexmk -xelatex card-linkedin.tex && pdftoppm -png -singlefile -scale-to 1080 card-linkedin.pdf linkedin
latexmk -xelatex card-github.tex   && pdftoppm -png -singlefile -scale-to-x 1280 -scale-to-y 640 card-github.pdf github-social-preview
latexmk -c
```
