# Edgar Gómez

**Investigación tecnológica · Arquitectura de sistemas · Integración de soluciones**

Costa Rica · [github.com/agomez356](https://github.com/agomez356)

---

No soy experto en un framework. Soy la persona que identifica qué tecnología necesita tu problema, la conecta con lo que ya existe en tu organización, y construye la solución.

El 50% de mi tiempo lo dedico a investigar y prototipar tecnologías emergentes. El otro 50% a construir sistemas que funcionen en producción con usuarios reales.

Trabajo con IA como herramienta activa de desarrollo — no para reemplazar el criterio técnico, sino para amplificarlo. Diseño flujos donde la IA ejecuta y yo dirijo: desde prototipado con V0, diseño con Google Stitch, hasta agentes que interactúan con ERPs en producción.

La seguridad y la privacidad no son un paso final — son parte del diseño desde el inicio. Cada sistema que construyo incluye auditoría, hardening y documentación de decisiones de seguridad.

---

## Proyectos con impacto

### Bolsa de Empleo Digital — CPIC
*En producción · ~2,000 profesionales IT · 350 usuarios activos*

Sistema completo de bolsa de empleo institucional construido de cero. Arquitectura multi-capa:

- **Frontend** — Next.js 16 App Router + shadcn/ui + Apollo Client. Prototipado con V0, integración backend con Claude Code. **PKCE (RFC 7636) implementado desde cero** con Web Crypto API nativa, sin librerías externas
- **Plugin WordPress** — PHP 8 + PSR-4 + WPGraphQL como API tipada. 10 Custom Post Types, session handoff JWT, arquitectura Zero Trust (Cloudflare)
- **API Layer** — FastAPI + PostgreSQL con Alembic, bridgeando el ERP legacy (SQL Server/Softland). RFC 9457, circuit breakers, Azure AD OAuth2, Sentry APM
- **Auth** — Azure AD / O365 + JWT + QR Login + PKCE
- **DevOps** — Docker multi-stage, Nginx, blue-green deployment en DigitalOcean, GitHub Actions CI/CD

### MCP Servers para Odoo — CPIC
*En producción*

Servidor MCP standalone (`cpic-mcp-server`) que conecta LLMs con Odoo 19 Enterprise via JSON-RPC: 6 tools para auth, proyectos, tareas y `ai_execute_agent` — permite que Claude invoque los AI agents nativos de Odoo 19. Compatible con Claude Desktop, Claude Code y Codex.

### FastAPI CPIC — API institucional
*En producción*

API REST enterprise que bridgea el ERP legacy (SQL Server/Softland) con PostgreSQL moderno y Odoo 19. Integración Azure AD, dual database con circuit breakers, RFC 9457, Sentry APM, multi-agent AI development system.

### Auditoría de Seguridad — VPS Producción
*Enero 2026 · 52/100 → 82/100 · $0 en tooling*

Auditoría completa + hardening sobre sitio WordPress institucional en Docker/DigitalOcean. 37 controles evaluados bajo ISO 27001, OWASP Top 10, CIS Docker Benchmark y leyes costarricenses (Ley 8787, Ley 8968, Decreto 45061-MICITT). **Docker/Infraestructura: 100% compliance**. Scripts propios para forensics automatizado con cadena de custodia legal.

### CI/CD Pipeline — Multi-repo
*GitHub Actions · SSH · Docker · 6 repos*

Pipeline centralizado con reusable workflow: toda la lógica de deploy vive en un solo archivo; cada repo lo referencia con un `uses:` mínimo. Soporta 5 tipos de repo con quality gates específicos.

| Tipo | Quality gate | Deploy |
|------|-------------|--------|
| `php-plugin / theme / mu` | PHP lint | `git reset` + `composer install` |
| `nextjs` | `pnpm build` | `docker compose build + up` |
| `docker-stack` | `docker compose config` | `docker compose up --remove-orphans` |

- **Git model**: `feature → staging (test) → main (prod)` — staging acumula commits de entorno que nunca deben llegar a producción, por eso el feature branch va directo a main
- **SSH hardening**: host key pinning sin `StrictHostKeyChecking=no`, usuario de deploy dedicado, puerto SSH no estándar en staging
- **Healthcheck**: workflow cada 5 minutos con alertas a Telegram — detecta DOWN y RECOVERY con state tracking via GitHub Variables
- **Rollback documentado**: objetivo < 2 minutos para cualquier tipo de repo

### Proyectos personales

**Miweb** — Blog técnico construido con Astro 4 + Vue 3 + MDX + KaTeX. Flujo: diseño con Google Stitch MCP → implementación con Claude Code. [agomez356.github.io/Miweb](https://agomez356.github.io/Miweb)

**Odoo — gestión agrícola** — Implementación y customización de Odoo para administración operativa de una finca familiar.

---

## Contribuciones open source

### apexive/odoo-llm — PR mergeado · Mayo 2026

Port de `apexive/odoo-llm` a Odoo 19.0: desarrollado localmente, validado en producción CPIC, luego contribuido upstream.

- Adoptó la nueva API de grupos de Odoo 19 (`res.groups.privilege` + `privilege_id`)
- 578 adiciones · 1,842 eliminaciones · 30 archivos modificados
- Revisado y mergeado por el equipo de Apexive

🔗 [github.com/apexive/odoo-llm/pull/252](https://github.com/apexive/odoo-llm/pull/252)

---

## Flujos de desarrollo AI-first

```
V0 → mock data MVP → Claude Code + Antigravity → integración backend → producción
Google Stitch MCP → design system → Claude Code → implementación → deploy
SDD: explore → propose → spec → design → tasks → apply → verify
MCP server: definir tools → implementar transport → Claude Desktop los descubre
```

---

## Stack

**Backend** · Python · FastAPI · PHP 8 · PostgreSQL · Alembic · SQL Server · JWT  
**Frontend** · TypeScript · Next.js 16 · React 19 · Astro 4 · Vue 3 · shadcn/ui · Tailwind v4 · Apollo Client  
**AI/LLM** · MCP Protocol · Claude Code · Goose · OpenAI Agents API · V0 · Google Stitch · A2A  
**ERP** · Odoo 19 Enterprise (módulos nativos + integración externa) · Softland/SQL Server  
**DevOps** · Docker · Nginx · DigitalOcean · GitHub Actions · Blue-Green Deployment  
**Auth** · Azure AD · OAuth2 · PKCE (RFC 7636) · JWT · Zero Trust · Cloudflare  
**Seguridad** · ISO 27001 · OWASP Top 10 · CIS Docker Benchmark · fail2ban · Trivy · Ley 8968 CR  
**Protocolos** · MCP 2025-06-18 · GraphQL · JSON-RPC · WebSocket · RFC 9457

---

## Formación

Diplomado en Informática — Universidad Estatal a Distancia (UNED) · En curso desde 2018  
Cursos aprobados: Programación Avanzada · Sistemas Operativos · Estructura de Datos · Introducción a la Programación · Lógica para Computación  
Inglés B1 — lectura técnica funcional

---

## Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=agomez356&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=agomez356&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)

</div>