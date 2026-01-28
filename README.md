# Funil TikTok Gol

Site estático de funil de vendas para TikTok.

## Estrutura do Projeto

- `/front` - Página inicial do funil
- `/gol` - Página de conversão
- `/up1` até `/up15` - Páginas intermediárias do funil

## Deploy no Vercel

### Opção 1: Via GitHub (Recomendado)

1. **Criar repositório no GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
   git push -u origin main
   ```

2. **Conectar ao Vercel:**
   - Acesse [vercel.com](https://vercel.com)
   - Faça login com sua conta GitHub
   - Clique em "Add New Project"
   - Importe o repositório do GitHub
   - O Vercel detectará automaticamente a configuração
   - Clique em "Deploy"

### Opção 2: Via CLI do Vercel

1. **Instalar Vercel CLI:**
   ```bash
   npm i -g vercel
   ```

2. **Fazer deploy:**
   ```bash
   vercel
   ```

3. **Para produção:**
   ```bash
   vercel --prod
   ```

## URLs das Páginas

Após o deploy, suas páginas estarão disponíveis em:
- Página principal: `https://seu-dominio.vercel.app/`
- Front: `https://seu-dominio.vercel.app/front/`
- Gol: `https://seu-dominio.vercel.app/gol/`
- Up1: `https://seu-dominio.vercel.app/up1/`
- (e assim por diante para up2 até up15)

## Configuração

O arquivo `vercel.json` está configurado para:
- Servir arquivos estáticos
- Redirecionar a raiz (`/`) para `/front/index.html`
- Manter as rotas das páginas intermediárias funcionando corretamente

## Notas

- Certifique-se de que todos os caminhos de imagens e scripts estão relativos ou usando caminhos absolutos corretos
- O Vercel suporta arquivos estáticos HTML/CSS/JS sem necessidade de build
