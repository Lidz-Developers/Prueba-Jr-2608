# Prueba técnica — Software Engineer Junior

**Tiempo estimado: 3–4 horas.** Si llegas a las 4 horas, entrega lo que tengas con un README honesto. Preferimos algo chico que funcione y que puedas defender, a algo grande a medias.

## El problema

En Lidz, cada inmobiliaria recibe cientos de conversaciones de WhatsApp al día. Un asistente con IA responde, pero los ejecutivos comerciales no alcanzan a leerlas todas y hoy eligen a quién llamar "a ojo". Se les escapan leads calientes y pierden tiempo con gente que se equivocó de número.

Queremos una herramienta que lea una conversación y le diga al ejecutivo, **sin que tenga que abrirla**, si vale la pena atenderla y con qué prioridad.

## Lo que necesita el equipo comercial

Cuando hablamos con los ejecutivos, esto es lo que dijeron que necesitan saber de cada conversación:

- Qué busca la persona (¿quiere comprar?, ¿invertir?, ¿solo preguntaba?, ¿es un reclamo?, ¿ni siquiera es un lead?).
- Qué tan apurada está.
- Si dijo cuánto puede pagar y qué tipo de departamento busca.
- Si hay algo que **el asistente no debería resolver solo** y necesita que un humano intervenga.
- Un resumen de una línea para decidir rápido.

Cómo modelas eso es decisión tuya. Lo único innegociable: **si la conversación no dice algo, la herramienta no lo inventa.** Un ejecutivo que llama a alguien con un "presupuesto" que nunca existió pierde la confianza en la herramienta para siempre.

## Lo que te entregamos

- `fixtures/conversaciones.json`: 10 conversaciones reales (anonimizadas y ficcionalizadas) del proyecto "Mirador Ñuñoa". Son variadas a propósito: hay leads buenos, curiosos, gente equivocada, un reclamo y alguien que intenta hacerle trampa al asistente.
- Una API key de OpenAI (variable de entorno `OPENAI_API_KEY`) con límite de gasto.

## Lo que esperamos de vuelta

1. La herramienta funcionando, en **TypeScript**, y expuesta de una forma en que otro sistema de Lidz pueda usarla (nuestro backend la va a llamar por HTTP para cada conversación nueva).
2. El resultado de pasar las 10 conversaciones por tu herramienta, incluido en el repo. Queremos ver cómo se comporta con los casos difíciles, no que nos lo cuentes.
3. Evidencia de que funciona y va a seguir funcionando cuando alguien lo toque: cómo lo probaste es parte de lo que evaluamos.
4. Un `README.md` **detallado y escrito por ti, no por una IA**. Queremos saber cómo piensas, y eso no lo podemos evaluar en un texto generado. Debe cubrir al menos:
   - Cómo correrlo.
   - Qué decidiste (qué campos, qué modelo, cómo estructuraste el código, cómo lo probaste) y **por qué**, incluyendo las alternativas que descartaste.
   - Qué te costó más y cómo lo resolviste.
   - Cuánto costó en dinero procesar las 10 conversaciones.
   - Qué harías distinto con más tiempo.

   Puede tener errores de redacción; no puede ser genérico. En la entrevista vamos a conversar sobre lo que escribiste.

## Entrega

- **Repo en GitHub**, público o privado. Si es privado, compártelo con **@joaquincastillo**. Debe contener el código y el `README.md`.
- **Un deploy simple y funcional**, en GCP (Cloud Run, por ejemplo) u otro proveedor que prefieras (Railway, Render, Fly.io, Vercel, AWS…). Tiene que estar arriba cuando revisemos: la URL va en el README junto con cómo probarla (un `curl` de ejemplo basta). Sí, evaluamos el deploy: que exista, que responda y que no exponga la key.
- No aceptamos `.zip` ni código por correo.

## Reglas

- La API key nunca va en el repo.
- Puedes usar cualquier herramienta de IA para programar. El README no: ese lo escribes tú. En la entrevista de seguimiento vas a explicar el código y cambiar algo en vivo, así que tienes que entenderlo.
