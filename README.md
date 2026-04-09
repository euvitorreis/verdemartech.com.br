# Verdemar Tech — Site Institucional v3

## Visão Geral
Site institucional premium do ecossistema Verdemar Tech, construído em HTML/CSS/JS puro (static), fiel à estrutura e ritmo visual aprovados em https://kpgojzwa.gensparkspace.com/.

---

## Funcionalidades Implementadas

### Visual & Estrutura
- Hero fullscreen com **vídeo + som do oceano** (Web Audio API, fade com scroll)
- Transições suaves entre seções via gradientes CSS (`linear-gradient`) — sem faixas bruscas
- Tipografia mista: Inter (corpo) + Playfair Display (títulos editoriais)
- Tema claro/escuro funcional — logo adapta cor automaticamente no tema claro
- Cursor customizado (desktop)
- Design 100% responsivo: desktop, tablet, mobile com drawer lateral

### Navegação
- Header fixo com logo, links, seletor de idiomas (bandeiras reais via flagcdn.com) e toggle de tema
- Menu mobile em drawer lateral deslizante
- Scroll to top flutuante

### Idiomas
- Tradução completa em 4 idiomas: **PT | EN | ES | FR**
- Tradução via sistema `data-i18n` + objeto `translations` em JS
- Bandeiras reais (imagens): Brasil, Reino Unido, Espanha, França

### Seções
1. **Hero** — vídeo fullscreen, logo flutuante, som do mar
2. **Intro** — estatísticas (7 patentes, +10 projetos, 4 idiomas, SP)
3. **Nossa Proposta** — layout split: texto à esquerda, imagem regeneração à direita (cristal verde sem texto)
4. **Sobre** — texto + 5 pilares (incluindo Sistemas & Softwares)
5. **Projetos** — grid filtável por categoria (Todos / Água / Energia / Construção / Conectividade / Softwares)
   - Novos projetos: **Pierre Med** (link para pierremed.com.br), **Marie Vet** (link para marievet.com.br), **Usina de Condensação Térmica**, **Saltria**, **Cubo Gaia**
   - **MIRA** corrigido: agregador Wi-Fi (combina 3-6 sinais fracos)
   - **Gerador PHP** corrigido: híbrido água + vento + painéis solares fixos/portáteis
6. **Usina de Condensação Térmica** — layout split: imagem praia à esquerda (água cristalina sem texto), texto à direita
7. **Missão, Visão & Valores** — cards numerados
8. **Fundador** — Vitor Reis (sem "visionário"), foto real circular, link LinkedIn
9. **Contato** — formulário completo integrado com **Formspree** (https://formspree.io/f/xkopabzw)
   - Envia emails para: **contato@verdemartech.com.br**
   - Suporta anexos até 10 MB (PDF, DOC, PPT)
   - Campos: nome, email, telefone, assunto (lista suspensa), anexo condicional, mensagem (contador 3000 chars)
10. **Footer** — links, redes sociais, LinkedIn Verdemar Tech, WhatsApp, fontes de pesquisa (modal)

### Correções Aplicadas (Última Revisão)
- [x] **Logos restaurados** — navbar, drawer, hero flutuante, footer — visíveis em ambos os temas
- [x] **Imagens trocadas** — regeneração e praia sem texto
- [x] **Foto do fundador** — Vitor Reis, circular, enquadrada
- [x] **"Visionário" removido** de todas as traduções
- [x] **Patentes removidas** — texto "Nossa Proposta", card PHP, rodapé
- [x] **MIRA** — descrição corrigida (agregador Wi-Fi)
- [x] **Gerador PHP** — descrição corrigida (híbrido água/vento/solar)
- [x] **Botões "Saiba mais"** — Pierre Med e Marie Vet com links externos
- [x] **Tema claro** — contraste melhorado, cards com sombras, texto mais legível
- [x] **Formulário Formspree** integrado e testado

### Layout Atualizado
- **Nossa Proposta**: texto esquerda | imagem regeneração direita (50/50 split)
- **Usina Condensação**: imagem praia esquerda | texto direita (50/50 split)
- Responsivo: em mobile, empilha verticalmente (texto no topo, imagem embaixo)

---

## Estrutura de Arquivos
```
index.html                      — Arquivo principal (HTML + CSS inline + JS inline)
assets/
  vt_logo_main.png              — Logo Verdemar Tech (branco, colorizado via CSS)
  vitor_reis_foto.jpg           — Foto do fundador Vitor Reis
  img_futuro_sem_desperdicio.jpg — Imagem hero / poster do vídeo
  img_regeneracao.jpg            — Cristal verde (Nossa Proposta) SEM TEXTO
  img_praia_usina.jpg            — Praia cristalina (Usina) SEM TEXTO
```

## Assets Externos
- Vídeo hero: `https://3000-iyitl0r1r7canjbtcs7y0-cc2fbc16.sandbox.novita.ai/assets/verdemar_hero.mp4`
- Bandeiras: `https://flagcdn.com/w40/{code}.png`
- Fontes: Google Fonts (Inter + Playfair Display)

---

## Integração Formspree

### Formulário de Contato
- **Endpoint**: `https://formspree.io/f/xkopabzw`
- **Email destino**: contato@verdemartech.com.br
- **Método**: POST com `multipart/form-data` (suporta anexos)
- **Campos enviados**:
  - `name` — Nome completo
  - `email` — Email do remetente
  - `phone` — Telefone
  - `subject` — Assunto selecionado (parceria, demo, fornecedor, candidato, imprensa, outro)
  - `attachment` — Arquivo anexado (PDF, DOC, PPT) — até 10 MB
  - `message` — Mensagem (máx. 3000 caracteres)

### Estados do Botão
1. **Loading** — "Enviando..." com spinner animado
2. **Sucesso** — "Mensagem enviada! Entraremos em contato em breve." (verde, 6s)
3. **Erro** — "Erro ao enviar. Tente novamente." (vermelho, 4s)

### Limite Gratuito Formspree
- ✅ 50 envios/mês
- ✅ Até 10 MB por anexo
- ✅ Emails enviados para contato@verdemartech.com.br

---

## Contatos
- **Email**: contato@verdemartech.com.br
- **WhatsApp**: (11) 9 3264-2307
- **LinkedIn Fundador**: linkedin.com/in/vitorpmreis
- **LinkedIn Empresa**: linkedin.com/company/verdemar-tech

---

## Publicação
Para publicar, acesse a **aba Publish** e clique em publicar.

Após publicação, o site estará acessível na URL fornecida pela plataforma.

---

## Próximos Passos Recomendados
1. ✅ ~~Adicionar foto real do Vitor Reis na seção Fundador~~ **CONCLUÍDO**
2. ✅ ~~Configurar envio real do formulário de contato~~ **CONCLUÍDO (Formspree)**
3. Hospedar o vídeo hero em servidor próprio para não depender do link original
4. SEO: Open Graph tags, sitemap, schema.org markup
5. Analytics: Google Analytics ou Plausible
6. Configurar domínio próprio (verdemartech.com.br)

---

*Última atualização: 09/04/2026 · Verdemar Tech · São Paulo, Brasil*
