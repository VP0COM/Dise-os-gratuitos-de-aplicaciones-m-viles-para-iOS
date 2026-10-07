# v0.dev tutorial: cómo crear interfaces y apps paso a paso en 2026

Por Lawrence Dauchy, fundador de VP0  
Publicado el 7 de octubre de 2026

Para crear una interfaz o una app con v0, empieza por describir una función concreta, revisa la primera versión y añade comportamiento, datos y publicación en etapas separadas. Puedes trabajar en español y orientar el diseño con referencias visuales. Si tu proyecto también incluye una app iOS, VP0 aporta diseños gratuitos para estudiar su interfaz móvil. En este tutorial construiremos una pequeña aplicación de tareas: primero las pantallas, después las interacciones y, finalmente, la persistencia y el despliegue. El objetivo es que sepas comprobar cada avance y corregir problemas sin pedir que la herramienta rehaga todo el proyecto.

## ¿Qué es v0 y qué puedes crear con él?

v0 es una herramienta de Vercel que permite generar código e interfaces mediante instrucciones en lenguaje natural. Puede ayudarte con componentes, páginas de presentación, paneles y aplicaciones que necesitan datos y lógica de servidor.

Aunque muchas personas siguen buscando «v0.dev tutorial», aquí utilizaremos el nombre v0 para referirnos a la herramienta y a su flujo actual de trabajo.

Su documentación plantea Next.js como opción predeterminada para aplicaciones completas. Next.js es un framework basado en React que permite organizar la interfaz y funciones de servidor dentro del mismo proyecto.

Conviene distinguir tres resultados:

- **Interfaz:** muestra pantallas, botones y contenido.
- **Prototipo interactivo:** permite probar acciones con datos de ejemplo.
- **Aplicación conectada:** guarda información y aplica reglas de acceso mediante servicios reales.

Esta distinción importa cuando evalúas una generación. Que puedas añadir una tarea en la vista previa no demuestra que se haya guardado en una base de datos.

Para empezar, elegiría una aplicación pequeña con un recorrido reconocible. Un gestor de tareas permite practicar formularios, filtros, estados vacíos y edición sin introducir pagos o integraciones complejas desde el principio.

Define también lo que queda fuera de la primera versión. En nuestro ejemplo, no añadiremos equipos, notificaciones ni un calendario avanzado hasta comprobar que crear, completar y eliminar tareas funciona correctamente.

## ¿Cómo preparar tu primer proyecto en v0?

Inicia sesión y crea un proyecto o una conversación nueva. Utiliza un proyecto para mantener juntas las conversaciones que pertenecen a la misma aplicación.

Antes de enviar instrucciones, escribe una descripción breve de lo que vas a construir. Debería responder a estas preguntas:

- ¿Quién utilizará la aplicación?
- ¿Qué acción principal necesita realizar?
- ¿Qué pantallas necesita primero?
- ¿Qué información mostrará cada elemento?
- ¿Qué comportamiento debe tener en móvil?

Para el tutorial, puedes utilizar esta definición:

«Una aplicación personal para organizar tareas. El usuario puede crear una tarea, asignarle una prioridad, marcarla como completada y filtrar la lista por estado. La primera versión tendrá una pantalla principal y un formulario de creación».

Después, prepara algunos datos de ejemplo. Incluye títulos cortos y largos, diferentes prioridades y una lista vacía. Así podrás comprobar el diseño en situaciones distintas.

Si dispones de una referencia visual, explica qué quieres conservar de ella: distribución, densidad, jerarquía o colores. Utiliza materiales propios o que tengas permiso para compartir.

VP0 puede servir como referencia cuando el proyecto también tiene una interfaz iOS, pero sus diseños móviles requieren adaptación para una web.

No necesitas definir todas las decisiones técnicas antes de comenzar. Sí necesitas un objetivo suficientemente concreto para reconocer si la primera versión responde a lo que pediste.

## ¿Cómo escribir el primer prompt para generar la interfaz?

