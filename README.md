# Portfólio — Cleber Cabral

Landing page estilo portfólio, pronta para GitHub Pages.

## Como publicar

1. **Crie um repositório novo no GitHub**, por exemplo `clebercmsf.github.io` (se usar exatamente esse nome, o site já sobe na raiz do domínio `clebercmsf.github.io`, sem subpasta).
   - Se preferir outro nome de repositório (ex: `portfolio`), o site fica em `clebercmsf.github.io/portfolio/` a menos que você aponte um domínio próprio (veja abaixo).

2. **Suba o arquivo `index.html`** (e o `CNAME`, se for usar domínio próprio) para a raiz do repositório:
   ```bash
   git init
   git add index.html CNAME
   git commit -m "Landing page do portfólio"
   git branch -M main
   git remote add origin https://github.com/clebercmsf/SEU-REPOSITORIO.git
   git push -u origin main
   ```

3. **Ative o GitHub Pages**:
   - Vá em `Settings` → `Pages` no repositório.
   - Em "Build and deployment", escolha `Deploy from a branch`.
   - Branch: `main`, pasta: `/ (root)`.
   - Salve. Em alguns minutos o site estará em `https://clebercmsf.github.io/SEU-REPOSITORIO/`.

## Como apontar seu domínio próprio

1. **Edite o arquivo `CNAME`** deste projeto e coloque seu domínio (ex: `www.seudominio.com` ou `seudominio.com`), sem `http://`.

2. **Na Locaweb** (já que você usa a plataforma), crie os registros DNS:
   - Para um **subdomínio** (ex: `www.seudominio.com`): registro **CNAME** apontando para `clebercmsf.github.io`.
   - Para o **domínio raiz** (ex: `seudominio.com`, sem `www`): crie 4 registros **A** apontando para os IPs do GitHub Pages:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```

3. Volte em `Settings` → `Pages` no GitHub e cadastre o domínio em "Custom domain". Marque **Enforce HTTPS** assim que o certificado for emitido (pode levar algumas horas).

4. A propagação de DNS pode levar de alguns minutos até 24h.

## Personalizar

Todo o conteúdo (textos, projetos, cores) está em um único arquivo `index.html`, sem dependências de build — é só editar direto. As descrições dos projetos foram escritas a partir do nome/linguagem de cada repositório (o GitHub não retornou descrições cadastradas); vale a pena ajustar os textos dos cards em `#projects` para descrever cada projeto com mais precisão.
