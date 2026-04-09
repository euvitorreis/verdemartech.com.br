# 🚀 Guia de Deploy — Verdemar Tech no GitHub Pages

## 📦 Estrutura Completa dos Arquivos

```
verdemar-tech-site/
├── index.html                      (119 KB — página principal)
├── README.md                       (6 KB — documentação)
├── CNAME                           (19 bytes — domínio personalizado)
├── .gitignore                      (138 bytes — arquivos ignorados)
├── assets/
│   ├── vt_logo_main.png            (68 KB — logo branco)
│   ├── vitor_reis_foto.jpg         (60 KB — foto fundador)
│   ├── img_futuro_sem_desperdicio.jpg  (1.2 MB — hero/poster vídeo)
│   ├── img_regeneracao.jpg         (1 MB — cristal verde SEM texto) ✅
│   └── img_praia_usina.jpg         (2.1 MB — praia SEM texto) ✅
└── flags/
    ├── br.png                      (452 bytes — bandeira Brasil)
    ├── gb.png                      (288 bytes — bandeira UK)
    ├── es.png                      (381 bytes — bandeira Espanha)
    └── fr.png                      (109 bytes — bandeira França)
```

**Total:** 15 arquivos | ~4.5 MB

---

## 🎯 Passo a Passo para Hospedar no GitHub Pages

### **1️⃣ Criar Repositório no GitHub**

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"** (botão verde)
3. Preencha:
   - **Repository name:** `verdemar-tech-site` (ou qualquer nome)
   - **Description:** "Site institucional Verdemar Tech"
   - **Public** ✅ (deixe público)
   - **NÃO** marque "Add a README file" (já temos um)
4. Clique em **"Create repository"**

---

### **2️⃣ Fazer Upload dos Arquivos**

**Opção A: Via interface web do GitHub (mais fácil)**

1. Na página do repositório recém-criado, clique em **"uploading an existing file"**
2. Arraste e solte **TODOS** os arquivos e pastas:
   ```
   ✅ index.html
   ✅ README.md
   ✅ CNAME
   ✅ .gitignore
   ✅ pasta assets/ (com todos os arquivos dentro)
   ✅ pasta flags/ (com todos os arquivos dentro)
   ```
3. Escreva uma mensagem de commit: `Initial commit - Verdemar Tech site`
4. Clique em **"Commit changes"**

**Opção B: Via Git CLI (linha de comando)**

```bash
# 1. Clone o repositório
git clone https://github.com/SEU-USUARIO/verdemar-tech-site.git
cd verdemar-tech-site

# 2. Copie todos os arquivos baixados para esta pasta

# 3. Adicione, commit e push
git add .
git commit -m "Initial commit - Verdemar Tech site"
git push origin main
```

---

### **3️⃣ Ativar GitHub Pages**

1. No repositório, vá em **Settings** (⚙️)
2. No menu lateral, clique em **Pages**
3. Em **Source**, selecione:
   - **Branch:** `main` (ou `master`)
   - **Folder:** `/ (root)`
4. Clique em **Save**
5. Aguarde ~1 minuto

🎉 Seu site estará em: `https://SEU-USUARIO.github.io/verdemar-tech-site/`

---

### **4️⃣ Configurar Domínio Personalizado (Opcional)**

Se você já tem o domínio **verdemartech.com.br**:

1. No painel do seu provedor de domínio (Registro.br, GoDaddy, etc.), adicione estes registros DNS:

   ```
   Tipo   | Nome/Host | Valor/Destino
   -------|-----------|-------------------------------
   A      | @         | 185.199.108.153
   A      | @         | 185.199.109.153
   A      | @         | 185.199.110.153
   A      | @         | 185.199.111.153
   CNAME  | www       | SEU-USUARIO.github.io
   ```

2. No GitHub Pages (Settings → Pages), em **Custom domain**, digite:
   ```
   verdemartech.com.br
   ```

3. Marque **"Enforce HTTPS"** ✅

4. Aguarde propagação DNS (~10 minutos a 48 horas)

🌐 Seu site estará em: **https://verdemartech.com.br**

---

## ✅ Checklist Pós-Deploy

- [ ] Site abre em `https://SEU-USUARIO.github.io/verdemar-tech-site/`
- [ ] Logo aparece no header e footer
- [ ] Foto do Vitor Reis aparece na seção Fundador
- [ ] Imagens "Nossa Proposta" e "Usina" aparecem sem texto
- [ ] Bandeiras (BR, UK, ES, FR) funcionam
- [ ] Formulário envia email para `contato@verdemartech.com.br` via Formspree
- [ ] Tema claro/escuro funciona
- [ ] Layout responsivo em mobile

---

## 🔧 Problemas Comuns

### **Imagens não aparecem**
- Certifique-se de que as pastas `assets/` e `flags/` estão no root do repositório
- Verifique se os nomes dos arquivos estão exatamente iguais (case-sensitive)

### **Formulário não envia**
- Teste em `https://formspree.io/forms/xkopabzw/integration` se está ativo
- Verifique se chegou o email de confirmação no `contato@verdemartech.com.br`

### **Site não atualiza**
- Limpe cache do navegador (Ctrl+Shift+R ou Cmd+Shift+R)
- Aguarde ~5 minutos para o GitHub Pages reprocessar

---

## 📞 Contatos

- **Email:** contato@verdemartech.com.br
- **WhatsApp:** (11) 9 3264-2307
- **GitHub:** https://github.com/SEU-USUARIO/verdemar-tech-site

---

*Documento criado em: 09/04/2026*
