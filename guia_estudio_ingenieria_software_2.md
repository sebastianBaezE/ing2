# Guía de Estudio Unificada — Ingeniería de Software II

> Construida a partir del análisis conjunto de **7 finales completos** + un **compilado de 37 preguntas** de finales de la cátedra. El criterio de organización es **pedagógico** (sigue el ciclo de vida del software y las dependencias entre temas), pero la profundidad de cada tema está calibrada según su **frecuencia real** en los exámenes. El plan de estudio del final reordena todo por prioridad de repaso.

---

## 1. Análisis de Frecuencia

Conteo sobre los 7 finales analizados (E1 = "final" suelto; E2 = 24/4/2013; E3 = lasaña; E4 = P-CMM/excavación; E5 = 6/2/13 completo; E6 = 11/2/2015 reducido; E7 = empresa de fletes 4-9-24).

| Tema | Apariciones | En qué finales | Clasificación |
|------|:-----------:|----------------|---------------|
| **Gestión de Configuración (GCS) / Línea base** | 6 | E1, E2, E3, E4, E5, E7 | 🔴 Muy frecuente |
| **PERT / CPM / Camino crítico** | 5 | E2, E3, E4, E5, E7 | 🔴 Muy frecuente |
| **Gestión de riesgos** (definición, características, clasificación, estrategias, línea de corte) | 5 | E1, E4, E5, E6, E7 | 🔴 Muy frecuente |
| **Diseño arquitectónico / Organización del sistema** (Repositorio vs Cliente-Servidor) | 5 | E1, E2, E4, E5, E7 | 🔴 Muy frecuente |
| **Rejuvenecimiento del software** (reingeniería) | 4 | E1, E3, E5, E6 | 🔴 Muy frecuente |
| **Verificación y Validación / Pruebas de integración** | 3 | E3, E4, E7 | 🟠 Frecuente |
| **Interfaz de usuario** (Nielsen, Recuperabilidad, consideraciones de UI) | 3 | E1, E5, E7 | 🟠 Frecuente |
| **Problema de las 4 P / ¿Qué es un proyecto?** | 2–3 | E2, E3 | 🟠 Frecuente |
| **Tipos / áreas de diseño de software** | 2 | E3, E4 | 🟠 Frecuente |
| **Principios de diseño** | 2 | E1, E2 | 🟠 Frecuente |
| Cohesión y acoplamiento | 1 | E6 | 🟡 Poco frecuente (pero fundamental) |
| Elementos clave de la gestión de proyectos | 1 | E2 | 🟡 Poco frecuente |
| Técnicas de estimación | 1 | E5 | 🟡 Poco frecuente |
| Modelo MOI | 1 | E2 | 🟡 Poco frecuente |
| P-CMM | 1 | E4 | 🟡 Poco frecuente |
| Estructura de equipos / factores | 1 | E7 | 🟡 Poco frecuente |
| Planificación temporal (seguimiento y control) | 1 | E3 | 🟡 Poco frecuente |
| Tipos de planificación organizacional | 1 | E1 | 🟡 Poco frecuente |

**Lectura clave del cuadro:** cinco temas (GCS, PERT, Riesgos, Arquitectura, Rejuvenecimiento) concentran casi toda la evaluación. Dominar esos cinco te permite responder, en promedio, **5 de las 7 preguntas** de cualquier final de esta cátedra.

### Actualización: segunda fuente incorporada (rejunte de 37 preguntas)

Se sumó un **compilado de 37 preguntas** de finales (que agrega varios exámenes, con solapamiento respecto de los 7 anteriores). No cambia el núcleo —**GCS, PERT, riesgos, arquitectura y mantenimiento vuelven a aparecer y se confirman como los dominantes**— pero **agrega temas nuevos** y **sube de categoría** a otros.

**Temas NUEVOS detectados (no estaban en los 7 finales):**

| Tema nuevo | Dónde aparece | Clasificación | Se desarrolla en |
|---|---|---|---|
| **Métricas e indicadores** (proceso/producto, objetivas/subjetivas, tempranas/post-mortem) | Q1, Q29 | 🟠 Frecuente (emergente) | Bloque B′ |
| **Tipos de mantenimiento** (correctivo, adaptativo, perfectivo, preventivo) | Q34 | 🟠 Frecuente | G.1 |
| **Barrera del mantenimiento** | Q37 | 🟡 Poco frecuente | G.1 |
| **RNF afectados por la arquitectura** | Q2 | 🟡 Poco frecuente | D.4 |
| **Ítems de mayor riesgo según Boehm (Top 10)** | Q3 | 🟡 Poco frecuente | C.3 |
| **Técnicas de validación** (estáticas vs dinámicas) | Q33 | 🟠 Frecuente | Bloque E |

**Reclasificaciones (el rejunte les da más peso):**
- **Cohesión y acoplamiento** sube de 🟡 a **🟠 Frecuente**: aparece 3 veces en el compilado (Q32 "cohesión funcional y grados", Q35, y dentro de Q32 los fundamentos del diseño).
- **Verificación y Validación** se refuerza (Q20, Q27, Q33, Q36): caja blanca/negra con ejemplos e integración son recurrentes.
- **Mantenimiento** (con rejuvenecimiento, Q6/Q21/Q34/Q37) queda claramente entre los **muy frecuentes**.
- **PERT** se confirma de forma rotunda: solo en el compilado hay **3 ejercicios** (Q7, Q22, Q30).

> Nota metodológica: el compilado es una lista de preguntas (no exámenes completos), así que para los temas nuevos uso "frecuente / poco frecuente" según cuántas veces aparece la consigna en el banco, no un conteo sobre 7 exámenes.

### Corrección con las diapositivas oficiales de la cátedra (2024)

Tras contrastar la guía con el **deck oficial** (525 láminas, 2024), ajusté varios puntos a **lo que efectivamente enseña la cátedra** (base **Pressman 7ª/9ª**, con **Sommerville** y **Pfleeger**). Cambios principales:

- **"Tipos de planificación organizacional"** → es la **planificación organizativa** (organización del *personal*, el activo más importante). Sus *tipos* son los **4 paradigmas organizacionales del equipo**: **cerrado, abierto, síncrono y aleatorio** (B.1). *(Antes había puesto una interpretación genérica; queda corregido.)*
- **Liderazgo** → la cátedra **no usa el "modelo MOI"**; enseña las **5 prácticas de líderes ejemplares** (modelar el camino, inspirar una visión compartida, desafiar el proceso, permitir que otros actúen, alentar) y al gerente que "planifica, motiva, organiza y controla" (A.3). Dejé MOI como nota para finales viejos.
- **Interfaz de usuario** → se enseña con **Pressman**: **reglas doradas de Mandel** (dar control al usuario, reducir la carga de memoria, consistencia) + **factores humanos** + **usabilidad** + las **10 heurísticas de Nielsen** (en la numeración de la cátedra). La lámina "6 principios de interfaz" es en realidad el **proceso de diseño de UI en 6 pasos** (D.6).
- **Recuperabilidad** → no figura como "principio" con ese nombre en el deck; la reencuadré como **principio/atributo de recuperarse de errores y fallas**, presente vía "deshacer/interrumpir" (Mandel) y copias de seguridad / pruebas de recuperación (D.5).
- **Boehm** → la cátedra lo cita como *"identificar y supervisar los 10 riesgos más altos"* (los que quedan por encima de la línea de corte), **no** como una lista fija de ítems (C.3).
- **Rejuvenecimiento** → los **4 tipos** según la cátedra (Pfleeger): **re-documentación, re-estructuración, ingeniería inversa y re-ingeniería** (G.2).
- **Métricas** → la cátedra profundiza en **LDC/KLDC** (productividad, calidad, costo), **Punto Función (Albrecht)** y métricas **postmortem**; suele haber **ejercicio de cálculo** (B′).

---

## 2. Temas Más Importantes (síntesis)

1. **GCS y línea base** — el tema más repetido. Casi siempre piden el *proceso* o la *definición de línea base con ejemplo*.
2. **PERT / camino crítico** — el ejercicio práctico aparece en casi todos los finales (suele ser la pregunta 6 o 7).
3. **Riesgos** — qué es, características, clasificación, y estrategias de tratamiento + línea de corte.
4. **Diseño arquitectónico** — organización del sistema, casi siempre comparando **Repositorio vs Cliente-Servidor**.
5. **Rejuvenecimiento del software** — definición y tipos (reingeniería, ingeniería inversa, reestructuración, etc.).

Estos cinco son el núcleo. Todo lo demás (V&V, UI, 4P, diseño, estimación) es complemento de alto valor que aparece de forma rotativa.

---

## 3. Desarrollo Completo de los Temas

> Orden pedagógico: recorremos el ciclo de vida. Gestión y personas → planificación y riesgos → diseño (conceptos, arquitectura, UI) → verificación → configuración → mantenimiento. La profundidad es proporcional a la frecuencia.

---

### BLOQUE A — Gestión de Proyectos (marco general)

#### A.1. ¿Qué es un proyecto? El problema de las 4 P 🟠

**Definición.** Un *proyecto de software* es un esfuerzo temporal, con principio y fin, orientado a crear un producto de software bajo restricciones de alcance, tiempo y costo. Pressman organiza la gestión de proyectos alrededor de **cuatro "P"**: **Personas, Producto, Proceso y Proyecto**.

**Objetivo.** Dar un marco para *gestionar* el desarrollo y reducir la probabilidad de que el proyecto fracase (entregue tarde, sobre presupuesto o sin calidad).

