# Edgar Gómez

**Investigación tecnológica · Arquitectura de sistemas · Integración de soluciones**

Costa Rica · [github.com/agomez356](https://github.com/agomez356)

---

No soy experto en un framework. Soy la persona que identifica qué tecnología necesita tu problema, la conecta con lo que ya existe en tu organización, y construye la solución.

El 50% de mi tiempo lo dedico a investigar y prototipar tecnologías emergentes. El otro 50% a construir sistemas que funcionen en producción con usuarios reales.

Trabajo con IA como herramienta activa de desarrollo — no para reemplazar el criterio técnico, sino para amplificarlo. Diseño flujos donde la IA ejecuta y yo dirijo: desde prototipado con V0, hasta agentes que interactúan con ERPs en producción.

La seguridad y la privacidad de los datos no son un paso final — son parte del diseño desde el inicio. Cada sistema que construyo incluye auditoría, hardening y documentación de decisiones de seguridad.

---

## Proyectos con impacto

### Bolsa de Empleo Digital — CPIC
*En producción · 350 usuarios activos*

Sistema completo de bolsa de empleo institucional construido de cero:

- **Frontend** — Next.js App Router + Shadcn/UI, prototipado con V0
- **Backend** — Plugin WordPress en PHP con GraphQL como API tipada (mutations para ofertas, postulación, empresas y perfiles)
- **API** — FastAPI + PostgreSQL con Alembic, migración progresiva desde Next.js
- **Auth** — Azure AD / O365 + JWT + QR Login
- **DevOps** — Docker multi-stage, Nginx, auto-deploy con GitHub, blue-green deployment en DigitalOcean
- **Seguridad** — Auditoría GraphQL documentada, RFC9457, hardening de producción

### MCP Servers para Odoo
*3 módulos en producción*

Servidores MCP propios en Python (`llm`, `llm_mcp_server`, `llm_tool`) para conectar LLMs con el ERP institucional. Permite que usuarios no técnicos interactúen con Odoo en lenguaje natural. Incluye auditoría de seguridad, OAuth2 y tests E2E.

### FastAPI CPIC — API institucional

API REST institucional con integración Azure AD, Docker, CI/CD con GitHub Actions, monitoreo y documentación RFC9457.

### Odoo para gestión agrícola
*Proyecto independiente*

Implementé y customicé Odoo para la administración operativa de una finca familiar. Primer proyecto con cliente real fuera del entorno institucional.

### Chorus — Orquestación Multi-Agente
*Investigación*

Sistema experimental de orquestación de agentes con roles especializados basado en el protocolo A2A de Google.

---

## Stack

**Backend** · Python · FastAPI · PHP · PostgreSQL · Alembic · JWT  
**Frontend** · TypeScript · Next.js · Shadcn/UI  
**DevOps** · Docker · Nginx · DigitalOcean · GitHub Actions  
**AI/LLM** · MCP Protocol · Claude · Odoo LLM modules · Multi-agent orchestration · V0  
**Seguridad** · Azure AD · OAuth2 · RFC9457 · hardening de producción  
**ERP** · Odoo (módulos e integraciones)

---

## Formación

Diplomado en Informática — Universidad Estatal a Distancia (UNED) · En curso desde 2018  
Cursos aprobados: Programación Avanzada · Sistemas Operativos · Estructura de Datos · Introducción a la Programación · Lógica para Computación

---

## Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=agomez356&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=agomez356&layout=compact&theme=tokyonight&hide_border=true&langs_count=6)

</div>
