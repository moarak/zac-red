# Red de procedencia: Álbum Zoila A. Cáceres y *Mujeres de ayer y de hoy*

Grafo dirigido, tipado y multipartito que vincula el álbum personal de Zoila Aurora
Cáceres (1872-1958) con los capítulos VIII-XV de *Mujeres de ayer y de hoy* (1909).

**67 nodos · 105 aristas · 6 tipos de nodo · 21 tipos de relación**

## Visualización

El grafo se abre directamente en Gephi Lite:

```
https://lite.gephi.org/?file=https://raw.githubusercontent.com/moarak/zac-red/refs/heads/main/data/zac_album_mujeres_piloto.json
```

## Contenido

| Archivo | Descripción |
|---|---|
| `data/zac_album_mujeres_piloto.gexf` | Grafo completo, formato GEXF 1.2 |
| `data/nodes.csv`, `data/edges.csv` | Tablas planas derivadas; no editar a mano |
| `lookup/autoridades.tsv` | Una fila por agente: forma canónica, fechas, QID de Wikidata |
| `lookup/variantes_personas.tsv` | Una fila por forma superficial atestiguada en las fuentes |
| `lookup/relaciones_vocabulario.tsv` | Definición y predicado PROV-O/CIDOC-CRM de cada tipo de relación |
| `lookup/colisiones_no_coincidencias.csv` | Registro de coincidencias descartadas |
| `revision_hipotesis.csv` | Las 16 aristas interpretativas, pendientes de revisión |

Los archivos de `lookup/` son la interfaz entre las decisiones interpretativas y el
código: toda corrección de criterio se hace ahí, no en los scripts.

## Tipos de nodo

`itemAlbum` (16) · `persona` (27) · `organización` (13) · `textoLibro` (6) ·
`publicación` (4) · `instrumento` (1)

El grano del lado libro es la sección cuando el capítulo tiene encabezados
(caps. XI-XIV) y el capítulo cuando no los tiene (caps. VIII, IX, X, XV).

## Estratos epistémicos

La columna `confianza` distingue dos clases de arista:

- **`confirmado`** (89): la fuente lo afirma explícitamente. No implica verificación
  histórica externa, sólo que el documento o el texto lo dice.
- **`hipótesis`** (16): afirmación interpretativa no verificada. Comprende las 15
  aristas de `derivación textual` —que postulan que un pasaje de 1909 se apoya en un
  ítem del álbum— y una vinculación institucional.

**Ninguna arista directa entre álbum y libro está confirmada.** Toda conexión
verificada entre las dos fuentes pasa por un nodo de agente. Suprimidas las personas
y organizaciones, el grafo se fragmenta por completo.

## Autoridades

31 de 52 agentes están anclados a Wikidata. Las formas canónicas siguen la autoridad,
no la grafía de Cáceres; las formas del libro se registran como variantes. Entre ellas
constan dos erratas del impreso de 1909: «Marcel Tinayre» por Marcelle Tinayre y
«Dihrenfurth» por Gertrud Dyhrenfurth.

## Advertencias de lectura

1. Los agrupamientos por capítulo reflejan el modelo de datos, no comunidades
   detectadas. No deben leerse como resultado del algoritmo de disposición.
2. La ausencia de aristas entre corresponsales no prueba que no se conocieran: no se
   buscaron vínculos entre ellas en fuentes externas al proyecto.
3. Las aristas del capítulo VIII registran lo que Cáceres afirma sobre las
   asociaciones alemanas, con cita de línea en `notaArista`. Su exactitud histórica es
   una verificación distinta y pendiente.

## Licencia

Datos: CC BY 4.0. Se ruega citar el proyecto y la edición de origen del texto de 1909.
