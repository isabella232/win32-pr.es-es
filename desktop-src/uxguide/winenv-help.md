---
title: Ayuda
description: Use la ayuda como mecanismo secundario para ayudar a los usuarios a completar y comprender mejor las tareas \ 8212; el mecanismo principal es la propia interfaz de usuario. Aplique estas directrices para que el contenido sea realmente útil y fácil de encontrar.
ms.assetid: 82ce076e-062b-4793-a1c0-ed96c0f2b284
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 907494e9a97ccaf51e4eba463c34e49854b14a81
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554578"
---
# <a name="help"></a>Ayuda

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Use la ayuda como mecanismo secundario para ayudar a los usuarios a completar y comprender mejor las tareas que el mecanismo principal es la propia interfaz de usuario. Aplique estas directrices para que el contenido sea realmente útil y fácil de encontrar.

Un sistema de ayuda se compone de varios tipos de contenido diseñados para ayudar a los usuarios cuando no pueden completar una tarea, desean comprender un concepto con más detalle o necesitan más detalles técnicos que los que están disponibles en la interfaz de usuario.

En este artículo, nos referimos a la ayuda como secundaria a la interfaz de usuario. La interfaz de usuario es la principal porque es donde los usuarios intentan resolver sus problemas en primer lugar. Consultan el sistema de ayuda solo si no pueden realizar su tarea con la interfaz de usuario.

![captura de pantalla de la página de ayuda y soporte técnico de Windows ](images/winenv-help-image1.png)

La Página principal de ayuda y soporte técnico de Windows, disponible en el menú Inicio.