**Problema que resuelve.** La industria del software tiene una alta tasa de proyectos "en problemas". Las 4 P obligan a no concentrarse solo en lo técnico y a atender los factores humanos, de alcance y de proceso que suelen ser la causa real del fracaso.

**Conceptos clave (las 4 P):**
- **Personas (People):** el factor más importante. Stakeholders, equipo, líderes. Se gestiona con modelos de madurez del personal (**P-CMM**) y de liderazgo (**MOI**).
- **Producto (Product):** *qué* se construye. Antes de planificar hay que definir **objetivos y alcance**, considerar soluciones alternativas y restricciones.
- **Proceso (Process):** el *marco de actividades* (framework) que da estructura al trabajo (comunicación, planeación, modelado, construcción, despliegue).
- **Proyecto (Project):** *cómo* se planifica, organiza, controla y monitorea el esfuerzo para evitar el fracaso.

**Ventajas / desventajas del enfoque.** Ventaja: visión integral (no solo código). Desventaja: es un marco conceptual, no una receta; requiere criterio para aplicarlo a cada caso.

**Relación con otros temas.** "Personas" enlaza con **MOI** y **P-CMM**; "Producto" con **estimación**; "Proceso" con los modelos de proceso; "Proyecto" con **planificación temporal, PERT y riesgos**.

**Ejemplo.** En E7 (fletes), Leandro piensa la *estructura del equipo* (Personas), el sitio web 24×7 define el *Producto*, y la decisión de controlar cambios define cómo se *gestiona el Proyecto*.

**Posibles preguntas de examen.**
- "¿Qué es un proyecto? Describa el problema de las 4 P." (textual, E2/E3)
- "¿Cuáles son los elementos clave de la gestión de proyectos?" (E2)

---

#### A.2. Elementos clave de la gestión de proyectos 🟡

**Respuesta de la cátedra (la que esperan, textual).** Los **elementos clave de la gestión de proyectos** son:
1. **Métricas** — medir el proceso, el producto y el proyecto para decidir con datos (ver Bloque B′).
2. **Estimaciones** — predecir esfuerzo, costo y duración (ver B.3).
3. **Calendario temporal** (planificación temporal / *scheduling*) — distribuir las tareas en el tiempo; se apoya en **PERT** (ver B.2 y B.4).
4. **Organización del personal** — constituir y estructurar el equipo (ver A.1 "Personas", A.4 P-CMM, A.5 estructura de equipos).
5. **Análisis de riesgos** — identificar, analizar y planificar respuestas a los riesgos (ver Bloque C).
6. **Seguimiento y control** — monitorear el avance real contra el plan y corregir desvíos (ver B.2).

> Notá que estos seis elementos son, en la práctica, el **índice de toda la parte de gestión** de la materia: cada uno se desarrolla en detalle en los bloques A, B, B′ y C de esta guía. Si te toca esta pregunta, enumerás los seis y explicás brevemente cada uno.

**Objetivo / Problema que resuelve.** Asegurar que **ningún aspecto de la gestión quede sin definir ni sin controlar**: medir, estimar, calendarizar, organizar a la gente, cubrir riesgos y hacer seguimiento. Es lo que separa un proyecto gestionado de uno "en problemas".

**Marco relacionado (por si lo piden con otro enfoque).** La cátedra también puede encarar la gestión desde **las 4 P** (Personas, Producto, Proceso, Proyecto — ver A.1) o el **principio W5HH de Boehm** (Why / What / When / Who / Where / How / How much), un set de preguntas para no dejar nada sin planificar. No los confundas con los seis elementos de arriba: las 4 P son el *marco conceptual*, los seis elementos son la *respuesta esperada* a esta consigna puntual.

**Posible pregunta.** "¿Cuáles son los elementos clave de la gestión de proyectos?" (E2) → los **seis** de arriba.

---

#### A.3. Liderazgo del proyecto (y el "modelo MOI") 🟡

**Lo que enseña la cátedra (Pressman Cap. 24).** El **gerente de proyecto / líder de equipo** *planifica, motiva, organiza y controla* a los profesionales. Un buen liderazgo se describe con las **5 prácticas de líderes ejemplares**:
1. **Modelar el camino** — predicar con el ejemplo; demostrar compromiso con el equipo y el proyecto.
2. **Inspirar una visión compartida** — motivar e involucrar al equipo desde la definición de metas.
3. **Desafiar el proceso** — buscar formas innovadoras de mejorar; animar a experimentar y asumir riesgos.
4. **Permitir que otros actúen** — fomentar la colaboración, generar confianza.
5. **Alentar** — celebrar los logros, generar espíritu de equipo.

**El "modelo MOI" (para finales viejos).** Algunos finales preguntan "Describa el modelo MOI". Es el modelo clásico de **Weinberg** (citado por Pressman): un buen líder combina **M**otivación (animar al equipo a dar lo mejor), **O**rganización (moldear procesos que conviertan la idea en producto) e **I**nnovación/Ideas (fomentar la creatividad dentro de las restricciones). ⚠️ *Ojo:* el deck actual **no usa la sigla MOI**; encara el liderazgo con las 5 prácticas de arriba. Si te toca "MOI", respondé el modelo clásico, pero sabé que la cátedra hoy lo da así.

**Relación.** Es la cara de "Personal" en las 4 P, junto con **P-CMM** (A.4) y los **paradigmas organizacionales del equipo** (B.1).

**Posible pregunta.** "Describa el modelo MOI." (E2) / "¿Qué prácticas realizan los líderes ejemplares?"

---

#### A.4. P-CMM (People Capability Maturity Model) 🟡

**Definición.** Marco para **gestionar y desarrollar el personal** de una organización de software (la cátedra lo llama "modelo de capacitación y motivación del personal"). Es la versión "de personas" del CMM.

**Objetivo.** Atraer, desarrollar, motivar y retener talento, elevando progresivamente la capacidad de la fuerza de trabajo.

**Conceptos clave — niveles de madurez:**
1. **Inicial** — prácticas inconsistentes, dependientes de individuos.
2. **Gestionado** — la organización se preocupa por la carga de trabajo, comunicación y desarrollo de su gente.
3. **Definido** — competencias y prácticas de personal estandarizadas.
4. **Predecible** — se mide y gestiona la capacidad cuantitativamente.
5. **En optimización** — mejora continua de las prácticas de personal.

**Relación con otros temas.** "Personas" (4P), **MOI** (motivación), estructura de equipos.

**Posible pregunta.** "Explique el P-CMM." (E4, textual)

---

#### A.5. Estructura de equipos: factores a considerar 🟡

**Definición / Conceptos clave.** Al armar un equipo se consideran factores como (Pressman):
- Dificultad / complejidad del problema a resolver.
- Tamaño del programa resultante (líneas de código o puntos de función).
- Tiempo de permanencia del equipo junto ("vida" del equipo).
- Grado en que el problema puede modularizarse.
- Calidad y confiabilidad requeridas.
- Rigidez de la fecha de entrega.
- Grado de comunicación/sociabilidad requerido en el proyecto.

**Relación.** Conecta con MOI/P-CMM y con las 4 P (Personas).

**Posible pregunta.** "Enumere al menos 3 factores a considerar al planificar una estructura de equipo." (E7)

---

### BLOQUE B — Planificación y Estimación

#### B.1. Planificación organizativa y paradigmas del equipo 🟡

**Definición (cátedra, Pressman Cap. 24).** La **planificación organizativa** se ocupa de **organizar al personal**, que es *el activo más importante* (capital intelectual) de una organización de software; una mala administración del personal es de las principales causas de fracaso de los proyectos. Por eso existe el **P-CMM** (A.4).

**Participantes a organizar:** gerentes ejecutivos (dueños del producto, definen los temas empresariales), gerentes de proyecto/líderes (planifican, motivan, organizan y controlan), profesionales especializados (aportan lo técnico), clientes (especifican requerimientos) y usuarios finales (interactúan con el software).

**Tipos = los 4 paradigmas organizacionales del equipo** (esta es la respuesta esperada a "tipos de planificación organizacional"):
1. **Cerrado** — jerarquía de autoridad tradicional, comunicación vertical jefe↔miembros. Bueno cuando el software es similar a esfuerzos previos; **poco innovador**.
2. **Abierto** — combina algunos controles del cerrado con la innovación del aleatorio: trabajo colaborativo, mucha comunicación, **decisiones consensuadas** (democrático). Bueno para problemas complejos; puede ser menos eficiente.
3. **Síncrono** — se apoya en la **compartimentalización natural** del problema; los miembros trabajan en partes con poca comunicación entre sí (descentralizado pero controlado, "divide y vencerás"). Bueno para problemas grandes; riesgo de producto mal integrado por falta de comunicación.
4. **Aleatorio** — estructura **holgada**, depende de la iniciativa individual, sin líder definido. Destaca cuando se necesita innovación o avance tecnológico; flojea en el "desempeño ordenado".

**Objetivo.** Sin importar el paradigma, la meta es un equipo **cohesionado** (más productivo y motivado): fija sus propios estándares de calidad, comparte conocimiento y alienta la mejora continua.

**Relación.** Enlaza con **Personal** (4 P, A.1), **P-CMM** (A.4), **factores de estructura de equipo** (A.5) y **liderazgo** (A.3).

**Posible pregunta.** "Tipos de planificación organizacional vistos en la materia." (E1) → los **4 paradigmas** (cerrado, abierto, síncrono, aleatorio).

---

#### B.2. Planificación temporal: seguimiento y control 🟡

**Definición.** La *planificación temporal* (scheduling) distribuye el esfuerzo estimado entre las tareas del proyecto a lo largo del tiempo, definiendo dependencias y asignando recursos.

