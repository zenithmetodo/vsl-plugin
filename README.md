# VSL Masterclass · Plugin Claude Code

Sistema completo de agentes Claude Code para construir Video Sales Letters (VSL), microleads, leads, landing pages y campañas de Direct Response. Basado en el módulo 02 de la formación **VSL's Millonarias** adaptada al español de España por Joseph Moreno.

Un orquestador padre coordina **16 subagentes especializados** + **4 skills de conocimiento compartido**. Cada agente domina una pieza del puzzle: desde detectar el nivel de consciencia del lead hasta diseñar el Complejo del Play Rate de tu landing.

---

## Instalación

```bash
claude /plugin install https://github.com/zenithmetodo/vsl-masterclass
```

Después de instalar:

```bash
# El orquestador padre — punto de entrada recomendado
/vsl-masterclass:vsl-master

# O invoca un agente concreto directamente
@agent-vsl-masterclass:vsl-headline
```

---

## Arquitectura

```
┌──────────────────────────────────────────────────────────────┐
│                      vsl-master (PADRE)                       │
│  Detecta intent, hace preguntas, decide qué agente lanzar     │
│  y compone la respuesta final                                 │
└──────────────────────────────────────────────────────────────┘
                              │
        ┌────────────┬────────┴────────┬────────────┐
        ▼            ▼                 ▼            ▼
   PRE-VSL       VSL CORE         POST-VSL       RESEARCH
        │            │                 │            │
  ┌─────┴─┐    ┌─────┴─────┐    ┌──────┴──┐  ┌─────┴──────┐
  │detector│   │microlead  │    │ landing │  │ trends     │
  │niveles │   │headline   │    │mini-vsl │  │ ad-library │
  └────────┘   │lead       │    │info-nutra│  │ test-ab    │
               │structure  │    │post-pitch│  └────────────┘
               │historia   │    └─────────┘
               │mecanismo  │
               │cierre     │
               │psicologia │
               └───────────┘
```

---

## Agentes incluidos

### Orquestador
| Agente | Qué hace |
|---|---|
| `vsl-master` | Padre. Pregunta el nicho, el avatar, el objetivo. Decide qué agentes lanzar y en qué orden. Compone la respuesta final. |

### Pre-VSL (research + estrategia)
| Agente | Qué hace |
|---|---|
| `vsl-detector-consciencia` | Detecta nivel de consciencia (Schwartz) del lead objetivo. Propone tipo de Lead idóneo. |
| `vsl-info-nutra` | Decide la estrategia: Info digital vs Nutra encapsulado. Adapta a España. |
| `vsl-research-trends` | Busca tendencias en Google Trends y YouTube para encontrar nichos calientes. |
| `vsl-research-ads` | Investiga la Meta Ads Library y swipe files (American Swipe, Seven Swipe) para extraer ofertas validadas. |

### VSL Core (estructura + copy)
| Agente | Qué hace |
|---|---|
| `vsl-structure` | Diseña la estructura completa del VSL (15 pasos canónicos) según el nivel de consciencia. |
| `vsl-microlead` | Crea microleads de 10-12s para anuncios — el primer impacto antes del lead. |
| `vsl-lead` | Genera leads usando uno de los 6 tipos canónicos del libro Great Leads (Masterson + Forde). |
| `vsl-headline` | Construye headlines con la trinity Beneficio + Credibilidad + Curiosidad. |
| `vsl-historia` | Diseña la sección historia / autoridad / protagonista según el perfil narrador. |
| `vsl-mecanismo` | Construye el "mecanismo único" (el cómo funciona) — clave para subir credibilidad. |
| `vsl-cierre` | Diseña el cierre agresivo: precio, garantía, escasez, urgencia. |
| `vsl-post-pitch` | Sección post-pitch: "ya hice todo lo que podía. La decisión es tuya". |
| `vsl-psicologia` | Loops mentales, Reason to stay, Reset on two state, Promesas de tiempo. |

### Página + Optimización
| Agente | Qué hace |
|---|---|
| `vsl-landing` | Diseña la landing: Complejo del Play Rate (Headline + Autoplay + Vídeo de Fondo), escasez y urgencia legítima. |
| `vsl-mini-vsl-quiz` | Construye mini VSLs y quizzes (estructura Keps) para ofertas low-ticket. |
| `vsl-test-ab` | Metodología de tests A/B con relevancia estadística. |

---

## Skills compartidas (conocimiento de referencia)

Cualquier agente puede precargarlas. Son la "base de conocimiento" del masterclass.

| Skill | Contenido |
|---|---|
| `vsl-niveles-consciencia` | Los 5 niveles de Eugene Schwartz + qué tipo de Lead usar en cada uno. |
| `vsl-tipos-de-lead` | Los 6 tipos canónicos del libro Great Leads (Masterson + Forde). |
| `vsl-formula-bencivenga` | Beneficio + Credibilidad − Costo = Persuasión. |
| `vsl-direct-response-glossary` | Glosario: VSL, Lead, Microlead, Pitch, Loop, Mecanismo, Nutra USA, Info, etc. |

---

## Cómo se llaman entre sí

El padre `vsl-master` recibe la petición del usuario y, según lo que detecte, lanza uno o varios subagentes en paralelo o en secuencia.

Ejemplo: el usuario dice *"quiero una VSL completa para un suplemento de próstata en España"*.

1. `vsl-master` pregunta lo mínimo (nicho ✓, mercado ✓, falta: avatar, oferta, presupuesto)
2. Lanza en paralelo:
   - `vsl-detector-consciencia` → "Consciente del problema"
   - `vsl-info-nutra` → "Mejor empezar Info digital 17€ con VSL Nutra USA traducida"
   - `vsl-research-ads` → busca VSLs ganadoras en swipe files
3. Cuando tiene la estrategia, lanza secuencialmente:
   - `vsl-structure` → 15 pasos del VSL
   - `vsl-headline`, `vsl-microlead`, `vsl-lead`, `vsl-historia`, `vsl-mecanismo`, `vsl-cierre` (en paralelo)
   - `vsl-landing` → diseña la página
   - `vsl-test-ab` → plan de tests

---

## Filosofía

Este plugin **no inventa**. Cada agente está construido a partir del masterclass real impartido en español. Las recomendaciones siguen exactamente:

- Eugene Schwartz (Breakthrough Advertising)
- Michael Masterson + John Forde (Great Leads)
- Gary Bencivenga (fórmula Beneficio + Credibilidad − Costo)
- Joe Sugarman (el tobogán engrasado)
- Stephan Georgia (RMBC framework)
- Marconi Rômulo (módulo 02 VSL's Millonarias, fuente original)

---

## Licencia

MIT — usa, modifica, distribuye. Atribución apreciada.

**Autor:** Joseph Moreno
**Año:** 2026
