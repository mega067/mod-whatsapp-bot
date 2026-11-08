# 🤖 Módulo WhatsApp Bot & Mensajería (mod-whatsapp-bot)

<p align="center">
  <img src="https://megaunlockphone-panel.alwaysdata.net/logo.png" width="130" alt="Bot Logo">
</p>

<p align="center">
  <strong>Demonio Socket Basado en Baileys para Notificaciones de Pedidos, Recargas, Comandos y Soporte 24/7</strong>
</p>

<p align="center">
  <a href="https://github.com/mega067/MegaUnlockPhone"><img src="https://img.shields.io/github/stars/mega067/MegaUnlockPhone?style=for-the-badge&color=f59e0b&logo=github" alt="Stars"></a>
  <a href="https://github.com/mega067/MegaUnlockPhone/releases"><img src="https://img.shields.io/github/downloads/mega067/MegaUnlockPhone/total?style=for-the-badge&color=10b981&logo=github" alt="Downloads"></a>
  <a href="https://megaunlockphone-panel.alwaysdata.net/"><img src="https://img.shields.io/badge/Bot_Daemon-Online-emerald?style=for-the-badge&logo=whatsapp" alt="Bot Status"></a>
  <img src="https://img.shields.io/badge/Anti--Ban-Protected-green?style=for-the-badge" alt="Anti Ban">
</p>

---

## 📌 1. ¿Qué es `mod-whatsapp-bot`?

**`mod-whatsapp-bot`** es el demonio de mensajería automatizada del ecosistema **[MegaUnlockPhone](https://github.com/mega067/MegaUnlockPhone)**. Construido sobre `@whiskeysockets/baileys`, opera de forma desacoplada para garantizar que el servidor web principal nunca sufra caídas de rendimiento por el tráfico de mensajería.

### Características Industriales:
- 🛡️ **Anti-Ban Avanzado con Delays Humanizados:** Despacho con jitter dinámico (`3.5s` a `7.0s`) y pausas de enfriamiento cada 5 envíos continuos.
- ✍️ **Simulación de Escritura Real (`composing`):** Envía señales de presencia y escritura antes de emitir cualquier mensaje para renovar las llaves de cifrado de Signal y erradicar el bug *"Esperando el mensaje"*.
- 🔒 **Gestión de Candado (`bot.lock` Process-Aware):** Auto-rescate si el proceso sufre cierres inesperados, previniendo errores de socket duplicado (Status 440 Replaced).
- 📲 **Comandos Disponibles para Clientes y Administradores:**
  - `/saldo` — Consulta de balance actual.
  - `/pedidos` — Estado de órdenes pendientes o completadas.
  - `/ticket` — Generación de comprobante digital de compra.
  - `/pago` o `/abono` — Registro directo en el módulo financiero.

---

## 🏛️ Integración Modular con MegaUnlockPhone

Este bot es un módulo satélite del proyecto **[MegaUnlockPhone](https://github.com/mega067/MegaUnlockPhone)**:

```
┌────────────────────────────────┐
│      🏛️ MUP-CORE (API)         │
│  Emite eventos de órdenes      │
└───────────────┬────────────────┘
                │ HTTP POST (Headers: X-Bot-Secret)
                ▼
┌────────────────────────────────┐
│      🤖 MOD-WHATSAPP-BOT       │
│  Gestiona la cola y el socket  │
└───────────────┬────────────────┘
                │ WebSockets
                ▼
┌────────────────────────────────┐
│      📱 WhatsApp Clientes      │
└────────────────────────────────┘
```

---

## 🚀 Inicio y Configuración

```bash
# Iniciar como demonio en AlwaysData o VPS:
./start_bot.sh

# Ver logs en vivo:
tail -f bot_logs.txt
```

---

<p align="center">
  <sub>WhatsApp Bot &copy; 2026. Módulo Oficial de MegaUnlockPhone.</sub>
</p>