**Tareas de seguimiento y control (Pressman):**
- Reuniones periódicas de estado (cada miembro informa avance y problemas).
- Evaluar resultados de todas las revisiones.
- Verificar el cumplimiento de **hitos** (milestones) en las fechas previstas.
- Comparar fecha de inicio real vs planificada de cada tarea.
- Reuniones informales con el equipo para conocer percepciones de avance.
- Usar el **análisis del valor ganado** (earned value) para medir cuantitativamente el progreso.

**Relación.** Es el "para qué" del **PERT/Gantt**: sin un cronograma de referencia no se puede controlar nada.

**Posible pregunta.** "En planificación temporal, ¿qué tareas se realizan para el seguimiento y control del proyecto?" (E3)

---

#### B.3. Técnicas de estimación 🟡

**Definición.** Métodos para predecir esfuerzo, costo y duración de un proyecto.

**Conceptos clave (técnicas):**
- **Juicio de expertos:** estimación basada en la experiencia de personas conocedoras. Rápida pero subjetiva.
- **Estimación por analogía:** comparar con proyectos similares ya realizados.
- **Método Delphi (Wideband Delphi):** estimación por **consenso de expertos** en rondas (anónimas) hasta converger; reduce el sesgo de un único estimador. *(La cátedra lo menciona explícitamente.)*
- **Descomposición (bottom-up):** dividir el sistema en tareas/componentes, estimar cada uno y sumar. Puede basarse en **LOC** (líneas de código) o en **Puntos de Función (PF)**.
- **Modelos algorítmicos de costos:** fórmulas paramétricas como **COCOMO / COCOMO II**, que relacionan tamaño (LOC o PF) con esfuerzo.
- **Ley de Parkinson:** "el trabajo se expande hasta llenar el tiempo disponible" → estimar según los recursos disponibles (riesgoso).
- **Precio para ganar (pricing to win):** estimar según lo que el cliente puede pagar (riesgoso).
- **Estimación de tres puntos (PERT):** combinar estimación optimista, más probable y pesimista.

**Ventajas/desventajas.** Juicio experto y analogía son rápidos pero dependen de la calidad de los datos históricos; los modelos algorítmicos son repetibles pero requieren calibración. Lo recomendable es **combinar** varias técnicas y comparar.

**Relación.** Alimenta la **planificación temporal** y el **PERT**; el tamaño estimado del producto influye en la **estructura del equipo**.

**Posible pregunta.** "Enumere y describa las técnicas de estimación que conozca." (E5)

---
Establecer lista de tareas 2. Fijar dependencia entre tareas y duración 3. Construir la red 4. Numerar los nodos 5. Calcular la fecha temprana y tardía de cada nodo Tei = Fecha temprana del nodo i Tai = Fecha tardía del nodo i 6. Calcular el camino crítico que une las tareas críticas ==> Tei = Tai
#### B.4. PERT / CPM y camino crítico 🔴 (ejercicio casi seguro)

**Definición.** **PERT** (Program Evaluation and Review Technique) y **CPM** (Critical Path Method) son técnicas de **red de actividades** para planificar y controlar la duración de un proyecto. Representan tareas, dependencias y duraciones, y permiten calcular el tiempo total y el **camino crítico**.

**Objetivo.** Determinar la **duración mínima** del proyecto, identificar las actividades que **no admiten retraso** (camino crítico) y calcular la **holgura** de las demás.

**Problema que resuelve.** Sin un análisis de red no se sabe qué tareas son críticas; un retraso en ellas retrasa todo el proyecto, mientras que un retraso en tareas con holgura puede absorberse.

**Conceptos clave.**
- **Tiempo temprano de inicio (ES / IC):** lo antes que puede empezar una actividad.
- **Tiempo temprano de fin (EF / FC):** `EF = ES + duración`.
- **Tiempo tardío de fin (LF / FL):** lo más tarde que puede terminar sin retrasar el proyecto.
- **Tiempo tardío de inicio (LS / IL):** `LS = LF − duración`.
- **Holgura (slack/float):** `Holgura = LS − ES = LF − EF`. Si es 0, la actividad es **crítica**.
- **Camino crítico:** secuencia de actividades con holgura 0; es el camino **más largo** de la red y define la duración total. Puede haber **más de uno**.

**Método (algoritmo).**
1. **Pasada hacia adelante** (forward): de izquierda a derecha. `ES` = máximo de los `EF` de los predecesores (las actividades iniciales arrancan en 0). `EF = ES + duración`.
2. La **duración del proyecto** = el mayor `EF` de las actividades finales.
3. **Pasada hacia atrás** (backward): de derecha a izquierda. `LF` de las finales = duración del proyecto. `LF` de una actividad = mínimo de los `LS` de sus sucesoras. `LS = LF − duración`.
4. **Holgura** y **camino(s) crítico(s)**: actividades con holgura 0.

---

##### ✅ Ejercicio resuelto 1 — Compra de vehículo (E7, el del adjunto)

| Act | Pred | Dur | ES | EF | LS | LF | Holgura | ¿Crítica? |
|:---:|:----:|:--:|:--:|:--:|:--:|:--:|:------:|:---------:|
| A | – | 3 | 0 | 3 | 0 | 3 | 0 | ✔ |
| B | A | 1 | 3 | 4 | 3 | 4 | 0 | ✔ |
| C | B | 3 | 4 | 7 | 4 | 7 | 0 | ✔ |
| D | C | 1 | 7 | 8 | 17 | 18 | 10 | ✘ |
| E | C | 2 | 7 | 9 | 7 | 9 | 0 | ✔ |
| F | B, E | 1 | 9 | 10 | 9 | 10 | 0 | ✔ |
| G | F | 2 | 10 | 12 | 10 | 12 | 0 | ✔ |
| H | G | 3 | 12 | 15 | 12 | 15 | 0 | ✔ |
| I | G | 3 | 12 | 15 | 12 | 15 | 0 | ✔ |
| J | H, I | 1 | 15 | 16 | 15 | 16 | 0 | ✔ |
| K | F, G, J | 2 | 16 | 18 | 16 | 18 | 0 | ✔ |

- **Duración total del proyecto = 18** (unidades de tiempo).
- **Caminos críticos (dos):**
  - `A → B → C → E → F → G → H → J → K`
  - `A → B → C → E → F → G → I → J → K`
  - (ambos suman 3+1+3+2+1+2+3+1+2 = 18)
- **Única actividad con holgura:** D (holgura 10).
- *Detalle fino:* `F` no se vuelve crítica por su predecesor B, sino por E (B→F tiene holgura porque `ES(F)` lo fija E con EF=9). Mostrá este razonamiento, suma puntos.

##### ✅ Ejercicio resuelto 2 — Lasaña HOGAREÑAS S.A. (E3)

| Act | Pred | Dur | ES | EF | LS | LF | Holgura | ¿Crítica? |
|:---:|:----:|:--:|:--:|:--:|:--:|:--:|:------:|:---------:|
| A | – | 30 | 0 | 30 | 6 | 36 | 6 | ✘ |
| B | A | 5 | 30 | 35 | 36 | 41 | 6 | ✘ |
| C | – | 2 | 0 | 2 | 39 | 41 | 39 | ✘ |
| D | C, B | 3 | 35 | 38 | 41 | 44 | 6 | ✘ |
| E | – | 7 | 0 | 7 | 0 | 7 | 0 | ✔ |
| F | E | 25 | 7 | 32 | 7 | 32 | 0 | ✔ |
| G | – | 15 | 0 | 15 | 17 | 32 | 17 | ✘ |
| H | G, F | 10 | 32 | 42 | 32 | 42 | 0 | ✔ |
| I | H | 2 | 42 | 44 | 42 | 44 | 0 | ✔ |
| J | I, F, D, B | 10 | 44 | 54 | 44 | 54 | 0 | ✔ |
| K | – | 15 | 0 | 15 | 39 | 54 | 39 | ✘ |
| L | J, K | 30 | 54 | 84 | 54 | 84 | 0 | ✔ |

- **Tiempo total = 84 minutos.**
- **Camino crítico:** `E → F → H → I → J → L` (7+25+10+2+10+30 = 84).

##### 🎯 La "pregunta trampa" del PERT (E4: "si llueve durante la excavación…")
Es la variante favorita de la cátedra. La regla:
- Si la demora ocurre en una **actividad crítica** → el proyecto se retrasa **exactamente** lo que dure la demora.
- Si ocurre en una **actividad con holgura** → el proyecto se retrasa solo si la demora **supera la holgura**; el exceso (`demora − holgura`) es el retraso real. Si la demora ≤ holgura, **no hay retraso**.

**Posibles preguntas.** "Halle tiempos tempranos y tardíos, camino(s) crítico(s) y duración total." / "Si la actividad X se demora N unidades, ¿cuánto se retrasa el proyecto?"

---

### BLOQUE B′ — Métricas e Indicadores (medición del software) 🟠

> Tema nuevo aportado por el segundo compilado (Q1 y Q29). Es **transversal**: sostiene la estimación, el control del proyecto y la evaluación de calidad. Va acá porque *"no se puede controlar lo que no se puede medir"*.

#### B′.1. ¿Qué es y para qué sirve un indicador? (Q1)

**Definición.** Conviene distinguir tres niveles, de menor a mayor abstracción:
- **Medida:** valor de un atributo (p. ej., "850 líneas de código").
- **Métrica:** medida cuantitativa del grado en que un sistema, componente o proceso posee un atributo (definición IEEE); relaciona medidas (p. ej., "defectos cada mil líneas").
- **Indicador:** una métrica (o combinación de métricas) que **proporciona conocimiento (insight)** sobre el proceso, el proyecto o el producto, **habilitando decisiones y ajustes**.

