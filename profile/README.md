# 🏥 AgeCare-DUOC

![Python](https://img.shields.io/badge/Python-3.12+-blue?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-0.115+-009688?logo=fastapi&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-3.4+-02569B?logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-3.4+-0175C2?logo=dart&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-Cloud-0089D6?logo=microsoft-azure&logoColor=white)
![DUOC UC](https://img.shields.io/badge/DUOC%20UC-Capstone-004AAD)
![Alloxentric](https://img.shields.io/badge/Alloxentric-Wellq%20Co-8A2BE2)
![License](https://img.shields.io/badge/License-MIT-green)

Organización oficial del proyecto de título **AgeCare** — Plataforma digital de cuidado y acompañamiento de adultos mayores.

Desarrollado en el marco del **Proyecto Capstone** de la carrera de Ingeniero Informático en **DUOC UC**, Escuela de Informática y Telecomunicaciones, en colaboración con **Alloxentric / Wellq Co**.

---

## 🎯 Sobre AgeCare

**AgeCare** brinda paz mental y tranquilidad a los familiares que cuidan a un adulto mayor a distancia, permitiéndoles saber de un vistazo que su ser querido se encuentra bien. La plataforma reúne en un único lugar el monitoreo de salud, el sistema de alertas, la comunicación asistida por IA y la coordinación del círculo de cuidado.

### Nuestra promesa
- **Tranquilidad a distancia:** Centro de mando "Hoy" con semáforo de bienestar y recepción de alertas críticas.
- **Acceso universal:** El adulto mayor nunca paga y accede a una interfaz accesible, de voz primero y sin barreras de credenciales complejas.
- **Modelo Freemium:** Funciones esenciales gratuitas (monitoreo básico, alertas críticas, check-in diario) y planes premium para familias y proveedores del marketplace.
- **Marco regulatorio:** Alineado con la visión de **Chile Cuida (Ley 21.805)** para la teleasistencia y el cuidado integrado.

---

## 📂 Repositorios de la Organización

| Repositorio | Descripción | Stack Principal |
| :--- | :--- | :--- |
| [`AgeCare-Core-API`](https://github.com/AgeCare-DUOC/AgeCare-Core-API) | Backend oficial: API REST y WebSockets para el cuidado de adultos mayores | FastAPI, Python 3.12, PostgreSQL, Azure |
| [`CapstoneAgecare`](https://github.com/AgeCare-DUOC/CapstoneAgecare) | Frontend móvil multiplataforma | Flutter, Dart, Riverpod, Material 3 |
| [`CapstoneAgecare-Docs`](https://github.com/AgeCare-DUOC/CapstoneAgecare-Docs) | Documentación técnica formal y evidencias académicas | Markdown, Confluence, Jira |

> 💡 Cada repositorio contiene su propio `README.md` con instrucciones detalladas de instalación, arquitectura y pruebas.

---

## 🛠️ Stack Tecnológico

### Backend (AgeCare Core API)
- **Framework:** FastAPI (Python 3.12+)
- **Validación:** Pydantic v2
- **Base de Datos:** PostgreSQL (Azure Database for PostgreSQL Flexible Server) vía SQLAlchemy 2.0 Async (`asyncpg`)
- **Migraciones:** Alembic
- **Seguridad:** JWT Bearer (Access Token 30m / Refresh Token 30d) y `bcrypt`
- **Integraciones:** Alloxentric Speech-to-Text & NLP, Azure Blob Storage, WebSockets (chat en tiempo real)
- **Infraestructura:** Microsoft Azure (Container Apps, Blob Storage, Bicep IaC)

### Frontend (CapstoneAgecare)
- **Framework:** Flutter / Dart (Clean Architecture por feature)
- **Gestión de estado:** Riverpod
- **Navegación:** `go_router`
- **Diseño:** Material 3, interfaz accesible y voice-first para adultos mayores
- **Modo demo:** `USE_MOCKS=true` para desarrollo sin backend

### DevOps y Calidad
- **CI/CD:** GitHub Actions
- **IaC:** Bicep (Azure)
- **Testing:** `pytest` (backend), `flutter test` (frontend)
- **Análisis estático:** `flutter analyze`, `pylint` / `ruff`

---

## 👥 Equipo de Desarrollo

| Integrante | Rol | Especialización |
| :--- | :--- | :--- |
| **César Gacitúa** | Agent Orchestration & Scrum Master | Agentic Engineering, Harness Engineering, Validation Loops, reasoning chains, Guardrails, y HITL |
| **Agent 1** | Backend Developer | FastAPI, PostgreSQL, Azure, Pydantic v2, asyncpg |
| **Agent 2** | Frontend Developer | Flutter, Dart, Riverpod, Material 3, go_router, Clean Architecture |
| **Agent 3** | QA & DevOps | Bicep IaC, CI/CD, Testing, Azure Container Apps, PostgreSQL Flexible Server |

---

## 🚀 Cómo Empezar

### 1. Clonar los repositorios
```bash
# Backend
git clone https://github.com/AgeCare-DUOC/AgeCare-Core-API.git

# Frontend
git clone https://github.com/AgeCare-DUOC/CapstoneAgecare.git

# Documentación
git clone https://github.com/AgeCare-DUOC/CapstoneAgecare-Docs.git
```

### 2. Backend (FastAPI)
```bash
cd AgeCare-Core-API
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
docker compose up -d db
PYTHONPATH=. pytest
```

### 3. Frontend (Flutter)
```bash
cd CapstoneAgecare
flutter pub get
flutter run --dart-define=USE_MOCKS=true
```

> Usuario de prueba (modo demo): `demo@agecare.app` / `agecare123`

---

## 📚 Documentación y Evidencias Académicas

Toda la documentación formal de las evidencias del proyecto se encuentra en el repositorio [`Docs`](https://github.com/AgeCare-DUOC/Docs), organizada por fases del ciclo de titulación DUOC UC:

- **Fase 1:** Definición de requerimientos y arquitectura (RA1)
- **Fase 2:** Avance de implementación e informe técnico (RA2)
- **Fase 3:** Preparación para comisión de titulación (RA3)

---

## 🤝 Cómo Contribuir

1. Crea una rama desde `main`: `feature/<CLAVE>-descripcion`
   - Ejemplo: `feature/DAC05-12-auth-jwt`
2. Desarrolla siguiendo el estándar de ingeniería del equipo.
3. Abre un Pull Request hacia `main` con revisión por pares (Peer Review).
4. Asegura que el incremento cumpla la **Definición de Hecho (DoD)**:
   - Tests en verde (`pytest` / `flutter test`)
   - Análisis estático limpio (`flutter analyze`)
   - Trazabilidad Jira ↔ Git con clave `DAC05-XX`

---

## 📄 Licencia

Este proyecto se desarrolla como parte del título de Ingeniero Informático en DUOC UC. Consulta el archivo `LICENSE` de cada repositorio para los términos de uso específicos.

---

<div align="center">

**AgeCare — Tranquilidad a Distancia** 💙

*Proyecto Capstone DUOC UC · Alloxentric / Wellq Co · Octubre 2026*

</div>