---
clase: 17
titulo: El Mecanismo en la VSL · mapa pieza → paso
fuente: Puente entre la Biblia del Mecanismo (clase 16) y la estructura canónica de 15 pasos
---

# El Mecanismo en la VSL · dónde va cada pieza

Este archivo es el **puente** entre la [Biblia del Mecanismo](16-biblia-del-mecanismo.md) (el cuerpo de conocimiento completo: las 4 capas, los 2 mecanismos, causa raíz, objeto brillante, nombre chicle, mito de origen, oferta única) y la **estructura canónica de 15 pasos de la VSL**.

> Si la Biblia es el QUÉ (qué es cada pieza del mecanismo), este archivo es el DÓNDE (en qué paso de la VSL se coloca cada una y qué agente la maneja).

## 0 · El intake de la oferta (OPCIONAL · si la tiene, mejor)

Este plugin y sus agentes ya saben construir una VSL perfecta por sí solos. Esta sección NO cambia eso: solo añade una capa **opcional** para cuando el usuario YA tiene su oferta construida (normalmente desde `zenith-crea-ofertas`) y quiere que la VSL la respete pieza por pieza.

**Cómo actuar:**

1. **Pregunta (opcional) al empezar:** "¿Ya tienes la oferta construida (promesa, mecanismo, nombre chicle, etc.) o la creamos sobre la marcha?"
2. **Si el usuario TIENE la oferta** → te pasará estas piezas. **Colócalas en su sitio** según el mapa de la sección 1 (no te las inventes, úsalas tal cual):

| Pieza de la oferta | Qué es | Dónde profundizar |
|---|---|---|
| **Nombre chicle** | El nombre pegadizo del mecanismo (2-3 palabras) | Biblia · PARTE 8 |
| **Mecanismo del problema** | El villano que explica el dolor | Biblia · PARTE 3 |
| **Causa raíz** | La cadena causal (mecánica + emocional) | Biblia · PARTE 4 |
| **Mecanismo de la solución** | El "cómo deseable" / huevo soplado | Biblia · PARTE 5 |
| **Objeto brillante** | Las piezas nombradas que rechean la oferta | Biblia · PARTE 7 |
| **Mito de origen** | El rostro y la historia del descubrimiento | Biblia · PARTE 6 |
| **Promesa** | El resultado prometido | — |

3. **Si el usuario NO tiene la oferta** → **no pasa nada: construye la VSL con normalidad.** `vsl-mecanismo` crea el mecanismo como siempre y la Biblia (clase 16) está ahí solo como referencia de respaldo por si quieres profundizar. NO bloquees al usuario ni le exijas tener la oferta hecha.

> Resumen: la oferta es un INPUT opcional. Si la tienes, este mapa te dice dónde colocar cada pieza. Si no, la VSL se hace igual de bien sin ella.

## 1 · El mapa · cada pieza en su paso de la VSL

La estructura canónica son 15 pasos (ver `vsl-structure`). Cada pieza del mecanismo tiene su sitio exacto:

