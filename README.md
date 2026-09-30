# POO em C# — site do material da disciplina

Site estático (HTML + CSS puro, sem JavaScript) com o material de Programação Orientada a Objetos em C#: introdução conceitual, aula técnica e tutorial prático no Visual Studio.

## Estrutura

```
.
├── index.html                    # página inicial
├── introducao.html               # introdução conceitual (analogias)
├── aula-tecnica.html             # aula técnica em C#, com código
├── tutorial-visual-studio.html   # tutorial passo a passo no Visual Studio
├── assets/
│   └── css/
│       └── style.css             # folha de estilos compartilhada
└── README.md
```

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ou use um já existente) e envie todos estes arquivos para a **raiz** dele, mantendo a pasta `assets/` no mesmo nível de `index.html`.

   ```
   git init
   git add .
   git commit -m "Publica material de POO em C#"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git
   git push -u origin main
   ```

2. No GitHub, abra o repositório → **Settings** → **Pages** (menu à esquerda).
3. Em **Build and deployment** → **Source**, selecione **Deploy from a branch**.
4. Em **Branch**, selecione `main` e a pasta `/ (root)`. Clique em **Save**.
5. Aguarde um ou dois minutos. O GitHub mostra o link no topo da mesma página, algo como:

   ```
   https://SEU-USUARIO.github.io/SEU-REPOSITORIO/
   ```

6. Pronto — o site está no ar. Qualquer novo `git push` para a branch `main` atualiza o site automaticamente em alguns minutos.

## Editando o conteúdo

Não há gerador de site nem build — cada `.html` é independente e pode ser editado direto. O visual inteiro é controlado por `assets/css/style.css`; para mudar cores, edite as variáveis no topo do arquivo (`:root { --purple: ...; }`).

## Compatibilidade

Sem dependências externas (sem CDN, sem fontes do Google, sem JavaScript) — funciona offline abrindo `index.html` direto no navegador, e não depende de nenhum serviço além do próprio GitHub Pages.
