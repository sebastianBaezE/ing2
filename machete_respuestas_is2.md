# Machete de respuestas — Ingeniería de Software II

> Respuesta **corta y modelo** a cada una de las **37 preguntas del banco** (que cubren también las de los 7 finales). Las definiciones siguen **lo que enseña la cátedra** (Pressman 7ª/9ª, Sommerville, Pfleeger), ya corregidas con las diapositivas oficiales. Cada respuesta remite al bloque de la guía donde está desarrollada (A.x, B.x, …).
> Para el final: respondé esto de memoria y, en las comparaciones, cerrá siempre con un ejemplo o una ventaja/desventaja.

---

## Gestión de proyectos y personas

**1. ¿Qué es y para qué sirve un indicador?** *(B′.1)*
Un **indicador** es una métrica (o combinación de métricas) que da una **visión del proceso, proyecto o producto** para **entender una situación y tomar decisiones / mejorar**. Sirve para evaluar y controlar (ej.: defectos/KLDC indica calidad).

**12. Describa el problema de las 4 P.** *(A.1)*
La gestión de proyectos se organiza en **4 P**: **Personal** (RRHH, el activo más importante), **Producto** (qué se construye; es intangible, cuesta ver el avance), **Proceso** (marco de trabajo que estructura el desarrollo) y **Proyecto** (se planea y controla para manejar su complejidad). El "problema" es atender las 4, no solo lo técnico, porque ahí está la causa real del fracaso.

**17. ¿Qué es un proyecto?** *(A.1)*
Un **esfuerzo temporal** (con principio y fin) para crear un **producto, servicio o resultado único**. Características: **temporal**, **resultado único** y **elaboración gradual** (por incrementos).

**13. ¿Cuáles son los elementos clave de la gestión de proyectos?** *(A.2)*
**Métricas, Estimaciones, Calendario temporal, Organización del personal, Análisis de riesgos y Seguimiento y control.** Juntos cubren todo el proceso de desarrollo (es, de hecho, el índice de toda la gestión).

**14. Describa el modelo MOI.** *(A.3)*
Modelo clásico de **Weinberg** sobre el liderazgo: un buen líder combina **M**otivación (animar al equipo a dar lo mejor), **O**rganización (moldear procesos que conviertan la idea en producto) e **I**nnovación/Ideas (fomentar la creatividad). *(Nota: el deck actual encara el liderazgo con las 5 prácticas de líderes ejemplares —modelar el camino, inspirar visión compartida, desafiar el proceso, permitir que otros actúen, alentar—; si solo piden "MOI", respondé el modelo de Weinberg.)*

**25. Explique el P-CMM.** *(A.4)*
**People-CMM**: modelo de madurez para **gestionar y desarrollar el personal**. Reconoce que la organización debe mejorar de forma continua su capacidad de **atraer, desarrollar, motivar, organizar y conservar** a su gente. Tiene 5 niveles (inicial → gestionado → definido → predecible → en optimización).

**8. Tipos de planificación organizacional vistos.** *(B.1)*
Se refiere a la **planificación organizativa** (organizar al personal). Sus tipos son los **4 paradigmas organizacionales del equipo**:
- **Cerrado**: jerarquía tradicional, comunicación vertical; poco innovador.
- **Abierto**: colaborativo, decisiones consensuadas (democrático); bueno para problemas complejos.
- **Síncrono**: divide el problema en partes con poca comunicación ("divide y vencerás").
- **Aleatorio**: estructura holgada, iniciativa individual, sin líder; bueno para innovar.

---

## Planificación, estimación y PERT

**18. En planificación temporal, ¿qué tareas se hacen para el seguimiento y control?** *(B.2)*
Reuniones periódicas de estado; evaluar las revisiones; verificar el cumplimiento de **hitos**; comparar fechas reales vs planificadas; reuniones informales con el equipo; y usar el **valor ganado** para medir el avance.

**26. Enumere y describa las técnicas de estimación.** *(B.3)*
**Juicio de expertos**, **estimación por analogía** (proyectos similares), **método Delphi** (consenso de expertos por rondas), **descomposición** (estimar por partes con **LDC** o **Puntos de Función**), **modelos algorítmicos** (**COCOMO / COCOMO II**), y técnicas riesgosas como **Ley de Parkinson** y **precio para ganar**. Lo ideal es combinar varias.

**7. Calcule el camino crítico** (tareas A–P, duración total) *(B.4)*