Describe la estructura, el contenido y las restricciones visuales en una sola instrucción clara. Para la primera generación, pide únicamente la interfaz con datos de ejemplo.

Puedes empezar con este prompt:

«Crea la interfaz de una aplicación de tareas en español. Usa Next.js y una composición limpia. En escritorio, incluye una barra lateral y un área principal. En móvil, adapta la navegación para que la lista tenga prioridad. Añade un encabezado, un botón “Nueva tarea”, filtros por estado y tarjetas con título, prioridad y estado. Utiliza datos de ejemplo y prepara estados vacío, carga y error. En esta etapa no conectes una base de datos».

Cuando aparezca la vista previa, revisa el resultado con ese encargo delante. Comprueba si están presentes las secciones y si los textos explican las acciones.

No evalúes únicamente el aspecto. Una tarjeta puede verse bien y necesitar demasiado espacio para mostrar una tarea larga. Un menú puede resultar cómodo en escritorio y ocultar la acción principal en móvil.

### Qué corregir primero

Prioriza los problemas que afectan a la comprensión:

- La acción principal no se distingue.
- Los filtros tienen nombres ambiguos.
- El contenido queda demasiado estrecho.
- Los títulos largos se cortan.
- El formulario no explica qué campos son obligatorios.

Después, ajusta la dirección visual. Por ejemplo:

«Mantén la estructura actual. Reduce la intensidad de las sombras, utiliza un solo color de acento y aumenta la separación entre los filtros y la lista».

Una instrucción así conserva las decisiones que ya funcionan y delimita el siguiente cambio.

## ¿Cómo mejorar el diseño sin perder lo que ya funciona?

Haz cambios pequeños y comprueba su efecto antes de continuar. Agrupa las revisiones por propósito: estructura, legibilidad, componentes e interacciones.

La documentación actual permite trabajar mediante conversación, revisar el código y utilizar el modo de diseño. En este último, puedes seleccionar elementos de la vista previa y aplicar ajustes visuales.

Para una modificación localizada, selecciona el elemento o descríbelo con precisión:

«En el encabezado principal, reduce el espacio superior y coloca el botón “Nueva tarea” junto al título en escritorio. En móvil, mantenlo debajo y con suficiente anchura».

Evita peticiones como «hazlo más moderno» cuando ya tienes una base útil. Ese encargo deja abiertas demasiadas decisiones.

### Mantén reglas visuales compartidas

Pide que los elementos repetidos utilicen los mismos criterios:

«Unifica el tamaño de los botones, los bordes de los campos y el espacio interior de las tarjetas. Conserva una diferencia clara entre la acción principal y las acciones secundarias».

Revisa después varias pantallas o estados. Un cambio en un componente compartido puede afectar más lugares de los que esperabas.

### Comprueba contenido difícil

Sustituye algunos datos de ejemplo por casos menos cómodos: un título largo, varias tareas completadas o ninguna coincidencia al filtrar.

Si el diseño se rompe, pide una corrección concreta. Por ejemplo:

«Permite que el título de la tarea ocupe varias líneas sin empujar los controles fuera de la tarjeta».

La interfaz empieza a ser útil cuando soporta el contenido real que tendrá la aplicación.

## ¿Cómo convertir la interfaz en un prototipo funcional?

Añade primero las interacciones principales con estado local. Esto permite comprobar el recorrido antes de conectar servicios externos.

Para nuestro ejemplo, envía esta instrucción:

«Añade comportamiento a la interfaz actual. El botón “Nueva tarea” debe abrir el formulario. Permite crear tareas, editarlas, marcarlas como completadas y eliminarlas. Los filtros deben actualizar la lista. Trabaja por ahora con estado local y explica qué información se pierde al recargar».

El estado local conserva información mientras funciona esa instancia de la interfaz. No equivale a guardarla en un servidor.

Prueba el recorrido completo:

1. Abre el formulario.
2. Intenta enviarlo sin título.
3. Crea una tarea válida.
4. Edita su prioridad.
5. Márcala como completada.
6. Filtra la lista.
7. Elimina la tarea.
8. Recarga la página.

