---
clase: 00
titulo: Índice del conocimiento del masterclass
fuente: Masterclass VSL de Joseph Moreno · adaptado al español de España
---

# Índice del conocimiento

Este directorio contiene el masterclass completo de VSL de Joseph Moreno en markdown limpio. Cada archivo es la transcripción depurada de una clase del masterclass original. Los agentes del plugin (`vsl-master`, `vsl-microlead`, `vsl-lead`, etc.) leen estos archivos on-demand cuando necesitan profundizar en un tema concreto.

## Archivos disponibles

| Clase | Archivo | Tema principal | Agentes que la usan |
|---|---|---|---|
| 01 | [01-fundamentos.md](01-fundamentos.md) | Fundamentos del copywriting de Direct Response | vsl-master, vsl-psicologia |
| 02 | [02-metodo-practico.md](02-metodo-practico.md) | Método práctico de trabajo | vsl-microlead, vsl-headline |
| 03 | [03-arsenal-formatos.md](03-arsenal-formatos.md) | Arsenal de formatos de microlead | vsl-microlead |
| 04 | [04-anatomia-lead.md](04-anatomia-lead.md) | Anatomía del Lead + 6 tipos canónicos | vsl-lead, vsl-detector-consciencia |
| 05 | [05-construccion-leads.md](05-construccion-leads.md) | Construcción de leads | vsl-lead, vsl-historia |
| 06 | [06-taller-lead.md](06-taller-lead.md) | Taller práctico de Leads | vsl-lead |
| 07 | [07-reglas-dr.md](07-reglas-dr.md) | Reglas operativas del Direct Response | vsl-master, vsl-research-trends, vsl-research-ads |
| 08 | [08-cierre-agresivo.md](08-cierre-agresivo.md) | Cierre agresivo + post-pitch | vsl-cierre, vsl-post-pitch |
| 09 | [09-info-vs-nutra.md](09-info-vs-nutra.md) | Info vs Nutra + estrategia España | vsl-info-nutra |
| 10 | [10-paginas-agresivas.md](10-paginas-agresivas.md) | Landings agresivas | vsl-landing |
| 11 | [11-mini-vsl-quiz.md](11-mini-vsl-quiz.md) | Mini VSLs + quiz funnels | vsl-mini-vsl-quiz |
| 12 | [12-headlines.md](12-headlines.md) | Headlines de VSL | vsl-headline |
| 13 | [13-complejo-play-rate.md](13-complejo-play-rate.md) | Complejo del Play Rate | vsl-landing |
| 14 | [14-psicologia-vsl.md](14-psicologia-vsl.md) | Psicología del VSL | vsl-psicologia, vsl-historia, vsl-mecanismo |
| 15 | [15-sistema-optimizacion.md](15-sistema-optimizacion.md) | Sistema de optimización + tests A/B | vsl-test-ab |
| 16 | [16-biblia-del-mecanismo.md](16-biblia-del-mecanismo.md) | ⭐ La Biblia del Mecanismo (131 formaciones · 4 capas · mecanismo problema/solución · causa raíz · objeto brillante · nombre chicle · mito de origen · 50+ ejemplos) | vsl-mecanismo, vsl-lead, vsl-historia, vsl-headline, vsl-microlead, vsl-cierre, vsl-post-pitch |
| 17 | [17-mecanismo-en-la-vsl.md](17-mecanismo-en-la-vsl.md) | ⭐ Mapa pieza → paso de la VSL (dónde colocar cada pieza si el usuario trae su oferta · intake OPCIONAL) | vsl-mecanismo, vsl-lead, vsl-historia, vsl-headline, vsl-microlead, vsl-cierre, vsl-post-pitch |

## Cómo lo usan los agentes

Cada agente tiene en su system prompt una referencia a los archivos relevantes. Cuando necesita profundizar (por ejemplo, recordar un ejemplo exacto, un % concreto, un nombre de framework), llama a `Read` sobre el archivo correspondiente.
