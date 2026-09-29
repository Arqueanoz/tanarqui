# Finanças Tanarqui — app no iPhone com notificações

## 1. Apps Script (versão v6)
1. Colem o `Codigo.gs` e o `Index.html` novos por cima dos actuais e guardem (💾).
2. **Permissões novas:** escolham a função `autorizar` → ▶ Executar → Rever autorizações → a vossa conta → Avançadas → Aceder → Permitir.
   (A app passa a poder falar com o OneSignal e a correr sozinha uma vez por dia.)
3. Implementar → Gerir implementações → lápis ✏️ → **Nova versão** → Quem tem acesso: **Qualquer pessoa** → Implementar.
4. Confirmem que o **PIN está activo** (⚙️ → PIN de acesso). Obrigatório com acesso «Qualquer pessoa».

## 2. GitHub Pages
**Primeira vez:**
1. Criem conta em github.com → **+** → **New repository** → nome `tanarqui` → **Public** → **Create repository**.
2. **uploading an existing file** → arrastem **todos os ficheiros desta pasta** → **Commit changes**.
3. **Settings → Pages** → Source: **Deploy from a branch** → **main** e **/(root)** → **Save**.

**Já tinham publicado a versão anterior?** Carreguem os ficheiros novos por cima (o GitHub substitui); não é preciso apagar nada.

**Nos dois casos:** abram `config.js` no GitHub → lápis ✏️ → colem o link `/exec` da app entre as aspas → **Commit changes**.
(O link agora vive no `config.js`, para que as próximas actualizações não o apaguem.)

O endereço da vossa app fica: `https://o-vosso-utilizador.github.io/tanarqui/`

## 3. Instalar em cada iPhone
Safari → abram o endereço → Partilhar ↑ → **Adicionar ao ecrã principal** → **Adicionar**. Abram pelo ícone e ponham o PIN.
Já tinham instalado? Não precisam de reinstalar.

## 4. Conta grátis no OneSignal (uma vez)
Os nomes dos botões podem variar um pouco.
1. onesignal.com → criar conta grátis.
2. **New App/Website** → nome `Tanarqui` → plataforma **Web** → seguinte.
3. Tipo de integração: **Custom Code** (não «Typical Site» — assim o OneSignal não mostra pedidos dele por cima do da app).
4. Preencham:
   - Site Name: `Tanarqui`
   - Site URL: `https://o-vosso-utilizador.github.io` — **só isto, sem /tanarqui**
   - Auto Resubscribe: **ligado**
   - Default Icon URL: `https://o-vosso-utilizador.github.io/tanarqui/icon-192.png`
5. Guardem. Ignorem o código que o OneSignal mostra — já está nestes ficheiros.
6. **Settings → Keys & IDs**: copiem o **App ID** e criem/copiem uma **API Key** (em contas antigas: «REST API Key»).

## 5. Ligar tudo
1. Abram a Tanarqui **pelo ícone** → ⚙️ Definições → **🔔 Notificações no telemóvel**.
2. Colem o App ID e a chave, escolham a hora, marquem «Enviar avisos todos os dias» → **Guardar**.
3. Aparece em baixo «Receber os avisos no telemóvel?» → **Activar** → **Permitir**.
4. **Enviar teste** — deve chegar em segundos.
5. No outro iPhone: abrir pelo ícone → **Activar** → **Permitir** (a chave já não é preciso pôr).

## O que chega e quando
Uma notificação por dia, à hora escolhida, só quando há avisos novos:
- fixos e prestações que vencem amanhã, hoje, ou venceram ontem sem registo;
- metas que terminam amanhã ou hoje;
- orçamentos a 80% e ultrapassados;
- mesada pessoal ultrapassada, saldo negativo;
- a revisão a dois, no 1.º e no 5.º dia do mês financeiro.

Cada aviso só chega uma vez. Os outros continuam no painel 🔔 da app.
Quem preferir privacidade: escolham **Conteúdo: Genérico** — a notificação diz só «Têm 3 avisos novos», sem valores.

## Se algo não funcionar
- **Não aparece o pedido:** abram pelo ícone (no Safari o iPhone não deixa) e confirmem iOS 16.4 ou mais recente. Em ⚙️ há «Activar neste telemóvel».
- **«Nenhum telemóvel activou»:** falta tocar em Activar → Permitir num dos iPhones.
- **Carregaram em «Não permitir»:** iPhone → Definições → Notificações → Tanarqui → Permitir.
- **Aviso sobre «Site URL»:** no OneSignal o Site URL tem de ser exactamente `https://o-vosso-utilizador.github.io`.
- **A app ficou presa:** fechem-na no alternador de apps e abram de novo.