| Act | Pred | Dur | ES | EF | LS | LF | Holg | Crít |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| A | – | 30 | 0 | 30 | 0 | 30 | 0 | ✔ |
| B | A | 10 | 30 | 40 | 30 | 40 | 0 | ✔ |
| C | B | 120 | 40 | 160 | 40 | 160 | 0 | ✔ |
| D | A | 15 | 30 | 45 | 70 | 85 | 55 | ✘ |
| E | A | 80 | 30 | 110 | 50 | 130 | 20 | ✘ |
| F | A | 20 | 30 | 50 | 200 | 220 | 170 | ✘ |
| G | C, I | 45 | 160 | 205 | 160 | 205 | 0 | ✔ |
| H | G | 25 | 205 | 230 | 205 | 230 | 0 | ✔ |
| I | D | 60 | 45 | 105 | 100 | 160 | 55 | ✘ |
| J | B, I | 25 | 105 | 130 | 200 | 225 | 95 | ✘ |
| K | D | 50 | 45 | 95 | 175 | 225 | 130 | ✘ |
| L | D | 30 | 45 | 75 | 195 | 225 | 150 | ✘ |
| M | J, K, L | 5 | 130 | 135 | 225 | 230 | 95 | ✘ |
| N | E | 100 | 110 | 210 | 130 | 230 | 20 | ✘ |
| O | F | 10 | 50 | 60 | 220 | 230 | 170 | ✘ |
| P | C,H,M,N,O | 10 | 230 | 240 | 230 | 240 | 0 | ✔ |

**Duración total = 240 min.** **Camino crítico: A → B → C → G → H → P** (30+10+120+45+25+10 = 240).

**22. Lasaña HOGAREÑAS S.A.** (camino crítico, tiempos, tiempo final) *(B.4)*

| Act | Pred | Dur | ES | EF | LS | LF | Holg | Crít |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| A | – | 30 | 0 | 30 | 6 | 36 | 6 | ✘ |
| B | A | 5 | 30 | 35 | 36 | 41 | 6 | ✘ |
| C | – | 2 | 0 | 2 | 39 | 41 | 39 | ✘ |
| D | C, B | 3 | 35 | 38 | 41 | 44 | 6 | ✘ |
| E | – | 7 | 0 | 7 | 0 | 7 | 0 | ✔ |
| F | E | 25 | 7 | 32 | 7 | 32 | 0 | ✔ |
| G | – | 15 | 0 | 15 | 17 | 32 | 17 | ✘ |
| H | G, F | 10 | 32 | 42 | 32 | 42 | 0 | ✔ |
| I | H | 2 | 42 | 44 | 42 | 44 | 0 | ✔ |
| J | I,F,D,B | 10 | 44 | 54 | 44 | 54 | 0 | ✔ |
| K | – | 15 | 0 | 15 | 39 | 54 | 39 | ✘ |
| L | J, K | 30 | 54 | 84 | 54 | 84 | 0 | ✔ |

**Tiempo total = 84 min.** **Camino crítico: E → F → H → I → J → L.**

**30. Desarrolle un PERT** (análisis de sistemas, tareas A–I) *(B.4)*

| Act | Pred | Dur | ES | EF | LS | LF | Holg | Crít |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| A | – | 4 | 0 | 4 | 0 | 4 | 0 | ✔ |
| B | A | 4 | 4 | 8 | 4 | 8 | 0 | ✔ |
| C | – | 8 | 0 | 8 | 0 | 8 | 0 | ✔ |
| D | B, C | 3 | 8 | 11 | 10 | 13 | 2 | ✘ |
| E | B, C | 8 | 8 | 16 | 8 | 16 | 0 | ✔ |
| F | E | 5 | 16 | 21 | 16 | 21 | 0 | ✔ |
| G | D | 8 | 11 | 19 | 13 | 21 | 2 | ✘ |
| H | F, G | 2 | 21 | 23 | 21 | 23 | 0 | ✔ |
| I | H | 2 | 23 | 25 | 23 | 25 | 0 | ✔ |

**Duración total = 25 días.** Dos caminos críticos: **A → B → E → F → H → I** y **C → E → F → H → I** (ambos 25). D y G tienen holgura 2.

> **Regla de oro PERT** (variante "si la actividad X se demora N"): si X es **crítica**, el proyecto se atrasa N; si X tiene **holgura**, solo se atrasa si **N > holgura** (atraso real = N − holgura).

---

## Riesgos