**Objetivo / para qué sirve.** Permite al gestor o al equipo **comprender y ajustar** el proceso, el proyecto o el producto para mejorarlo (p. ej., si el indicador de densidad de defectos sube, se dispara una revisión del proceso de pruebas).

**Problema que resuelve.** Reemplaza la intuición por **evidencia cuantitativa** para estimar, evaluar calidad y controlar el avance.

#### B′.2. Tipos de métricas (Q29)

**Por su foco:**
- **Del proceso:** miden la eficacia/eficiencia del proceso (a largo plazo, para mejorarlo). Ej.: defectos detectados antes de la entrega, tiempo de ciclo, productividad.
- **Del producto:** miden características del software. Ej.: tamaño (LOC, PF), complejidad (ciclomática), densidad de defectos, mantenibilidad.
- **Del proyecto:** las usa el gestor para controlar y adaptar el proyecto. Ej.: esfuerzo, costo, cumplimiento de cronograma, exposición a riesgos.

**Objetivas vs subjetivas:**
- **Objetivas:** se cuentan/miden sin ambigüedad; cualquiera obtiene el mismo valor (LOC, número de defectos, horas-persona).
- **Subjetivas:** dependen del juicio del evaluador y pueden variar entre personas (facilidad de uso percibida, calidad del diseño valorada por un experto).

**Tempranas vs post mortem:**
- **Tempranas:** se recolectan **durante** el desarrollo; son predictivas y permiten **corregir a tiempo** (p. ej., cobertura de pruebas o velocidad de avance en curso).
- **Post mortem:** se recolectan **al finalizar** el proyecto; son retrospectivas y sirven para **aprender y mejorar proyectos futuros** (lecciones aprendidas, desvío final de costo/cronograma, defectos hallados en producción).

**Ventaja/desventaja.** Ventaja: base objetiva para decidir y mejorar. Desventaja: medir mal o medir de más genera burocracia y puede inducir comportamientos perversos (optimizar la métrica en lugar del objetivo real).

**Relación.** Alimenta la **estimación** (B.3, vía LOC/PF), el **seguimiento y control** (B.2), la evaluación de **calidad** (V&V) y la decisión de **rejuvenecer** (métricas de mantenibilidad: cohesión, acoplamiento, complejidad).

**Posibles preguntas.** "¿Qué es y para qué sirve un indicador?" (Q1) / "Defina métricas del proceso y del producto, objetivas y subjetivas. ¿Qué son las post mortem y las tempranas?" (Q29)

#### B′.3. Métricas de tamaño: LDC y Punto Función (cátedra)

La cátedra profundiza en dos **métricas de tamaño** del producto y suele tomar un **ejercicio de cálculo**:

- **LDC / KLDC (líneas de código / miles de líneas):** medida directa pero discutida (depende del lenguaje y del estilo). De ella se derivan:
  - **Productividad** = KLDC / persona-mes
  - **Calidad** = errores / KLDC
  - **Costo** = $ / KLDC
  - **Documentación** = págs. de doc. / KLDC
- **Punto Función (PF) — Albrecht (1978):** mide la **funcionalidad** descrita en la especificación, independiente del lenguaje. Se cuentan entradas, salidas, consultas, almacenamientos internos e interfaces externas (ponderados simple/medio/complejo) y se ajusta con **14 factores** (0–5):
  `PF = TOTAL × [0,65 + 0,01 × Σ Fi]`

**Atributos de calidad:** la cátedra distingue **atributos externos** (visibles al usar el software: fiabilidad, usabilidad…) de **atributos internos** (medibles en el producto: tamaño, complejidad, acoplamiento…), que se relacionan de forma indirecta con la calidad.

**Métricas postmortem — utilidad:** conformar una **línea base** para métricas futuras, ayudar al **mantenimiento** (conociendo complejidad, tamaño y módulos críticos) y apoyar la **reingeniería**.

**Posible ejercicio.** "Con los datos de estos proyectos, calcule productividad, calidad y costo usando LDC."

---

### BLOQUE C — Gestión de Riesgos 🔴

#### C.1. ¿Qué es un riesgo? Características y clasificación

**Definición.** Un **riesgo** es un evento o condición **futura e incierta** que, de ocurrir, tiene un **efecto negativo** sobre el proyecto, el producto o el negocio. "Algo que puede salir mal."

**Objetivo de gestionarlo.** Anticiparse: identificar problemas potenciales *antes* de que ocurran y preparar respuestas, en lugar de reaccionar tarde.

**Características de un riesgo (clave en E1, E6):**
- **Incertidumbre:** puede ocurrir o no (probabilidad entre 0 y 1, sin los extremos). Si es seguro que ocurre, no es riesgo: es un hecho.
- **Pérdida / impacto:** si ocurre, produce consecuencias indeseadas (en costo, plazo, calidad o alcance).
- (Derivadas) **Exposición al riesgo** = probabilidad × impacto; permite priorizar.

**Categorías de riesgos (Sommerville):**
- **Riesgos del proyecto:** afectan cronograma o recursos (ej.: rotación de personal).
- **Riesgos del producto:** afectan la calidad o el desempeño del software (ej.: una librería no rinde lo esperado).
- **Riesgos del negocio:** afectan a la organización que desarrolla o adquiere (ej.: un competidor saca un producto antes).

**Para cada una de las categorias existen dos tipos distintos de riesgos: (Pressman Cap. 26):**
- Los **riesgos genericos**, que representan una amenaza potencial para todo proyecto de software.
- Los **riesgos especificos del producto** que los pueden identificar solo quienes tienen un claro entendimiento de la tecnologia, el personal y el entorno especifico para el que se va a crear el software.

**Ventajas/desventajas de la gestión de riesgos.** Ventaja: reduce sorpresas y costos de "apagar incendios". Desventaja: consume tiempo y puede caer en exceso de burocracia si no se prioriza (de ahí la **línea de corte**).

**Relación.** Se integra con la **planificación** (un plan realista contempla riesgos) y con todos los temas técnicos (un riesgo puede ser arquitectónico, de personal, de requisitos, etc.).

**Posibles preguntas.** "¿Qué es un riesgo? ¿Cuáles son sus características?" (E6) / "¿Qué es un riesgo? ¿Cómo se clasifican?" (E4)

---

#### C.2. Proceso de gestión de riesgos y estrategias de tratamiento

**Proceso (Sommerville), 4 etapas iterativas:**
1. **Identificación:** listar posibles riesgos (tecnológicos, de personal, organizacionales, de requisitos, de estimación…) **categorizarlos**.
![[Pasted image 20260618204245.png]]
2. **Análisis:** estimar probabilidad e impacto de cada uno → **exposición**. Realizar tabla de riesgo, determinar linea de corte la tabla de ordena por probabilidad (desc de arriba para abajo)  y impacto (asc de arriba para abajo).
	1. Un factor de riesgo que tenga gran impacto pero poca probabilidad de que ocurra, no debería absorber un tiempo significativo. Los riesgos de gran impacto con una probabilidad de moderada a alta y los riesgos de poco impacto pero con gran probabilidad deberían tomarse en cuenta.
	2. **Línea de corte (cutline) — clave en E7.** Tras ordenar los riesgos por exposición/prioridad, es la **línea que separa los riesgos que se gestionarán activamente de los que se aceptan** (porque su exposición es baja o porque mitigarlos cuesta más de lo que valen). Es una decisión costo/beneficio.
3. **Planificación:** definir cómo tratar cada riesgo (**Estrategias de tratamiento** (Sommerville)): 
	- **De evitación (avoidance):** reducir la **probabilidad** de que el riesgo ocurra.
	- **De minimización (minimization):** reducir el **impacto** si llegara a ocurrir.
	- **Planes de contingencia:** preparar qué hacer **si** el riesgo se materializa.
4. **Supervisión (monitoreo):** seguir los riesgos a lo largo del proyecto y reevaluar.


**Ejemplo integrador (caso E5/E7: "no se consigue personal con las habilidades adecuadas").**
- *Análisis:* riesgo **del proyecto**, alta probabilidad e impacto (afecta plazo y calidad) → por encima de la línea de corte.
- *Evitación:* capacitar al personal actual con anticipación; iniciar la búsqueda temprano.
- *Minimización:* rediseñar tareas para que las haga gente menos especializada; documentar muy bien.
- *Contingencia:* contratar consultores externos / tercerizar el módulo crítico.

**Posibles preguntas.** "Analice el riesgo y planifique estrategias de tratamiento." (E5) / "Defina línea de corte; enumere 3 riesgos con su estrategia." (E7)

---

#### C.3. Los riesgos de mayor exposición según Boehm (Q3)

**Lo que dice la cátedra (Pressman Cap. 26).** Como priorizar "parece arbitrario", **Boehm recomienda identificar y supervisar los 10 riesgos más altos** (los de mayor **exposición** = probabilidad × impacto). El **número exacto depende del proyecto**, pero debe ser **manejable**. Los riesgos **por encima de la línea de corte** reciben atención y plan de mitigación; los de **debajo** se reevalúan con prioridad de segundo orden. Regla práctica: un riesgo de **gran impacto pero baja probabilidad** no debería consumir tiempo significativo; sí merecen atención los de **gran impacto y probabilidad moderada-alta**, y los de **bajo impacto pero alta probabilidad**.

