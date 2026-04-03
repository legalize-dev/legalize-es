# Legalize — Spain

> **Early stage** — This repository is under active development. File structure, commit history, and content may undergo significant changes, including full regeneration. Do not build tooling against the current layout without expecting breaking changes.
>
> **Fase inicial** — Este repositorio está en desarrollo activo. La estructura de archivos, el historial de commits y el contenido pueden sufrir cambios importantes, incluyendo regeneración completa. No construyas herramientas basándote en la estructura actual sin esperar cambios incompatibles.

Legislación española consolidada en Markdown, versionada con Git.

Cada ley es un fichero. Cada reforma es un commit.

Parte del proyecto [Legalize](https://github.com/legalize-dev/legalize) · [legalize.dev](https://legalize.dev)

## Estructura

```
es/                          ← legislación estatal
  BOE-A-1978-31229.md        — Constitución Española
  BOE-A-2015-11430.md        — Estatuto de los Trabajadores
  BOE-A-1889-4763.md         — Código Civil
  ...
es-ct/                       ← Cataluña
  BOE-A-2006-13087.md        — Estatuto de Autonomía de Cataluña
es-pv/                       ← País Vasco
  BOE-A-1979-30177.md        — Estatuto de Autonomía del País Vasco
...
```

El rango normativo (ley, real decreto, ley orgánica, etc.) va en el frontmatter YAML de cada fichero, no en la estructura de directorios.

## Fuente

Datos obtenidos de la API de datos abiertos del [BOE](https://www.boe.es/datosabiertos/) (Boletín Oficial del Estado), publicados por la [Agencia Estatal Boletín Oficial del Estado](https://www.boe.es/).

## Formato

Cada fichero contiene:

- **Frontmatter YAML**: metadatos (título, identificador, rango, fecha, estado jurídico, departamento, número oficial, diario)
- **Cuerpo Markdown**: texto consolidado con estructura jerárquica

Los commits usan la fecha histórica de publicación oficial en el BOE.

## Licencia

Los textos legislativos son de dominio público. La estructuración y el formato están bajo licencia [MIT](LICENSE).

---

Creado por [Enrique Lopez](https://enriquelopez.eu) · [legalize.dev](https://legalize.dev)