**Nota:** Las instrucciones relacionadas con el [estilo y el tono](text-style-tone.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿Cuál es la motivación de los usuarios de destino?** Cuanto más motivado sea la detección de la funcionalidad del programa y que se convierta en usuarios intermedios o incluso avanzados, más dispuestos serán investigar las respuestas a sus preguntas consultando los temas de ayuda.
-   **¿Usa la ayuda para corregir una interfaz de usuario incorrecta?** Cuanto mejor sea su interfaz de usuario, menos usuarios buscarán ayuda adicional. Si el programa tiene una interfaz de usuario principal muy clara y útil (por ejemplo, mensajes de error sin jerga, asistentes bien escritos y cuadros de diálogo no ambiguos), es posible que no necesite un sistema de ayuda secundario.
-   **¿Su programa es relativamente sencillo?** Si es así, considere incorporar todo el contenido de asistencia necesario en las superficies de la interfaz de usuario principal. Es más probable que los usuarios busquen ayuda adicional en los programas que realizan tareas complejas.
-   **¿La aplicación está pensada para desarrolladores, profesionales de ti u otros expertos de software?** Estos usuarios tienden a esperar la ayuda de referencia de las convenciones del lenguaje de programación y la ayuda conceptual detallada para dominar las características.

## <a name="design-concepts"></a>Conceptos de diseño

Si decide incluir la ayuda en el programa, puede integrarla en el diseño general. La interfaz de ayuda debe ser simple, eficaz y relevante; debe permitir que los usuarios obtengan ayuda fácilmente y vuelvan a su tarea. Piense en el sistema de ayuda en lo que respecta a la hora de los usuarios: minimice primero la interrupción Si prevé dónde encontrará problemas en el programa y, a continuación, solucione estos problemas mediante la incorporación de asistencia básica directamente en la interfaz de usuario y la creación de puntos de entrada claros y coherentes en la ayuda más detallada.

La asistencia de Windows se diseñó según estos principios. Estos son algunos de los cambios de diseño de la experiencia del usuario de la ayuda de Windows:

-   Más puntos de entrada reconocibles para ayudar desde la interfaz de usuario principal (especialmente nuevos vínculos de ayuda desde superficies de la interfaz de usuario, como cuadros de diálogo, mensajes de error y asistentes). Los vínculos de ayuda le llevan directamente al tema pertinente de la ayuda de.
-   Hay un icono de botón de ayuda disponible en la esquina superior derecha de la mayoría de las páginas del concentrador del panel de control, así como las carpetas de Shell.
-   Los usuarios pueden optar por obtener el contenido de ayuda más actualizado de la ayuda y soporte técnico en línea de Windows cuando estén en línea.
-   Los temas de ayuda ahora están basados en tareas, en lugar de centrarse en características, de modo que los usuarios puedan realizar sus tareas de forma rápida y eficaz.
-   Los temas de ayuda se basan en gran medida en los principales escenarios de usuario conocidos.
-   Los temas de ayuda tienen un [tono](text-style-tone.md)más flexible e informal, con un lenguaje real.
-   Los temas de ayuda están diseñados para un análisis eficaz, ya que los usuarios rara vez leen el contenido palabra para palabra.

### <a name="an-analogy-for-help"></a>Una analogía para la ayuda

Para pensar más en el diseño del sistema de ayuda, considere una analogía de la vida diaria. Se pierde en una ciudad desconocida. ¿Qué puede hacer? Muchos reaccionarían de la siguiente manera:

-   Obtener orientación; busque puntos de referencia, señales de calle (nombres y punteros a lugares).
-   Busque Maps.
-   Por último, como último recurso, pida instrucciones o llame a un amigo.

El diseño de la "interfaz" de la ciudad afecta a la necesidad de asistencia. Calles bien etiquetadas, direcciones explícitas (punteros a hospitales, aeropuertos, museos y la oficina de correos) y claros puntos de referencia, como características geográficas o edificios destacados, le ayudarán a encontrar su manera.

Pida ayuda como último recurso. Es una indicación de que se ha producido un error en la "interfaz" de la ciudad Al diseñarse mal y confuso. Es más probable que pida ayuda en un lugar que tenga una etiqueta específica que sugiera utilidad. Por ejemplo, es más probable que le pida ayuda en un lugar con la etiqueta "directions" o "Information" que un lugar general como City Hall, aunque casi todos los usuarios de City Hall puedan proporcionarle instrucciones.

Cuando pida ayuda, lo más probable es que se sienta frustrado y simplemente quiera llegar al destino previsto. Probablemente no esté en el ambiente para dedicar tiempo a realizar un paseo por la ciudad o el aprendizaje de su historial. Además, su motivación depende de la importancia de la tarea. Si está intentando encontrar su habitación de Hotel, hará lo que tarde. Sin embargo, si su objetivo es encontrar un lugar de menor importancia, lo más probable es que solo se produzca después de un esfuerzo modesto.

Todos estos aspectos de la búsqueda del modo en el espacio real se corresponden con el modo en que los usuarios suelen encontrar su forma en el espacio virtual del programa. La búsqueda de ayuda más allá de la interfaz de usuario principal es por su naturaleza desorientada; Haga todo lo posible para mitigar este tipo de experiencia mediante la interfaz de usuario bien diseñada y las "señales de calles" inteligentes para dirigir a los usuarios a las respuestas que necesitan.

### <a name="designing-ui-so-that-help-is-unnecessary"></a>Diseñar la interfaz de usuario para que la ayuda sea innecesaria

Intente hacer que la ayuda sea innecesaria en primer lugar, por:

-   Facilitar la detección y la realización de tareas comunes.
-   Proporcionar [instrucciones principales](text-ui.md)claras.
-   Proporcionar etiquetas de control claras y concisas orientadas a tareas y objetivos.
-   Proporcionar instrucciones complementarias y explicaciones cuando sea necesario.
-   Anticipar problemas al usar controles restringidos a opciones válidas, proporcionar valores predeterminados adecuados, controlar todos los formatos de entrada y evitar errores.
-   Escribir mensajes de error que proporcionan una solución o acción claras que el usuario debe realizar.
-   Evite diseños de interfaz de usuario confusos, como las tareas con un flujo deficiente o el uso de controles deshabilitados sin motivo aparente.
-   Trabajar con escritores y editores en las primeras fases del ciclo de desarrollo para crear texto de [interfaz de usuario](text-ui.md) coherente y de alta calidad en todo el programa.

Los usuarios no deben tener que ir a otra parte para averiguar cómo usar la interfaz de usuario. Agregue información esencial directamente a la interfaz de usuario principal, en lugar de obligar a los usuarios a salir de su contexto inmediato y en el panel de ayuda. Si solo existe información importante en un tema de ayuda, es posible que los usuarios no la vean. Para obtener información que es opcional y más explicativa, use los vínculos de ayuda de la interfaz de usuario principal al tema de ayuda correspondiente para obtener asistencia complementaria.

### <a name="considering-user-motivation"></a>Consideración de la motivación del usuario

Para la mayoría de los usuarios, la velocidad y la eficacia se encuentran entre las virtudes más fundamentales de los buenos programas. Los usuarios quieren realizar su trabajo. Por lo general, no están interesados en obtener información sobre el programa y la tecnología por sí solos. su paciencia solo se extiende en la medida en que ese programa atiende sus intereses y resuelve problemas a mano.

Diseñe el sistema de ayuda para que coincida con la motivación de los usuarios. Por ejemplo, Imagine un usuario que ha strolled hasta un quiosco en un museo. Si no puede averiguar cómo llevar a cabo la tarea rápidamente, es probable que tenga que hacerlo. No es probable que dedique tiempo a usar la ayuda. Como alternativa, un usuario muy motivado tiene una mayor tolerancia al tiempo dedicado a investigar el sistema de ayuda para obtener respuestas. Un usuario empresarial que debe equilibrar los libros, por ejemplo, probablemente esté dispuesto a consultar el contenido de la ayuda para sacar el máximo partido de esa nueva aplicación de contabilidad.

### <a name="writing-content-for-scanning"></a>Escribir contenido para el análisis

Escriba los temas de ayuda para saber que se examinarán para obtener información específica, no para leer palabras. Escriba de forma concisa, obtenga el punto rápidamente y proporcione información sobre la que los usuarios pueden actuar.

-   Escriba temas de procedimientos con los pasos numerados en un formato coherente para que los usuarios reconozcan que están obteniendo ayuda de procedimientos.
-   Escriba temas de referencia con facilidad de análisis en mente, utilizando tablas, por ejemplo, para presentar las opciones de la interfaz de usuario o la sintaxis del lenguaje.
-   Escribir temas conceptuales organizados lógicamente por subtítuloes, de modo que el usuario pueda omitir secciones enteras de menor interés.

En todo el contenido de la ayuda, es más fácil examinar listas con viñetas que los bloques de texto estándar. Utilice las listas de viñetas con prudencia, no como crutch para el material desorganizado.

### <a name="creating-content-that-matters"></a>Crear contenido que sea importante

Dado que ningún sistema de ayuda puede anticipar cada una de las preguntas que pueda tener cada usuario, céntrese en la mayor parte del contenido de responder a las preguntas más importantes en los escenarios principales de los usuarios de destino. Por ejemplo, la búsqueda eficaz y el establecimiento de la conectividad de red (entre otras tareas) pueden ser temas muy buscados. Además, céntrese en las tareas que se encuentran en los principales escenarios de usuario, en lugar de documentar una característica o tecnología de manera exhaustiva por su cuenta.

**Sugerencia:** El soporte técnico es una buena fuente para el contenido de la ayuda. Los departamentos de soporte técnico a menudo mantienen registros de las preguntas más frecuentes sobre programas o tareas concretos que los usuarios están intentando realizar (y con errores).

No es necesario proporcionar ayuda para todas las características de la interfaz de usuario. **Con bastante frecuencia, los resultados de la ayuda no se pueden obtener al intentar crear ayuda para todo.** Si la interfaz de usuario está bien diseñada, la mayoría de estos temas de ayuda no serán muy útiles. solo volverán a tener el estado obvio.

Si hay más de una forma de realizar una tarea, en la mayoría de los casos puede simplemente documentar la manera más común que usan los usuarios indebidos. Entre las excepciones a esto se incluyen consideraciones de accesibilidad (documentar los equivalentes de teclado de acciones del mouse, por ejemplo) y consideraciones sobre la plataforma (documentar el factor de forma de Tablet PC, por ejemplo, o para los entornos de servidor en los que la línea de comandos puede sustituir la interfaz gráfica de usuario).

Recuerde que los usuarios no suelen pensar en los problemas que se encuentran exactamente en los mismos términos que usted. Por ejemplo, los usuarios pueden resultar extraño que se consideren como una "cuenta". Asegúrese de diseñar la funcionalidad de búsqueda e indización y, a continuación, para tener en cuenta los sinónimos y las variaciones de terminología probables.

Sin embargo, entre la interfaz de usuario principal y el sistema de ayuda, los términos deben ser muy similares si no son idénticos. Los usuarios pueden confundirse cuando el idioma del sistema de ayuda no se corresponda muy estrechamente con lo que ven en la pantalla.

### <a name="writing-compelling-help-link-text"></a>Escribir texto de vínculo de ayuda atractivo

Al vincular a un tema de ayuda desde la interfaz de usuario principal, asegúrese de escribir texto de vínculo de ayuda atractivo. Un lenguaje claro y específico inspira confianza. Los usuarios suelen creer que los vínculos de ayuda genéricos (un botón con la palabra "ayuda" u "más información") no llevarán a la información correcta sin una importante inversión de tiempo.

**Si solo hace cinco cosas...**

1.  Diseñe la interfaz de usuario para que los usuarios no necesiten ayuda.
2.  Haga que su ayuda le resulte útil centrándose en el contenido de las principales preguntas de los principales escenarios de los usuarios de destino.
3.  Presente el contenido de la ayuda para que sea fácil de analizar.
4.  Comprenda que no tiene que proporcionar ayuda para todas las características de la interfaz de usuario.
5.  Haga que los puntos de entrada de la ayuda sean reconocibles y atractivos.

## <a name="usage-patterns"></a>Patrones de uso

Los diferentes tipos de contenido tienen distintos fines.



|                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ayuda de procedimientos**<br/> proporciona los pasos para llevar a cabo una tarea. <br/>                       | La ayuda de procedimientos debe centrarse en "cómo" información en lugar de "qué" o "por qué". <br/> ![captura de pantalla de la página de ayuda "eliminar archivos temporales" ](images/winenv-help-image2.png)<br/> En este ejemplo, el tema de ayuda describe cómo usar una característica de la utilidad liberador de espacio en disco, que proporciona los pasos que deben seguirse en la secuencia.<br/>                                              |
| **Ayuda conceptual**<br/> proporciona información general, información general sobre características o procesos. <br/> | La ayuda conceptual debe proporcionar la información "qué" o "por qué" más allá de lo necesario para completar una tarea. <br/> ![captura de pantalla de la página de ayuda del escritorio (Introducción) ](images/winenv-help-image3.png)<br/> En este ejemplo, el tema de ayuda define el escritorio y proporciona detalles adicionales sobre lo que contiene y por qué los usuarios interactúan con él.<br/>           |
| **Ayuda de referencia**<br/> actúa como un libro de referencia en línea. <br/>                                | Puede usar la ayuda de referencia para documentar un lenguaje de programación o interfaces de programación. <br/> ![captura de pantalla de la página de ayuda de ' convenciones de anotaciones ' ](images/winenv-help-image4.png)<br/> En este ejemplo, en el tema de ayuda se enumeran las convenciones tipográficas que se usan para este idioma o aplicación en particular, lo que proporciona la información en una tabla de análisis sencillo.<br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="entry-points"></a>Puntos de entrada

-   **Vínculo a temas de ayuda específicos y relevantes.** No vincular a la Página principal de la ayuda, la tabla de contenido, una lista de resultados de la búsqueda o una página que solo se vincula a otras páginas. Evite la vinculación a páginas estructuradas como una gran lista de preguntas más frecuentes, ya que obliga a los usuarios a buscar la que coincida con el vínculo en el que se hizo clic. No vincule a temas de ayuda específicos que no sean relevantes y útiles para la tarea a mano. No vincule nunca a páginas vacías.
-   **No coloque vínculos de ayuda en todas las ventanas o páginas para garantizar la coherencia.** Proporcionar un vínculo de ayuda en un lugar no significa que tenga que proporcionarlos en todas partes.
-   **Use los vínculos de ayuda para los cuadros de diálogo, mensajes de error, asistentes y hojas de propiedades.** Si el vínculo de ayuda se aplica a controles específicos, colóquelo debajo de ellos, alineado a la izquierda. Si el vínculo de ayuda se aplica a toda la ventana, colóquelo en la esquina inferior izquierda del área de contenido de la ventana.

    ![captura de pantalla de la hoja de propiedades con el cuadro de grupo ](images/winenv-help-image5.png)

    En este ejemplo, el segundo vínculo de ayuda se aplica a un grupo de controles.

    ![captura de pantalla de la hoja de propiedades y el vínculo de ayuda ](images/winenv-help-image6.png)

    En este ejemplo, el vínculo de ayuda se aplica a toda la ventana.

-   **Utilice vínculos de ayuda en lugar de referencias de texto genéricas para ayudar siempre que sea técnicamente posible.**

    **Correcto:**

    ¿Cómo puedo reparar errores de disco?

    **Incorrecto:**

    Para obtener más información acerca de cómo reparar errores de disco, consulte ayuda y soporte técnico.

-   **Use un botón ayuda con el icono de ayuda para las páginas del concentrador de elementos del panel de control.** Colóquelo en la esquina superior derecha. Estos botones no tienen etiqueta, pero tienen una información sobre herramientas que lee la ayuda.

    ![captura de pantalla del elemento del panel de control con el botón ayuda ](images/winenv-help-image7.png)

    Un elemento del panel de control con un botón ayuda.

-   **La ayuda F1 es opcional.** Los usuarios han ido acostumbrados a buscar información de ayuda relacionada con el contexto inmediato de la interfaz de usuario en la pantalla presionando la tecla F1, que está etiquetada como ayuda sobre teclados estándar. Puede incluir la ayuda de F1 si, por ejemplo, los estudios de uso muestran que los usuarios esperan encontrarla, o la interfaz de usuario del programa es lo suficientemente compleja como para beneficiarse de la ayuda contextual.
-   **Los programas con barras de menús pueden tener una categoría de menú ayuda.** Para obtener instrucciones sobre el menú ayuda, vea [menús](cmd-menus.md).

    ![captura de pantalla de la ayuda a la que se tiene acceso desde la barra de menús ](images/winenv-help-image8.png)

    En este ejemplo, el accesorio Paint de Windows tiene una categoría de menú ayuda.

-   **Para la accesibilidad del teclado, proporcione tabulaciones para botones y vínculos de ayuda.**
-   El botón ayuda y el comportamiento de los vínculos deben ser los siguientes: se abre el panel de ayuda y se muestra un tema de ayuda dedicado. la interfaz de usuario que invocó el panel de ayuda debe permanecer abierta para conservar la experiencia contextual.
-   **No use los siguientes estilos de punto de entrada de ayuda obsoletos: "más información" o "más información acerca de..." vínculos, botones de ayuda genéricos y botones de ayuda contextual en la barra de título.** Aunque se han usado en el pasado, los estudios de facilidad de uso han determinado que los usuarios tienden a omitirlos. En su lugar, use vínculos a temas de ayuda específicos. Para obtener instrucciones sobre cómo escribir buenos vínculos de ayuda, vea [vínculos de ayuda](#text).

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con el vínculo "más información" ](images/winenv-help-image9.png)

    No use "más información" o "más información acerca de..." vínculos.

    **Incorrecto:**

    ![captura de pantalla del botón ayuda junto a botones de confirmación ](images/winenv-help-image10.png)

    No use botones de ayuda genéricos.

    **Incorrecto:**

    ![captura de pantalla de un icono de signo de interrogación en la barra de título ](images/winenv-help-image11.png)

    No use botones de ayuda contextual en la barra de título.

### <a name="content"></a>Contenido

-   **No cree contenido obvio.** Los temas de ayuda que repiten lo que hay en la interfaz de usuario principal no agregan valor.
-   **No cree contenido en el que el usuario no pueda actuar de alguna manera.**
    -   **Excepción:** Algunos contenidos conceptuales ofrecen información básica importante sin necesidad de una acción del usuario.
-   **Evite resoluciones imprecisas de problemas.** Por ejemplo, "Póngase en contacto con el administrador del sistema" o "reinstalar la aplicación" tiende a frustrar a los usuarios.
    -   **Excepción:** Se recomienda ponerse en contacto con el administrador del sistema si esta es la única solución práctica y los administradores del sistema esperan que se ponga en contacto con el problema.
-   **Evite el contenido que se redirige a escenarios de usuario muy poco probables.** Desarrollar el contenido de ayuda principal para lo que se prevé será el uso normal; Tenga en cuenta las excepciones importantes al uso esperado, pero trate este contenido como una prioridad más baja.
-   **Recopile comentarios de los usuarios sobre la utilidad de los temas de ayuda.** Permitir a los usuarios valorar temas individuales. Lleve a cabo [estudios de facilidad de uso](glossary.md) en su documentación para averiguar problemas relacionados con la calidad y la detectabilidad del contenido.
    -   **Sugerencia:** Los comentarios de los usuarios también son una excelente manera de generar más contenido basado en tareas, centrado en lo que los usuarios hacen realmente con el programa, en lugar de en el contenido basado en características, centrado simplemente en una descripción de la tecnología.
-   **Proporcionan varias maneras de obtener acceso al contenido.** Una tabla de contenido, un índice y un mecanismo de [búsqueda](ctrl-search-boxes.md) son tres de los métodos más comunes para mejorar la detectabilidad.
-   **Si hay más de una forma de realizar una tarea, en la mayoría de los casos puede simplemente documentar la manera más común que usan los usuarios indebidos.**

### <a name="icons"></a>Iconos

-   Use el icono ayuda solo para las ventanas del explorador y las páginas del concentrador de elementos del panel de control. No use el icono de ayuda con vínculos de ayuda.

**Correcto:**

![captura de pantalla de la ventana con el icono de signo de interrogación ](images/winenv-help-image12.png)

En este ejemplo, una ventana del explorador de Windows usa un icono de ayuda para proporcionar acceso a la ayuda de.

**Incorrecto:**

![captura de pantalla de la ventana con el icono de ayuda en el panel izquierdo ](images/winenv-help-image13.png)

En este ejemplo, el icono de ayuda situado en la parte inferior izquierda se usa incorrectamente con un vínculo de ayuda.

## <a name="text"></a>Texto

**Vínculos a la Ayuda**

-   Proporcionar información específica sobre el contenido del tema de ayuda, utilizando el texto conciso más relevante según sea necesario. Los usuarios a menudo omiten los vínculos de ayuda genéricos. Asegúrese de que los resultados del vínculo son usuarios predecibles no deberían sorprender en los resultados.

    -   **Excepción:** Puede usar "más información" para complementar las instrucciones que están directamente en la interfaz de usuario, especialmente si proporcionar información específica en el vínculo de ayuda conduce a una repetición innecesaria o hace que el vínculo sea menos atractivo.

    **Incorrecto:**

    Una contraseña segura tiene al menos seis letras, números y símbolos de mayúsculas y minúsculas mixtas. ¿Qué es una contraseña segura?

    **Correcto:**

    Una contraseña segura tiene al menos seis letras, números y símbolos de mayúsculas y minúsculas mixtas. Más información

    En el ejemplo incorrecto, el vínculo de la ayuda es repetitivo. Realiza una pregunta que ya se ha respondido.

-   Siempre que sea posible, phrase el texto del vínculo de la ayuda en términos de la pregunta principal respondida por el contenido de la ayuda. No use "obtener más información acerca de", "más información" o "obtener ayuda con esta".

    **Incorrecto:**

    Más información sobre cómo agregar excepciones

    **Correcto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    ¿Cómo agregar excepciones?

    En los ejemplos correctos, el vínculo se formula en función de la pregunta principal respondida por el tema de ayuda.

-   Si la información más relevante se puede resumir brevemente, coloque el resumen directamente en la interfaz de usuario en lugar de usar un vínculo de ayuda. Sin embargo, puede usar un vínculo de ayuda para proporcionar información complementaria.

    **Incorrecto:**

    ![captura de pantalla del vínculo a ¿qué es una contraseña segura? ](images/winenv-help-image14.png)

    **Correcto:**

    ![captura de pantalla de texto complementario sobre contraseñas ](images/winenv-help-image15.png)

    **Manera**

    ![captura de pantalla de texto con vínculo para obtener más información ](images/winenv-help-image16.png)

    En el ejemplo correcto se resume la información de ayuda Subienda, mejorando considerablemente la probabilidad de que los usuarios la lean. El mejor ejemplo proporciona un vínculo de ayuda para obtener más información sobre este asunto complejo.

-   Expresión ayuda vínculos para indicar claramente la asistencia. Los vínculos de ayuda nunca deben leer como vínculos de acción.
-   Use el vínculo de ayuda completo para el texto del vínculo, no solo las palabras clave.

    **Correcto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    **Incorrecto:**

    ¿Cuáles son los riesgos de permitir excepciones?

    En el ejemplo correcto, se usa la oración de vínculo de ayuda completa para el texto del vínculo.

    -   **Excepción:** Los vínculos de ayuda a sitios web externos simplemente deben usar el nombre del sitio o la página como vínculo. No es necesario incluir ningún texto que introduzca el nombre del sitio en el propio vínculo.

-   Los vínculos de ayuda no tienen que coincidir exactamente con los encabezados del tema de ayuda, pero debe haber una conexión segura y obvia entre ambos. Diseñe vínculos y encabezados en pares por este motivo.

    **Correcto:**

    ¿Cómo puedo mejorar el rendimiento de esta característica? (texto de vínculo)

    Configuración de esta característica para obtener un rendimiento óptimo (encabezado de tema)

    **Incorrecto:**

    ¿Cómo puedo mejorar el rendimiento de esta característica? (texto de vínculo)

    Información general completa de esta característica (encabezado de tema)

    En el ejemplo incorrecto, el encabezado del tema de ayuda difiere sustancialmente en el ámbito del texto del vínculo de ayuda y podría desorientarse.

-   Si el contenido de la ayuda está en línea, desactívela en el texto del vínculo. Al hacerlo, se facilita el resultado de la predicción de los vínculos.

    **Correcto:**

    Para obtener más formatos y herramientas, vaya al sitio web de Microsoft.

    **Incorrecto:**

    ¿Dónde puedo encontrar más herramientas y formatos?

-   Use frases completas.
-   No use signos de puntuación finales, excepto los signos de interrogación.
-   No use puntos suspensivos para vínculos de ayuda o comandos.

**Contenido de ayuda**

-   Aplique formato de negrita a los elementos de la interfaz de usuario para facilitar su identificación. Esto es especialmente útil para los temas de ayuda de procedimientos, lo que permite a los usuarios examinar los procedimientos y ver rápidamente los elementos de la interfaz de usuario pertinentes.
-   Aplicar formato a los títulos con cursiva. Esto se aplica a las tablas, las imágenes, las capturas de pantallas y otros elementos gráficos que se benefician de una breve explicación textual.
-   Consulte la ayuda de como ayuda. Por lo general, no use la frase de la ayuda en línea a menos que vaya a hacer referencia al contenido de su sitio Web.

 