**Versión clásica del libro (por si piden la lista).** El "Top 10" histórico de Boehm incluye: deficiencias de personal; cronogramas/presupuestos irreales; desarrollar funciones equivocadas; desarrollar la UI equivocada; *gold plating* (ornamentar de más); flujo continuo de cambios en requisitos; deficiencias en componentes externos; deficiencias en tareas tercerizadas; problemas de rendimiento en tiempo real; exigir capacidades por encima del estado del arte.

**Relación.** Conecta directamente con la **línea de corte** y el **análisis de riesgos** (C.2); el ítem de personal es el riesgo del caso E5/E7; el de cambios de requisitos se controla con **GCS**.

**Posible pregunta.** "¿Qué es un riesgo? ¿Cuáles son los ítems de más alto riesgo según Boehm?" (Q3) → enfocá en *supervisar los 10 de mayor exposición por encima de la línea de corte*.

---

### BLOQUE D — Diseño de Software

#### D.1. Tipos / áreas de diseño de software 🟠

**Definición.** Pressman divide el diseño en **cuatro áreas/modelos**, que van de lo más abstracto a lo más concreto:
- **Diseño de datos:** estructuras de datos y modelo de información (transforma el modelo de análisis en estructuras necesarias para implementar el software).
- **Diseño arquitectónico:** estructura global del sistema, relación entre subsistemas/componentes (ver D.4).
- **Diseño de interfaz (UI):** cómo se comunican el sistema y el usuario, y los sistemas entre sí (ver D.5).
- **Diseño a nivel de componentes (procedimental):** lógica interna de cada componente/módulo.

**Objetivo / problema que resuelve.** Transformar los requisitos en una representación técnica del software que pueda construirse, separando preocupaciones por nivel de detalle.

**Relación.** El diseño arquitectónico es la base sobre la que se hace el de componentes; el de datos atraviesa a todos; el de interfaz aplica los principios de UI y las heurísticas de Nielsen.

**Posibles preguntas.** "¿Cuáles son los tipos (áreas) de diseño de software? Describa." (E3, E4)

---

#### D.2. Conceptos de diseño: abstracción, modularidad, ocultación de información

**Definición / conceptos clave.**
- **Abstracción:** centrarse en *qué* hace algo, ocultando el *cómo*. Hay abstracciones de datos, de procedimiento y de control.
- **Modularidad:** dividir el software en módulos (componentes con nombre y función definidos). "Divide y vencerás": la complejidad total baja al modularizar (pero existe un punto donde demasiados módulos aumentan el costo de integración).
- **Ocultación de información (information hiding):** cada módulo oculta sus decisiones de diseño internas; los demás solo ven su interfaz. Reduce el efecto dominó ante cambios.
- **Refinamiento:** descomposición progresiva (de lo general a lo detallado), complementaria de la abstracción.
- **Independencia funcional:** consecuencia de aplicar bien los anteriores; se mide con **cohesión** y **acoplamiento**.

**Relación.** Son la base teórica de **cohesión/acoplamiento** (D.3) y de la **mantenibilidad** (y por lo tanto del **rejuvenecimiento**: el software viejo suele tener baja modularidad y por eso es difícil de cambiar).

---

#### D.3. Cohesión y acoplamiento 🟡 (fundamental aunque aparezca poco)

**Definición.**
- **Cohesión:** grado en que los elementos *dentro* de un módulo están relacionados entre sí y contribuyen a una única tarea. **Se busca cohesión ALTA.**
- **Acoplamiento:** grado de interdependencia *entre* módulos. **Se busca acoplamiento BAJO.**

**Objetivo.** Lograr **independencia funcional** → módulos más fáciles de entender, probar, mantener y reutilizar.

**Conceptos clave — niveles de cohesión (de peor a mejor):**
coincidental → lógica → temporal → procedimental → comunicacional → secuencial → **funcional** (la mejor: todo el módulo cumple una sola función bien definida).

**Niveles de acoplamiento (de peor a mejor):**
de contenido → común (datos globales) → de control (se pasan banderas que controlan el flujo) → de sello/estampado (se pasa una estructura completa usando solo parte) → **de datos** (solo se pasan los parámetros simples necesarios: el mejor).

**Ventaja/desventaja.** Alta cohesión + bajo acoplamiento = sistema mantenible, pero exige más esfuerzo de diseño inicial. El acoplamiento de contenido o común genera sistemas frágiles ("tocás acá, se rompe allá").

**Relación.** Indicador directo de **mantenibilidad** → conecta con **rejuvenecimiento** (la reingeniería busca, entre otras cosas, mejorar cohesión y reducir acoplamiento).

**Posible pregunta.** "Defina cohesión y acoplamiento." (E6)

---

#### D.4. Diseño arquitectónico y organización del sistema 🔴

**Definición.** El **diseño arquitectónico** define la **estructura global** del sistema: cuáles son los subsistemas/componentes principales, sus responsabilidades y cómo se comunican. Es la primera y más importante decisión de diseño.

**¿Qué define el diseño arquitectónico? (E2):** la **organización del sistema** (modelo estructural), la **descomposición en módulos** (cómo se subdividen los subsistemas) y el **estilo de control** (cómo se coordinan).

**Modelos de organización del sistema (Sommerville):**

##### Modelo de Repositorio
Los subsistemas **comparten datos en un repositorio (base de datos) central**. Cada subsistema interactúa con ese almacén común.
- **Ventajas:** eficiente para compartir **grandes volúmenes** de datos; un subsistema no necesita saber cómo otro usa los datos; gestión centralizada de respaldo, seguridad y control de acceso; fácil integrar nuevos subsistemas que entiendan el modelo de datos.
- **Desventajas:** los subsistemas deben **acordar un modelo de datos común** (compromiso que limita a cada uno); evolucionar el modelo de datos es costoso (afecta a todos); difícil de **distribuir** eficientemente; **punto único de falla** (si cae el repositorio, cae todo).

##### Modelo Cliente-Servidor
Sistema **distribuido**: un conjunto de **servidores** ofrece servicios, un conjunto de **clientes** los consume, y una **red** los conecta.
- **Ventajas:** **distribución natural** de datos y procesamiento; **escalable** (se agregan servidores fácilmente); permite usar hardware/equipos heterogéneos; los clientes acceden a los servicios sin conocer la implementación interna.
- **Desventajas:** **no hay un modelo de datos compartido** (cada servicio puede tener el suyo → posible redundancia); no hay un registro central de qué servicios existen (puede ser difícil saber qué hay disponible); el **rendimiento depende de la red** (puede ser cuello de botella); la gestión está distribuida → más compleja.

##### Comparación directa (la pregunta clásica)
| Criterio | Repositorio | Cliente-Servidor |
|---|---|---|
| Datos | Centralizados, modelo común | Distribuidos, sin modelo único |
| Acoplamiento de datos | Alto (todos dependen del repositorio) | Bajo entre servicios |
| Distribución | Difícil | Natural |
| Escalabilidad | Limitada | Alta (agregar servidores) |
| Punto único de falla | Sí (el repositorio) | Menor (depende de la red/servidores) |
| Compartir grandes volúmenes | Muy eficiente | Menos directo |

> *Otros modelos que la cátedra menciona:* **Máquina abstracta / por capas** (cada capa usa servicios de la inferior; flexible pero a veces poco eficiente) y los **modelos de control** (centralizado vs basado en eventos).

##### Requerimientos no funcionales afectados por la arquitectura (Q2)
La decisión arquitectónica impacta de lleno en varios **requerimientos no funcionales (RNF)**:
- **Rendimiento (performance):** localizar las operaciones críticas en pocos componentes grandes y minimizar la comunicación entre ellos.
- **Seguridad / protección (security):** usar arquitectura en **capas**, con los activos más críticos en las capas internas.
- **Seguridad de funcionamiento (safety):** concentrar las funciones críticas de seguridad en pocos subsistemas (menos a verificar).
- **Disponibilidad (availability):** incluir **componentes redundantes** y mecanismos de tolerancia a fallos.
- **Facilidad de mantenimiento (maintainability):** usar componentes **finos, autocontenidos y reemplazables**.

⚠️ **Conflictos típicos:** estos RNF compiten entre sí. *Rendimiento* favorece componentes grandes (menos comunicación), mientras que *mantenibilidad* favorece componentes chicos: optimizar uno suele perjudicar al otro, y el arquitecto debe negociar un equilibrio. (Pregunta de examen: "¿Qué RNF se ven afectados por la arquitectura?" — Q2.)

**Justificación de elección (caso E7).** Para la empresa de fletes —demanda fuerte de accesos 24×7, usuarios geográficamente dispersos, necesidad de escalar de 20 a más empresas— se elige **cliente-servidor**: permite atender muchos clientes simultáneos desde cualquier lugar y **escalar agregando servidores**, algo que el repositorio centralizado no resuelve bien.

**Relación.** El diseño arquitectónico es un **tipo de diseño** (D.1); las decisiones se evalúan con **cohesión/acoplamiento** (D.3); influye en los **riesgos** técnicos y en la **mantenibilidad**.

**Posibles preguntas.** "Diferencie modelo de repositorio y cliente-servidor." (E1, E5) / "¿Qué define el diseño arquitectónico? Tipos de organización del sistema." (E2) / "¿Cómo puede ser la organización del sistema?" (E4)

---

#### D.5. Principios de diseño y "Recuperabilidad" 🟠

