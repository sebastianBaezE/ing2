## Estructura del libro 
La estructura del libro está basada en los procesos fundamentales de la ingeniería del software. Está organizado en seis partes, con varios capítulos en cada parte: 
- **Parte 1:** Introduce la ingeniería del software, situándola en un amplio contexto de sistemas y presentando las nociones de procesos y gestión de ingeniería del software. 
- **Parte 2:** Trata los procesos, técnicas y documentación asociados con los requerimientos de ingeniería. Incluye un estudio sobre los requerimientos software, modelado de sistemas, especificación formal y técnicas para especificar la fiabilidad. 
- **Parte 3:** Esta parte está dedicada al diseño de software y a los procesos de diseño. Tres de los seis capítulos se centran en el importante tema de las arquitecturas software. Otros temas incluyen diseño orientado a objetos, diseño de sistemas en tiempo real y diseño de interfaces de usuario.
- **Parte 4:** Describe una serie de aproximaciones a la implementación, incluyendo métodos ágiles, reutilización, CBSE y desarrollo de sistemas críticos. Como los cambios son una parte importante de la implementación, he integrado temas de evolución y mantenimiento en esta parte. 
- **Parte 5:** Se centra en temas de verificación y validación. Incluye capítulos de validación y verificación estática, testeo y validación de sistemas críticos. 
- **Parte 6:** La parte final abarca una serie de lemas de gestión: gestión de personal, estimación de costes, gestión de calidad, procesos de mejora y gestión de cambios.

La ingenieria de software es una disciplina que se interesa en todos los aspectos del desarrollo de software, desde la especificacion de requerimientos primera hasta el mantenimiento del software luego de puesto en operacion. 

**Proceso de software:** el enfoque sistematico empleado para el desarrollo de software. Por lo general todos los procesos software comparten las siguientes etapas: 
- **Elicitacion del software:** donde los ingenieros definen lo que hara el programa y que restricciones tendra en su operacion.
- **Desarrollo de software:** Donde se diseña y se implementa el software.
- **Validacion de softare:** Se verifica que el software funcione y realice las tareas requeridas por el cliente.
- **Evolucion del software:** Etapa donde se mantiene el software, corrigen errores y se lo adapta a las demandas cambiantes del entorno y los clientes.
## Requerimientos
Los requerimientos son descripciones de lo que debe hacer un sistema: el servicio que ofrece y las restricciones en su operacion.
**Funcionales:** Enunciados que describen las tareas que el sistema debe realizar. De como debe reaccionar ante determinaod inputs y como debe comportarse en situaciones especificas. A veces tambien describen lo que no debe hacer el sistema.
**No funcionales:** Describen aspectos que sin ser funcionales son deseables para el usuario, como tiempo de respuesta, seguridad, facilidad de mantenimiento. Los requerimientos no funcionales surgen a través de necesidades del usuario, debido a restricciones presupuestales, políticas de la organización, necesidad de interoperabilidad con otro software o sistemas de hardware, o factores externos como regulaciones de seguridad o legislación sobre privacidad.

### Documento de requerimientos de software - SRS -  IEEE 830
Es una especificación de lo que debe hacer el sistema, donde se detallan los requerimientos del usuario y los requerimientos detallados del sistema. 
 - **Requerimientos del usuario**: son enunciados que especifican que servicios esperan los usuarios que brinde el sistema, junto con las restricciones que debe respetar. 
 - **Requerimientos del sistema:** son descripciones mas detalladas de las funciones, los servicios y las restricciones operacionales del sistema. Detallan que van a implementar los desarrolladores del sistema.
El estandar IEEE 830 - 1998 brinda un modelo generico de lo que debe tener el documento, es como una especie de guia. Esto despues se puede adaptar a las necesidades de la organizacion y lo que convenga para el proyecto. El nivel de detalle que se incluya en un documento depende del tipo de sistema a diseñar y el proceso de desarrollo utilizado. Los sistemas críticos requieren un srs bien detallado y analizado previo a la implementación, para poder garantizar atributos como seguridad y fiabilidad. Si fuese el caso de un desarrollo iterativo interno a la organizacion (hay facil acceso al cliente), entonces el documento suele ser mucho menos detallado y cualquier ambigüedad se resuelve durante el desarrollo. 

## Mejoras de procesos
 
![[Pasted image 20260611104641.png]]

