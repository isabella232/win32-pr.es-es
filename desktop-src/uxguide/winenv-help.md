---
title: Ayuda
description: Use la Ayuda como mecanismo secundario para ayudar a los usuarios a completar y comprender mejor las tareas \8212; el mecanismo principal es la propia interfaz de usuario. Aplique estas directrices para que el contenido sea realmente útil y fácil de encontrar.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2a71abf4b90aeaf19f43997c5d8e98ad42f56d5daa86699ff8504ca5a3080bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935841"
---
# <a name="help"></a>Ayuda

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Use la Ayuda como mecanismo secundario para ayudar a los usuarios a completar y comprender mejor las tareas, ya que el mecanismo principal es la propia interfaz de usuario. Aplique estas directrices para que el contenido sea realmente útil y fácil de encontrar.

Un sistema de Ayuda se compone de varios tipos de contenido diseñados para ayudar a los usuarios cuando no pueden completar una tarea, quieren comprender un concepto con más detalle o necesitan más detalles técnicos de los que están disponibles en la interfaz de usuario.

En este artículo, nos referimos a la Ayuda como secundaria a la interfaz de usuario. La interfaz de usuario es principal porque es donde los usuarios primero intentan resolver sus problemas. Consultan el sistema de Ayuda solo si no pueden realizar su tarea con la interfaz de usuario.

![captura de pantalla de la página de ayuda y soporte técnico de Windows ](images/winenv-help-image1.png)

La Windows principal ayuda y soporte técnico, disponible en la página menú Inicio.

