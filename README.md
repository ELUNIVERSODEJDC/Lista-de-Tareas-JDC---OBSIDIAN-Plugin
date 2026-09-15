# LISTA DE TAREAS JDC

LISTA DE TAREAS JDC es un remix comunitario del plugin de Obsidian [Task List Kanban](https://github.com/ErikaRS/task-list-kanban). Mantiene el flujo de tareas Markdown del proyecto original y adapta la experiencia a una interfaz bilingüe Español/Inglés, con subtareas anidadas, filtros, panel de listas y columnas pensadas para revisión y seguimiento.

Este repositorio publica únicamente el paquete limpio del plugin. No incluye datos personales, capturas ni configuración local.

## Funciones Principales

- Interfaz bilingüe con selector `Language` y opciones exactas `Español` y `English`.
- **Soporte Multi-Agente de IA y Generador de `AGENTS.md`**: Genera normas universales de trabajo autónomo (jerarquía CEO/Dubby, compuerta de rol, comando `/objetivo`, ciclo de vida de tareas `T-###` y validación empírica sin inventar datos).
- **Ruta Libre y Selector Nativo**: Generación de `AGENTS.md` en cualquier directorio de tu ordenador (con botón nativo `Examinar PC...`) o dentro de la bóveda (`Examinar Bóveda...`).
- **Control de Tamaño de Texto en Vista**: Deslizador interactivo en el menú *Vista* para regular el tamaño de fuente (10px - 20px) en tiempo real con persistencia.
- **Tablero Optimizado**: Vista despejada que arranca limpia desde el borde izquierdo sin superposiciones ni columnas fantasma.
- Tareas Markdown dentro de las notas del usuario, sin base de datos externa.
- Subtareas anidadas visibles dentro de la tarea principal.
- Panel de listas para abrir y gestionar vistas de tareas.
- Filtros, contadores, menús, modales y ajustes adaptados al remix JDC.
- Columnas lado a lado para flujos de revisión (`PENDIENTES`, `PARA AUDITAR`, `NO FUNCIONA DESCARTADO`, `COMPLETADO Y VALIDADO`).
- `Uncategorized` oculto por defecto para una lectura más limpia.

## Instalación Manual

1. Descarga los tres archivos del paquete desde la [página de Releases](https://github.com/ELUNIVERSODEJDC/Lista-de-Tareas-JDC---OBSIDIAN-Plugin/releases):
   - `main.js`
   - `manifest.json`
   - `styles.css`
2. Crea esta carpeta dentro de tu bóveda de Obsidian:

```text
.obsidian/plugins/lista-de-tareas-jdc/
```

3. Copia los tres archivos dentro de esa carpeta.
4. Abre Obsidian.
5. Entra en `Ajustes > Complementos comunitarios`, recarga los complementos si hace falta y activa `LISTA DE TAREAS JDC`.

No copies `data.json` de otra bóveda. Obsidian crea la configuración local de cada bóveda.

## Uso

Abre la vista del plugin desde Obsidian y trabaja sobre tareas Markdown normales. El plugin lee las tareas de tus notas y permite revisar, editar, completar y organizar tareas sin sacar el contenido de la bóveda.

Para cambiar el idioma de la interfaz:

```text
Ajustes > LISTA DE TAREAS JDC > Language
```

Selecciona `Español` o `English`.

Para crear una nueva lista, usa el comando de Obsidian:

```text
Nueva lista de tareas JDC
```

También puedes abrir el panel de listas desde el plugin para localizar y gestionar tus tableros.

## Créditos

LISTA DE TAREAS JDC es un remix de [Task List Kanban](https://github.com/ErikaRS/task-list-kanban), creado originalmente por Chris Kerr y mantenido por Erika Rice Scherpelz.

El proyecto original usa licencia MIT. Este remix conserva la atribución original y añade la atribución de ELUNIVERSODEJDC en `NOTICE`.

## English

LISTA DE TAREAS JDC is a community remix of the Obsidian plugin [Task List Kanban](https://github.com/ErikaRS/task-list-kanban). It keeps the original Markdown task workflow and adapts the experience with a bilingual Spanish/English interface, nested subtasks, filters, a list panel, and side-by-side columns for review workflows.

This repository publishes only the clean plugin package. It does not include personal data, screenshots, or local settings.

### Main Features

- Bilingual interface with a `Language` selector and exact options `Español` and `English`.
- **AI Multi-Agent Support & Universal `AGENTS.md` Generator**: Generates universal autonomous workflow rules (CEO/Dubby hierarchy, role gate, `/objetivo` command, `T-###` task lifecycles, and strict empirical validation).
- **Free Destination Path & Native Folder Picker**: Generate `AGENTS.md` in any PC directory (`Browse PC...` native Windows dialog) or within the vault (`Browse Vault...`).
- **Interactive Font Size Slider**: Dynamically adjust board font size (10px - 20px) from the *View* menu with live scaling and persistence.
- **Clean Board Layout**: Zero ghost columns or floating overlays, starting flush from the left margin.
- Markdown tasks remain inside the user's notes.
- Nested subtasks shown inside their parent task.
- List panel for opening and managing task views.
- Filters, counters, menus, modals, and settings adapted for the JDC remix.
- Side-by-side columns for review and tracking (`PENDIENTES`, `PARA AUDITAR`, `NO FUNCIONA DESCARTADO`, and `COMPLETADO Y VALIDADO`).
- `Uncategorized` hidden by default for a cleaner board.

### Manual Installation

1. Download the three package files from the [Releases page](https://github.com/ELUNIVERSODEJDC/Lista-de-Tareas-JDC---OBSIDIAN-Plugin/releases):
   - `main.js`
   - `manifest.json`
   - `styles.css`
2. Create this folder inside your Obsidian vault:

```text
.obsidian/plugins/lista-de-tareas-jdc/
```

3. Copy the three files into that folder.
4. Open Obsidian.
5. Go to `Settings > Community plugins`, reload plugins if needed, and enable `LISTA DE TAREAS JDC`.

Do not copy `data.json` from another vault. Obsidian creates local plugin settings for each vault.

To change the interface language:

```text
Settings > LISTA DE TAREAS JDC > Language
```

Choose `Español` or `English`.

To create a new board, use the Obsidian command:

```text
New task list JDC
```

## Package Contents

- `main.js`
- `manifest.json`
- `styles.css`
- `versions.json`
- `README.md`
- `LICENSE`
- `NOTICE`

Local vault settings are intentionally not part of the public package.