### Medición del proceso 
Se miden atributos del proyecto actual. La meta es mejorar las medidas de acuerdo con los objetivos de la organización implicada.
### Análisis del proceso: 
Se valora el proceso actual y se identifican las debilidades y los cuello de botella del 
proceso. 
El análisis del proceso es el estudio de los procesos para ayudar a entender sus características clave y como las personas que implicadas realizan las tareas para llevarlo a cabo.
### Cambio del proceso: 
Los cambios del proceso son propuestos para atacar debilidades identificadas en el proceso. Luego de esto se repite el ciclo, volviendo a la medición para identificar si hubo mejoras.

### Atributos a mejorar 
![[Pasted image 20260611105714.png]]
## GCS - Gestion de la configuracion de software.

- **¿Qué es?** Al crear software de computadora, ocurren cambios. Y debido a que ocurren, es necesario gestionarlos de manera efectiva. La gestión de confi guración del software (GCS, o Software Confi guration Management, SCM por sus siglas en inglés), es también conocida como gestión del cambio, es un conjunto de actividades diseñadas para gestionar el cambio. 
- **¿Quién lo hace?** Todos los que participan en el proceso de software se involucran en la gestión del cambio en cierta medida, pero algunas veces se crean posiciones de apoyo especializadas para gestionar el proceso de GCS. 
- **¿Por qué es importante?** Si no controla el cambio, este lo controla a uno. Y eso nunca es bueno. Es muy fácil que un flujo de cambios descontrolados convierta un proyecto de software bien ejecutado en un caos. Como consecuencia, la calidad del software sufre y se retrasa la entrega. 
- **¿Cuáles son los pasos?** Puesto que se generan muchos productos de trabajo cuando se crea el software, cada uno debe identifi carse en forma única. Una vez que se logra esto, pueden establecerse mecanismos para el control de versiones y del cambio.
- **¿Que es el producto de trabajo?** Un producto de trabajo es cualquier resultado tangible generado durante el desarrollo de software que debe gestionarse y mantenerse bajo control de versiones y cambios.
**GCS:**
- Es un conjunto de actividades orientadas a gestionar el cambio.
- Es el proceso de Identificar y definir los elementos en el sistema, controlando el cambio de estos elementos a lo largo de su ciclo de vida, registrando y reportando el estado de los elementos y las solicitudes de cambio, y verificando que los elementos estén completos y que sean los correctos.

Los elementos que conforman lo que se produce luego de un proceso de software se englobal colectivamente bajo el concepto de Elementos de Configuracion de Software (ECS).

**¿Cuales podrian ser los elementos de configuracion de software?** 
![[Pasted image 20260612140700.png]]
Cambios en un elemento generalmente generan cambios en varios mas, el control exhaustivo de estos cambios es la GCS.

Estos se pueden subdividir en tres amplias categorias: 
- Programas de computo (codigo fuente o ejecutable).
- Productos de trabajo que describen a los programas de computadora (cualquier tipo de documentacion).
- Datos o contenido.

### Repositorio
Se cuenta con un repositorio, que es la base de datos donde se almacenan todos los ECS y las relaciones entre si. 
Los elementos de configuración de software se relacionan entre si, por lo que un cambio en uno puede afectar a otros
![[Pasted image 20260615141551.png]]

### Linea de referencia/base - "versionado"
- Una línea base es un punto de referencia en el desarrollo del software que queda marcado por el envío de uno o más ECS y su aprobación
- Una especificación o producto que se revisó y acordó de manera formal, que en lo sucesivo sirve como la base para el desarrollo posterior y que puede cambiarse solo a través de procedimientos de control de cambio formales

![[Pasted image 20260615140118.png]]

### El proceso de gestión del cambio
Debe permitir a un equipo de desarrollo de software poder elaborar respuestas a las preguntas: 
- ¿Cómo identifica y gestiona una organización las diferentes versiones existentes de un programa (y su documentación) de forma que se puedan introducir cambios eficientemente?  
- ¿Cómo controla la organización los cambios antes y después de que el software sea distribuido al cliente? 
- ¿Quién tiene la responsabilidad de aprobar y de asignar prioridades a los cambios? 
- ¿Cómo podemos garantizar que los cambios se han llevado a cabo adecuadamente?  
- ¿Qué mecanismo se usa para avisar a otros de los cambios realizados?