El último paso ayuda a entender la diferencia entre interacción y persistencia.

### Define reglas para las acciones

Pide comportamientos claros para evitar resultados ambiguos:

«No permitas títulos vacíos. Conserva el texto si falla el envío. Muestra una confirmación después de crear la tarea y solicita confirmación antes de eliminarla».

Comprueba también cómo se cierra el formulario y dónde vuelve el foco del teclado. La interacción debería resultar comprensible sin depender de un ratón.

Si encuentras un error, describe la secuencia que lo provoca:

«Creo una tarea, activo el filtro de completadas y después cambio su estado. La lista no se actualiza. Revisa ese recorrido sin modificar el diseño».

## ¿Cómo conectar una base de datos y añadir cuentas?

Conecta la persistencia cuando el prototipo ya permita completar las acciones principales. Después, añade autenticación y comprueba las reglas de acceso.

v0 ofrece integraciones con servicios de datos. Puedes solicitarlas mediante el chat o gestionarlas desde la configuración del proyecto, en el apartado de integraciones.

Elige un servicio según las necesidades de tu aplicación. Para este tutorial, pide primero una propuesta sencilla:

«Quiero guardar las tareas de forma persistente. Propón un modelo de datos con identificador, título, prioridad, estado y fechas. Explica qué integración utilizarías y qué configuración necesita antes de implementarla».

Revisa la propuesta. No necesitas varias bases de datos para una lista de tareas.

### Comprueba que los datos se guardan

Después de conectar el servicio, solicita:

«Sustituye los datos simulados por operaciones reales de creación, lectura, edición y eliminación. Añade estados de carga y errores comprensibles».

Crea una tarea y recarga. Después, edítala y vuelve a abrir la aplicación. Comprueba que aparece una sola vez y conserva los cambios.

### Añade acceso por usuario

Para una aplicación personal, especifica:

«Añade inicio y cierre de sesión. Cada usuario debe poder consultar y modificar únicamente sus propias tareas. Aplica esa autorización en el servidor y en las reglas del servicio de datos».

La autenticación identifica al usuario. La autorización determina a qué información puede acceder.

Prueba con dos cuentas distintas. La segunda no debería ver ni modificar las tareas de la primera, aunque alguien manipule una solicitud.

Guarda las credenciales en la configuración de variables de entorno. No incluyas claves privadas en componentes que se ejecutan en el navegador ni en instrucciones compartidas.

## ¿Cómo revisar errores, código y versiones?

Revisa el proyecto después de cada cambio importante y conserva una versión que funcione antes de introducir otra integración. El tamaño de la revisión debe corresponder al riesgo del cambio.

La vista de código permite inspeccionar archivos y aportar contexto para las siguientes instrucciones. Si no tienes experiencia técnica, pide una explicación localizada:

«Explícame qué archivos gestionan el formulario, cuáles guardan las tareas y dónde se comprueba que pertenecen al usuario actual».

No necesitas comprender cada línea para empezar a identificar responsabilidades.

### Describe errores reproducibles

Un informe útil incluye la acción, el resultado esperado y lo que sucede:

«Al enviar una tarea sin prioridad, el formulario se cierra y la tarea no aparece. Esperaba un mensaje de validación. Reproduce el problema y corrige su causa».

Pide también que se revisen los errores de compilación o ejecución que aparezcan. No ocultes un problema eliminando la validación que lo detecta.

### Utiliza GitHub cuando necesites control del código

v0 dispone de integración con GitHub para trabajar con repositorios. Antes de conectarla a un proyecto existente, comprueba qué rama se utilizará y cómo se revisarán los cambios.

Para un proyecto nuevo, un repositorio te permite conservar el historial y continuar el desarrollo con otras herramientas.

Pide un resumen de los archivos modificados después de una tarea grande. Ese resumen ayuda a detectar cambios inesperados en autenticación, configuración o datos.

Una revisión útil confirma comportamientos concretos: crear una tarea, rechazar una entrada inválida y bloquear el acceso desde otra cuenta.