**Principios del modelado de diseño (cátedra, Pressman Cap. 8).** Para "Enumere y describa los principios de diseño" (E2), la lista de la cátedra es:
1. El diseño debe poder **rastrearse hasta el modelo de requerimientos**.
2. Considerar siempre la **arquitectura** del sistema a crear.
3. El **diseño de datos** es tan importante como el de funciones.
4. Las **interfaces** deben diseñarse con cuidado.
5. El diseño de interfaz debe **ajustarse a las necesidades del usuario** (facilidad de uso).
6. El diseño a nivel de **componentes** debe ser **funcionalmente independiente**.
7. Los componentes deben tener **bajo acoplamiento**.
8. Las representaciones de diseño deben **entenderse fácilmente**.
9. El diseño debe desarrollarse de manera **iterativa**.
10. Crear un modelo de diseño **no impide** una metodología ágil.

**"Recuperabilidad" (lo que pide E1/Q10).** Es el principio/atributo de que el sistema y el usuario puedan **recuperarse de errores y fallas** minimizando la pérdida de información. ⚠️ *Aclaración tras revisar el deck:* la cátedra **no lo da como un "principio" con ese nombre**; el concepto aparece en dos lugares:
- En **interfaz de usuario**, dentro de la regla dorada de Mandel "**dar control al usuario**", que incluye **interrumpir y deshacer (undo)** acciones (D.6).
- En **calidad/fiabilidad**, como capacidad de **restaurar servicio y datos tras una falla**: copias de seguridad y de recuperación, y **pruebas de recuperación** (recovery testing, Bloque E).

Para responder: definí recuperabilidad como *la capacidad de volver a un estado correcto tras un error o falla* y dá ejemplos (deshacer, confirmar acciones destructivas, backups, puntos de control). Si tu cursada lo tomó de **Sommerville**, ahí sí es uno de los 6 principios de diseño de interfaz (familiaridad, consistencia, mínima sorpresa, **recuperabilidad**, guía al usuario, diversidad) — conviene mencionarlo.

**Relación.** Conecta **diseño** (bajo acoplamiento, independencia funcional, D.3) con **interfaz** (D.6) y con **fiabilidad / pruebas de recuperación** (E).

**Posibles preguntas.** "Defina Recuperabilidad (principio de diseño)." (E1/Q10) / "Enumere y describa los principios de diseño." (E2) → los **10 principios del modelado de diseño**.

---

#### D.6. Diseño de interfaz de usuario: reglas doradas, usabilidad y Nielsen 🟠

**Cómo lo enseña la cátedra (Pressman, Cap. 11–12).** El diseño de UI es un **proceso iterativo y centrado en el usuario**, con 6 pasos: (1) analizar y comprender las actividades del usuario → (2) diseño del prototipo en papel → (3) evaluar con usuarios finales → (4) diseño dinámico del prototipo → (5) evaluar con usuarios → (6) implementar la interfaz definitiva. *(Esa es la lámina rotulada "6 principios de interfaz": en realidad es el proceso, no una lista de principios.)*

**Reglas doradas del diseño — Theo Mandel (consideraciones de UI, E5/Q28):**
1. **Dar control al usuario** — interacción flexible; **incluir interrumpir y deshacer**; ocultar lo técnico interno; interacción directa con objetos en pantalla. *(Acá vive la "recuperabilidad".)*
2. **Reducir la carga de memoria del usuario** — valores por defecto con significado, accesos directos intuitivos, metáforas de la realidad, información progresiva.
3. **Lograr una interfaz consistente** — mismas reglas para las mismas interacciones; el usuario sabe de dónde viene y a dónde puede ir.
- Sumar **factores humanos** (percepción, memoria, razonamiento, habilidades) y **diversidad de usuarios** (casuales necesitan guía; expertos, agilidad).

**Usabilidad (Donahue).** Medida de cuán bien un sistema facilita el aprendizaje, ayuda a recordar lo aprendido, reduce errores, permite eficiencia y deja satisfecho al usuario. Se determina **evaluándola/probándola** con usuarios reales.

**Las 10 heurísticas de Nielsen (numeración de la cátedra):**
1. Diálogo simple y natural · 2. Lenguaje del usuario · 3. Minimizar el uso de la memoria del usuario · 4. Consistencia · **5. Feedback** · 6. Salidas evidentes · 7. Mensajes de error · **8. Prevención de errores** · 9. Atajos · 10. Ayudas.

**Para E7/Q4 (feedback + prevención de errores):**
- **#5 Feedback** → el sistema siempre informa qué está pasando (ej.: estado de cada solicitud de flete, confirmación de envío).
- **#8 Prevención de errores** → diseñar para que el error no ocurra (validar datos, confirmar acciones destructivas). *(La #7 "mensajes de error" ayuda a recuperarse de ellos.)*

**Posibles preguntas.** "Mencione dos principios de Nielsen para feedback y prevención de errores." (E7) → #5 y #8. / "¿Qué consideraciones al desarrollar una UI?" (E5) → reglas de Mandel + factores humanos + usabilidad + proceso iterativo.

---

### BLOQUE E — Verificación y Validación (Testing) 🟠

**Definición (la dupla clave).**
- **Verificación:** *"¿Estamos construyendo el producto **correctamente**?"* — comprobar que el software cumple su **especificación**.
- **Validación:** *"¿Estamos construyendo el producto **correcto**?"* — comprobar que el software satisface las **necesidades reales del usuario**.

**Objetivo / problema que resuelve.** Detectar defectos y asegurar que el software es a la vez *bien hecho* (verificación) y *lo que el cliente necesitaba* (validación). Un producto puede estar perfectamente construido según la especificación y aun así ser inútil si la especificación estaba mal: por eso hacen falta ambas.

**Conceptos clave — técnicas de prueba.**
- **Caja blanca (estructural):** se conoce el código; se prueban caminos, condiciones, bucles, cobertura. Tiende a ser **verificación**.
- **Caja negra (funcional):** no se mira el código; se prueban entradas/salidas contra los requisitos. Tiende a la **validación**.
- *Ejemplo de caja blanca:* prueba del **camino básico**, asegurando que cada rama de un `if` y cada bucle se ejecuten al menos una vez (cobertura).
- *Ejemplo de caja negra:* **partición de equivalencia / valores límite**: si un campo acepta 1–100, probar 0, 1, 100 y 101.

**Técnicas de validación — estáticas vs dinámicas (Q33).** La V&V se realiza con dos familias de técnicas:
- **Estáticas (sin ejecutar el software):** **inspecciones**, revisiones por pares (*walkthroughs*) y **análisis estático automatizado**. Detectan defectos temprano y son baratas.
- **Dinámicas (ejecutando el software):** las **pruebas**. Incluyen las de desarrollo (unitarias, integración, sistema), las de **versión** (release) y las de **usuario** (alfa, beta y de **aceptación**). Las de usuario/aceptación son las que claramente **validan**.

**Niveles de prueba y su relación con V&V:**
- **Unitarias** (módulo individual) → verificación.
- **Integración** (módulos juntos) → verificación.
- **De sistema** (sistema completo) → entre verificación y validación.
- **De aceptación** (con el usuario, datos reales) → **validación**.

**Pruebas de integración (clave en E4 y E7):**
- **Big-bang (no incremental):** integrar todo de golpe y probar. Simple pero difícil de localizar fallas.
- **Incremental descendente (top-down):** se integra desde el módulo de más alto nivel hacia abajo; se necesitan **stubs** (módulos ficticios que simulan a los aún no integrados).
- **Incremental ascendente (bottom-up):** se integra desde los módulos de bajo nivel hacia arriba; se necesitan **drivers/controladores** (que simulan a los módulos superiores).
- **Sándwich / híbrida:** combina top-down y bottom-up.

**¿Cuál usar? (E7).** En un sistema con lógica crítica en módulos base (cálculo de rutas, geolocalización) conviene **ascendente (bottom-up)**, para probar primero y bien esos componentes fundamentales; si lo crítico es la interfaz y el flujo general, **descendente (top-down)**. Justificá según el caso.

**Ventaja/desventaja.** La integración incremental localiza fallas más fácilmente que big-bang, pero requiere construir stubs/drivers (costo extra).

**Relación.** Verifica/valida lo producido en **diseño**; su planificación es un **tipo de plan** (B.1); los defectos no resueltos son **riesgos** de producto.

**Posibles preguntas.** "¿Qué es verificación? ¿Qué es validación? De las pruebas vistas, ¿cuál verifica y cuál valida?" (E3) / "Diferencie verificación y validación. Enumere las pruebas de integración." (E4) / "¿Qué integración usaría y por qué?" (E7)

---

### BLOQUE F — Gestión de Configuración (GCS) 🔴 (el tema #1)

**Definición.** La **Gestión de Configuración del Software (GCS / SCM)** es el conjunto de **actividades para identificar, controlar y auditar los cambios** de los artefactos del software (programas, documentos, datos) a lo largo de **todo** el ciclo de vida.

**Objetivo.** Controlar la evolución del software de forma ordenada: saber **qué** cambió, **quién**, **cuándo** y **por qué**, y poder reconstruir cualquier versión.

**Problema que resuelve.** El software cambia constantemente (requisitos cambiantes —como en E7—, correcciones, mejoras). Sin GCS aparece el caos: versiones que se pisan, cambios no autorizados, imposibilidad de reproducir una versión entregada.

**Conceptos clave — el proceso de GCS (Pressman), 5 actividades:**
1. **Identificación de la configuración:** definir los **Elementos de Configuración del Software (ECS/SCI)** — qué se va a controlar.
2. **Control de versiones:** gestionar las distintas versiones de cada elemento.
3. **Control de cambios:** todo cambio pasa por una solicitud que se evalúa (impacto/costo), se aprueba o rechaza (a menudo por un **Comité de Control de Cambios**) y luego se realiza y verifica.
4. **Auditoría de configuración:** verificar que el cambio se hizo correctamente y según lo aprobado.
5. **Generación de informes de estado:** comunicar qué cambió, cuándo y a quién afecta.

