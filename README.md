# legalize-es

Legislación de España en formato Markdown, versionada como repositorio git.

Cada ley es un archivo; cada reforma es un commit con la fecha real de publicación oficial. El `git log` de cada ley te muestra su historia completa — cuándo se sancionó, qué artículos se modificaron y por qué norma.

Incluye el catálogo de legislación consolidada del BOE, sin corte de antigüedad, y disposiciones de la Sección I desde 2010 disponibles como texto original. Abarca normativa estatal y autonómica publicada por el BOE. Cada norma declara si su cuerpo es una versión histórica consolidada (point_in_time) o el texto original sin incorporar reformas posteriores (as_enacted). Las rutas por jurisdicción están declaradas en .legalize.yml.

## Qué contiene

- **Constitución** (`BOE-A-AAAA-N.md`) — `es/bb/BOE-A-1978-31229.md`
- **Ley orgánica** (`BOE-A-AAAA-N.md`) — Rango: ley_organica.
- **Ley** (`BOE-A-AAAA-N.md`) — `es/70/BOE-A-2015-11430.md`
- **Real Decreto-ley** (`BOE-A-AAAA-N.md`) — Rango: real_decreto_ley.
- **Real Decreto Legislativo** (`BOE-A-AAAA-N.md`) — `es/d9/BOE-A-1996-8930.md`
- **Real Decreto** (`BOE-A-AAAA-N.md`) — Rango: real_decreto.
- **Otros rangos estatales** (`BOE-A-AAAA-N.md`) — Orden, Resolución, Circular, Instrucción, Acuerdo, Decreto, Acuerdo internacional.
- **Normativa autonómica (foral/regional)** (`es-XX/XX/BOE-A-AAAA-N.md`) — Leyes y decretos de comunidades autónomas, ubicados en directorios por jurisdicción ELI (es-pv, es-ct, es-ga, etc.). Incluye rangos forales: ley foral, decreto legislativo, decreto-ley, decreto-ley foral, decreto foral legislativo.

## Fuente de los datos

- **BOE — Agencia Estatal Boletín Oficial del Estado**
  - Portal: https://www.boe.es
  - Datos abiertos (API): https://www.boe.es/datosabiertos
  - Legislación consolidada: https://www.boe.es/legislacion/legislacion_ava.php
  - Condiciones de reutilización / Aviso legal: https://www.boe.es/informacion/aviso_legal/index.php

## Atribución

> Fuente de los datos: Agencia Estatal Boletín Oficial del Estado (https://www.boe.es). Datos reutilizados conforme a las condiciones de reutilización del BOE (Resolución de 27 de junio de 2024). Este repositorio es una obra derivada basada en datos de la Agencia Estatal Boletín Oficial del Estado.

## Estructura de ficheros

Un directorio por ámbito (es/ para el Estado; es-XX/ por comunidad autónoma según código ELI), dividido en subdirectorios con los dos primeros caracteres del SHA-1 del identificador. El manifiesto .legalize.yml declara la ruta de cada norma. El rango figura en el frontmatter YAML.

## Limitaciones

Texto consolidado de carácter meramente informativo. El historial refleja las versiones proporcionadas por el BOE; puede no incluir redacciones anteriores que la fuente no exponga. El texto se transforma a Markdown; se conservan referencias a imágenes oficiales, sin copiar activos binarios. Las tablas anidadas se representan como HTML para preservar sus celdas. Las fechas de publicación y de entrada en vigor se distinguen: Source-Date fecha la publicación del acto, y last_updated la entrada en vigor de la redacción incluida. Si una publicación tiene varias fases de entrada en vigor, cada fase conserva su propio commit y Effective-Date. Cuando el BOE no declara la fecha de vigencia de un bloque, last_updated se omite y extra.effective_date_unknown_blocks identifica la incertidumbre. Los actos sin consolidación conservan su cuerpo original y registran las reformas conocidas sin inventar texto consolidado. Se excluyen actos judiciales, correcciones como documentos independientes y publicaciones dominadas por imágenes; las exclusiones se registran durante la descarga.

## Otros países

Este repositorio es parte del proyecto **Legalize**, que mantiene legislación de múltiples países como repos git. Ver https://legalize.dev para el catálogo completo.

## Apoyar

Legalize es libre y abierto. Si este trabajo te resulta útil, puedes ayudar a sostener su alojamiento y desarrollo: [Apoya este proyecto](https://buymeacoffee.com/legalizedev).

## Licencia

- **Código del pipeline**: MIT (https://github.com/legalize-dev/legalize-pipeline)
- **Datos**: Condiciones de reutilización del BOE — cita obligatoria de la fuente