**Nota:** Las directrices [relacionadas con el estilo y el tono](text-style-tone.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿Qué motivación tienen los usuarios de destino?** Entre más motivadas estén en descubrir la funcionalidad del programa y convertirse en usuarios intermedios o incluso avanzados de él, más dispuestos estarán a investigar las respuestas a sus preguntas mediante la consulta de temas de Ayuda.
-   **¿Usa ayuda para corregir una interfaz de usuario no buena?** Entre mejor sea la interfaz de usuario, menos usuarios buscarán ayuda adicional. Si el programa tiene una interfaz de usuario principal muy clara y útil (como mensajes de error sin jerga, asistentes bien escritos y cuadros de diálogo inequívocos), es posible que no necesite un sistema de Ayuda secundario en absoluto.
-   **¿El programa es relativamente sencillo?** Si es así, considere la posibilidad de incorporar todo el contenido de asistencia necesario en las superficies principales de la interfaz de usuario. Es más probable que los usuarios busquen ayuda adicional en programas que realizan tareas complejas.
-   **¿La aplicación está pensada para desarrolladores, profesionales de TI u otros expertos en software?** Estos usuarios tienden a esperar ayuda de referencia para las convenciones del lenguaje de programación y ayuda conceptual detallada para el dominio de las características.

## <a name="design-concepts"></a>Conceptos de diseño

Si decide incluir ayuda en el programa, inténtela en el diseño general. La interfaz de ayuda debe ser sencilla, eficaz y pertinente. debe permitir que los usuarios obtengan ayuda fácilmente y, a continuación, vuelvan a su tarea. Piense en el sistema de Ayuda en términos de tiempo de los usuarios: minimice la interrupción primero anticipando dónde se encontrarán con problemas en el programa y, a continuación, resolviendo esos problemas mediante la incorporación de asistencia fundamental directamente en la interfaz de usuario y la creación de puntos de entrada claros y coherentes en la Ayuda más detallada.

Windows asistencia se diseñó según estos principios. Estos son algunos de los cambios de diseño en la experiencia Windows ayuda del usuario:

-   Puntos de entrada más reconocibles a la Ayuda desde la interfaz de usuario principal (especialmente nuevos vínculos de Ayuda desde superficies de interfaz de usuario, como cuadros de diálogo, mensajes de error y asistentes). Los vínculos de Ayuda le llevan directamente al tema pertinente de la Ayuda.
-   Hay un icono de botón Ayuda disponible en la esquina superior derecha de la mayoría de las Panel de control centrales, así como en las carpetas de shell.
-   Los usuarios pueden optar por obtener el contenido de ayuda más actualizado de Windows Ayuda y soporte técnico en línea cuando están en línea.
-   Los temas de ayuda ahora se basan en tareas en lugar de en características, para que los usuarios puedan realizar sus tareas de forma rápida y eficaz.
-   Los temas de ayuda ahora se basan en gran medida en escenarios de usuario principales conocidos.
-   Los temas de ayuda tienen un tono más [relajada](text-style-tone.md)e informal, con lenguaje real.
-   Los temas de ayuda están diseñados para un análisis eficaz, ya que los usuarios rara vez leen el contenido palabra por palabra.

### <a name="an-analogy-for-help"></a>Una analogía de la Ayuda

Para pensar en mayor profundidad sobre el diseño del sistema de Ayuda, considere una analogía de la vida diaria. Se pierde en una ciudad desconocida. ¿Qué puede hacer? Muchos reaccionarían de la siguiente manera:

-   Obtener orientado; busque puntos de referencia, signos de calle (nombres y punteros a lugares).
-   Busque mapas.
-   Por último, como último recurso, pida instrucciones o llame a un amigo.

El diseño de la "interfaz" de la ciudad afecta a la necesidad de ayuda. Las calles bien etiquetadas, las direcciones explícitas (punteros a hospitales, aeropuertos, vecinos y oficinas postales) y puntos de referencia claros, como características geográficas o edificios destacados, le ayudan a encontrar el camino.

Pide ayuda como último recurso. Es una indicación de que la "interfaz" de la ciudad no se ha diseñado correctamente y es confusa. Es más probable que pida ayuda en un lugar que tenga una etiqueta específica que sugiere utilidad. Por ejemplo, es más probable que pida ayuda en un lugar con la etiqueta "Directions" o "Information" que en un lugar general como el City Hall, aunque casi cualquier persona del City Hall pueda darle instrucciones.

Cuando pide ayuda, lo más probable es que esté frustrado y solo quiera llegar a su destino previsto. Probablemente no esté deseando dedicar tiempo a dar un paseo por la ciudad o a aprender sobre su historia. Además, la motivación depende de la importancia de la tarea. Si está intentando encontrar la habitación de hotel, hará lo que sea necesario. Sin embargo, si el objetivo es encontrar un lugar de importancia menor, lo más probable es que simplemente se des porte después de un esfuerzo moderado.

Todos estos aspectos de la búsqueda en el espacio real se corresponden con la forma en que los usuarios suelen encontrar su camino en el espacio virtual del programa. Buscar ayuda más allá de la interfaz de usuario principal es por su naturaleza desorienta; Haga todo lo posible para mitigar esta experiencia mediante una interfaz de usuario bien diseñada y "señales de calle" inteligentes para dirigir a los usuarios a las respuestas que necesitan.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Diseño de la interfaz de usuario para que la Ayuda no sea necesaria

Intente que la Ayuda sea innecesaria en primer lugar, por:

-   Hacer que las tareas comunes se detecte y realicen fácilmente.
-   Proporcionar instrucciones [principales claras](text-ui.md).
-   Proporcionar etiquetas de control claras y concisas orientadas a objetivos y tareas.
-   Proporcionar instrucciones complementarias y explicaciones cuando sea necesario.
-   Anticipar problemas evitables mediante controles restringidos a opciones válidas, proporcionar valores predeterminados adecuados, controlar todos los formatos de entrada y evitar errores.
-   Escribir mensajes de error que proporcionen una solución o acción clara para que el usuario pueda realizarla.
-   Evitar diseños de interfaz de usuario confusos, como tareas con un flujo deficiente o el uso de controles que están deshabilitados sin motivo aparente.
-   Trabajar con escritores y editores al principio del ciclo de desarrollo para crear texto de interfaz de usuario coherente y de [alta calidad](text-ui.md) en todo el programa.

Los usuarios no deben tener que ir a otro lugar para averiguar cómo usar la interfaz de usuario. Agregue información esencial directamente a la interfaz de usuario principal, en lugar de obligar a los usuarios a salir de su contexto inmediato y en el panel Ayuda. Si solo existe información importante en un tema de Ayuda, es muy posible que los usuarios no la vean. Para obtener información opcional y más explicativa, use vínculos de Ayuda de la interfaz de usuario principal al tema de Ayuda correspondiente para obtener ayuda complementaria.

### <a name="considering-user-motivation"></a>Consideración de la motivación del usuario

Para la mayoría de los usuarios, la velocidad y la eficacia se encuentran entre las principales virtudes de los buenos programas. Los usuarios quieren realizar su trabajo. Por lo general, no están interesados en aprender sobre el programa y la tecnología por sí mismos. su paciencia se extiende solo en la medida en que ese programa atiende sus propios intereses y resuelve los problemas que se están teniendo.

Diseñe el sistema de Ayuda para que coincida con la motivación de los usuarios. Por ejemplo, considere un usuario que ha llegado a un quiosco en un hotel. Si no puede averiguar cómo realizar la tarea rápidamente, es probable que simplemente se dé por hecho y se vaya. Es poco probable que pase tiempo con ayuda. Como alternativa, un usuario altamente motivada tiene una mayor tolerancia al tiempo dedicado a investigar las respuestas en el sistema de ayuda. Un usuario empresarial que debe equilibrar los libros, por ejemplo, probablemente esté dispuesto a consultar contenido de ayuda para sacar el máximo partido de esa nueva aplicación de contabilidad.

### <a name="writing-content-for-scanning"></a>Escribir contenido para el examen

Escribir temas de Ayuda sabiendo que se examinarán para obtener información específica, no leer palabra por palabra. Escriba de forma concisa, llegar al punto rápidamente y proporcionar información sobre la que los usuarios puedan actuar.

-   Escriba temas de procedimientos mediante pasos numerados en un formato coherente para que los usuarios reconozcan que están recibiendo asistencia de procedimientos.
-   Escribir temas de referencia con facilidad de análisis en mente, mediante tablas, por ejemplo, para presentar opciones de interfaz de usuario o sintaxis de lenguaje.
-   Escriba temas conceptuales organizados lógicamente por subpartidas, de modo que el usuario pueda omitir secciones enteras de menor interés.

En todo el contenido de ayuda, es más fácil examinar listas con viñetas que los bloques de párrafo estándar de texto; Sin embargo, use listas de viñetas de forma judiosa, no como una muleta para el material no organizado.

### <a name="creating-content-that-matters"></a>Creación de contenido que importa

Dado que ningún sistema de Ayuda puede prever todas las preguntas que pueda tener cada usuario, centre la mayor parte del contenido en responder a las principales preguntas de los escenarios principales para los usuarios de destino. Por ejemplo, la búsqueda eficaz y cómo establecer la conectividad de red (entre otras tareas) pueden ser temas muy solicitados. Además, céntrate en las tareas dentro de los principales escenarios de usuario, en lugar de documentar exhaustivamente una característica o tecnología por su propio bien.

**Sugerencia:** El soporte técnico es una buena fuente de contenido de Ayuda. A menudo, los servicios de asistencia mantienen registros de las preguntas más frecuentes sobre determinados programas o tareas que los usuarios intentan (y no logran) realizar.

No es necesario proporcionar ayuda para todas las características de la interfaz de usuario. **A menudo, la ayuda poco útil resulta de intentar crear ayuda para todo.** Si la interfaz de usuario está bien diseñada, la mayoría de estos temas de Ayuda no serán muy útiles. simplemente restablecerán lo obvio.

Si hay más de una manera de realizar una tarea, en la mayoría de los casos solo puede documentar la manera más común que usan los usuarios sin experiencia. Entre las excepciones a esto se incluyen consideraciones de accesibilidad (documentando equivalentes de teclado de acciones del mouse, por ejemplo) y consideraciones de plataforma (documentación para el factor de forma de tableta, por ejemplo, o para entornos de servidor en los que la línea de comandos puede sustituir por la interfaz gráfica de usuario).

Recuerde que los usuarios no suelen pensar en los problemas que se encuentran exactamente en los mismos términos que usted. Por ejemplo, es posible que a los usuarios le resulta extraño pensar en sí mismos como una "cuenta". Asegúrese de diseñar la funcionalidad de búsqueda e indexación, a continuación, para tener en cuenta las variaciones y sinónimos de terminología probables.

Sin embargo, entre la interfaz de usuario principal y el sistema de Ayuda, los términos deben ser muy similares si no son idénticos. Los usuarios se pueden confundir cuando el lenguaje del sistema de Ayuda no se correlaciona muy estrechamente con lo que ven en la pantalla.

### <a name="writing-compelling-help-link-text"></a>Escribir texto atractivo del vínculo de ayuda

Al vincular a un tema de Ayuda desde la interfaz de usuario principal, asegúrese de escribir texto de vínculo de Ayuda atractivo. Un lenguaje claro y específico inspira confianza. Los usuarios tienden a pensar que los vínculos genéricos de ayuda (un botón con la palabra "Ayuda" o "Más información") no darán lugar a la información correcta sin una inversión significativa de tiempo.

**Si solo hace cinco cosas...**

1.  Diseñe la interfaz de usuario para que los usuarios no necesiten ayuda.
2.  Para que la Ayuda sea útil, centre el contenido en las preguntas principales de los escenarios principales para los usuarios de destino.
3.  Presente el contenido de la Ayuda para que sea fácil de examinar.
4.  Comprenda que no tiene que proporcionar ayuda para todas las características de la interfaz de usuario.
5.  Haga que los puntos de entrada de la Ayuda se puedan detectar y sea atractivo.

## <a name="usage-patterns"></a>Patrones de uso

Los distintos tipos de contenido sirven para distintos propósitos.



|    Tipo de contenido                                                                                                        |   Ejemplo                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ayuda de procedimientos**<br/> proporciona los pasos para llevar a cabo una tarea. <br/>                       | La ayuda de procedimientos debe centrarse en la información de "cómo" en lugar de en "qué" o "por qué". <br/> ![captura de pantalla de la página de ayuda "Eliminar archivos temporales" ](images/winenv-help-image2.png)<br/> En este ejemplo, en el tema de Ayuda se describe cómo usar una característica de la utilidad Limpieza de disco y se proporcionan los pasos que se deben seguir en secuencia.<br/>                                              |
| **Ayuda conceptual**<br/> proporciona información general, información general de características o procesos. <br/> | La ayuda conceptual debe proporcionar información sobre "qué" o "por qué" más allá de la necesaria para completar una tarea. <br/> ![captura de pantalla de la página de ayuda de "el escritorio (información general)" ](images/winenv-help-image3.png)<br/> En este ejemplo, el tema ayuda define qué es el escritorio y proporciona detalles adicionales sobre lo que contiene y por qué los usuarios interactúan con él.<br/>           |
| **Ayuda de referencia**<br/> sirve como libro de referencia en línea. <br/>                                | Puede usar la ayuda de referencia para documentar un lenguaje de programación o interfaces de programación. <br/> ![captura de pantalla de la página de ayuda "convenciones notales" ](images/winenv-help-image4.png)<br/> En este ejemplo, en el tema de Ayuda se enumeran las convenciones tipográficas que se usan para este lenguaje o aplicación concretos, lo que proporciona la información de una tabla fácil de examinar.<br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="entry-points"></a>Puntos de entrada

-   **Vínculo a temas de Ayuda específicos y pertinentes.** No vincule a la página principal de la Ayuda, a la tabla de contenido, a una lista de resultados de búsqueda o a una página que solo se vincule a otras páginas. Evite vincular a páginas estructuradas como una lista grande de preguntas más frecuentes, ya que obliga a los usuarios a buscar la que coincida con el vínculo en el que han hecho clic. No vincule a temas de Ayuda específicos que no sean relevantes y útiles para la tarea en cuestión. No vincular nunca a páginas vacías.
-   **No coloque vínculos de Ayuda en todas las ventanas o páginas por coherencia.** Proporcionar un vínculo de Ayuda en un solo lugar no significa que tenga que proporcionarlos en todas partes.
-   **Use vínculos de Ayuda para cuadros de diálogo, mensajes de error, asistentes y hojas de propiedades.** Si el vínculo ayuda se aplica a controles específicos, colómelo debajo de ellos, alineado a la izquierda. Si el vínculo ayuda se aplica a toda la ventana, colómelo en la esquina inferior izquierda del área de contenido de la ventana.

    ![captura de pantalla de la hoja de propiedades con el cuadro de grupo ](images/winenv-help-image5.png)

    En este ejemplo, el segundo vínculo de Ayuda se aplica a un grupo de controles.

    ![captura de pantalla de la hoja de propiedades y el vínculo de ayuda ](images/winenv-help-image6.png)

    En este ejemplo, el vínculo ayuda se aplica a toda la ventana.

-   **Use vínculos de Ayuda en lugar de referencias textuales genéricas a la Ayuda siempre que sea técnicamente posible.**

    **Correcto:**

    ¿Cómo se pueden reparar errores de disco?

    **Incorrecto:**

    Para obtener más información sobre la reparación de errores de disco, consulte Ayuda y soporte técnico.

-   **Use un botón Ayuda con el icono ayuda para las páginas centrales de los elementos del panel de control.** Colóctelo en la esquina superior derecha. Estos botones no tienen una etiqueta, pero tienen una información sobre herramientas que lee Ayuda.

    ![captura de pantalla del elemento del panel de control con el botón de ayuda ](images/winenv-help-image7.png)

    Elemento del panel de control con un botón Ayuda.

-   **La Ayuda F1 es opcional.** Los usuarios se han acostumbrado a buscar información de Ayuda relacionada con el contexto inmediato de la interfaz de usuario en la pantalla presionando la tecla F1, que se etiqueta como Ayuda en los teclados estándar. Puede incluir la Ayuda F1 si, por ejemplo, los estudios de facilidad de uso muestran que los usuarios esperan encontrarla, o la interfaz de usuario del programa es lo suficientemente compleja como para beneficiarse de la asistencia contextual.
-   **Los programas con barras de menús pueden tener una categoría de menú Ayuda.** Para obtener instrucciones del menú Ayuda, vea [Menús](cmd-menus.md).

    ![captura de pantalla de la ayuda a la que se accede desde la barra de menús ](images/winenv-help-image8.png)

    En este ejemplo, el Windows Paint tiene una categoría de menú Ayuda.

-   **Para la accesibilidad del teclado, proporcione tabulaciones para los botones y vínculos de Ayuda.**
-   El comportamiento del botón Ayuda y del vínculo debe ser el siguiente: se abre el panel ayuda y se muestra un tema de Ayuda dedicado. la interfaz de usuario que invocó el panel ayuda debe permanecer abierta para conservar la experiencia contextual.
-   **No use los siguientes estilos obsoletos de punto de entrada de Ayuda: "Más información" o "Más información sobre...". vínculos, botones genéricos de Ayuda y botones de Ayuda contextuales en la barra de título.** Aunque se han usado en el pasado, los estudios de facilidad de uso han determinado que los usuarios tienden a ignorarlos. En su lugar, use vínculos a temas de Ayuda específicos. Para obtener instrucciones sobre cómo escribir buenos vínculos de Ayuda, consulte [Vínculos de Ayuda](#text).

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con un vínculo "Más información" ](images/winenv-help-image9.png)

    No use "Más información" o "Más información sobre...". Enlaces.

    **Incorrecto:**

    ![captura de pantalla del botón de ayuda junto a los botones de confirmación ](images/winenv-help-image10.png)

    No use botones genéricos de Ayuda.

    **Incorrecto:**

    ![captura de pantalla del icono de signo de interrogación en la barra de título ](images/winenv-help-image11.png)

    No use botones de Ayuda contextuales en la barra de título.

### <a name="content"></a>Content

-   **No cree contenido obvio.** Los temas de ayuda que repiten lo que hay en la interfaz de usuario principal no agregan valor.
-   **No cree contenido sobre el que el usuario no pueda actuar de alguna manera.**
    -   **Excepción:** Algunos contenidos conceptuales proporcionan información general importante sin llevar necesariamente a la acción del usuario.
-   **Evite soluciones imprecisas a los problemas.** Por ejemplo, "ponerse en contacto con el administrador del sistema" o "reinstalar la aplicación" tienden a frustrar a los usuarios.
    -   **Excepción:** Se recomienda ponerse en contacto con el administrador del sistema si esa es la única solución práctica y los administradores del sistema esperan ponerse en contacto con el problema.
-   **Evite el contenido que aborda escenarios de usuario muy poco probables.** Desarrolle el contenido de ayuda principal para lo que prevé que será un uso normal. tenga en cuenta las excepciones importantes al uso esperado, pero trate este contenido como una prioridad menor.
-   **Recopilo comentarios de los usuarios sobre lo útiles que son los temas de Ayuda.** Permitir a los usuarios calificar temas individuales. Realice [estudios de facilidad de](glossary.md) uso en la documentación para determinar los problemas relacionados con la calidad y la detectabilidad del contenido.
    -   **Sugerencia:** Los comentarios de los usuarios también son una excelente manera de generar más contenido basado en tareas, centrado en lo que los usuarios hacen realmente con el programa, en lugar de en el contenido basado en características, centrado simplemente en una descripción de la tecnología.
-   **Proporcione varias maneras de acceder al contenido.** Una tabla de contenido, un índice y un mecanismo [de](ctrl-search-boxes.md) búsqueda son tres de los métodos más comunes para mejorar la detectabilidad.
-   **Si hay más de una manera de realizar una tarea, en la mayoría de los casos solo puede documentar la manera más común que usan los usuarios sin experiencia.**

### <a name="icons"></a>Iconos

-   Use el icono ayuda solo para las ventanas del Explorador y las páginas centrales de los elementos del panel de control. No use el icono ayuda con vínculos de Ayuda.

**Correcto:**

![captura de pantalla de la ventana con el icono de signo de interrogación ](images/winenv-help-image12.png)

En este ejemplo, una ventana Windows Explorer usa un icono de Ayuda para proporcionar acceso a la Ayuda.

**Incorrecto:**

![captura de pantalla de la ventana con el icono de ayuda en el panel izquierdo ](images/winenv-help-image13.png)

En este ejemplo, el icono ayuda de la parte inferior izquierda se usa incorrectamente con un vínculo de Ayuda.

## <a name="text"></a>Texto

**Vínculos a la Ayuda**

-   Proporcione información específica sobre el contenido del tema de Ayuda, usando tanto texto relevante y conciso como sea necesario. A menudo, los usuarios omiten los vínculos de Ayuda genéricos. Asegúrese de que los resultados del vínculo son predecibles. Los usuarios no deben despreorse de los resultados.

    -   **Excepción:** Puede usar "Más información" para complementar las instrucciones que están directamente en la interfaz de usuario, especialmente si proporcionar información específica en el vínculo ayuda conduce a repeticiones innecesarias o hace que el vínculo sea menos atractivo.

    **Incorrecto:**

    Una contraseña segura tiene al menos seis letras de mayúsculas y minúsculas mixtas, números y símbolos. ¿Qué es una contraseña segura?

    **Correcto:**

    Una contraseña segura tiene al menos seis letras de mayúsculas y minúsculas mixtas, números y símbolos. Más información

    En el ejemplo incorrecto, el vínculo ayuda es repetitivo. Hace una pregunta que realmente ya está respondida.

-   Siempre que sea posible, la frase Ayuda vincula el texto en términos de la pregunta principal que responde el contenido de la Ayuda. No use las expresiones "Más información sobre", "Cuéndome más información" o "Obtener ayuda con esto".

    **Incorrecto:**

    Más información sobre cómo agregar excepciones

    **Correcto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    Cómo agregar excepciones?

    En los ejemplos correctos, el vínculo se dice en términos de la pregunta principal que responde el tema de Ayuda.

-   Si la información más relevante se puede resumir de forma concisa, coloque el resumen directamente en la interfaz de usuario en lugar de usar un vínculo de Ayuda. Sin embargo, puede usar un vínculo de Ayuda para proporcionar información complementaria.

    **Incorrecto:**

    ![captura de pantalla del vínculo a ¿Qué es una contraseña segura? ](images/winenv-help-image14.png)

    **Correcto:**

    ![captura de pantalla de texto complementario sobre contraseñas ](images/winenv-help-image15.png)

    **Mejor:**

    ![captura de pantalla de texto con vínculo a más información ](images/winenv-help-image16.png)

    En el ejemplo correcto se resume la información de ayuda de forma concisa, lo que mejora enormemente la probabilidad de que los usuarios la lean. El mejor ejemplo proporciona un vínculo de Ayuda para obtener más información sobre este tema complejo.

-   Vínculos de ayuda de frases para indicar claramente la asistencia. Los vínculos de ayuda nunca deben leerse como vínculos de acción.
-   Use el vínculo de Ayuda completo para el texto del vínculo, no solo las palabras clave.

    **Correcto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    **Incorrecto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    En el ejemplo correcto, se usa toda la oración del vínculo de Ayuda para el texto del vínculo.

    -   **Excepción:** Los vínculos de ayuda a sitios web externos simplemente deben usar el nombre del sitio o la página como vínculo. No es necesario incluir ningún texto que presente el nombre del sitio en el propio vínculo.

-   Los vínculos de Ayuda no tienen que coincidir exactamente con los encabezados del tema de Ayuda, pero debe haber una conexión sólida y obvia entre los dos. Por este motivo, diseñe vínculos y encabezados en pares.

    **Correcto:**

    ¿Cómo puedo mejorar el rendimiento de esta característica? (texto del vínculo)

    Configuración de esta característica para un rendimiento óptimo (encabezado del tema)

    **Incorrecto:**

    ¿Cómo puedo mejorar el rendimiento de esta característica? (texto del vínculo)

    Información general completa de esta característica (encabezado del tema)

    En el ejemplo incorrecto, el encabezado del tema de Ayuda difiere considerablemente en el ámbito del texto del vínculo de Ayuda y podría ser desorientado.

-   Si el contenido de la Ayuda está en línea, aclare esto en el texto del vínculo. Esto ayuda a que el resultado de los vínculos sea predecible.

    **Correcto:**

    Para obtener formatos y herramientas adicionales, vaya al sitio web de Microsoft.

    **Incorrecto:**

    ¿Dónde puedo encontrar formatos y herramientas adicionales?

-   Use oraciones completas.
-   No use signos de puntuación finales, excepto los signos de interrogación.
-   No use puntos suspensivos para vínculos o comandos de Ayuda.

**Contenido de ayuda**

-   Dar formato a los elementos de la interfaz de usuario mediante negrita para facilitar su identificación. Esto es especialmente útil para los temas de Ayuda de procedimientos, lo que permite a los usuarios examinar los procedimientos y ver rápidamente los elementos de interfaz de usuario pertinentes.
-   Dar formato a los títulos mediante cursiva. Esto se aplica a las tablas, el arte, las capturas de pantalla y otros elementos gráficos que se benefician de una breve explicación textual.
-   Consulte Ayuda simplemente como Ayuda. Por lo general, no use la frase Ayuda en línea a menos que de hecho haga referencia al contenido de su sitio web.

 