**Línea base (baseline) — ⭐ casi siempre piden definirla y ejemplificar:**
> **Definición (IEEE):** una **línea base** es una especificación o producto que ha sido **formalmente revisado y aprobado**, que sirve como **base para el desarrollo posterior** y que **solo puede modificarse mediante el procedimiento formal de control de cambios.**

Es decir: un ECS empieza siendo modificable libremente; una vez **revisado y aprobado**, se convierte en línea base y queda "congelado": cambiarlo requiere autorización formal.

**Ejemplos de líneas base (Pressman):** Especificación del sistema → **Especificación de requisitos** (aprobada tras su revisión) → **Especificación de diseño** → **Código fuente** → **Planes/casos de prueba** → **Sistema operativo/en producción**. Cada uno se vuelve línea base al pasar su revisión técnica formal.

**Elementos de configuración (qué controlar) — E7:** documentos de requisitos, especificación de diseño, **código fuente**, casos y datos de prueba, manuales, e incluso herramientas/entorno. (En E7 alcanza con dar 2 ejemplos: p. ej. *código fuente* y *documento de requisitos*.) La cátedra agrupa los **ECS en 3 categorías: programas, productos de trabajo y datos**, y señala 4 **orígenes del cambio**: nuevas condiciones de negocio/mercado, nuevas necesidades de las partes interesadas, reorganización (crecimiento/reducción) de la empresa, y restricciones de presupuesto/calendario.

**Ventaja/desventaja.** Ventaja: trazabilidad, reproducibilidad, control del caos y soporte al trabajo en equipo. Desventaja: introduce burocracia/overhead; mal aplicada, frena el desarrollo.

**Relación.** Es **transversal** a todo el ciclo: las líneas base se apoyan en las **revisiones** (V&V); el plan de GCS es un **tipo de plan** (B.1); en proyectos con **requisitos cambiantes** (E7) la GCS es indispensable; cambios mal gestionados son un **riesgo**.

**Posibles preguntas (todas reales).** "¿Qué es GCS? Defina línea base y ejemplifique." (E1, E5) / "Defina y describa GCS." (E2) / "Describa el proceso de GCS." (E3, E4) / "Identificar y controlar los elementos del sistema a lo largo del desarrollo: ¿a qué se refiere y qué elementos se controlan?" (E7)

---

### BLOQUE G — Mantenimiento y Evolución del Software 🔴

#### G.1. Tipos de mantenimiento y barrera del mantenimiento (Q34, Q37)

**Definición.** El **mantenimiento** es la modificación del software **después de su entrega** (solucionar errores, añadir mejoras, optimizar). Es la fase **más larga y costosa** del ciclo de vida: según la cátedra (Pfleeger) involucra entre el **40 % y el 70 % del costo total de desarrollo**.

**Tipos de mantenimiento (Q34):**
- **Correctivo:** corregir defectos/errores descubiertos tras la entrega.
- **Adaptativo:** adaptar el software a cambios del entorno (nuevo SO, hardware, normativa).
- **Perfectivo (de mejora):** agregar o mejorar funciones a pedido del usuario, o mejorar rendimiento/mantenibilidad. Suele ser el de **mayor proporción**.
- **Preventivo:** modificar el software para **prevenir** problemas futuros y mejorar su estructura antes de que falle (se solapa con la reingeniería).

**Barrera del mantenimiento (Q37).** Es el **fenómeno** (Pfleeger Cap. 11) por el cual mantener el software —corregir errores, añadir mejoras y optimizar— genera **altos costos adicionales** que terminan **frenando otros desarrollos**: como el mantenimiento absorbe entre el 40 % y el 70 % del costo total, la organización queda "atrapada" sosteniendo lo viejo en vez de construir lo nuevo. Además tiene **efectos secundarios** sobre código, datos y documentación, puede **disminuir la calidad** total del producto y obliga a **reiniciar las fases** de análisis, diseño e implementación. Se alinea con las **leyes de evolución de Lehman** (Sommerville Cap. 21): la complejidad crece y la calidad decae si no se invierte en mejorarla. La respuesta es el **mantenimiento preventivo** y el **rejuvenecimiento / reingeniería** (G.2).

**Ingeniería inversa y reingeniería (Q34) — definiciones puntuales:**
- **Ingeniería inversa:** analizar el sistema para **recuperar su diseño/especificación** a partir del código (de lo concreto a lo abstracto). *No* modifica el sistema; produce información.
- **Reingeniería:** **reestructurar o reescribir** parte o todo un sistema legado **sin cambiar su funcionalidad**, para mejorarlo. Combina ingeniería inversa + reestructuración + ingeniería directa.

**Relación.** El mantenimiento preventivo y la reingeniería combaten la **barrera del mantenimiento**; la causa de fondo es la degradación de **cohesión/acoplamiento** (D.3); cada cambio genera versiones que la **GCS** (Bloque F) debe controlar.

**Posibles preguntas.** "¿Qué tipos de mantenimiento conoce? Defina ingeniería inversa y reingeniería." (Q34) / "¿Qué es la barrera del mantenimiento?" (Q37)

---

#### G.2. Rejuvenecimiento del software (reingeniería) 🔴

**Definición (cátedra, Pfleeger Cap. 11).** El rejuvenecimiento del software es **un desafío del mantenimiento que busca aumentar la calidad global de un sistema existente**. Contempla **retrospectivamente** los subproductos del sistema para **derivar información adicional o reformularlo** de un modo más comprensible, sin (necesariamente) cambiar su funcionalidad.

**Objetivo.** Extender la vida útil de sistemas viejos pero valiosos, reduciendo el costo y el riesgo de mantenerlos, en lugar de reescribirlos desde cero.

**Problema que resuelve.** El software envejece: la documentación se desactualiza, el código se degrada con cada parche y la estructura se deteriora. Esto eleva el costo y el riesgo de cada cambio. El rejuvenecimiento ataca esa degradación.

**Tipos de rejuvenecimiento (los 4 de la cátedra):**
1. **Re-documentación** — recrear o actualizar la documentación a partir del sistema actual (nivel menos invasivo).
2. **Re-estructuración** — transformar el software para hacerlo **más fácil de entender y de cambiar** sin alterar su funcionalidad (mejora cohesión/acoplamiento; aplica a código y a datos). La cátedra la describe interpretando el código fuente y representándolo internamente (red semántica / grafo) para luego mejorarlo.
3. **Ingeniería inversa** — analizar el sistema para **recuperar su diseño y especificación** a partir del código (de lo concreto a lo abstracto). No modifica el sistema; produce información.
4. **Re-ingeniería** — rehacer/reconstruir el sistema (normalmente combinando ingeniería inversa + reestructuración + ingeniería directa) para obtener una versión más mantenible.

**Ventaja/desventaja.** Ventaja: menor costo y riesgo que reescribir; conserva conocimiento del negocio embebido en el sistema. Desventaja: tiene límites (a veces el sistema está tan degradado que reescribir conviene más); puede ser costoso si la documentación se perdió por completo.

**Relación.** Es la respuesta a la **degradación de la cohesión/acoplamiento** (D.3) y de los **conceptos de diseño** (D.2). Fuerte vínculo con **GCS** (la reingeniería genera muchas versiones a controlar) y con **mantenibilidad** como atributo de calidad.

**Posibles preguntas (todas reales).** "Describa el rejuvenecimiento." (E1, E5) / "¿Qué es el rejuvenecimiento del software? Describa los tipos." (E3) / "Defina rejuvenecimiento." (E6)

---

## 4. Relaciones entre Conceptos

Mapa mental de cómo se conectan los temas (úsalo para responder las preguntas "relacione X con Y", muy valoradas):

- **Las 4 P son el paraguas.** *Personas* → MOI, P-CMM, estructura de equipos. *Producto* → estimación. *Proceso* → modelos de proceso. *Proyecto* → planificación temporal, PERT, riesgos.
- **Planificación ⇄ Estimación ⇄ PERT:** se estima el tamaño/esfuerzo → se arma el cronograma → PERT calcula duración y camino crítico → el seguimiento y control compara real vs plan.
- **Las métricas sostienen todo lo cuantitativo:** las de tamaño (LOC, PF) alimentan la **estimación**; las de proyecto, el **seguimiento y control**; las de producto, la evaluación de **calidad** (V&V) y la decisión de **rejuvenecer**. Un **indicador** convierte esas métricas en decisiones.
- **Riesgos atraviesan todo:** un riesgo puede ser de personal (Personas), arquitectónico (Diseño), de requisitos cambiantes (que GCS ayuda a controlar) o de calidad (que V&V detecta). La planificación realista contempla riesgos; la línea de corte decide cuáles gestionar.
- **Diseño en cascada de detalle:** áreas de diseño (datos → arquitectura → interfaz → componentes). La calidad de cada uno se mide con **cohesión (alta) y acoplamiento (bajo)**, que nacen de **abstracción, modularidad y ocultación de información**.
- **Recuperabilidad conecta diseño ↔ UI ↔ fiabilidad:** se realiza en la interfaz con interrumpir/deshacer (regla de Mandel "dar control al usuario") y en el sistema con copias de seguridad y **pruebas de recuperación**; en Nielsen se apoya en #5 (feedback), #7 (mensajes de error) y #8 (prevención de errores).
- **V&V verifica/valida lo diseñado y construido;** sus líneas base aprobadas alimentan la **GCS**.
- **GCS es transversal** al ciclo entero: cada artefacto revisado y aprobado se vuelve **línea base** y entra al control de cambios.
- **Rejuvenecimiento cierra el ciclo:** cuando la cohesión baja y el acoplamiento sube con los años, se aplica reingeniería; eso genera versiones que la **GCS** debe controlar.
- **El mantenimiento es la fase más larga:** sus cuatro tipos (correctivo, adaptativo, perfectivo, preventivo) y la **barrera del mantenimiento** explican *por qué* se llega a necesitar rejuvenecimiento; la degradación de cohesión/acoplamiento es la causa raíz, y el mantenimiento preventivo la prevención.

