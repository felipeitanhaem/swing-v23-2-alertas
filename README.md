# Swing V23.2 — Alertas com celular bloqueado

App de acompanhamento de swing trade que lê a carteira do Firebase e dispara
alertas (RA/RB e Laranja) mesmo com o celular bloqueado.

## ⚙️ Configuração obrigatória no Xiaomi 12S (HyperOS/MIUI)

Para o alerta aparecer na tela de bloqueio e tocar o som, ative TODOS os itens:

1. **Configurações > Tela de bloqueio > Ativar tela ao receber notificação** → ON
2. **Configurações > Notificações > Notificações na tela de bloqueio** → Permitir
3. **Configurações > Notificações > Notificações flutuantes** → Permitir
4. **Configurações > Bateria e desempenho > Economia de energia** → Desativar
5. **Configurações > Gerenciamento de autorizações > Inicialização automática** → Permitir
6. **Gerenciamento de autorizações > Exibir na tela de bloqueio** → Permitir
7. **Gerenciamento de autorizações > Iniciar em segundo plano** → Permitir
8. **Gerenciamento de autorizações > Exibir janelas pop-up** → Permitir
9. **Notificação pop-up** → Alterar para **"Apenas na tela de bloqueio"**
10. **Configurações > Papel de parede e personalização > Efeito de notificação** → **"Ativar tela"**

## 🐛 Limitações conhecidas

- Android 14+ pode bloquear `USE_FULL_SCREEN_INTENT` para apps que não são
  despertador/chamada. Nesse caso, a notificação vira "heads-up" (topo da tela).
- Em MIUI/HyperOS, se o app for fechado na tela de recentes, o polling para.
  Solução futura: usar FCM push (Firebase Cloud Messaging).

## 📦 Build

O APK é gerado automaticamente pelo GitHub Actions (`.github/workflows/build.yml`).
Vá em **Actions → Build APK V23.2 → Run workflow** e baixe em **Artifacts**.