---
title: Interfaz de usuario principios
description: En este tema se describe cómo implementar principios de diseño intuitivos de la interfaz de usuario y la experiencia del usuario en Windows aplicaciones.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57781ab2cb0a2d9574288000f65805c981afa391d49263bd21e23eeed432416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021498"
---
# <a name="user-interface-principles"></a>Interfaz de usuario principios

En este tema se describe cómo implementar principios de diseño intuitivos de la interfaz de usuario y la experiencia del usuario en Windows aplicaciones.

-   [Introducción](#introduction)
-   [Principios básicos de la interfaz de usuario adecuada](#the-basic-principles-of-proper-ui)
    -   [Espaciado y posicionamiento](#spacing-and-positioning)
    -   [Tamaño](#size)
    -   [Agrupación](#grouping)
    -   [Intuición](#intuitiveness)
-   [20 Sugerencias una experiencia de usuario mejor y funcional](#20-tips-for-a-better-functional-user-experience)
    -   [Usar estándares](#use-standards)
    -   [Llamar la atención sobre los botones importantes](#draw-attention-to-important-buttons)
    -   [Simplificar el reconocimiento con iconos](#simplify-recognition-with-icons)
    -   [Simplificar el reconocimiento con encabezados](#simplify-recognition-with-headers)
    -   [Usar cuadros de mensaje personalizados](#use-custom-message-boxes)
    -   [Incluir comandos alternativos](#include-alternate-commands)
    -   [Cómo controlar acciones críticas](#how-to-handle-critical-actions)
    -   [¿RadioButtons o ComboBoxes?](#radiobuttons-or-comboboxes)
    -   [No interrumpa nunca al usuario.](#never-disrupt-the-user)
    -   [Proporcionar el estado de progreso](#provide-progress-status)
    -   [Simplificar pasos complejos con asistentes](#simplify-complex-steps-with-wizards)
    -   [Obtener el tono del texto a la derecha](#get-the-tone-of-your-text-right)
    -   [A veces, un control ListView es mejor](#sometimes-a-listview-is-better)
    -   [Simplificar la navegación con controles y barras laterales de ruta de navegación](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Usar gráficos bastante](#use-pretty-graphics)
    -   [Proporcionar formularios de tamaño ajustable cuando sea posible](#provide-resizable-forms-when-possible)
    -   [Proporcionar más funcionalidad con barras laterales o paneles de tareas](#provide-more-functionality-with-sidebarstask-panes)
    -   [Dar una opción de notificación](#give-a-notification-choice)
    -   [Proporcione información sobre herramientas.](#provide-tooltips)
    -   [No olvide las cosas pequeñas](#do-not-forget-the-little-things)
-   [Conclusión](#conclusion)

## <a name="introduction"></a>Introducción

A menudo, los desarrolladores no tienen en cuenta la perspectiva del usuario final. Los desarrolladores trabajan duro para que la aplicación funcione: los clientes esperan que funcione y su percepción de los centros de software en torno a este requisito. Esto es especialmente cierto si desarrolla software comercial o algo que usarán personas no técnicas. Los desarrolladores deben ser conscientes de las necesidades del usuario final a lo largo de todo el proceso de diseño de software.

Una aplicación de software debe ser lo más fácil de navegar y usar posible. Con la cantidad de software que se va a crear, se calcula que 4 de cada 10 aplicaciones de software tienen una interfaz de usuario realmente excelente que realmente le gusta al usuario final y que se siente cómodo al instante al usar.

Se crea una gran cantidad de software de uso interno para las empresas. Tanto si se desarrolla de forma local como bajo el cuidado de un consultor, a menudo se invierte un mínimo de tiempo, esfuerzo o dinero en crear una interfaz de usuario mejor. El rol "diseñador" es poco frecuente en el ciclo de desarrollo, especialmente en el mundo de Windows aplicaciones.

Hay algunas reglas básicas que se deben seguir para tener una interfaz de usuario mucho más adecuada y que funcione mejor para la aplicación. No requiere demasiada inversión de tiempo o dinero por su parte y agrega una buena rentabilidad de la inversión.

Antes de continuar, vamos a diferenciar entre la interfaz de usuario y la experiencia del usuario, al menos para el ámbito de este artículo. La interfaz de usuario, o interfaz de usuario, hace referencia a los objetos visuales y controles de la aplicación, mientras que la experiencia del usuario, o UX, abarca tanto la interfaz de usuario como el comportamiento de la aplicación relacionado con la interfaz de usuario, así como el "sentimiento" que el usuario obtiene de la aplicación. No se trata solo de diseñar una interfaz de usuario de gran aspecto, sino también de asegurarse de que funciona bien.

Aquí trataremos 20 puntos de diseño de la experiencia de usuario que puede integrar fácilmente en la fase de diseño de aplicaciones. El resultado serán aplicaciones más enriquecciones con una mejor funcionalidad intuitiva: una "experiencia de usuario humana". Como todos sabemos, Windows generación de aplicaciones de Vista tendrá que tener un aspecto y un comportamiento distintos. Este tema le ayudará a prepararse para futuras aplicaciones a la vez que ofrece a los usuarios actuales una vista del futuro.

En las secciones siguientes se de abordan los aspectos básicos del diseño adecuado de la interfaz de usuario.

## <a name="the-basic-principles-of-proper-ui"></a>Principios básicos de la interfaz de usuario adecuada

Una experiencia de usuario profesional depende de estos cuatro factores:

-   Espaciado y posicionamiento
-   Size
-   Agrupación
-   Intuición

Con las versiones de Microsoft Visual Studio anteriores a la 8.0, el espaciado y el tamaño era suboptimable. Una cuadrícula 4x4 o 8x8 no siempre funciona. Con la inclusión de SnapLines, el proceso se ha simplificado en gran medida. Alinear una etiqueta con un cuadro de texto, o incluso peor, alinear varias etiquetas con sus cuadros de texto correspondientes era muy difícil en versiones anteriores de Visual Studio. Las snaplines han simplificado en gran medida este proceso.

En las secciones siguientes se describen cuatro de los aspectos más importantes del diseño de experiencia de usuario profesional.

### <a name="spacing-and-positioning"></a>Espaciado y posicionamiento

El espaciado entre dos controles es importante. En la siguiente captura de  pantalla se muestra un formulario de entrada de información de usuario mal diseñado: los dos cuadros de texto principales están demasiado cerca, la lista debajo de ellos está demasiado lejos y hay una gran cantidad de espacio sin usar en el formulario.

![captura de pantalla de un formulario mal diseñado.](images/humanux-01.png)

En la siguiente captura de pantalla, puede ver un cuadro de diálogo de aspecto más profesional con un espaciado adecuado y controles con el tamaño adecuado. Se trata del mismo formato que en la captura de pantalla anterior, pero se modificó para usar el espaciado recomendado por las líneas de ajuste. Siempre se recomienda alinear una etiqueta con la línea base de texto del cuadro de texto u otro control situado junto a ella, en lugar del borde inferior real del control. Las líneas de ajuste giran un color diferente cuando se alcanza esa alineación, normalmente unos pocos píxeles por encima del borde inferior.

![captura de pantalla de un formulario más bien diseñado.](images/humanux-02.png)

Aunque no hay reglas exactas para el espaciado, las snaplines proporcionan directrices muy útiles para el espaciado adecuado. Otras herramientas que le ayudarán a mantener el espaciado adecuado son los controles Diseño del grupo de herramientas Contenedores. TableLayoutPanel también es muy útil para crear cuadros de diálogo de estilo de formulario de entrada.

### <a name="size"></a>Size

Las mismas consideraciones se aplican al tamaño. Al arrastrar un botón desde el cuadro de herramientas hasta el formulario, tiene el alto y el ancho perfectos. El ancho máximo recomendado (sin tener en cuenta las razones muy importantes) es duplicar el ancho original.

Si observa la ventana Ejecutar  en el  menú Inicio o el cuadro de diálogo Propiedades de cualquier objeto Windows Explorer, los tamaños de los botones son "correctos".  Si tiene una función muy importante que necesita que el usuario final observe sin errores, hay otros métodos que no son el uso de un botón grande o colores no estándares (más adelante).

En la imagen siguiente, puede ver tres botones. El primer botón es el tamaño más recomendado y es el tamaño que se crea de forma predeterminada cuando se arrastra (o se hace doble clic) desde el cuadro de herramientas. A veces, el texto adicional requiere que el botón sea más grande. El segundo botón muestra un tamaño grande pero aceptable. No crearía un desorden para la creación de otros controles. Sin embargo, el tercer botón es un tamaño completamente inaceptable. Puede ver que incluso distorsiona ligeramente los mapas de bits del tema Windows usa para dibujar controles con temas. También hará que sea difícil alinear otros controles de forma intuitiva a su alrededor.

![imagen de tres botones, aumentando su tamaño de izquierda a derecha.](images/humanux-03.png)

### <a name="grouping"></a>Agrupación

Normalmente, una aplicación contiene muchos controles. Solo mediante una agrupación adecuada e intuitiva puede facilitar el uso de todos estos controles. La agrupación basada en funciones o clasificada se realiza mejor mediante controles Tab. Por ejemplo, "Cuentas", "Informes", "Empleados" y "Proyectos" serían candidatos perfectos para las pestañas en una aplicación empresarial típica. La agrupación del mismo nivel(los controles que contribuyen al mismo resultado final) se realiza mejor mediante controles de grupo. No se recomienda usar paneles con bordes para dicha agrupación. Los controles de grupo le ahorran el peso adicional de un control de etiqueta, especialmente si los controles secundarios se explican por sí solos.

No se recomiendan controles de grupo dentro de controles de grupo a menos que no haya más de 2 o 3 de ellos dentro de un control de grupo grande.

### <a name="intuitiveness"></a>Intuición

Este es el aspecto más importante de una experiencia de usuario excelente. La experiencia de usuario intuitiva abate la necesidad de explicaciones. El usuario solo sabe lo que hacen los controles.

Un tema importante en el diseño intuitivo es la codificación de colores. Un buen ejemplo se presenta en Windows XP, que presenta nuevos botones de cuadrado  flexible  para funciones como la navegación en aplicaciones con temas, los cuadros de diálogo Cerrar sesión y Desactivar equipo, etc.

El color de estos controles se determinó en función de la gravedad del resultado del botón que se va a insertar. La navegación es verde, muy parecido a un semáforo "Go". Apagar, lo que daría lugar a una posible pérdida de trabajo, se coloreó de rojo como un signo de advertencia. Los botones semi críticos, como Cerrar sesión o Hibernar, son amarillos. Los botones neutros que no tienen ningún efecto crítico en los procesos de trabajo del usuario, como la Ayuda, son de color azul suave. Al crear una interfaz de usuario con máscara, estos aspectos de color deben tenerse en cuenta.

Un buen ejemplo de reconocimiento de contenido por colores es Microsoft Office OneNote. Las pestañas de la aplicación se pueden establecer en distintos colores y, al mismo tiempo, parecerse esencialmente a una parte adecuada del diseño Windows estilo XP.

Otro aspecto importante es el texto de las aplicaciones. Recientemente, se han realizado varios esfuerzos para simplificar el lenguaje usado para las instrucciones escritas en Windows software. El uso de texto dentro del software se analizará más adelante, pero tenga en cuenta los siguientes detalles pequeños pero importantes.

MSN Messenger tenía una casilla en el cuadro de diálogo **Opciones** marcada como "Compartir funcionalidades de cámara web". Los desarrolladores y los expertos en tecnología saben lo que eso significa, pero un usuario principiante podría pensar que podría permitir que otro usuario del otro extremo del chat también use su cámara web. En una versión reciente, la cambiaron a "Mi cámara web: permitir que otros usuarios vean que tengo una cámara web". Esto es perfecto para el público de destino que puede que no tenga conocimientos técnicos y que estén acostumbrados a un lenguaje sencillo.

Aunque un lenguaje más sencillo facilita la información, también hay una ventaja adicional. Los estudios científicos muestran que nuestra mente funciona más fácilmente con un lenguaje más sencillo al intentar comprender algo nuevo. A menudo, nuestro cerebro procesa palabras como "it", "for", "that" y otras palabras comunes con tanta rapidez y esfuerzo que se asigna más "ancho de banda" para comprender las palabras que destacan, como "Cámara web" u "Otros", en el ejemplo anterior.

Los títulos del cuadro de mensaje, los títulos de GroupBox y otros bloques de texto de este tipo hacen que sea fácil transmitir la función de un grupo de controles al usuario final con solo unas pocas palabras.

La intuitiva también se debe a la familiaridad. Por ejemplo, la colocación  de los botones **Aceptar** y Cancelar es tan uniforme y bien colocada en nuestra mente que si un cuadro de diálogo contiene estos botones en una secuencia inversa (**Cancelar**, luego Aceptar **;** en lugar de Aceptar **,** cancelar **),** simplemente podría hacer clic en **Cancelar** en su lugar. Después de usar un estándar determinado para hacer cosas(por ejemplo Windows aplicaciones basadas en aplicaciones basadas en aplicaciones) durante más de un año, los hábitos se desarrollan. Seguir los estándares del sector (por no estar establecidos) facilita el uso del software.

En una de las primeras compilaciones Windows vista previa de  Vista, los botones **Minimizar,** **Maximizar** y Cerrar de cualquier ventana se diferenciaron. En versiones anteriores de Windows (especialmente cuando se usa un solo monitor), se desarrolla el hábito de mover el cursor en la esquina superior derecha de la pantalla y hacer clic en él. Esto siempre ha provocado el cierre de la ventana. Ahora, en esta compilación concreta de Windows Vista, había aproximadamente 8 píxeles de espacio entre el botón Cerrar y el borde más a la derecha de la ventana. El espacio adicional hizo que parezca es cool (y probablemente era necesario para la animación de efecto del botón), pero estaba desenlomezándose porque no permitía a los usuarios cerrar las ventanas abiertas tan fácilmente. La reacondición de la mente puede ser difícil. Afortunadamente, en la siguiente compilación, se ha solucionado este problema. Ahora, todavía hay espacio entre el borde de la ventana y el botón Cerrar, pero al hacer clic en ese espacio también se cierra la ventana.

Un factor muy importante del diseño intuitivo es la cantidad de "ancho de banda mental", la cantidad de tiempo que se puede tardar en comprender algo, que usa. Entre menor sea el uso del "ancho de banda", mejor será la experiencia del usuario.

Estas son pequeñas cosas que contribuyen a la "experiencia" de uso de una aplicación de software. En los ejemplos siguientes se proporcionan sugerencias para mejorar las aplicaciones con sugerencias y trucos del mundo real.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 Sugerencias una experiencia de usuario mejor y funcional

El objetivo de una mejor experiencia del usuario es tener una interfaz de usuario más sencilla, más sencilla y funcional que también tenga un aspecto bueno. Estas sugerencias le ayudarán a dar forma a la interfaz de usuario para que sea más eficaz.

### <a name="use-standards"></a>Usar estándares

Los estándares establecidos de cualquier entorno de software, ya sea en el nivel de sistema operativo, nivel de marca o nivel de aplicación, son muy importantes. Además de la personalidad de marca, los estándares actúan como un esquema demostrativo en la mente del usuario. Cuando el usuario pasa largos períodos de tiempo trabajando con una aplicación de software, aumentará automáticamente la productividad debido a la creciente familiaridad.

Antes de analizar los estándares, primero vamos a analizar cuáles son exactamente estos estándares. Los estándares incluyen todo, desde el diseño de controles  de  una manera determinada en los cuadros de diálogo, como los botones Aceptar y Cancelar, la forma de la interfaz de usuario, las esquinas redondeadas de la parte superior de la ventana, como en los cuadros de diálogo xp de Windows, los estilos de iconos, los estilos de cualquier otro gráfico, el comportamiento interactivo de la aplicación y otros.

Si la aplicación se encuentra en un sector específico, puede que sea mejor seguir un conjunto diferente de estándares. Por ejemplo, si la aplicación admite, una aplicación o un complemento para, Office OneNote 2003, es aconsejable seguir los estilos de los estándares de interactividad y de interfaz de usuario de Office, y OneNote sí mismo, en particular. Esto incluye el uso de Office de comandos en lugar de las barras de herramientas estándar y otras cosas, tanto visuales como de comportamiento. Si la aplicación va a formar parte de la Microsoft Visual Studio de .NET, tiene un conjunto independiente de estándares. De hecho, para tales aplicaciones de complemento o soporte técnico, empresas como Microsoft sí publica directrices escritas. Tenga en cuenta también que, a veces, los conceptos gráficos y de diseño son propiedades intelectuales protegidas. Compruebe siempre la documentación adecuada para asegurarse de que tiene la licencia para crear estos diseños.

Un tercer ejemplo de estándares sería el entorno de Tablet PC. Estos estándares cruzan los límites entre las directrices del sistema operativo y las directrices de aplicación. La [documentación del SDK de Tablet PC](/previous-versions/ms840465(v=msdn.10)) contiene información muy útil en el tema "Planeamiento de la aplicación". A diferencia de las directrices de Office 2003 o Visual Studio, estas recomendaciones de diseño afectan directamente a cómo interactuará el usuario con la aplicación y cómo debe comportarse a su vez. Por ejemplo, si tiene ventanas acopladas en la aplicación, la documentación recomienda asegurarse de que puede detectar cuándo se cambia la orientación de la pantalla y de que las ventanas de acoplamiento se reorganizan correctamente en una orientación vertical u horizontal según sea necesario. Incluso si no está diseñando la aplicación para que sea específica de la tableta, debe seguir estas directrices.

Con el aumento de los clientes inteligentes, las aplicaciones ahora cruzan los límites entre diferentes hardware: equipos normales, tabletas, dispositivos móviles o Ultra, equipos de Media Center, entre otros. Cada situación requiere que se sigan un conjunto de estándares diferente (o adicional).

Cuando las aplicaciones comparten los estándares de nivel de sistema operativo o de aplicación, los usuarios se sientan más cómodos con el software, lo que facilita el aprendizaje y el uso. Estos resultados son un aumento directo de la productividad. Los usuarios quieren ser productivos con nuevo software lo más rápido posible.

### <a name="draw-attention-to-important-buttons"></a>Llamar la atención sobre los botones importantes

En ocasiones, es necesario dirigir al usuario a los botones más importantes, incluso si tiene cuatro o cinco botones más a su alrededor. Si experimenta con el tamaño, el color o la fuente, interrumpiría los estándares, lo que no se recomienda. En su lugar, puede usar un par de trucos sencillos para lograr esto.

La primera es convertir los demás botones no críticos en LinkLabels, como se muestra en la imagen siguiente. De este modo, el usuario sabe que estos vínculos realizarán una tarea, pero su atención irá primero al botón que destaca, sin romper las directrices de diseño estándar.

![imagen de tres botones convertidos en etiquetas de vínculo.](images/humanux-04.png)

La segunda es colocar el botón crítico en primer lugar en línea, ya sea a la izquierda para los diseños horizontales, como se muestra en la imagen siguiente, o encima para los diseños verticales. Tenga en cuenta que esto puede cambiar en función de la referencia cultural del usuario de destino: puede que le conste mejor si coloca el botón en cuestión en el extremo derecho si la aplicación es cualquier idioma escrito de derecha a izquierda.

![imagen de tres botones donde el botón crítico está situado más a la izquierda en un diseño horizontal.](images/humanux-05.png)

La opción recomendada es establecer para recibir el foco de forma predeterminada. Por ejemplo, en un cuadro de diálogo de confirmación de eliminación, se debe resaltar la opción **No,** ya que esto impide que el usuario elimine accidentalmente algo.

### <a name="simplify-recognition-with-icons"></a>Simplificar el reconocimiento con iconos

Los iconos, especialmente los iconos de Windows XP y Office 2003 y los mapas de bits de la barra de herramientas, ayudan a acelerar la cognición de la interfaz de usuario y la tarea que el usuario tiene que realizar.

Por ejemplo, cuando ve el icono de exclamación más a menudo en el cuadro de mensaje, al instante se da cuenta del nivel de riesgo asociado a los controles situados junto a ese icono. De forma similar, cuando la aplicación coloca una gran cantidad de controles, independientemente de cómo se organizan correctamente, puede ser desalentador encontrar el conjunto de controles que está buscando.

En Windows XP Service Pack 2, se agrega una pestaña actualizada al applet del panel de **control** Propiedades del sistema denominado "Actualizaciones automáticas". Hay cuatro opciones: descargar actualizaciones automáticamente, descargar actualizaciones, pero dejar que el usuario decida cuándo instalarlas, notificar al usuario si hay actualizaciones disponibles, pero no iniciar la descarga, y deshabilitar completamente las actualizaciones automáticas.

Es posible que un nuevo usuario del equipo no sepa cuáles son estas actualizaciones y que no sepa qué opción sería mejor elegir. Por lo tanto, Microsoft ha puesto un icono de escudo verde con una marca de verificación grande junto al más recomendado que indica una opción "segura" y un icono de escudo rojo con una "x" grande junto a la que podría ser perjudicial para el usuario. Esto es muy útil en situaciones críticas, especialmente cuando el usuario no tiene tiempo para leer demasiado texto.

En el mismo applet **Propiedades** del sistema, cada pestaña tiene varios GroupBoxes con controles diferentes para diferentes tareas. Se coloca un gráfico relativo junto a cada grupo que significaría fácilmente la tarea del grupo de control. Este tipo de código gráfico es similar a la codificación por colores en archivos físicos o lotes de aparcamiento. Esto también funciona con el mismo principio de tener al menos algunos objetos visuales en un artículo de una revista: mantiene el interés del lector.

También es importante elegir el icono derecho. Microsoft proporciona muchos gráficos estándar como parte de Visual Studio 2005. Esta sería la mejor opción. Si crea sus propios iconos, se recomienda encarecidamente seguir los estándares de nivel de [](#use-standards) sistema operativo o de aplicación para estos gráficos, como se mencionó en la sección Usar estándares anterior.

El [Windows de interacción de la experiencia del](/windows/apps/desktop/) usuario contiene una guía muy útil para crear iconos Windows estilo [.](https://msdn.microsoft.com/library/aa511280.aspx)

### <a name="simplify-recognition-with-headers"></a>Simplificar el reconocimiento con encabezados

Los encabezados son la manera perfecta de explicar todo el cuadro de diálogo en una sola oración (y, opcionalmente, un gráfico). A veces, los encabezados también pueden ayudarle a acomodar la navegación y los comandos dentro de ellos. Los encabezados funcionan de forma más eficaz que las etiquetas de descripción normales porque son lo primero que un usuario ve cuando aparece el cuadro de diálogo.

Los asistentes Windows installer son quizás los encabezados más populares: un icono simple en el extremo derecho; una etiqueta de título que describe el cuadro de diálogo (por ejemplo, Seleccionar carpeta de instalación); y un subpartido que describe el propósito del cuadro de diálogo (por ejemplo, Seleccione la carpeta donde se instalarán los archivos de software).

Supongamos que tenemos una aplicación empresarial típica con una sección de cuentas. Siguiendo el paradigma de diseño de Windows Vista, podemos proporcionar información crítica y comandos relacionados en el propio encabezado (o pie de página, si el escenario lo requiere). Nuestro usuario ha abierto el archivo de cuenta para "Big Company" y el encabezado tendría un aspecto parecido al que se muestra en la siguiente captura de pantalla.

![captura de pantalla de un cuadro de diálogo que contiene un pie de página detallado.](images/humanux-06.png)

En la siguiente captura de pantalla se muestra un ejemplo de un encabezado detallado en un cuadro de diálogo.

![captura de pantalla de un cuadro de diálogo que contiene un encabezado detallado.](images/humanux-07.png)

Del mismo modo, puede evitar tener que agregar Windows paneles de tareas de estilo XP, especialmente cuando solo tiene unos pocos comandos, lo que desperdiciaría mucho espacio vertical, moviendo estos comandos al encabezado.

Hay algunas cosas que debe tener en cuenta al diseñar encabezados:

-   Asegúrese de que el color de fondo es diferente del color de fondo del cuadro de diálogo. Con más frecuencia que no, un encabezado blanco sobre un Windows el color de la cara de control intrínseco. Pero si realmente quiere asegurarse de que ningún tema especial o colores personalizados desaconsejen el encabezado, dibuje un **objeto LinearGradient** con **color.FromKnownColor** con los colores **ControlLight** y **ControlDark**.
-   Si es posible, mantenga el alto del encabezado por debajo de 150 píxeles. Normalmente, una altura de 100 o 120 lo hará. Como regla general, asegúrese de que sea inferior a 1/4 de la altura de todo el formulario.
-   Si desea agregar la edición en contexto para la información que se muestra en el encabezado anterior, reemplace dinámicamente LinkLabel por un cuadro de texto e intercambie de nuevo una vez que se haya realizado la edición.
-   Si tiene una etiqueta de título con una fuente de más de 10 puntos de tamaño, use Arial o El medio Desconsocario. MS Sans Serif tendrá un aspecto demasiado irregular y poco profesional. Se recomienda en la documentación de Windows XP Design Guidelines. En el caso de las aplicaciones Windows Vista, use la Segoe UI que es la fuente predeterminada del sistema.

### <a name="use-custom-message-boxes"></a>Usar cuadros de mensaje personalizados

Las opciones disponibles en el cuadro de Windows estándar son muy limitadas. Cuando tiene que hacer al usuario una pregunta que no se puede responder con un sí/no simple o aceptar/cancelar, se complica.

Windows aplicaciones se están volviendo más fáciles de usar debido al gran volumen de usuarios no técnicos. A veces, puede ser mucho más sencillo proporcionar botones con textos más descriptivos e incluso algunos controles adicionales (LinkLabels, por ejemplo) para facilitar la realización de la tarea a mano.

Microsoft .NET Framework facilita la implementación de diálogos personalizados. Simplemente asignando un par de propiedades en el formulario de diálogo personalizado o con una sola línea de código, el formulario puede funcionar igual que un cuadro de mensaje estándar. En un evento de clic de botón, establezca la propiedad **DialogResult** del diálogo en **DialogResult.Ok** o **DialogResult.Cancel**. Use el **método ShowDialog( \[ OwnerForm \] )** del formulario primario. Este método devuelve el valor **DialogResult.**

Puede usar todos los **miembros DialogResult.** El método **MessageBox.Show** estándar usa estas mismas opciones.

Como alternativa, puede establecer la propiedad **AcceptButton** del cuadro de diálogo en **btnOK** y la **propiedad CancelButton** en **btnCancel**. Esto asignará automáticamente las teclas **Entrar** y **Esc** a los eventos Click correspondientes de los botones **btnOK** y **btnCancel.**

Estas son algunas sugerencias para crear diálogos personalizados:

-   Para temas complicados, proporcione vínculos a la Ayuda local o en línea con una etiqueta de vínculo que indique "Más información" en la etiqueta de texto adecuada.
-   En **lugar** de los botones Sí No Cancelar, use texto que indica claramente el resultado de hacer clic en el botón, como "Guardar archivo y /  /  salir", "Salir sin guardar" y "No salir". Sin embargo, se adhiere a los botones **Estándar Sí** / **No,** **Aceptar** Cancelar y / estos botones estándar siempre que sea posible. La familiaridad permite una gran productividad.
-   Mantenga un espacio de margen de 50 píxeles en el lado izquierdo (o en el lado derecho según la configuración de la referencia cultural de destino) y agregue un icono que represente el escenario del cuadro de diálogo. Si se trata de un cuadro de diálogo de información, puede usar el icono "i" que usan los cuadros de mensaje estándar; Si se trata de un cuadro de diálogo de seguridad, puede usar un icono de bloqueo o un icono de clave. Visual Studio 2005 se incluye con algunos gráficos de alta calidad excelentes.
-   Asegúrese siempre de proporcionar la navegación con el teclado adecuada para estos botones: los usuarios usan los métodos abreviados de teclado para los cuadros de mensaje (por ejemplo, O para Aceptar, Y para Sí, C para Cancelar, y así sucesivamente) en gran medida. Si el cuadro de diálogo personalizado no los usara, resultaría molesto.

### <a name="include-alternate-commands"></a>Incluir comandos alternativos

Dos factores importantes determinan la necesidad de métodos de entrada alternativos: frustración y latencia. La frustración es algo que se produce con demasiada frecuencia para los usuarios del equipo. Cuando esté frustrado, querrá que la tarea se haga rápidamente. Un clic adicional o una espera adicional de unos segundos realmente inquiete a una persona bajo presión, ya sabe cómo está, todos hemos estado allí. Laziness a menudo le anima a finalizar la tarea con solo el teclado o el mouse, lo que se use en este momento. Pero, aparte de estos dos factores, tener métodos de entrada alternativos facilita al usuario la realización de tareas.

Por ejemplo, si tiene un cuadro de lista con dos botones("Agregar" y "Quitar") a cada lado, debe agregar un menú contextual para ese cuadro de lista con comandos de menú análogos a esos botones. Esto ofrece al usuario la oportunidad de elegir el método que encuentra más adecuado. Los usuarios principiantes, como el estado Windows directrices de experiencia del usuario de Vista, usan mucho los menús contextuales y esperan que sean en cualquier lugar en el que hacen clic con el botón derecho.

De forma similar, usamos controles visuales para texto o entrada numérica. Por ejemplo, los controles deslizantes se usan para especificar enteros y los controles Calendar se usan para la entrada de fecha. A veces puede ser más cómodo simplemente escribir. A menudo puede marcar una diferencia para el usuario si agrega un control Numeric Up-Down vinculado a un control Slider, o bien usa dateTimePicker en lugar del control Calendar.

### <a name="how-to-handle-critical-actions"></a>Cómo controlar acciones críticas

Al realizar una función crítica y irrecuperable, suele ser un procedimiento recomendado hacer que un cuadro de mensaje emergente confirme la acción. Vamos a tomarlo en una notch. En la siguiente captura de pantalla puede ver un cuadro de mensaje personalizado similar, pero con una ventaja adicional: un temporizador que se muestra visualmente con la ayuda de una barra de progreso.

![captura de pantalla de un cuadro de diálogo de acción crítica.](images/humanux-08.png)

Hay algunas variaciones específicas del escenario que puede usar. Si la acción que se va a realizar es muy crítica (desde la sobrecarga de una central eléctrica hasta la eliminación permanente de archivos), la acción predeterminada después de que se agote el temporizador debe cancelarse. El cuadro de diálogo no debe desaparecer, sino que la etiqueta de texto cambia para mostrar que la acción se ha cancelado. El usuario puede optar por confirmar el comando o la cancelación.

Asegúrese siempre de que los botones que realizan operaciones críticas estén claramente marcados; use siempre texto sin formato que describa con precisión la acción. Si la acción es la eliminación de archivos, no escriba "Quitar archivos del repositorio"; escriba "Eliminar archivos del repositorio". Al trabajar con listas de archivos, si un comando de menú Eliminar elimina los archivos seleccionados del propio disco duro (en lugar de quitarse solo de la lista de archivos), debe destacar correctamente la naturaleza crítica de esto y hacer que la acción elimine permanentemente los archivos.

Alguien ha dicho una vez: "Es tan bueno como su peor trabajo". Lo mismo se aplica a las aplicaciones de software. Una sola mala experiencia con la aplicación puede dar una gran impresión negativa al usuario. Para asegurarse de que esto no sucede, una cosa que puede hacer es asegurarse de que, si la aplicación se bloquea, se bloquea correctamente. Si puede agregar recuperación de datos o permitir que el usuario intente guardar una copia de los datos, puede ser una gran ventaja. Si la aplicación se bloquea, se debe notificar correctamente al usuario. Un JIT-Debugger diálogo de error crítico no es una buena cosa. Aunque hablar sobre cómo controlar los bloqueos va más allá del ámbito de este artículo, le recomendaré que un diálogo sencillo que se disculpe al usuario y le informe de la situación (y posiblemente con un vínculo a más información sobre cómo recuperarse de este bloqueo) sería muy útil para el usuario.

Si quiere ir un paso más allá, puede hacer lo que hace una de mis aplicaciones favoritas de diseño gráfico. Si se bloquea, se mostrará un cuadro de diálogo de recuperación que le permitiría guardar una copia independiente del archivo en el que se está trabajando y, a continuación, le proporcionaría un cuadro de diálogo de comentarios donde puede escribir información sobre el bloqueo (información personal opcional, por supuesto) y enviarla a los creadores.

### <a name="radiobuttons-or-comboboxes"></a>¿RadioButtons o ComboBoxes?

A primera vista, el método para realizar una selección de uno de varios no parece tan difícil o importante. A veces puede serlo, especialmente si el escenario es una aplicación que se usa para el trabajo con una especificaciones de tiempo.

Echemos un vistazo a un ejemplo real. Microsoft ha publicado recientemente una versión preliminar de una aplicación gráfica, Expression Graphics Designer (anteriormente denominada "Acrylic"). Tenía unos 20 objetos gráficos a los que tenía que asignar una determinada propiedad por separado en esta aplicación. Fue un proceso muy lúcido. Para ello, tenía que seleccionar el objeto, hacer clic en el botón para abrir la ventana de configuración y establecer las opciones. En una de estas opciones, se tenían que elegir dos opciones de comboBox, como puede ver en la siguiente captura de pantalla.

![captura de pantalla del cuadro de diálogo textura de textura de textura para el diseñador de gráficos de expresión.](images/humanux-09.png)

Cuando tenga que colocar la lista ComboBox y seleccionar el segundo elemento (de solo 2 elementos), puede resultar realmente tentador. Por lo general, lo que no sabemos es el tiempo que tarda en aparecer la lista desplegable. Puede perder mucho tiempo y puede resultar frustrante. Esto se podría resolver fácilmente colocando un GroupBox con dos RadioButtons, especialmente cuando hay tanto espacio disponible. He encontrado problemas similares en aplicaciones comoIbudraw, Microsoft Access y otras.

Además de perder tiempo debido a la animación de lista desplegable, también desperdicia nuestro "ancho de banda mental". Con dos radioButtons "siempre visibles", nuestra mente conocería sin problemas la posición del cursor para hacer clic. Con ComboBox se procesará solo después de que se haya dibujado la lista. Aunque puede parecer demasiado poco importante, en realidad es muy importante.

A veces es mejor usar RadioButtons, especialmente si tiene 4 opciones o menos.

### <a name="never-disrupt-the-user"></a>No interrumpa nunca al usuario.

A corto plazo de ponerse un revólver en la cabeza, esto es lo más destructivo que un desarrollador puede hacer a los usuarios. Cuando la aplicación, innecesaria o de otro modo, interrumpe al usuario mientras trabaja en otra aplicación con un cuadro de mensaje o un flash de la barra de tareas, obtiene puntos negativos del usuario.

Los flashes de la barra de tareas pueden ser útiles, por supuesto, pero solo se debe llamar a ellos cuando el proceso de la aplicación requiere la entrada del usuario para continuar, o si tiene algo crítico que transmitir al usuario. Si el usuario ha mantenido la barra de tareas en Ocultar automáticamente, un botón de la barra de tareas parpadeante puede impedir que el usuario acceda a la barra de estado u otros controles de anclaje bajo, ya que la barra de tareas estaría encima de ella y no se ocultará de nuevo hasta que el usuario haya hecho clic en el botón de parpadeo.

![captura de pantalla de una ventana del sistema.](images/humanux-10.png)

Las ventanas del sistema (consulte la figura 10), que hacen famosos los clientes de mensajería instantánea como MSN Messenger, son una excelente solución para informar al usuario de algo sin alterar o interrumpir su flujo de trabajo. Hay un excelente artículo ( por https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) Bill Bill Bill sobre la creación de ventanas del sistema. Es una buena directiva (y maneras) no alterar las notificaciones del sistema de ninguna otra aplicación. La deserción de estas ventanas puede ser molesto e improductiva. Una solución es usar la exclusión mutua de ToastSemaphore (/library/WinMediceger/winmediceger/overview/toast.asp) proporcionada por el sistema operativo para evitar colisiones del sistema.

A veces, es posible que deba mostrar varios elementos mediante el sistema. En realidad, no sería aconsejable mostrar tres o más notificaciones del sistema. En su lugar, sería mejor pasar por cada uno de ellos mediante el desvanece de una notificación del sistema después de la otra. Microsoft Outlook implementa una solución similar al notificar al usuario los correos electrónicos entrantes.

### <a name="provide-progress-status"></a>Proporcionar el estado de progreso

A menudo hay tareas que requieren que el usuario espere. Por supuesto, esta es una de las cosas que el usuario simplemente no quiere hacer. Pero peor es cuando esperan sin saber lo que sucede. A veces, es posible que la aplicación tenga que conectarse a un servicio web o a un equipo remoto, o quizás esté procesando grandes fragmentos de datos, sea cual sea el motivo, el usuario debe ser consciente, o al menos de forma imprecisa, de lo que sucede en segundo lugar. Hay diferentes métodos para hacerlo, en función de la situación.

Si se conecta a algún objeto lejano, como un servicio web o algo colocado en una red o un servidor de Internet, sería aconsejable mostrar un cuadro de diálogo de progreso simple (vea la siguiente imagen) o una barra de progreso hospedada en la barra de estado. Una etiqueta que lo acompaña debe describir el estado actual del proceso. Por ejemplo, si se conecta a un servicio web para procesar algunos datos, simplemente diga "Conexión al servicio web... " o "Espere, procese... " Si este proceso es sincrónico, es aconsejable deshabilitar todos los controles a los que el usuario puede acceder hasta que se haya completado el proceso, o simplemente mostrar el progreso como un cuadro de diálogo modal.

![captura de pantalla de un cuadro de diálogo de barra de progreso.](images/humanux-11.png)

Se recomienda encarecidamente establecer el estilo de la barra de progreso en el modo Marquee si usa una barra de progreso y se desconoce el tiempo de procesamiento, o si no tiene un valor máximo.

Otro método que se está volviendo popular es una ventana fija "toast" que muestra el progreso. El descargador o actualizador de Microsoft AntiSpyware o las notificaciones del sistema de análisis de correo electrónico de AntiVirus son buenos ejemplos de esto. Por supuesto, esto solo se debe usar para procesos asincrónicos. De lo contrario, es posible que el usuario se sienta desconcertado. Estas ventanas se usan mejor para el procesamiento en segundo plano, como descargar una actualización o realizar una tarea programada, y nunca deben establecerse en "Siempre encima".

### <a name="simplify-complex-steps-with-wizards"></a>Simplificar pasos complejos con asistentes

Es seguro suponer que, si se enfrenta a una gran cantidad de controles en un solo formulario, un usuario típico se confundirá sin ningún fin. A veces, ninguna cantidad de agrupación, tamaño o espaciado puede ayudarle cuando tiene muchos controles importantes.

Un asistente es lo mejor para estos escenarios. Puede dividir los controles por tarea o categorías según corresponda y colocarlos en pasos independientes. Esto puede ayudar al usuario a centrarse y no desalentarse por la tarea. Puede proporcionar ayuda específica de pasos o tareas con un botón Ayuda. Puede encontrar las directrices de creación del asistente en MSDN Library.

Los asistentes también son una buena manera de ayudar a configurar la configuración inicial de la aplicación. Muchas aplicaciones usan este tipo de asistente para configurar una configuración personalizada justo después de que se complete la instalación o en el primer uso. Este asistente inicial también debe ser opcional, si es posible: si el usuario cancela en cualquier momento, la configuración no especificada pasa a los valores predeterminados. Si puede hacer que el asistente [](#use-pretty-graphics) sea un poco gráfico (consulte la sección Usar gráficos bastante), la tarea de configuración será mucho más fácil.

### <a name="get-the-tone-of-your-text-right"></a>Obtener el tono del texto a la derecha

En el [Windows de interacción de la experiencia del](/windows/apps/desktop/)usuario, se ha hecho un punto muy importante sobre "Tono de texto". Esta es la impresión y la sensación que da el texto de la aplicación. Puede ser cualquier cosa, desde una información sobre herramientas simple hasta un control de etiqueta de instrucciones.

Anteriormente se ha analizado el cambio de texto en la opción Cámara web en MSN Messenger. Esto se denomina tono de texto adecuado. Cuando se trabaja con usuarios no técnicos o no expertos, la obtención del mensaje entre toma un aspecto diferente.

Si escribe "Ruta de acceso de destino" encima de un cuadro de texto en una aplicación autoextrayéndola, un usuario técnico puede saber fácilmente que escribe algo parecido a "C: \\ Temp \\ MyPath". Un usuario principiante (piense en "Mamá") se puede desconcertar fácilmente y tendría que hacer referencia al manual, llamar al soporte técnico o, peor aún, dar por hecho. Una buena alternativa es especificar lo que quiere que haga el usuario: "Seleccione la carpeta donde desea colocar estos archivos". Incluso puede cambiar el nombre de "Examinar... Botón " que reside junto a ese cuadro de texto en "Seleccionar carpeta... "

Si proporciona una descripción clara de lo que quiere que haga el usuario, también se disminuirá la necesidad de archivos de Ayuda o, al menos, se reducirán los detalles que se deben incluir en los archivos de Ayuda.

Una sugerencia muy buena de las [directrices Windows interacción de](/windows/apps/desktop/) la experiencia del usuario se aplica a cualquier software. Indica que el escritor debe mantener el texto conversacional. Las directrices definen esto como "Evitar palabras que no se digan a otra persona".

Algunas sugerencias para escribir texto:

-   Evite hablar sobre el usuario en tercera persona. Diga "Usted" en lugar de "El usuario".
-   Siempre que sea posible, use con inteligencia "Mi nombre:" o "Mi dirección de correo electrónico:" en lugar de "Nombre:" o "Correo electrónico:"
-   Al dar varias opciones, escriba el texto desde la perspectiva del usuario. Por ejemplo, si tiene dos RadioButtons bajo una etiqueta como "Select permission for Username on this network" (Seleccionar permiso para el nombre de usuario en esta red) encima de dos RadioButtons, como "Allow" y "Deny", reemplace el texto RadioButton por "I want to allow Username" (Quiero permitir el nombre de usuario) y \[ \] \[ \] "I want to disallow \[ Username \] ".
-   Texto subrayado solo si se usa para los vínculos. Confundirá al usuario si el texto subrayado no es un vínculo.
-   Preste atención a información importante con una etiqueta en negrita, pero úsela con cuidado. Demasiado texto en negrita es confuso y reduce el impacto general del formulario.
-   Al escribir el texto de una casilla, asegúrese de que es fácil saber qué ocurrirá cuando esté seleccionado y cuando no esté seleccionado o desactivado. La opción recomendada es escribir el texto directamente como resultado de la casilla que se está seleccionando. Por ejemplo, escriba "Enviarme información útil de sus asociados" en lugar de "No enviarme información útil de sus asociados". Aunque puedo imaginar que muchas personas de marketing argumentan sobre este ejemplo en particular, estoy seguro de que sabe lo que quiero decir.
-   Si tiene un control similar a un botón (normalmente un RadioButton con una apariencia de botón de comando) que controla Habilitado/Deshabilitado, asegúrese de etiquetar correctamente. Si el proceso está habilitado, escriba "Habilitado" en lugar de "Habilitar" o "Deshabilitar". Si escribe Habilitado, se muestra el estado actual. Si se hace clic en el botón (habilitado) y el botón indica "Habilitar", puede resultar confuso y problemático. "Habilitar" podría pedir al usuario que haga clic en él pensando que el proceso no está activo.

### <a name="sometimes-a-listview-is-better"></a>A veces, un control ListView es mejor

A menudo nos quedamos con DataGrid, ListBox o incluso ComboBox para las tareas de selección, pero con Windows XP y versiones posteriores de Windows, el uso de listView puede proporcionar opciones más grandes.

Puntos precisos del control ListView:

-   Acelera el reconocimiento de elementos con iconos y mapas de bits.
-   Muestra información adicional con las vistas Detalles o Mosaico.
-   Con Visual Studio 2005, incluso puede tener grupos para la categorización adicional. Los grupos abarcan todas las vistas y son flexibles. Los grupos también se pueden usar para aplanar una vista de jerarquía (como treeView) donde hay más nodos secundarios que nodos primarios. Un buen ejemplo de esto es el cuadro de diálogo Conexiones de red de Windows XP, cuando se ve con "Mostrar en grupos" y la vista establecida en Detalles.
-   Para personalizar un control ListView, pinte manualmente estableciendo la propiedad **OwnerDraw** y usando los eventos **DrawItem** **y DrawSubItem.**
-   Admite la edición rápida en contexto de elementos ListView.
-   Admite fácilmente la reordenación manual.
-   Permite a los usuarios seleccionar la vista (iconos grandes, iconos pequeños, lista, entre otros) con la que están más cómodos.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Simplificar la navegación con controles y barras laterales de ruta de navegación

"Sub-navigation" es la clave de la interfaz de usuario compleja. A veces no se puede escapar al tener una interfaz de usuario complicada. Lo mejor que se puede hacer en una situación de este tipo es que la experiencia sea lo más fácil posible para el usuario. Una barra lateral que consta de etiquetas de vínculo o TreeView para la navegación basada en jerarquías sugiere una navegación de nivel relacionado para la tarea del cuadro de diálogo actual. Resulta muy fácil para el usuario saltar entre los pasos del proceso a la vez que se sabe dónde está.

Si va a realizar una navegación basada en jerarquías con TreeViews u otra navegación similarmente compleja, una buena utilidad para el usuario sería un control de ruta de navegación. Aunque Visual Studio no se incluye con un control integrado para esto todavía, consulte [Creating A Breadcrumb Control](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) (Creación de un control de ruta de navegación) para obtener información sobre cómo crear uno usted mismo. Un control de ruta de navegación facilita la tarea de encontrar la ubicación actual en relación con la jerarquía.

La navegación por ruta de navegación se puede combinar fácilmente en el encabezado si el formulario tiene una. Consulte la sección anterior sobre los [encabezados](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Usar gráficos bastante

A todo el mundo le encantan las aplicaciones con gráficos interesantes, al menos la mayoría. Aunque una interfaz de usuario con gráficos bastantes no es una opción lógica para todas las aplicaciones, sí ayuda a dar una buena impresión y puede ser una gran satisfacción trabajar en ella. Por supuesto, los gráficos no deberían impedir la productividad, pero si se usan correctamente, pueden aumentarla.

No tiene que haber muchos gráficos ni requieren necesariamente mucho trabajo. Una pantalla de presentación diseñada profesionalmente o un encabezado (como el que hemos mencionado anteriormente) hace el truco. Si el presupuesto lo permite, puede usar gráficos bien diseñados para barras de herramientas, asistentes y mucho más. Hacen que la aplicación sea bastante y más profesional también. Es un efecto sutil, pero un aspecto profesional transmite confianza y estabilidad. Si es una empresa relativamente pequeña que crea aplicaciones comerciales, este es un aspecto clave que se debe tener en cuenta.

Haga siempre un punto para usar gráficos diseñados profesionalmente. Los gráficos sin impuestos están disponibles fácilmente y son asequibles. También puede contratar a un diseñador. Pero si los gráficos no son su nombre, no pruébalo usted mismo. Si no puede adquirir ni usar gráficos diseñados profesionalmente, es mejor no usarlos en absoluto.

Para gráficos pequeños, siempre puede buscar los iconos y mapas de bits que se envían con Visual Studio 2005. (No se recomiendan los gráficos incluidos con versiones anteriores).

### <a name="provide-resizable-forms-when-possible"></a>Proporcionar formularios de tamaño ajustable cuando sea posible

Las ventanas que se pueden cambiar de tamaño son algo parecido a las ventanas independientes de la resolución. Las ventanas independientes de la resolución tienen el mismo aspecto si se usan pantallas 96DPI o 300DPI. Independientemente de si la interfaz de usuario de la aplicación es independiente de la resolución, la tarifa será mejor si es ajustable. Por supuesto, esto no se aplicaría a muchos escenarios, pero es una buena regla de uso general.

Si la ventana trata con listas de cualquier tipo, especialmente ListViews, esto se vuelve aún más importante. Cambiar el tamaño permite al usuario ver más datos al mismo tiempo.

Por ejemplo, tenemos una aplicación en la que el usuario tiene que seleccionar una imagen de una colección grande. El cuadro de diálogo abierto permite seleccionar una vista en miniatura, pero el cuadro de diálogo tiene un tamaño fijo y la lista de miniaturas muestra solo 4 miniaturas a la vez. Si la colección tiene cien imágenes, desplazarse y buscar (una tarea repetitiva) puede ser bastante pesado y reducir la eficacia. Si el cuadro de diálogo se puede cambiar de tamaño, el usuario puede hacerlo tan grande como sea cómodo o al menos tan grande como la pantalla permitiría, y poder finalizar la tarea rápidamente. Si la lista tiene desplazamiento horizontal,como un Control ListView o DataGrid detallado, es incluso más pesado. Las ventanas que se pueden redimensionar son muy útiles en este tipo de situación.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Proporcionar más funcionalidad con barras laterales o paneles de tareas

Al igual que los encabezados de los que hemos hablado anteriormente, las barras laterales y los paneles de tareas son una manera magnífica de proporcionar funcionalidad adicional y comandos de utilidad. Por ejemplo, los paneles de tareas de Office Word 2003 son muy prácticos, accesibles y no intrusivos. También funcionan de forma asincrónica al conectarse a recursos en línea, lo que proporciona al usuario la opción de varias tareas.

Crear un panel de tareas o una barra lateral es tan fácil como crear un panel de acoplamiento, con la opción de colocar un gráfico de acoplamiento en la parte superior para que actúe como una barra de título. Incluso puede usar un control Etiqueta coloreado para eso. Las oportunidades de los paneles de tareas son muchas.

Si tiene funcionalidad adicional y desea proporcionarla de forma no intrusiva al usuario, no hay ningún lugar como el panel de tareas. También puede hacer que los paneles de tareas "Ocultar automáticamente" o se contraigan como las Visual Studio herramientas.

### <a name="give-a-notification-choice"></a>Dar una opción de notificación

Anteriormente vimos cómo crear un cuadro de mensaje personalizado. Si un cuadro de mensaje de la aplicación se va a mostrar con frecuencia al usuario, puede ser prudente agregar una casilla que el usuario puede seleccionar para deshabilitar que ese cuadro de diálogo se muestra en el futuro. Esta opción es especialmente buena para los mensajes más obvios.

Un ejemplo conocido de esto es el cuadro de diálogo Visual Studio buscar. Al buscar o reemplazar texto, Visual Studio muestra un cuadro de mensaje que indica los resultados. Pero también se le ofrece la opción de deshabilitar ese cuadro de mensaje. Puede ser realmente molesto si tiene que pulsar Entrar o hacer clic en Aceptar cada vez que busque.

Otra cosa interesante que Visual Studio es que, incluso si el cuadro de diálogo está deshabilitado, todavía muestra los resultados de esa operación en la barra de estado.

### <a name="provide-tooltips"></a>Proporcione información sobre herramientas.

A veces, la información sobre herramientas puede ahorrar mucho tiempo. Los botones, las casillas y otros controles pueden ser ambiguos y es posible que el usuario no esté seguro de qué hacer. La información sobre herramientas proporciona la mejor forma de ayuda contextual en una sola línea. El usuario puede decidir rápidamente qué hacer sin buscar nada en el archivo de Ayuda ni abrir otra ventana.

A menudo, los usuarios omiten esto en sus aplicaciones. Haga un punto para agregar información sobre herramientas a todos los controles ambiguos, o a todos los controles si es posible. No repita el texto de una etiqueta complementaria o el propio texto de ese control, sino que proporcione información adicional sobre ese control. El texto debe explicar la función del control en unas pocas palabras.

### <a name="do-not-forget-the-little-things"></a>No olvide las cosas pequeñas

Las pequeñas cosas pueden afectar, pero ignorarlas puede afectar a la impresión que se da. Una vez usé una aplicación realizada por una persona importante del sector del software que tenía el valor BorderStyle de su formulario establecido en Sizeable, pero los controles del lado derecho del formulario no estaban delimitados. Por este problema, la aplicación creada por un pesado del sector tenía una sensación no profesional.

Estos tipos de "pequeñas cosas" son el núcleo de la impresión general. La interfaz de usuario y la experiencia de usuario de la aplicación son las que los usuarios juzguen a la aplicación, al menos al principio. Si ven errores obvios en la interfaz de usuario, pueden percibir que la aplicación es menos eficaz y eficaz.

## <a name="conclusion"></a>Conclusión

Solo hemos tocado una pequeña parte de la experiencia del usuario humano. A medida que la experiencia del usuario se vuelve más sencilla, eficaz, divertida y fácil de usar, la tarea de crear esa experiencia de usuario se vuelve mucho más compleja. Pero con cierta previsión y buen planeamiento, puede crear una experiencia de usuario excelente.

La mejor manera de crear la experiencia de usuario perfecta es realizar pruebas de facilidad de uso dirigidas especialmente a la interfaz de usuario, ya sea con un grupo de pruebas especial o por sí mismo. Cuando más tiempo dedica a probar la experiencia del usuario antes de publicar la aplicación, mejor. Le ahorrará muchos problemas más adelante.

 

 