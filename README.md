# Padronizador

Aplicação web simples para gerar mensagens de commit e encaminhamento de protocolo a partir de um formulário.

## Tecnologias

- HTML
- TypeScript
- Tailwind CSS (via CDN)

## Como usar

1. Instale as dependências:
```bash
npm install
```

2. Compile o TypeScript:
```bash
npm run build
```

3. Abra o `index.html` no navegador ou configure o GitHub Pages para servir os arquivos estáticos.

## Deploy no GitHub Pages

O projeto está configurado para fazer deploy automático no GitHub Pages usando GitHub Actions.

### Configuração Inicial (apenas uma vez)

1. No repositório do GitHub, vá em **Settings** → **Pages**
2. Em **Source**, selecione **GitHub Actions** (não "Deploy from a branch")
3. Salve as configurações

### Deploy Automático

O deploy acontece automaticamente quando você faz push para a branch `main`:

1. Faça commit e push das suas alterações:
```bash
git add .
git commit -m "Sua mensagem de commit"
git push origin main
```

2. O GitHub Actions irá:
   - Instalar as dependências
   - Compilar o TypeScript
   - Fazer deploy no GitHub Pages

3. Após alguns minutos, seu site estará disponível em:
   - `https://[seu-usuario].github.io/padronizador/`
   - ou `https://[seu-usuario].github.io/[nome-do-repositorio]/`

### Deploy Manual

Se quiser fazer deploy manualmente, você também pode:

1. Compile o projeto: `npm run build`
2. Faça commit dos arquivos estáticos (index.html, dist/app.js)
3. Configure o GitHub Pages para servir da raiz do repositório

**Nota:** Com o workflow automático, você não precisa fazer commit do diretório `dist/` - ele é gerado automaticamente durante o deploy.

