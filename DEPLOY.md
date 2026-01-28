# 🚀 Guia de Deploy - Passo a Passo

## ✅ O que já foi feito:
- ✅ Repositório Git inicializado
- ✅ Arquivo `.gitignore` criado
- ✅ Arquivo `vercel.json` configurado
- ✅ Commit inicial realizado

## 📋 Próximos Passos:

### 1. Criar Repositório no GitHub

1. Acesse [github.com](https://github.com) e faça login
2. Clique no botão **"+"** no canto superior direito
3. Selecione **"New repository"**
4. Escolha um nome para o repositório (ex: `funil-tiktok-gol`)
5. **NÃO** marque "Initialize with README" (já temos arquivos)
6. Clique em **"Create repository"**

### 2. Conectar o Repositório Local ao GitHub

Execute os seguintes comandos no terminal (substitua `SEU_USUARIO` e `SEU_REPOSITORIO`):

```bash
cd "/Users/carlosmoreira/Downloads/funil tiktok gol completo sem erro"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```

**Exemplo:**
```bash
git remote add origin https://github.com/carlosmoreira/funil-tiktok-gol.git
git push -u origin main
```

### 3. Deploy no Vercel

#### Opção A: Via Interface Web (Mais Fácil)

1. Acesse [vercel.com](https://vercel.com)
2. Clique em **"Sign Up"** ou **"Log In"**
3. Escolha **"Continue with GitHub"** para conectar sua conta
4. Após login, clique em **"Add New Project"**
5. Na lista de repositórios, encontre seu repositório `funil-tiktok-gol`
6. Clique em **"Import"**
7. O Vercel detectará automaticamente as configurações:
   - Framework Preset: **Other**
   - Root Directory: **./** (raiz)
   - Build Command: (deixe vazio - site estático)
   - Output Directory: (deixe vazio)
8. Clique em **"Deploy"**
9. Aguarde alguns segundos e seu site estará no ar! 🎉

#### Opção B: Via CLI do Vercel

1. Instale o Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. No diretório do projeto, execute:
   ```bash
   vercel
   ```

3. Siga as instruções:
   - Login na primeira vez
   - Escolha o projeto
   - Confirme as configurações

4. Para fazer deploy em produção:
   ```bash
   vercel --prod
   ```

### 4. Acessar seu Site

Após o deploy, você receberá uma URL como:
- `https://funil-tiktok-gol.vercel.app`

### 5. URLs das Páginas

Seu funil estará disponível em:
- **Página Principal:** `https://seu-dominio.vercel.app/` → redireciona para `/front/`
- **Front:** `https://seu-dominio.vercel.app/front/`
- **Gol:** `https://seu-dominio.vercel.app/gol/`
- **Up1:** `https://seu-dominio.vercel.app/up1/`
- **Up2 até Up15:** `https://seu-dominio.vercel.app/up2/` ... `up15/`

### 6. Atualizações Futuras

Sempre que fizer alterações:

```bash
git add .
git commit -m "Descrição das alterações"
git push
```

O Vercel detectará automaticamente e fará um novo deploy! 🚀

## 🔧 Troubleshooting

### Problema: Erro ao fazer push para GitHub
**Solução:** Verifique se você está autenticado:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Problema: Vercel não encontra os arquivos
**Solução:** Verifique se o `vercel.json` está na raiz do projeto

### Problema: Páginas não carregam corretamente
**Solução:** Verifique se os caminhos de imagens e scripts estão relativos (ex: `./images/logo.png`)

## 📞 Precisa de Ajuda?

- Documentação Vercel: https://vercel.com/docs
- Documentação GitHub: https://docs.github.com
