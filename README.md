# LISTA DE TAREAS JDC

LISTA DE TAREAS JDC es un remix comunitario del plugin de Obsidian [Task List Kanban](https://github.com/ErikaRS/task-list-kanban). Mantiene el flujo de tareas Markdown del proyecto original y adapta la experiencia a una interfaz bilingüe Español/Inglés, con subtareas anidadas, filtros, panel de listas, columnas pensadas para revisión y seguimiento, y un sistema completo de normas para orquestación de agentes de inteligencia artificial.

Este repositorio publica únicamente el paquete limpio del plugin. No incluye datos personales, capturas ni configuración local.

---

## Funciones Principales

- **Interfaz bilingüe completa**: Selector `Language` con opciones exactas `Español` y `English`.
- **Soporte Multi-Agente de IA y Generador de `AGENTS.md`**: Genera normas universales de trabajo autónomo (jerarquía CEO/Dubby, compuerta de rol, comando `/objetivo`, ciclo de vida de tareas `T-###`, agentes persistentes y validación empírica sin inventar datos).
- **Ruta Libre y Selector Nativo de Carpetas**: Generación de `AGENTS.md` en cualquier directorio de tu ordenador (con botón nativo `Examinar PC...` en Windows) o dentro de la bóveda (`Examinar Bóveda...`).
- **Índice Automático de Tareas (`T-###`)**: Asignación correlativa automática al crear tareas (en modal y en columnas Kanban). Prefijo configurable, número base/inicio ajustable, botón interactivo para **detectar la última tarea existente en las notas** y autoincremento automático que previene duplicados o desajustes por parte de la IA o el usuario.
- **Control de Tamaño de Texto y Escalado Proporcional de Etiquetas**: Deslizador interactivo en el menú *Vista* para regular el tamaño de fuente (10px - 20px) en tiempo real con persistencia. Las etiquetas (`#TAG`, `#PRIORIDAD_ALTA`) escalan proporcionalmente de forma compacta.
- **Tablero Optimizado**: Vista despejada que arranca limpia desde el borde izquierdo sin superposiciones ni columnas fantasma.
- **Tareas Markdown nativas**: Las tareas residen directamente en los archivos Markdown del usuario, sin base de datos externa ni formatos propietarios.
- **Subtareas anidadas visibles**: Las subtareas con casillas de verificación `- [ ]` y `- [x]` se muestran de forma jerárquica dentro de la tarjeta principal.
- **Columnas oficiales de flujo continuo**: `PENDIENTES`, `PARA AUDITAR`, `NO FUNCIONA DESCARTADO` y `COMPLETADO Y VALIDADO`.
- **`Uncategorized` oculto por defecto**: Diseñado para una lectura limpia de los tableros Kanban.

---

## Tutorial: Cómo Orquestar Agentes de IA con un CEO y Agentes Dubby Persistentes

`LISTA DE TAREAS JDC` incluye un motor de generación de normas operativas de nivel industrial (`AGENTS.md`) para trabajar con herramientas de IA como Codex, Antigravity, Claude Code, Cursor u otros agentes autónomos.

### Paso 1: Generar `AGENTS.md` desde la Configuración
1. Abre Obsidian y ve a **Ajustes** (`Settings`) > **LISTA DE TAREAS JDC**.
2. Desplázate hasta la sección **Generar AGENTS.md de Codex**.
3. Haz clic en el botón **Generar Agents.md**.
4. En el diálogo emergente, selecciona la ruta de destino:
   - Haz clic en **Examinar PC...** si deseas colocar la norma en cualquier carpeta o proyecto de tu ordenador fuera de la bóveda.
   - O haz clic en **Examinar Bóveda...** para elegir una carpeta interna de tu bóveda de Obsidian.
5. Pulsa **Generar AGENTS.md de Codex**. El plugin creará automáticamente la norma canónica con:
   - Definición del rol **CEO** y compuerta de rol (*Role Gate*).
   - Protocolo de carriles persistentes **Dubby** (hasta 10 carriles continuos, no desechables).
   - Tabla de registro de `ThreadId` / `ConversationId` para invocar a cada agente sin perder contexto.
   - Formato obligatorio de informes de entrega con evidencias empíricas (comandos, códigos de salida, hashes y pruebas).
   - Comando formal `/objetivo`.
   - Flujo de estados en el tablero Kanban.

---

### Paso 2: Inicializar la IA como CEO Orquestador
Abre tu terminal, entorno de desarrollo o chat de IA en la carpeta del proyecto donde se generó `AGENTS.md`, y envíale el siguiente prompt inicial:

```text
Lee atentamente el archivo AGENTS.md de la raíz de este proyecto. Compórtate como el CEO orquestador de este proyecto. Inicializa el equipo de agentes Dubby persistentes, anota sus ConversationId / ThreadId en la tabla de registro de AGENTS.md, y comienza a estructurar y coordinar las tareas del tablero LISTA DE TAREAS.md respetando rigurosamente la compuerta de rol (Role Gate) y el protocolo /objetivo.
```

---

### Paso 3: Flujo de Asignación con el Protocolo `/objetivo`
1. **El CEO no ejecuta trabajo técnico**: El CEO planifica la arquitectura, crea las tarjetas `T-###` en `PENDIENTES` y asigna cada tarea técnica a un agente ejecutor Dubby.
2. **Encargo formal**: Toda orden de trabajo hacia un Dubby debe iniciarse obligatoriamente con la directiva literal `/objetivo`:
   ```text
   /objetivo
   La tarea es T-001 y está en LISTA DE TAREAS.md
   Resultado exigido: Implementar la función de hashing y sus pruebas unitarias.
   Subtareas y evidencias esperadas:
     - [ ] Crear src/hash.js
     - [ ] Ejecutar node test.js (Exit code: 0)
   Archivos autorizados: src/hash.js, test.js
   Límites: Solo lectura en el resto del proyecto.
   ```

---

### Paso 4: Trabajo Persistente del Dubby y Formato de Informe
- Los agentes Dubby **no son de usar y tirar**: conservan su memoria, contexto e historial de ejecución en su propio carril persistente.
- El Dubby marca sus subtareas completadas (`- [x]`) en la tarjeta del tablero.
- Al finalizar, el Dubby traslada la tarea a la columna `PARA AUDITAR` y remite su informe estructurado al CEO:

```markdown
### INFORME DE AVANCE / ENTREGA — [Dubby_1]
- **Tarea**: T-001 — Hashing y tests unitarios
- **Estado**: PARA AUDITAR
- **Subtareas Marcadas**:
  - [x] Crear src/hash.js
  - [x] Ejecutar tests unitarios
- **Archivos Modificados / Creados**: `src/hash.js`, `test.js`
- **Evidencias Técnicas**: `node test.js` completado con Exit code 0 (12 pruebas superadas).
- **Bloqueos o Límites**: Ninguno.
- **Siguiente Acción Requerida**: Auditoría y validación por CEO.
```

---

### Paso 5: Auditoría Empírica y Cierre
- El CEO inspecciona las evidencias de la columna `PARA AUDITAR`.
- **Si la auditoría es satisfactoria**: El CEO traslada la tarjeta a `COMPLETADO Y VALIDADO`.
- **Si se detectan fallos**: El CEO devuelve la tarjeta a `PENDIENTES` y reactiva al **mismo Dubby** (usando su `ThreadId` registrado en la tabla) enviándole la solución y contexto técnico con `/objetivo`.

---

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

*Nota: No copies `data.json` de otra bóveda. Obsidian genera automáticamente la configuración local correspondiente.*

---

## Uso Básico

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

---

## Créditos

LISTA DE TAREAS JDC es un remix de [Task List Kanban](https://github.com/ErikaRS/task-list-kanban), creado originalmente por Chris Kerr y mantenido por Erika Rice Scherpelz.

El proyecto original usa licencia MIT. Este remix conserva la atribución original y añade la atribución de ELUNIVERSODEJDC en `NOTICE`.

---

## English

LISTA DE TAREAS JDC is a community remix of the Obsidian plugin [Task List Kanban](https://github.com/ErikaRS/task-list-kanban). It keeps the original Markdown task workflow and adapts the experience with a bilingual Spanish/English interface, nested subtasks, filters, a list panel, side-by-side review columns, and an integrated autonomous AI multi-agent orchestration system.

This repository publishes only the clean plugin package. It does not include personal data, screenshots, or local settings.

### Main Features

- **Full Bilingual Interface**: `Language` selector supporting both `Español` and `English`.
- **AI Multi-Agent Support & Universal `AGENTS.md` Generator**: Generates universal autonomous operating rules (CEO/Dubby hierarchy, Role Gate, `/objetivo` command, `T-###` task lifecycle, persistent threads, and strict empirical validation).
- **Free Destination Path & Native Folder Picker**: Generate `AGENTS.md` in any PC directory (`Browse PC...` native Windows dialog) or within the vault (`Browse Vault...`).
- **Automatic Task Indexing (`T-###`)**: Automatic sequential task ID prefixing when creating cards (both in modal and inline column inputs). Fully configurable prefix and start counter, with a one-click button to **detect the highest existing task in notes** and automatic counter incrementing to avoid AI or user collision.
- **Font Size Controls & Proportional Tag Scaling**: Interactive slider in the *View* menu (10px - 20px) with live scaling and persistence. Tags (`#TAG`, `#PRIORIDAD_ALTA`) automatically scale down compactly and proportionally.
- **Clean Board Layout**: Zero ghost columns or floating overlays, starting flush from the left margin.
- **Native Markdown Tasks**: Tasks live directly within the user's Markdown notes.
- **Nested Subtasks**: Checkboxes `- [ ]` and `- [x]` rendered hierarchically inside parent task cards.
- **Review Columns**: `PENDIENTES`, `PARA AUDITAR`, `NO FUNCIONA DESCARTADO`, and `COMPLETADO Y VALIDADO`.
- **`Uncategorized` Hidden by Default**: Produces a clutter-free Kanban board.

---

### Tutorial: Multi-Agent AI Orchestration with a CEO and Persistent Dubbys

`LISTA DE TAREAS JDC` includes an industrial-grade rule generator (`AGENTS.md`) designed for autonomous multi-agent environments such as Codex, Antigravity, Claude Code, Cursor, and custom CLI agents.

#### Step 1: Generate `AGENTS.md` from Settings
1. Open Obsidian and go to **Settings** > **LISTA DE TAREAS JDC**.
2. Scroll to the **Generate Codex AGENTS.md** section.
3. Click the **Generate Agents.md** button.
4. Select your destination directory:
   - Click **Browse PC...** to place the file in any folder or external project on your computer.
   - Or click **Browse Vault...** to select a folder within your active Obsidian vault.
5. Click **Generate Codex AGENTS.md**. The plugin creates a comprehensive ruleset containing:
   - CEO orchestrator definitions and Role Gate enforcement.
   - Persistent Dubby worker lanes (up to 10 threads, non-disposable).
   - `ThreadId` / `ConversationId` tracking registry table.
   - Standard progress/delivery reporting format with mandatory technical evidence.
   - Mandatory `/objetivo` task assignment directive.

#### Step 2: Initialize the AI as Project CEO
Open your terminal, AI assistant, or agent framework in the project folder and send this initial prompt:

```text
Read AGENTS.md in the root of this project carefully. Act as the orchestrating CEO for this project. Initialize the persistent Dubby agent team, register their ConversationId / ThreadId in the AGENTS.md tracking table, and coordinate tasks on the LISTA DE TAREAS.md board strictly following the Role Gate and the /objetivo protocol.
```

#### Step 3: Task Delegation via `/objetivo`
The CEO never executes assigned technical tasks directly. Instead, the CEO structures tasks as `T-###` in `PENDIENTES` and delegates them to Dubbys using the `/objetivo` command:

```text
/objetivo
The task is T-001 located in LISTA DE TAREAS.md
Required outcome: Implement hashing utility with unit tests.
Subtasks & expected evidence:
  - [ ] Create src/hash.js
  - [ ] Run node test.js (Exit code: 0)
Authorized files: src/hash.js, test.js
Limits: Read-only for other files.
```

#### Step 4: Persistent Dubby Execution & Delivery Reports
Dubby workers retain execution history across sessions. When done, Dubby moves the card to `PARA AUDITAR` and sends a structured report with technical proofs (exit code, test logs, hashes).

#### Step 5: CEO Audit and Completion
The CEO audits the submission. If verified with empirical evidence, the CEO moves the task to `COMPLETADO Y VALIDADO`. If issues are found, the CEO returns the card to `PENDIENTES` and reactivates the same Dubby (via its saved `ThreadId`) with corrective guidance.

---

### Package Contents

- `main.js`
- `manifest.json`
- `styles.css`
- `versions.json`
- `README.md`
- `LICENSE`
- `NOTICE`