**3. ¿Qué es un riesgo? ¿Cuáles son los ítems de más alto riesgo según Boehm?** *(C.1, C.3)*
Riesgo = problema **potencial** con dos rasgos: **incertidumbre** (puede ocurrir o no) y **pérdida** (impacto negativo si ocurre). Según **Boehm**, hay que **identificar y supervisar los 10 riesgos de mayor exposición** (los que quedan **por encima de la línea de corte**); el número exacto depende del proyecto.

**9. Característica de todos los riesgos.** *(C.1)*
**Incertidumbre** y **pérdida** (exposición = probabilidad × impacto).

**23. ¿Cómo se clasifican los riesgos?** *(C.1)*
Por **categoría**: del **proyecto** (calendario, presupuesto, recursos), del **producto** (calidad/requerimientos) y del **negocio** (estratégico, gerencial, de mercado). Por **tipo**: **genéricos** vs **específicos**, y cada uno puede ser **conocido, predecible o impredecible**.

**31. Enumere las actividades del análisis de riesgo.** *(C.2)*
El proceso de gestión de riesgos tiene 4 etapas: **1) Identificación, 2) Análisis** (probabilidad e impacto → priorización), **3) Planeación** (anulación/contingencia) y **4) Supervisión**. Es iterativo y se documenta.

---

## Diseño

**19. ¿Cuáles son los tipos (áreas) de diseño de software? Describa.** *(D.1)*
Cuatro: **diseño de datos** (estructuras de datos a partir del modelo del dominio), **diseño arquitectónico** (estructura global del sistema), **diseño de interfaz** (comunicación usuario↔sistema) y **diseño a nivel de componentes** (lógica interna de cada módulo).

**32. Describa los fundamentos del diseño. ¿Qué es la cohesión funcional? Describa los grados de cohesión.** *(D.2, D.3)*
Fundamentos: **abstracción, modularidad, ocultación de información, refinamiento e independencia funcional**. **Cohesión funcional** = el grado más alto: todo el módulo contribuye a **una única función** bien definida. Grados (de peor a mejor): coincidental → lógica → temporal → procedimental → comunicacional → secuencial → **funcional**.

**35. Describa el concepto de cohesión y sus grados.** *(D.3)*
**Cohesión** = grado en que los elementos *dentro* de un módulo se relacionan y aportan a una sola tarea; **se busca alta**. Grados: coincidental → lógica → temporal → procedimental → comunicacional → secuencial → **funcional** (la mejor).

**16. Enumere y describa los principios de diseño.** *(D.5)*
Los **10 principios del modelado de diseño** (Pressman): rastreable a requerimientos; considerar la arquitectura; datos tan importantes como funciones; cuidar las interfaces; ajustar la UI al usuario; componentes funcionalmente independientes; bajo acoplamiento; representaciones fáciles de entender; diseño iterativo; y que no impida una metodología ágil.

**10. Definición de recuperabilidad (principio de diseño).** *(D.5)*
Capacidad de que el sistema y el usuario **se recuperen de errores y fallas** minimizando la pérdida de información. Se logra con **deshacer/interrumpir** y confirmación de acciones (regla de Mandel "dar control al usuario") y con **copias de seguridad** y **pruebas de recuperación** a nivel sistema. *(En Sommerville es uno de los 6 principios de UI; conviene mencionarlo.)*

**4 / 28. Consideraciones al diseñar / desarrollar una interfaz de usuario.** *(D.6)*
Aplicar las **reglas doradas de Mandel**: **dar control al usuario** (incluye interrumpir/deshacer), **reducir la carga de memoria** y **lograr consistencia**; sumar **factores humanos** y **diversidad de usuarios**; cuidar la **usabilidad** (Donahue) y seguir un **proceso iterativo centrado en el usuario** (analizar tareas → prototipo en papel → evaluar → prototipo dinámico → evaluar → UI definitiva).

---

## Arquitectura

**15. ¿Qué define el diseño arquitectónico? Describa los tipos de organización del sistema.** *(D.4)*
Define la **estructura global**: organización del sistema, descomposición en módulos y estilo de control. Tipos de **organización del sistema**: **repositorio** (datos en una base compartida), **cliente-servidor** (servicios distribuidos por red) y **capas** (máquina abstracta), o combinaciones.

**24. ¿Cómo puede ser la organización del sistema?** *(D.4)*
**Repositorio**, **cliente-servidor** o **por capas** (o combinaciones).