| # Paso VSL | Pieza(s) del mecanismo que van aquí | Cómo se usan | Agente |
|---|---|---|---|
| **01 · Headline (encima del play)** | **Nombre chicle** + promesa | El nombre chicle abre la curiosidad ("¿qué es eso?"). Cabe en la headline con beneficio + credibilidad + curiosidad. | `vsl-headline` |
| **02 · Microlead** | **Nombre chicle** + teaser de la **causa raíz** | Confirma las 3 preguntas (¿es verdad? ¿funciona? ¿es para mí?) y planta el nombre chicle + el "no es lo que crees". | `vsl-microlead` |
| **03-04 · Lead + Agitación del dolor** | **Mecanismo del problema (villano)** + **causa raíz emocional** | Nombra el villano y **externaliza la culpa** ("no es tu culpa, es X"). Agita el dolor visceral. La causa raíz emocional (los 5 porqués) conecta con la herida. | `vsl-lead` |
| **05 · Loops de curiosidad** | "Por qué fallaron las soluciones anteriores" | Cada solución previa que falló = un loop ("ya probaste X, pero…"). El villano explica por qué fallaron (atacaban el síntoma, no la raíz). | `vsl-lead`, `vsl-psicologia` |
| **06-07 · Historia del protagonista** | **Mito de origen** | El rostro (persona común / fuente oculta / ritual ancestral), los 5 pasos (quién era → incidente → jornada → **gran descoberta** → resultado), el fracaso previo que legitima. La "gran descoberta" = el momento en que halla el mecanismo de la solución. | `vsl-historia` |
| **08 · Mecanismo único (científico)** | **Mecanismo único + causa raíz fisiológica + mecanismo de la solución** | El corazón. Las **4 capas** encadenadas: nombre chicle → mecanismo único → mecanismo del problema → causa raíz. Estructura `causa raíz → ruta → activador → resultado`. Luego el "cómo deseable" (el huevo soplado: la solución fácil que nadie pensó). | `vsl-mecanismo` |
| **09-10 · Prueba del mecanismo** | **Credibilidad del mecanismo** | Los 8 tipos de prueba · **prueba por negación** (quita el ingrediente, el resultado cae) · especificidad numérica · **dimensionalización** (analogía visual: "tu cerebro es como un fregadero atascado") · **super estructura** (credibilidad prestada). | `vsl-mecanismo`, `vsl-psicologia` |
| **11 · Reset de objeciones** | **El mecanismo rompe las objeciones** | "Ya lo probé todo" → el villano explica por qué falló. "No es para mí" → el mecanismo es más fácil (huevo soplado). Cada objeción se desmonta con una capa del mecanismo. | `vsl-cierre`, `vsl-psicologia` |
| **12-13 · Transición + Pitch + oferta + bonos** | **Objeto brillante + oferta única** | Cada bono/módulo/entregable se nombra como **objeto brillante** ("¿qué es eso?") → oferta CON brillo, no genérica. La **ecuación de Hormozi**: el mecanismo sube la probabilidad percibida y baja el esfuerzo → justifica el precio. El nombre chicle es lo último antes del precio. | `vsl-cierre` |
| **14 · CTA** | **Nombre chicle** (cierre) | El nombre chicle se repite como última señal: "esto es lo que yo quería". | `vsl-cierre` |
| **15 · Post-pitch** | **FAQ del mecanismo + future pacing** | Las FAQ NO son genéricas: son del mecanismo ("¿el [nombre chicle] funciona para…?"). Future pacing usando el mecanismo. Última oportunidad. | `vsl-post-pitch` |

## 2 · Las 4 capas, mapeadas a la VSL

La VSL despliega las 4 capas del mecanismo en orden inverso al de profundidad: primero el síntoma/villano (Lead), luego la revelación del agente y la cadena (Mecanismo), y el nombre chicle envuelve todo de principio a fin.

```
Headline/Microlead  →  NOMBRE CHICLE (la etiqueta · abre curiosidad)
Lead/Agitación      →  MECANISMO DEL PROBLEMA (el villano · externaliza culpa)
Mecanismo (paso 08) →  MECANISMO ÚNICO + CAUSA RAÍZ (el agente + la cadena causal)
Mecanismo + Pitch   →  MECANISMO DE LA SOLUCIÓN (el cómo deseable)
```

## 3 · Regla de oro de coherencia

El **nombre chicle** y el **villano** que se prometen en la Headline/Microlead **tienen que ser los mismos** que se desarrollan en el Mecanismo y se cierran en el Pitch. Cero traición de mensaje: si el anuncio/headline dice "el método X", la VSL entera gira sobre "el método X". (Biblia · PARTE 13 · congruencia.)

## 4 · Bencivenga · dónde sube cada palanca

- **Beneficio** ↑ → Lead + Historia (promesa + mito de origen).
- **Credibilidad** ↑ → **Mecanismo** (las 4 capas + prueba). ← aquí manda el mecanismo.
- **Costo** ↓ → Cierre (objeto brillante + oferta única + garantía).

> El Mecanismo es la pata de la **Credibilidad**. Sin un mecanismo bien colocado, la VSL promete (Beneficio) pero no se cree (Credibilidad) → no convierte.
