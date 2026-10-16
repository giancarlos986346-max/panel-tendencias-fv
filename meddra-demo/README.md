# MedDRA DEMO (ficticio)

**Estos archivos NO son MedDRA.** Son un diccionario ficticio y ligero con el mismo formato que los archivos ASCII oficiales (campos separados por `$`). Sirven solo para validar el flujo del módulo «Consultas MedDRA» del panel, sin publicar contenido licenciado.

No deben usarse para decisiones clínicas ni regulatorias.

## Qué contiene

| Archivo | Contenido |
|---|---|
| `meddra_release.asc` | Versión `99.0` (ficticia) e idioma |
| `llt.asc` | 332 LLT: los códigos de las RAM de los datos de prueba más 12 términos ficticios (`9000000x`) para el escenario de linfohistiocitosis hemofagocítica |
| `pt.asc` | 250 PT con códigos ficticios (`92xxxxxx`) |
| `hlt.asc`, `hlgt.asc`, `soc.asc` | Niveles superiores; HLT y HLGT ficticios (`93xxxxxx`, `94xxxxxx`) |
| `mdhier.asc` | Jerarquía PT → HLT → HLGT → SOC, con SOC primaria y secundarias |
| `smq_list.asc`, `smq_content.asc` | 11 SMQ de prueba (`2000xxxx`), todas llamadas «SMQ DEMO – …» |

Las SMQ de prueba cubren los distintos tipos:

- **Simple:** Linfohistiocitosis hemofagocítica; Reacciones adversas cutáneas graves (incluye un término a nivel LLT y uno inactivo).
- **Algorítmica:** Reacción anafiláctica, con categorías A/B/C/D y el algoritmo `A or (B and C) or (D and (B or C))`.
- **Jerárquicas:** Trastornos hepáticos relacionados con fármacos (2 sub-SMQ); Citopenias hematopoyéticas (4 sub-SMQ).

## Cómo lo usa el panel

El panel lee estos archivos desde la carpeta `meddra-demo/` del mismo sitio cuando se abre la pestaña «Consultas MedDRA». Funciona desde GitHub Pages o un servidor local; abriendo `index.html` con doble clic el navegador bloquea la lectura y el panel ofrece seleccionar los archivos `.asc` a mano.

Para usar el MedDRA oficial más adelante se sustituirán estos archivos por los de la suscripción, cargados de forma privada (nunca en un repositorio público).