**11. Diferencia entre modelo repositorio y modelo cliente-servidor.** *(D.4)*
**Repositorio**: datos **centralizados** en un modelo común → eficiente para grandes volúmenes, pero acoplamiento alto, difícil de distribuir y punto único de falla. **Cliente-servidor**: servicios **distribuidos** por red → escalable y distribuible, pero sin modelo de datos único y con rendimiento dependiente de la red.

**2. ¿Qué requerimientos no funcionales se ven afectados por la arquitectura?** *(D.4)*
Principalmente **rendimiento**, **seguridad**, **disponibilidad/fiabilidad** y **mantenibilidad** (Sommerville). Ej.: para seguridad conviene una arquitectura **en capas**, protegiendo los recursos críticos en las capas internas.

---

## Verificación y validación (testing)

**20. ¿Qué es verificación? ¿Qué es validación? ¿Cuál prueba verifica y cuál valida?** *(Bloque E)*
**Verificación**: ¿estamos construyendo el producto **correctamente**? (cumple la especificación). **Validación**: ¿estamos construyendo el producto **correcto**? (satisface al usuario). Unitarias e integración → verificación; aceptación → validación; sistema → entre ambas.

**27. Defina y diferencie pruebas de caja blanca y caja negra. Dé un ejemplo.** *(Bloque E)*
**Caja blanca** (estructural): se mira el **código**; se prueban caminos/condiciones/bucles. *Ej.: prueba del **camino básico** con complejidad ciclomática.* **Caja negra** (funcional): no se mira el código; se prueban **entradas/salidas** contra la interfaz. *Ej.: **partición de equivalencia / valores límite** (campo 1–100 → probar 0, 1, 100, 101).*

**33. Enumere las técnicas de validación que conozca.** *(Bloque E)*
Pruebas de **caja negra** (funcionales), pruebas de **sistema** y de **aceptación** (con el usuario/datos reales), **pruebas de recuperación**, y **revisiones/inspecciones**. Validar = comprobar que es lo que el usuario necesita.

**36. Defina las estrategias de integración.** *(Bloque E)*
**Big-bang** (todo junto), **incremental descendente / top-down** (de arriba hacia abajo, con **stubs**), **incremental ascendente / bottom-up** (de abajo hacia arriba, con **drivers**) y **sándwich** (combinación). La incremental localiza fallas más fácil.

---

## Configuración (GCS)

**5. ¿Qué es la gestión de configuración? Defina línea base y ejemplifique.** *(Bloque F)*
**GCS**: actividades para **identificar, controlar y auditar los cambios** de los artefactos del software a lo largo de todo el ciclo. **Línea base (IEEE)**: especificación o producto **formalmente revisado y aprobado**, que sirve de base para el desarrollo posterior y **solo se cambia por procedimiento formal**. *Ej.: la especificación de requisitos, una vez aprobada, se vuelve línea base.* (Proceso: identificación, control de versiones, control de cambios, auditoría, informes.)

---

## Mantenimiento

**34. ¿Qué tipos de mantenimiento conoce? Defina ingeniería inversa y reingeniería.** *(G.1)*
Tipos: **correctivo** (corregir errores), **adaptativo** (adaptar al entorno), **perfectivo** (mejoras/funciones) y **preventivo** (prevenir problemas futuros). **Ingeniería inversa**: recuperar diseño/especificación a partir del código (no modifica). **Reingeniería**: rehacer/reestructurar el sistema (combina ingeniería inversa + reestructuración + ingeniería directa) para mejorarlo.

**37. ¿Qué es la barrera del mantenimiento?** *(G.1)*
Fenómeno (Pfleeger) por el cual mantener el software genera **altos costos adicionales** (40–70 % del costo total) que terminan **frenando el desarrollo de software nuevo**: la organización queda atrapada sosteniendo lo viejo. Se combate con **mantenimiento preventivo** y **rejuvenecimiento/reingeniería**.

**6 / 21. Rejuvenecimiento del software (y tipos).** *(G.2)*
Desafío del mantenimiento que busca **aumentar la calidad global** de un sistema existente, reformándolo para hacerlo más comprensible. **4 tipos** (Pfleeger): **re-documentación**, **re-estructuración**, **ingeniería inversa** y **re-ingeniería**.

---

> **Cómo usarlo:** tapá la respuesta, leé la pregunta y respondé en voz alta; si dudás, abrí el bloque indicado en la guía. Las preguntas 7, 22 y 30 (PERT) practicalas **rehaciéndolas en papel**, no solo leyendo la tabla.