El proceso de gestion del cambio define tareas con objetivos precisos con respecto a los ECS que los componen:
- Identificacion de ECS
	- Nombre: cadena de carcteres sin ambiguedad
	- Descripcion: lista de elementos de datos que identifican
	- Tipo de ECS: (Documento, codigo fuente, datos)
	- Identificador del proyecto
	- Informacion de la version y/o cambio
- Control de versiones (basicamente GIT)
	- Herramientas que permitan administrar y almacenar las distintas versiones de los ECS que se crean a lo largo del proceso de software.
- Control de cambios
	- Todo el proceso que conlleva el realizar un cambio, de principio a fin. 
	- Cuando un usuario solicita una modificación, esta se evalúa y puede ser rechazada, pospuesta o aprobada. Si se aprueba, se identifican y extraen los elementos de configuración (productos de trabajo como código, documentos o pruebas), se realizan y auditan los cambios, se ejecutan pruebas de calidad, y finalmente los cambios se integran en una nueva versión del software que es revisada y distribuida a los usuarios.
- Auditar de la configuracion
	- Es la forma de cersiorarse finalmente que el cambio introducido funciona correctamente. 
	- Se analizan los metadatos del proceso de cambio
- Generacion de informes
	- Se documentan los metadatos
	- Responde ¿Qué pasó? ¿Quién lo hizo? ¿Cuándo pasó? ¿Qué más se vio afectado?

## Gestión de proyectos
Un proyecto de software es un esfuerzo temporal, es decir que tiene principio y fin, orientado a crear un producto de software, que esta restringido por alcance, tiempo y costo. 

Gestionar un proyecto es complejo y es importante que se haga de una manera correcta para no sobrepasar las restricciones anteriormente mencionadas. 

Para lograrlo, se ha visto el enfoque de las '4P', personas, procesos, producto y proyecto que busca no solo enfocarse en lo técnico sino en todas las partes involucradas en un proyecto. Todas las personas involucradas se deben organizar para realizar el producto de forma efectiva. Se debe saber el alcance del producto y los objetivos necesarios, analizar requerimientos y alternativas. El marco de actividades que conforman los procesos deben achicar el margen de error humano. Y el proyecto es lo que engloba a todo, como se gestiona, organiza, planifica y monitorea el esfuerzo para evitar el fracaso. 

La gestion del proyecto implica la planeacion, monitoreo y coordinacion de personas, procesos y eventos que ocurren a meidda que el software evoluciona de un conepto preliminar hasta su despliegue operacional completo. 
### Producto de trabajo
Se crea un plan de proyecto y evoluciona a medida que comienzan las actividades del proyecto. El plan es un documento viviente que define el procesos y las tareas a realizar, las personas que realizaran el trabajo y los mecanismos para evaluar riesgos, controlar el cambio y evaluar la calidad. 

### Las 4 P: 
La gestión efectiva de proyectos de software se enfoca en las cuatro P: personas, producto, proceso y proyecto. Las personas deben organizarse para realizar el trabajo de software de manera efectiva. Hay que entender el alcance del producto y los requerimientos. Es necesario seleccionar un proceso que sea apropiado para las personas y el producto. Para planear el proyecto se deben estimar el esfuerzo y el tiempo de calendario para realizar las tareas del trabajo.

### Elementos clave de la gestión de proyectos
- Métricas: medir el proceso, el producto y el proyecto, para trabajar la gestion con datos. 
- Estimaciones: predecir esfuerzo, costo y duracion. 
- Calendario temporal: *Scheduling,* distribuir las tareas en el tiempo.
- Organizacion del personal: generar una estructura de personal efectiva
- Analisis de riesgos: predecir, analizar y elaborar respuestas ante posibles riesgos
- Seguimiento de control: realizar un seguimiento del proyecto, comparar con estimaciones y corregir desvios

¿Por que es necesario identificarlos? Para asegurar que ningun aspecto de la gestion quede sin definir o controlar. Todos estos elementos controlados diferencian a un proyecto exitoso de uno que fracasa. 


## Planificacion
La planificiacion establece una secuencia operativa. Dice que debe hacerse, con que recursos debe hacerse y en que orden. 

**Definición.** La *planificación temporal* (scheduling) distribuye el esfuerzo estimado entre las tareas del proyecto a lo largo del tiempo, definiendo dependencias y asignando recursos.

### Gestión del riesgo

