# Gestor de Agenda Digital Inteligente

> Asistente robótico para **gestión integral de calendarios y comunicaciones**, con **sincronización bidireccional**, **notificaciones** y **panel de productividad**.

## 🎯 Objetivo
Centralizar, sincronizar y optimizar la administración de eventos personales/profesionales; mejorar la comunicación y ofrecer *insights* de gestión del tiempo.

## 🧩 Componentes
- **Calendarios**: Google Calendar y Outlook (lectura/escritura, sync en tiempo real).
- **Comunicación**: recordatorios vía **WhatsApp** y email.
- **Estadísticas**: cumplimiento, retrasos, tendencias, métricas de uso.
- **Filtros**: por **responsable**, **categoría** y **lugar**.

## ⚙️ Tecnologías
- **Backend/API**: Python (FastAPI)
- **DB**: MySQL
- **Frontend**: HTML + CSS
- **Contenedores**: Docker / Docker Compose
- **Control de versiones**: Git/GitHub

## 🔐 Seguridad y Cumplimiento
- OAuth + 2FA, tokens cifrados en BD
- Logs de auditoría
- GDPR/CCPA (privacidad por diseño)

## 📈 KPIs
- Tiempo de sincronización **< 500ms**
- Disponibilidad **99.99%**
- Precisión de notificaciones **99.5%**

---

## 🏗️ Arquitectura (vista lógica)
- **api/**: REST (auth, eventos, filtros, estadísticas)
- **sync/**: integración OAuth + Webhooks (Google/Outlook), reconciliación de cambios
- **notifier/**: envíos WhatsApp/email, reintentos, bitácora
- **web/**: UI estática (HTML/CSS) consumiendo API
- **infra/**: Dockerfiles, docker-compose, nginx

```
agenda-assistant/
 ├─ api/
 ├─ sync/
 ├─ notifier/
 ├─ web/
 └─ infra/
```