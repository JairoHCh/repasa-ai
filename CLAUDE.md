@AGENTS.md

# Repasa.ai

App web para una hackatón. El usuario pega sus apuntes de clase y la app genera un resumen corto y 5 preguntas de opción múltiple. El usuario las responde y ve su puntaje.

Prioridad: que funcione y esté desplegada en todo momento.

## Stack

- Next.js (App Router) + TypeScript + Tailwind + shadcn/ui
- IA en una API route del servidor: `/api/generar`, con el SDK de Anthropic.
  - La key va en `ANTHROPIC_API_KEY` y nunca se expone en el cliente.
  - Si `ANTHROPIC_API_KEY` no existe, la API devuelve una respuesta de ejemplo realista (modo demo) para que la app nunca se rompa en el pitch.
- Sin base de datos ni login.
- Deploy en Vercel (cada push a `main` se despliega solo).

## Reglas

- Toda la interfaz en español.
- No agregar librerías sin preguntar primero.
- Componentes pequeños.
- Antes de cada commit, correr `npm run build` y corregir los errores.
- Hacer commit después de cada feature que funcione.
