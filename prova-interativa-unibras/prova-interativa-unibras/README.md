# Prova Interativa UniBRAS

Prova de Introdução à Programação Estruturada (Engenharia de Software, 2º período) em formato interativo, com o professor Paulo Victor de Morais.

## Como abrir
Não precisa de servidor nem de instalação. Dê dois cliques em `index.html` e ele abre no navegador.
No VSCode, também funciona com a extensão Live Server.

## O que tem
- Abertura animada com a logo e hero de entrada nas cores do logotipo (grafite e cinza)
- Cadastro do aluno (nome e data editáveis; curso, período, disciplina e professor são fixos)
- Orientações da prova em texto
- 6 questões, 1 ponto cada (prova vale 6,0; média para aprovação 3,0), com as figuras da prova
- Palavras em azul abrem um pop-up com o significado
- Clicar na logo volta ao início (com confirmação) para refazer a prova
- Resultado com animação de aprovado (confete) ou reprovado
- Revisão com filtro de acertos/erros e explicação de cada resposta
- O progresso fica salvo ao atualizar a página (por sessão do navegador)

## Editar
Tudo está em `index.html`, no bloco `<script>`:
- `Q`: questões, gabarito (`c`), explicações (`x`) e por que cada erro está errado (`r`)
- `G`: glossário das palavras clicáveis. No texto, use `{{chave|texto}}`
- `DISC`, `PROF`, `TOTAL` e `MEDIA`: disciplina, professor, nota total e média
- Cores: variáveis no começo do CSS (`--bg`, `--card`, `--acc` etc.)

A pasta `img/` guarda as figuras em arquivo. As mesmas imagens estão embutidas no `index.html`, para ele funcionar sozinho; para trocar uma figura, edite o item correspondente em `IMG`.

## Privacidade
- O projeto não usa chaves nem senhas. O `.gitignore` já bloqueia `.env`, chaves (`*.key`, `*.pem`), credenciais, `node_modules` e arquivos de editor.
- Não suba fotos originais da prova nem arquivos com nome de aluno. A pasta `originais/` já está ignorada.
- As respostas ficam só no navegador do aluno (sessionStorage). Nada é enviado a nenhum servidor.

## Subir para o GitHub
```bash
git init
git add .
git status        # confira o que vai subir
git commit -m "Prova interativa UniBRAS"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/prova-interativa-unibras.git
git push -u origin main
```
Para deixar online de graça: no repositório, Settings > Pages > Branch `main` > Save.
