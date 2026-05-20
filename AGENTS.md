# Repository Guidelines

## Estructura del Proyecto y Organización

Este repositorio es intencionalmente mínimo. La raíz contiene `README.md`, con la visión de AI Radar, la arquitectura objetivo y el stack esperado.

Cuando empiece la implementación, mantén esta estructura base:

- `src/` para código de aplicación y lógica compartida.
- `src/app/` o `src/pages/` para rutas de React.
- `src/components/` para componentes reutilizables.
- `src/lib/` para APIs, transformaciones, ranking, validación y deduplicación.
- `tests/` o `*.test.*` junto al código para pruebas.
- `assets/` o `public/` para imágenes, íconos y demo.
- `docs/` para arquitectura, operación y decisiones.

## Comandos de Desarrollo, Pruebas y Build

Todavía no hay package manager, framework ni scripts configurados. No documentes comandos inexistentes sin agregar su configuración.

Cuando se agregue la app JavaScript/React, documenta comandos reales aquí y en `README.md`:

- `npm install` instala dependencias.
- `npm run dev` inicia la aplicación local.
- `npm test` ejecuta la suite de pruebas.
- `npm run lint` revisa formato y calidad.
- `npm run build` genera el build de producción.

## Estilo de Código y Convenciones de Nombres

Usa JavaScript o TypeScript de forma consistente. Prefiere TypeScript para modelos de backend: señales, fuentes, corridas y evidencia.

Usa indentación de 2 espacios en JS, TS, JSON, Markdown y config. Nombra componentes React en `PascalCase`, hooks como `useSomething`, utilidades en `camelCase` y archivos descriptivos como `signal-ranking.ts` o `SourceStatusBadge.tsx`.

Mantén el vocabulario alineado con el README: señales, fuentes, evidencia, corridas, ranking, guías y panel operador.

## Guía de Pruebas

No hay framework de pruebas configurado. Cuando agregues código, prioriza pruebas de ranking, validación, deduplicación y transformación de datos antes que pruebas visuales.

Usa fixtures determinísticos para noticias de IA, papers, changelogs y duplicados. Nombra pruebas como `signal-ranking.test.ts` o `SignalCard.test.tsx`. Cada regla de datos debe cubrir un caso positivo y uno negativo.

## Guía de Commits y Pull Requests

El historial tiene un único commit inicial: `Initial AI Radar README`. Mantén mensajes cortos, en imperativo y con alcance claro, por ejemplo `Add source ingestion model` o `Document Supabase schema`.

Los pull requests deben incluir resumen, notas de prueba, capturas para cambios de UI, issues vinculados y cambios de configuración necesarios.

## Seguridad y Configuración

Nunca subas API keys, credenciales de Supabase, tokens de Notion ni credenciales de scraping. Usa `.env.local` para secretos y documenta variables requeridas con placeholders seguros en `.env.example`.
