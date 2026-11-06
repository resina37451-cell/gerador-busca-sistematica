# Gerador de Estratégia de Busca

> Ferramenta web gratuita para gerar estratégias de busca em revisões sistemáticas.

Cole seus termos MeSH e termos livres, selecione as bases de dados e a estratégia sai pronta para copiar e colar — com o operador **OR** já aplicado — para **PubMed**, **Scopus**, **Web of Science** e **Embase**.

🔗 **Acesse em:** `https://<seu-usuario>.github.io/<nome-do-repositorio>/`

---

## Funcionalidades

- Aceita termos separados por linha, vírgula, ponto e vírgula ou com marcadores de lista
- Remove termos duplicados automaticamente
- Gera a sintaxe correta para cada base:
  - **PubMed** — `[MeSH Terms]` + `[Title/Abstract]` com parênteses aninhados
  - **Scopus** — `TITLE-ABS-KEY ( termo )`
  - **Web of Science** — `termo (Topic)`
  - **Embase** — `'termo':ti,ab,kw`
- Botão **Copiar** para cada base
- Contador de termos em tempo real
- Funciona 100% no navegador — sem servidor, sem dados enviados à internet
- Pode ser instalado como aplicativo pelo Chrome / Edge (PWA)

---

## Uso rápido

1. Acesse o link acima
2. Cole os **termos MeSH** no campo da esquerda
3. Cole os **termos livres** no campo da direita
4. Selecione as bases desejadas
5. Copie a estratégia de cada base com o botão **Copiar**
6. Cole diretamente no campo de busca avançada da base de dados
7. Use o operador **AND** entre os componentes do PICOS diretamente na base

---

## Instalar como aplicativo (PWA)

No **Google Chrome** ou **Microsoft Edge**:

1. Acesse o site
2. Clique no ícone de instalação na barra de endereços (ícone de computador com seta ↓), ou abra o menu `⋮` → **Instalar Gerador de Estratégia de Busca**
3. Confirme a instalação
4. O aplicativo aparecerá na área de trabalho ou no menu de apps com o ícone da lupa

---

## Estrutura do repositório

```
├── index.html       # Aplicação principal (página única, sem dependências externas além das fontes)
├── manifest.json    # Manifesto PWA (ícone, nome, cores)
├── icon-192.png     # Ícone 192 × 192 px (usado pelo Chrome e Android)
├── icon-512.png     # Ícone 512 × 512 px (telas de alta resolução)
└── README.md        # Este arquivo
```

---

## Como publicar no GitHub Pages (passo a passo)

Veja a seção **Deploy** abaixo.

---

## Deploy

### 1. Criar o repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **New repository** (botão verde no canto superior direito)
3. Dê um nome ao repositório (ex.: `gerador-busca-sistematica`)
4. Deixe como **Public**
5. **Não** marque "Add a README file" (já temos um)
6. Clique em **Create repository**

### 2. Enviar os arquivos

Pela interface web do GitHub (mais simples, sem precisar instalar Git):

1. Na página do repositório recém-criado, clique em **uploading an existing file**
2. Arraste todos os arquivos (`index.html`, `manifest.json`, `icon-192.png`, `icon-512.png`, `README.md`) para a área indicada
3. Role até o fim da página e clique em **Commit changes**

### 3. Ativar o GitHub Pages

1. No repositório, clique em **Settings** (aba no topo)
2. No menu lateral esquerdo, clique em **Pages**
3. Em **Source**, selecione **Deploy from a branch**
4. Em **Branch**, selecione **main** e a pasta **/ (root)**
5. Clique em **Save**
6. Aguarde ~1 minuto e atualize a página — o link do site aparecerá em destaque

> O link será: `https://<seu-usuario>.github.io/<nome-do-repositorio>/`

---

## Tecnologias

- HTML5 + CSS3 + JavaScript puro (sem frameworks)
- Fontes: [Fraunces](https://fonts.google.com/specimen/Fraunces), [Inter Tight](https://fonts.google.com/specimen/Inter+Tight), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts
- PWA: Web App Manifest

---

## Licença

MIT — use, adapte e redistribua livremente com atribuição.