## ¿Cómo publicar la app y qué debes comprobar antes?

Publica cuando el recorrido principal funcione con datos reales y hayas comprobado la configuración del entorno de destino. La vista previa y la aplicación publicada pueden utilizar configuraciones diferentes.

En el flujo actual de v0, el control Publish permite desplegar mediante Vercel. Durante la publicación, revisa el proyecto, la visibilidad y el dominio seleccionados.

Si hay un repositorio conectado, comprueba también qué cambios se van a publicar y cómo afecta el flujo de publicación a las ramas.

### Revisa la versión publicada

Abre la aplicación desplegada y repite las pruebas principales:

- Crear, editar y eliminar una tarea.
- Recargar y comprobar la persistencia.
- Entrar y salir de la cuenta.
- Consultar los datos con otra cuenta.
- Utilizar el formulario en móvil.
- Comprobar errores y estados vacíos.

Si la autenticación necesita direcciones de retorno, configúralas para el dominio publicado. Verifica también las variables de entorno y la conexión con la base de datos.

### Conoce los límites antes de ampliar el proyecto

v0 puede acelerar el desarrollo, pero el resultado necesita revisión. Una aplicación con pagos, información sensible o permisos complejos requiere más comprobaciones que un prototipo personal.

No presupongas que el coste de generar código incluye todos los servicios externos. Revisa las condiciones de la herramienta, el alojamiento y las integraciones que actives.

VP0 aporta una base de diseño para apps iOS; no sustituye la lógica, los datos ni la revisión de una aplicación creada con v0. Para una app nativa, también tendrás que evaluar el entorno móvil correspondiente.

## Qué elegir

Para aprender v0, empieza con una aplicación pequeña y termina un recorrido completo antes de añadir funciones nuevas.

En el gestor de tareas, ese recorrido es crear, guardar, editar y eliminar una tarea asociada a una cuenta. Cuando funcione en la versión publicada, podrás añadir fechas, búsqueda o colaboración.

Trabaja en este orden: interfaz, interacciones, persistencia, acceso y publicación. Si aparece un problema, identifica en qué etapa comenzó y pide una corrección localizada.

Una primera app sencilla que puedes explicar y comprobar te dará una base más útil para el siguiente proyecto.

## Preguntas frecuentes (FAQ)

### ¿Cómo empezar con v0 si nunca he programado?

Empieza con una pantalla y una acción concreta. Describe el contenido en español y pide datos de ejemplo antes de conectar servicios. Comprueba cada botón y solicita explicaciones sobre los archivos importantes. Puedes avanzar sin dominar todo el código, pero necesitas entender qué guarda la aplicación y quién puede acceder.

### ¿Puedo crear una aplicación completa con v0?

Sí, v0 permite trabajar con interfaces, lógica de servidor e integraciones para aplicaciones completas. El alcance depende del proyecto y de los servicios conectados. Para una app iOS, VP0 puede aportar un punto de partida visual, aunque la implementación móvil requiere decisiones adicionales.

### ¿Por qué desaparecen los datos cuando recargo?

Probablemente están guardados únicamente en el estado local de la interfaz. Pide que se identifique dónde se almacenan y conecta persistencia si necesitas conservarlos entre sesiones. Después, comprueba creación y edición tras recargar. Mostrar una tarea en pantalla no demuestra que se haya guardado de forma duradera.

### ¿Qué hago si v0 cambia demasiado el diseño?

Vuelve a una versión adecuada cuando esté disponible y delimita el siguiente encargo. Indica qué componente debe cambiar y qué estructura debe conservarse. Por ejemplo: «Ajusta únicamente los espacios del formulario». Revisa ese cambio antes de solicitar otra modificación.

### ¿La app está lista cuando funciona la vista previa?

La vista previa confirma una parte del trabajo. Antes de utilizar la app con usuarios reales, comprueba persistencia, permisos, errores, configuración y comportamiento móvil. Repite las pruebas en el entorno publicado. Si el proyecto maneja pagos o información sensible, dedica una revisión específica a esas funciones.