**Cadena de dependencias para estudiar en secuencia:**
`Conceptos de diseño (abstracción/modularidad/ocultación) → Cohesión y acoplamiento → Áreas de diseño → Arquitectura (repositorio vs C/S) → UI + Recuperabilidad + Nielsen → V&V → GCS → Rejuvenecimiento.`

---

## 5. Patrones de Evaluación de la Cátedra

Observaciones explícitas a partir de los 7 finales:

1. **Estructura fija del examen:** ~**6 preguntas conceptuales + 1 ejercicio de PERT**. En finales "reducidos", 3 preguntas conceptuales sin ejercicio.
2. **El PERT casi nunca falta** y suele ser la última pregunta. Practicá el método hasta automatizarlo, incluida la **variante "si la actividad X se demora N, ¿cuánto se retrasa el proyecto?"** (depende de si es crítica o de su holgura).
3. **Eje fuerte en GESTIÓN (no en UML ni en metodologías ágiles).** Esto es clave: a diferencia de otras cátedras, **no hay énfasis en UML, Scrum/ágil, casos de uso ni patrones de diseño GoF**. El peso está en **gestión de proyectos, configuración, arquitectura, V&V y mantenimiento**. No "malgastes" repaso en UML/ágil salvo que tu cursada lo indique aparte.
4. **Preguntas casi textuales y repetidas:** GCS/línea base, riesgos, repositorio vs C/S y rejuvenecimiento aparecen reformuladas una y otra vez. El banco de preguntas es estable → estudiar finales viejos es altísimamente rentable.
5. **Bibliografía base:** **Pressman** (gestión, diseño, GCS, riesgos, métricas, interfaz) y **Sommerville** (organización del sistema, gestión de riesgos), con **Pfleeger** en mantenimiento. Si dudás de una definición, priorizá estos autores (el detalle de capítulos está en el punto 9).
6. **Tendencia reciente a formato "caso integrador":** el final 2024 (fletes) presenta **un caso único** del que cuelgan todas las preguntas, en vez de preguntas sueltas. Preparate para **aplicar** los conceptos a un escenario (elegir y justificar una arquitectura, identificar riesgos con estrategias, elegir tipo de integración), no solo a recitarlos.
7. **Énfasis creciente en interfaz de usuario** (Nielsen + recuperabilidad + consideraciones de UI): apareció en E1, E5 y E7. Es un "frecuente" en alza.
8. **El banco confirma dos ejes que conviene no descuidar:** **medición** (indicadores y métricas de proceso/producto) y **mantenimiento** (tipos + barrera + ingeniería inversa/reingeniería). Ambos aparecen de forma recurrente en el compilado y enlazan con los temas core (calidad, GCS, rejuvenecimiento).
9. **Bibliografía y encuadre (diapositivas 2024):** la cátedra es **Pressman-céntrica** (Cap. 8 diseño · 9/22 GCS · 11–12 interfaz · 24 gestión/personal · 26 riesgos), con **Sommerville** (12 riesgos · 25 personal/arquitectura) y **Pfleeger** (11 mantenimiento/rejuvenecimiento). Consecuencias prácticas: interfaz con **Mandel + Nielsen** (no Sommerville); liderazgo con **prácticas de líderes ejemplares** (no MOI); y hay **3 tipos de ejercicio de cálculo**: PERT, línea de corte de riesgos y métricas LDC/PF.

---

## 6. Ranking de Prioridades de Estudio

Ordenado por frecuencia observada (de más a menos rentable):

| # | Tema | Frecuencia | ¿Por qué priorizarlo? |
|:-:|------|:----------:|----------------------|
| 1 | **GCS / Línea base** | 6/7 | El más repetido; definición + proceso + ejemplo. Imprescindible. |
| 2 | **PERT / Camino crítico** | 5/7 | Ejercicio casi seguro; se "regalan" puntos si lo dominás. |
| 3 | **Riesgos** | 5/7 | Definición, características, clasificación y estrategias + línea de corte. |
| 4 | **Arquitectura (Repositorio vs C/S)** | 5/7 | Comparación clásica; aprendete el cuadro de memoria. |
| 5 | **Rejuvenecimiento** | 4/7 | Definición + tipos; respuesta corta y de alto rendimiento. |
| 6 | **Verificación y Validación / Integración** | 3/7 | La dupla "¿bien hecho?" vs "¿lo correcto?" + tipos de integración. |
| 7 | **Interfaz de usuario (Nielsen + Recuperabilidad)** | 3/7 | En alza; conecta varios temas. |
| 8 | **4 P / ¿Qué es un proyecto?** | 2–3/7 | Marco general; fácil de recordar. |
| 9 | **Áreas de diseño / Principios / Cohesión-acoplamiento** | 2/7 | Base conceptual del diseño. |
| 10 | **MOI, P-CMM, estimación, planificación, equipos** | 1/7 c/u | Complementos de "Personas/Planificación"; repaso rápido. |

> **Ajuste tras la segunda fuente:** subí **Cohesión y acoplamiento** a 🟠 (aparece 3× en el compilado) y agregá al repaso **Métricas e indicadores** 🟠 y **Tipos de mantenimiento + barrera** 🟠 (nuevos y recurrentes). En la práctica, ubicalos junto a los temas #6–#9 de la tabla.

---

## 7. Plan de Estudio Recomendado

### 🥇 Qué estudiar PRIMERO (núcleo imprescindible — sin esto no se aprueba)
1. **GCS:** memorizá la definición, las **5 actividades del proceso** y la **definición de línea base con un ejemplo** (requisitos → diseño → código).
2. **PERT:** practicá el algoritmo completo (pasada adelante/atrás, holgura, camino crítico) con los **dos ejercicios resueltos** de esta guía hasta hacerlo sin mirar. Incluí la variante de "demora en una actividad".
3. **Riesgos:** definición + **características (incertidumbre y pérdida)** + clasificación (proyecto/producto/negocio) + **estrategias (evitación, minimización, contingencia)** + **línea de corte**.
4. **Arquitectura:** el **cuadro comparativo Repositorio vs Cliente-Servidor** y saber **justificar** una elección ante un caso.
5. **Rejuvenecimiento:** definición + **tipos** (redocumentación, ingeniería inversa, reestructuración de código/datos, ingeniería directa/reingeniería).

> Con estos 5 podés responder ~5 de 7 preguntas de casi cualquier final.

### 🥈 Qué estudiar DESPUÉS (completar para apuntar a buena nota)
6. **V&V + pruebas de integración:** verificación vs validación, caja blanca/negra, top-down/bottom-up (stubs vs drivers).
7. **Interfaz de usuario:** 2–3 heurísticas de Nielsen (feedback #1, prevención #5) + **Recuperabilidad** como principio + consideraciones de UI.
8. **Diseño:** las **4 áreas** (datos, arquitectura, interfaz, componentes) y **cohesión/acoplamiento** (qué es cada uno y que se busca alta cohesión / bajo acoplamiento).
9. **Las 4 P** y los **elementos clave de la gestión** (W5HH).
10. **Métricas e indicadores:** qué es un indicador (vs medida/métrica) y los tipos (proceso/producto, objetivas/subjetivas, tempranas/post-mortem).
11. **Mantenimiento:** los 4 tipos (correctivo/adaptativo/perfectivo/preventivo), la **barrera del mantenimiento** e **ingeniería inversa vs reingeniería**.

### 🥉 Repaso rápido (poco frecuentes — leer una vez, no memorizar a fondo)
12. **MOI** (Motivación/Organización/Innovación), **P-CMM** (5 niveles), **técnicas de estimación**, **planificación temporal**, **factores de estructura de equipos**, **tipos de planificación organizacional**.

### 🎯 Estrategia para el día del final
- Empezá por el **PERT** (es mecánico y asegura puntos), luego las preguntas de **GCS, riesgos, arquitectura y rejuvenecimiento** (las que más dominás).
- Si el final es un **caso integrador** (estilo 2024), leé primero todo el enunciado e identificá qué concepto pide cada inciso antes de escribir.
- En las comparaciones (repositorio vs C/S, verificación vs validación), **siempre cerrá con ventajas/desventajas o un ejemplo**: la cátedra valora que relaciones, no solo que definas.

---

> **Nota de alcance.** Esta guía se construyó sobre **7 finales completos + un compilado de 37 preguntas** y luego se **contrastó íntegramente con las 525 diapositivas oficiales de la cátedra (2024)**, ajustando definiciones, listas y enfoques a lo que efectivamente se enseña (ver "Corrección con las diapositivas oficiales" al inicio). Se cerraron también la **"barrera del mantenimiento"** (G.1, con las cifras de Pfleeger) y la **"recuperabilidad"** (D.5). Único matiz que conviene tener presente: "recuperabilidad" no figura como *principio nombrado* en el deck —ahí está reencuadrada con criterio. Si aparece algún teórico suelto que la nombre distinto, pasámelo y lo termino de calzar.
