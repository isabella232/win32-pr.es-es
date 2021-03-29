---
title: Principios de la interfaz de usuario
description: En este tema se describe cómo implementar los principios de diseño de la interfaz de usuario y la experiencia del usuario intuitivos en una aplicación Windows.
ms.assetid: 603bc184-3eec-4281-8caa-993834da3131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98383f9379248570ef8b254c647ab8348d703696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078124"
---
# <a name="user-interface-principles"></a>Principios de la interfaz de usuario

En este tema se describe cómo implementar los principios de diseño de la interfaz de usuario y la experiencia del usuario intuitivos en una aplicación Windows.

-   [Introducción](#introduction)
-   [Principios básicos de la interfaz de usuario adecuada](#the-basic-principles-of-proper-ui)
    -   [Espaciado y posición](#spacing-and-positioning)
    -   [Tamaño](#size)
    -   [Agrupación](#grouping)
    -   [Intuitivo](#intuitiveness)
-   [20 sugerencias para mejorar la experiencia del usuario funcional](#20-tips-for-a-better-functional-user-experience)
    -   [Usar estándares](#use-standards)
    -   [Atraer la atención a los botones importantes](#draw-attention-to-important-buttons)
    -   [Simplificar el reconocimiento con iconos](#simplify-recognition-with-icons)
    -   [Simplifique el reconocimiento con encabezados](#simplify-recognition-with-headers)
    -   [Usar cuadros de mensaje personalizados](#use-custom-message-boxes)
    -   [Incluir comandos alternativos](#include-alternate-commands)
    -   [Cómo controlar acciones críticas](#how-to-handle-critical-actions)
    -   [¿Botones o ComboBox?](#radiobuttons-or-comboboxes)
    -   [No interrumpa nunca al usuario.](#never-disrupt-the-user)
    -   [Proporcionar el estado de progreso](#provide-progress-status)
    -   [Simplifique los pasos complejos con los asistentes](#simplify-complex-steps-with-wizards)
    -   [Obtener el tono del texto a la derecha](#get-the-tone-of-your-text-right)
    -   [A veces, un control ListView es mejor](#sometimes-a-listview-is-better)
    -   [Simplificar la navegación con controles de ruta de navegación y barras laterales](#simplify-navigation-with-breadcrumb-controls-and-sidebars)
    -   [Usar gráficos de gran uso](#use-pretty-graphics)
    -   [Proporcionar formatos ajustables siempre que sea posible](#provide-resizable-forms-when-possible)
    -   [Proporcionar más funcionalidad con barras laterales/paneles de tareas](#provide-more-functionality-with-sidebarstask-panes)
    -   [Conceder una opción de notificación](#give-a-notification-choice)
    -   [Proporcione información sobre herramientas.](#provide-tooltips)
    -   [No olvide las pocas cosas](#do-not-forget-the-little-things)
-   [Conclusión](#conclusion)

## <a name="introduction"></a>Introducción

A menudo, los desarrolladores no pueden tener en cuenta la perspectiva del usuario final. Los desarrolladores trabajan de manera difícil para que la aplicación funcione; los clientes solo esperan que funcionen y su percepción del software centrado en este requisito. Esto es especialmente cierto si desarrolla software comercial, o algo que se usará por personas no técnicas. Los desarrolladores deben tener en cuenta las necesidades del usuario final en todo el proceso de diseño de software.

Una aplicación de software debe ser tan fácil de navegar y usar como sea posible. Con la cantidad de software que se va a crear, un 4 de los 10 aplicaciones de software estimados tienen una interfaz de usuario realmente excelente que el usuario final me gusta y se siente al instante mediante.

Se crea una cantidad masiva de software de uso interno para las empresas. Tanto si se desarrolla internamente como si se trata de un consultor, a menudo se invierte en la creación de una interfaz de usuario con un tiempo mínimo, esfuerzo o dinero. El rol ' diseñador ' es poco habitual en el ciclo de desarrollo, especialmente en el mundo de las aplicaciones Windows.

Hay algunas reglas básicas que hay que seguir para tener una interfaz de usuario que tenga un aspecto mucho más agradable y una mejor funcionalidad para la aplicación. No requiere una gran inversión de tiempo o dinero por su parte y agrega un buen retorno de la inversión.

Antes de continuar, vamos a diferenciar entre la interfaz de usuario y la experiencia del usuario, al menos para el ámbito de este artículo. La interfaz de usuario, o la interfaz de usuario, hace referencia a los objetos visuales y controles de la aplicación, mientras que la experiencia del usuario, o UX, engloba tanto la interfaz de usuario como el comportamiento de la aplicación relacionada con la interfaz de usuario, así como la "sensación" que el usuario obtiene de la aplicación. No solo se trata de diseñar una interfaz de usuario de aspecto excelente, sino que también se asegura de que funciona bien.

Aquí se tratarán 20 puntos de diseño de la experiencia del usuario que puede integrar fácilmente en la fase de diseño de la aplicación. El resultado será aplicaciones más enriquecidas con una funcionalidad mejor intuitiva, una "experiencia humana". Como sabemos, la generación de aplicaciones de Windows Vista tendrá que buscarse y comportarse de manera diferente. Este tema le ayudará a prepararse para futuras aplicaciones, al tiempo que proporciona a los usuarios actuales un gusto del futuro.

En las secciones siguientes se describen los conceptos básicos del diseño adecuado de la interfaz de usuario.

## <a name="the-basic-principles-of-proper-ui"></a>Principios básicos de la interfaz de usuario adecuada

Una experiencia de usuario de aspecto profesional depende de estos cuatro factores:

-   Espaciado y posición
-   Tamaño
-   Agrupación
-   Intuitivo

Con versiones de Microsoft Visual Studio anteriores a 8,0, el espaciado y el tamaño eran poco óptimos. Una cuadrícula 4x4 o de 8 x 8 no siempre funciona. Con la inclusión de las líneas de ajuste, el proceso se ha simplificado en gran medida. Alinear una etiqueta con un cuadro de texto, o incluso peor, alinear varias etiquetas con sus cuadros de texto correspondientes era extremadamente difícil en versiones anteriores de Visual Studio. Las guías de alineación han simplificado enormemente este proceso.

En las secciones siguientes se describen cuatro de los aspectos más importantes del diseño de la experiencia de usuario profesional.

### <a name="spacing-and-positioning"></a>Espaciado y posición

Es importante el espaciado entre dos controles. En la captura de pantalla siguiente se muestra un formulario de entrada de **información de usuario** mal diseñado: los dos cuadros de texto superiores están demasiado cercanos, la lista bajo ellos está demasiado lejos y hay una gran cantidad de espacio sin usar en el formulario.

![captura de pantalla de un formulario mal diseñado.](images/humanux-01.png)

En la siguiente captura de pantalla, puede ver un cuadro de diálogo más profesional con el espaciado adecuado y los controles con el tamaño adecuado. Esta es la misma forma que en la captura de pantalla anterior, pero se modificó para usar el espaciado recomendado por las líneas de ajuste. Siempre se recomienda alinear una etiqueta con la línea de base del texto del cuadro de texto u otro control junto a ella, en lugar del borde inferior real del control. Las guías de alineación convierten un color diferente cuando se alcanza esa alineación, normalmente solo unos pocos píxeles por encima del borde inferior.

![captura de pantalla de un formulario más bien diseñado.](images/humanux-02.png)

Aunque no hay ninguna regla exacta para el espaciado, las guías de alineación proporcionan instrucciones muy útiles para el espaciado adecuado. Otras herramientas que le ayudarán a mantener el espaciado adecuado son los controles de diseño del grupo del cuadro de herramientas contenedores. TableLayoutPanel también es muy útil para crear cuadros de diálogo de estilo de formulario de entrada.

### <a name="size"></a>Tamaño

Las mismas consideraciones se aplican al tamaño. Al arrastrar un botón desde el cuadro de herramientas al formulario, tiene el alto y el ancho perfectos. El ancho máximo recomendado (salvo por cualquier motivo gravemente importante) es doblar el ancho original.

Si observa la ventana **Ejecutar** en el menú **Inicio** o el cuadro de diálogo **propiedades** de cualquier objeto del explorador de Windows, los tamaños de los botones son "solo derecha". Si tiene una función muy importante que necesita que el usuario final tenga en cuenta sin errores, hay otros métodos que usar un botón grande o llamativa colores no estándar (más información sobre esto más adelante).

En la imagen siguiente, puede ver tres botones. El primer botón es el tamaño recomendado y es el tamaño que se crea de forma predeterminada al arrastrarlo (o hacer doble clic en él) desde el cuadro de herramientas. A veces, el texto adicional requiere que el botón sea más grande. El segundo botón muestra un tamaño grande que todavía es aceptable. No crearía un desorden para diseñar otros controles. Sin embargo, el tercer botón es un tamaño completamente inaceptable. Puede ver que incluso distorsiona ligeramente los mapas de bits del tema que Windows usa para dibujar controles con temas. También dificultará la alineación de otros controles de forma intuitiva.

![imagen de tres botones, con un tamaño de izquierda a derecha.](images/humanux-03.png)

### <a name="grouping"></a>Agrupación

Normalmente, una aplicación contiene muchos controles. Solo mediante una agrupación intuitiva adecuada puede hacer que todos estos controles sean más fáciles de usar. La agrupación basada en funciones o en categorías se realiza mejor mediante controles de ficha. Por ejemplo, ' Accounts, ' ' Reports, ' ' Employees ' y ' projects ' serían candidatos perfectos para las pestañas de una aplicación empresarial típica. La agrupación del mismo nivel (controles que contribuyen al mismo resultado final) se realiza mejor mediante controles de grupo. No se recomienda el uso de paneles con bordes para este tipo de agrupación. Los controles de grupo le ahorran el peso extra de un control de etiqueta, especialmente si los SubControles se explican por sí solos.

No se recomiendan los controles de grupo dentro de los controles de grupo a menos que no haya más de 2 o tres de ellos dentro de un control de grupo grande.

### <a name="intuitiveness"></a>Intuitivo

Este es el aspecto más importante de una experiencia de usuario excelente. Una experiencia de usuario intuitiva reduce la necesidad de explicaciones. El usuario solo sabe lo que hacen los controles.

Un tema importante en el diseño intuitivo es la codificación de colores. En Windows XP, se presenta un buen ejemplo en el que se presentan nuevos botones de cuadrado automático para funciones como la navegación en aplicaciones de la aplicación, el cierre de **sesión** y la desactivación de los cuadros de diálogo del **equipo** , entre otros.

El color de estos controles se determinó en función de la gravedad del resultado de la inserción de ese botón. La navegación es verde, como una luz de tráfico "Go". Apagar, lo que daría lugar a una pérdida potencial de trabajo, se colorea en rojo como un signo de advertencia. Los botones semicríticos, como cerrar sesión o hibernar, son amarillos. Los botones neutros que no tienen ningún efecto crítico en los procesos de trabajo del usuario, como la ayuda, son un azul blando. Al crear una interfaz de usuario con máscaras, deben tenerse en cuenta estos aspectos de color.

Un buen ejemplo de reconocimiento de contenido por colores es Microsoft Office OneNote. Las pestañas de la aplicación se pueden establecer en diferentes colores, al mismo tiempo que se trata de una parte adecuada del diseño de estilo general de Windows XP.

Otro aspecto importante es el texto de las aplicaciones. Recientemente, se han realizado varios esfuerzos para simplificar el lenguaje usado para las instrucciones escritas en el software de Windows. El uso de texto dentro del software se tratará más adelante, pero tenga en cuenta los siguientes detalles pequeños pero importantes.

MSN Messenger tenía una casilla en el cuadro de diálogo **Opciones** marcada como "compartir capacidades de cámara web". Los desarrolladores y las personas con conocimientos técnicos saben lo que significa, pero un usuario inexperto podría pensar que podría permitir que otro usuario en el otro extremo del chat usara también su cámara web. En una versión reciente, la hemos cambiado a "mi cámara web: permitir a otros usuarios ver que tengo una cámara web". Esto es idóneo para el público de destino que puede que no tenga conocimientos técnicos y que se use para el lenguaje sencillo.

Aunque el lenguaje más sencillo facilita la comprensión, también hay una ventaja adicional. Los estudios científicos demuestran que nuestra mente es más fácil con el lenguaje más sencillo al intentar comprender algo nuevo. A menudo, nuestro cerebro procesa palabras como "ti", "para", "" y otras palabras comunes, de forma rápida y sencilla que se asigna más "ancho de banda" para comprender las palabras que destacan, como "Webcam" u "otras", en el ejemplo anterior.

Los títulos de cuadro de mensaje, los títulos de GroupBox y otros bloques de texto permiten transmitir fácilmente la función de un grupo de controles al usuario final con solo unas pocas palabras.

La intuitivo también nació de la familiaridad. Por ejemplo, la colocación de los botones **Aceptar** y **Cancelar** es tan uniforme y bien colocada en nuestras mentes que, si un cuadro de diálogo contiene estos botones en una secuencia inversa (**Cancelar**, después en **Aceptar**; en lugar de **Aceptar**, **Cancelar**), es posible que solo se pueda presionar **Cancelar** en su lugar. Después de usar un estándar determinado para realizar cosas (por ejemplo, aplicaciones basadas en Windows) durante más de un año, se desarrollan hábitos. Los siguientes estándares del sector (aunque no estén en estado) hacen que el software sea más fácil de usar.

En una de las primeras compilaciones de vista previa de Windows Vista, los botones **minimizar**, **maximizar** y **cerrar** de cualquier ventana se han convertido en diferentes. En versiones anteriores de Windows (especialmente cuando se usa un monitor único), se desarrolla un hábito de mover el cursor en la esquina superior derecha de la pantalla y hacer clic en. Esto siempre provocó el cierre de la ventana. Ahora, en esta compilación concreta de Windows Vista, había aproximadamente 8 píxeles de espacio entre el botón Cerrar y el borde derecho de la ventana. El espacio adicional hizo que parezca frío (y probablemente era necesario para la animación de resplandor frío con el botón deportivo), pero fue irritante porque no permitió a los usuarios cerrar ventanas abiertas tan fácilmente. La recondición de su mente puede ser difícil. Afortunadamente, en la siguiente compilación, se solucionó este problema. Ahora, todavía hay espacio entre el borde de la ventana y el botón Cerrar, pero al hacer clic en ese espacio también se cierra la ventana.

Un factor muy importante de diseño intuitivo es la cantidad de ' mental bandwidth': la cantidad de tiempo que puede tardar en comprenderse algo — lo usa. Cuanto menor sea el uso del ancho de banda, mejor será la experiencia del usuario.

Son pequeñas cosas que contribuyen a la "experiencia" del uso de una aplicación de software. En los ejemplos siguientes se proporcionan sugerencias para mejorar las aplicaciones con sugerencias y trucos del mundo real.

## <a name="20-tips-for-a-better-functional-user-experience"></a>20 sugerencias para mejorar la experiencia del usuario funcional

El objetivo de una mejor experiencia de usuario es tener una interfaz de usuario más sencilla y funcional que también tenga un buen aspecto. Estas sugerencias le ayudarán a dar forma a la interfaz de usuario para que sea más eficaz.

### <a name="use-standards"></a>Usar estándares

Los estándares establecidos de cualquier entorno de software, ya sea en el nivel de sistema operativo, en el nivel de marca o en el nivel de aplicación, son muy importantes. Además de la personalización de marca, los estándares actúan como un esquema de proverbial en la mente del usuario. Cuando el usuario invierte largos períodos de tiempo trabajando con una aplicación de software, aumentará automáticamente la productividad debido al creciente conocimiento.

Antes de analizar los estándares, Analicemos primero qué son exactamente estos estándares. Los estándares incluyen todo el diseño de los controles de una manera determinada en los cuadros de diálogo, como los botones **Aceptar** y **Cancelar** , la forma de la interfaz de usuario, los vértices redondeados de la parte superior de la ventana, como en los cuadros de diálogo de Windows XP, los estilos de los iconos, los estilos de cualquier otro gráfico, el comportamiento interactivo de la aplicación y el tipo de

Si su aplicación se encuentra en un nicho específico, es posible que se le importe mejor el siguiente conjunto de estándares. Por ejemplo, si la aplicación es compatible con, la aplicación o un complemento para, Office OneNote 2003, es aconsejable seguir los estilos de los estándares de interfaz de usuario e interactividad de Office, y OneNote, en particular. Esto incluye el uso de las barras de comandos de estilo Office en lugar de las barras de herramientas estándar y otras cosas, tanto visuales como de comportamiento. Si la aplicación va a formar parte de la categoría Microsoft Visual Studio .NET, tendrá un conjunto independiente de estándares. De hecho, en el caso de estas aplicaciones complementarias o de soporte técnico, las empresas como, por ejemplo, las instrucciones escritas de Microsoft. Tenga en cuenta también que, a veces, los conceptos de diseño y gráficos son propiedades intelectuales protegidas. Compruebe siempre la documentación adecuada para asegurarse de que tiene la licencia para crear dichos diseños.

Un tercer ejemplo de normas sería el entorno de Tablet PC. Estos estándares cruzan los límites entre las instrucciones del sistema operativo y las instrucciones de la aplicación. La [documentación del SDK de Tablet PC](/previous-versions/ms840465(v=msdn.10)) contiene información muy útil en el tema "Planeación de la aplicación". A diferencia de las directrices de Office 2003 o Visual Studio, estas recomendaciones de diseño afectan directamente a la forma en que el usuario interactúa con la aplicación y cómo debe comportarse a su vez. Por ejemplo, si tiene acopladas ventanas en la aplicación, la documentación recomienda asegurarse de que puede detectar cuándo se cambia la orientación de la pantalla y que las ventanas de acoplamiento se reorganizan de forma adecuada en una orientación vertical u horizontal según sea necesario. Incluso si no está diseñando la aplicación para que sea específica de la tableta, debe seguir estas instrucciones.

Con el aumento de los clientes inteligentes, las aplicaciones ahora atraviesan los límites entre el hardware diferente (equipos normales, Tablet PC, dispositivos móviles o ultra móviles, equipos con Media Center, etc.). Cada situación llama a un conjunto de estándares diferente (o adicional) que se va a seguir.

Cuando las aplicaciones comparten los estándares de nivel de sistema operativo o de aplicación, los usuarios se sienten más en casa con el software, lo que facilita su aprendizaje y uso. El resultado es un aumento directo en la productividad. Los usuarios desean ser capaces de ser productivos con el nuevo software lo más rápido posible.

### <a name="draw-attention-to-important-buttons"></a>Atraer la atención a los botones importantes

A veces, es necesario dirigir al usuario a los botones más importantes aunque tenga cuatro u otros cinco botones en torno a él. Si experimenta con el tamaño, el color o la fuente, debe romper los estándares, lo que no se recomienda. En su lugar, puede usar un par de trucos sencillos para lograrlo.

La primera consiste en convertir los otros botones no críticos en LinkLabels, tal como se muestra en la siguiente imagen. De este modo, el usuario sabe que estos vínculos realizarán una tarea, pero su atención irá primero al botón que destaca, sin interrumpir las directrices de diseño estándar.

![imagen de tres botones convertidos en linklabels.](images/humanux-04.png)

La segunda consiste en colocar el botón crítico en primer lugar, en la parte izquierda para los diseños horizontales, tal como se muestra en la siguiente imagen, o en la parte superior de los diseños verticales. Tenga en cuenta que esto puede variar en función de la referencia cultural del usuario de destino, por lo que puede obtener un mejor rendimiento si coloca el botón en cuestión en el extremo derecho si la aplicación es cualquier idioma que se escribe de derecha a izquierda.

![imagen de tres botones en los que el botón crítico está más a la izquierda en un diseño horizontal.](images/humanux-05.png)

La opción recomendada es establecer para recibir el foco de forma predeterminada. Por ejemplo, en un cuadro de diálogo de confirmación de eliminación, la opción **no** se debe resaltar, ya que esto impide que el usuario elimine accidentalmente algo.

### <a name="simplify-recognition-with-icons"></a>Simplificar el reconocimiento con iconos

Iconos, especialmente los iconos y los mapas de bits de la barra de herramientas y los iconos de Windows XP y Office 2003, ayudan a acelerar el cognitiva de la interfaz de usuario y la tarea que el usuario tiene que realizar.

Por ejemplo, cuando vea el icono de exclamación más frecuente en el cuadro de mensaje, conocerá al instante el nivel de riesgo asociado a los controles que aparecen junto a ese icono. Del mismo modo, cuando la aplicación pone una gran cantidad de controles, independientemente de cómo se organicen correctamente, puede ser desalentadora encontrar el conjunto de controles que está buscando.

En Windows XP Service Pack 2, se agrega una pestaña actualizada al applet del panel de control **propiedades del sistema** denominado "actualizaciones automáticas". Existen cuatro opciones: descargar actualizaciones automáticamente, descargar actualizaciones, y dejar que el usuario decida cuándo instalarlas, notificar al usuario si hay actualizaciones disponibles pero no iniciar la descarga y deshabilitar las actualizaciones automáticas por completo.

Un nuevo usuario de PC puede no ser consciente de lo que son estas actualizaciones y es posible que no sepa qué opción sería mejor elegir. Por lo tanto, Microsoft ha colocado un icono de escudo verde con una marca de verificación grande junto al recomendado que indica una opción "segura" y un icono de escudo rojo con una "x" grande junto al que podría ser perjudicial para el usuario. Esto resulta muy útil en situaciones críticas, especialmente cuando el usuario no tiene tiempo para leer demasiado texto.

En el mismo applet de **propiedades del sistema** , cada pestaña tiene varios GroupBoxes con distintos controles para diferentes tareas. Un gráfico relativo se coloca junto a cada grupo que indicaría fácilmente la tarea del grupo de control. Este tipo de código gráfico es similar a la codificación de colores en archivos físicos o en lotes de aparcamiento. Esto también funciona en el mismo principio de tener al menos algunos objetos visuales en un artículo de la revista: mantiene el interés del lector.

También es importante elegir el icono de la derecha. Microsoft proporciona muchos gráficos estándar como parte de Visual Studio 2005. Esta es la mejor opción. Si crea sus propios iconos, se recomienda encarecidamente que siga los estándares de nivel de sistema operativo o de nivel de aplicación para estos gráficos, como se mencionó en la sección [uso de estándares](#use-standards) anteriores.

Las [instrucciones de interacción](/windows/apps/desktop/) de la experiencia del usuario de Windows contienen una guía muy útil para crear [iconos](https://msdn.microsoft.com/library/aa511280.aspx)de estilo de Windows.

### <a name="simplify-recognition-with-headers"></a>Simplifique el reconocimiento con encabezados

Los encabezados son la manera perfecta de explicar el cuadro de diálogo completo en una sola oración (y, opcionalmente, un gráfico). A veces, los encabezados pueden incluso ayudarle a incluir también la navegación y los comandos dentro de ellos. Los encabezados funcionan de manera más eficaz que las etiquetas de Descripción normales porque son lo primero que un usuario ve cuando se abre el cuadro de diálogo.

Los asistentes para Windows Installer son quizás los encabezados más populares: un icono simple en el extremo derecho; una etiqueta de título que describe el cuadro de diálogo (por ejemplo, Seleccionar carpeta de instalación); y un subtítulo que describe el propósito del cuadro de diálogo (por ejemplo, seleccione la carpeta en la que se instalarán los archivos de software).

Supongamos que tenemos una aplicación empresarial típica con una sección de cuentas. Siguiendo el paradigma de diseño predicho en Windows Vista, podemos proporcionar información crítica y comandos relacionados en el encabezado (o pie de página, si el escenario lo llama). Nuestro usuario ha abierto el archivo de la cuenta de "Big Company" y el encabezado tendría un aspecto similar al que se muestra en la siguiente captura de pantalla.

![captura de pantalla de un cuadro de diálogo que contiene un pie de página detallado.](images/humanux-06.png)

En la captura de pantalla siguiente se muestra un ejemplo de un encabezado detallado en un cuadro de diálogo.

![captura de pantalla de un cuadro de diálogo que contiene un encabezado detallado.](images/humanux-07.png)

Del mismo modo, puede evitar tener que agregar paneles de tareas de estilo Windows XP, especialmente si tiene unos pocos comandos, que desaprovecharían una gran cantidad de espacio vertical, moviendo estos comandos al encabezado.

Hay algunas cosas que debe tener en cuenta al diseñar encabezados:

-   Asegúrese de que el color de fondo es diferente del color de fondo del cuadro de diálogo. Con mayor frecuencia que no, se producirá un encabezado blanco sobre un color de superficie de control intrínseco de Windows estándar. Pero si realmente desea asegurarse de que ningún tema especial o colores personalizados disponen el encabezado, dibuje un **LinearGradient** mediante el **color. FromKnownColor** con los colores **ControlLight** y **ControlDark**.
-   Si es posible, mantenga el alto del encabezado en 150 píxeles. Normalmente, se producirá un alto de 100 o 120. Como norma general, asegúrese de que sea inferior a 1/4 de la altura del formulario completo.
-   Si desea agregar la edición en contexto para la información que se muestra en el encabezado anterior, reemplace de forma dinámica el LinkLabel con un cuadro de texto y vuelva a intercambiarlo una vez que se haya realizado la edición.
-   Si tiene una etiqueta de título con una fuente superior a 10 pt de tamaño, use Arial o Franklin Gothic Medium. MS Sans Serif tendrá un aspecto demasiado dentado y poco profesional. Franklin Gothic Medium es la recomendación de la documentación sobre las directrices de diseño de Windows XP. En el caso de las aplicaciones que tienen como destino Windows Vista, use la fuente Segoe UI que sea la fuente predeterminada del sistema.

### <a name="use-custom-message-boxes"></a>Usar cuadros de mensaje personalizados

Las opciones disponibles en el cuadro de mensaje estándar de Windows son muy limitadas. Cuando tenga que formular a su usuario una pregunta que no se pueda responder con un simple sí/no o aceptar o cancelar, se vuelve complicado.

Las aplicaciones de Windows ahora son más fáciles de usar debido al elevado volumen de usuarios no técnicos. A veces, puede ser mucho más sencillo proporcionar botones con textos más descriptivos e incluso algunos controles adicionales (LinkLabels, por ejemplo) para que sea más fácil realizar la tarea a mano.

Microsoft .NET Framework facilita la implementación de cuadros de diálogo personalizados. Con solo asignar un par de propiedades en el formulario de diálogo personalizado o con una sola línea de código, el formulario puede funcionar como un cuadro de mensaje estándar. En un evento de clic de botón, establezca la propiedad **DialogResult** del cuadro de diálogo en **DialogResult. OK** o **DialogResult. Cancel**. Use el método **ShowDialog ( \[ OwnerForm \] )** del formulario primario. Este método de método devuelve el valor **DialogResult** .

Puede usar todos los miembros **DialogResult** . Estas mismas opciones las utiliza el método **MessageBox. show** estándar.

Como alternativa, puede establecer la propiedad **AcceptButton** del cuadro de diálogo en **btnOK** y la propiedad **CancelButton** en **btnCancel**. Esto asignará automáticamente las teclas **entrar** y **ESC** a los eventos Click correspondientes de los botones **btnOK** y **btnCancel** .

Estas son algunas sugerencias para enriquecer los cuadros de diálogo personalizados:

-   En el caso de los temas complicados, proporcione vínculos a la ayuda local o en línea con un LinkLabel que indique "Buscar más" en la etiqueta de texto correspondiente.
-   En lugar de botones **sí** / **no** / **Cancelar** , use textos que indiquen claramente el resultado de hacer clic en el botón, como "guardar archivo y salir", "salir sin guardar" y "no salir". Sin embargo, siempre que sea posible, debe ajustarse a los botones estándar **sí** / **no**, **Aceptar** / **Cancelar** y como estándar. La familiaridad hace que la productividad sea excelente.
-   Mantenga 50 píxeles de espacio de margen en el lado izquierdo (o en el lado derecho según la configuración de la referencia cultural de destino) y agregue un icono que represente el escenario para el cuadro de diálogo. Si se trata de un cuadro de diálogo de información, puede usar el icono "i" que se usa en los cuadros de mensaje estándar. Si se trata de un cuadro de diálogo de seguridad, puede usar un icono de candado o un icono de llave. Visual Studio 2005 se incluye con algunos gráficos excelentes de alta calidad.
-   Asegúrese siempre de proporcionar una navegación de teclado adecuada para estos botones: los usuarios usan los métodos abreviados de teclado para los cuadros de mensaje (por ejemplo, O para aceptar, Y para sí, C para cancelar, etc.) en gran medida. Seguramente le resultaría molesto si el cuadro de diálogo personalizado no los usó.

### <a name="include-alternate-commands"></a>Incluir comandos alternativos

Dos factores importantes determinan la necesidad de métodos de entrada alternativos: frustración y Laziness. La frustración suele producirse en los usuarios del equipo. Cuando se sienta frustrado, desea que la tarea se realice rápidamente. Un clic adicional o una espera adicional de unos segundos realmente infuriates a una persona con mucha carga, ya que sabe cómo es, hemos hecho todo. Laziness a menudo le pide que finalice la tarea con solo el teclado o el mouse (lo que esté usando en ese momento). Pero además de estos dos factores, tener métodos de entrada alternativos facilita que el usuario pueda realizar tareas.

Por ejemplo, si tiene un cuadro de lista con dos botones ("agregar" y "quitar") en cualquier lado, debe agregar un menú contextual para ese cuadro de lista con comandos de menú análogos a esos botones. Esto ofrece al usuario la oportunidad de elegir el método que encuentre el más adecuado. Los usuarios inexpertos, como el estado de las instrucciones de la experiencia del usuario de Windows Vista, usan menús contextuales mucho y esperan que estén en cualquier lugar en el que hagan clic con el botón secundario.

Del mismo modo, usamos controles visuales para la entrada de texto o numérica. Por ejemplo, los controles deslizantes se usan para especificar enteros, y los controles de calendario se utilizan para la entrada de fecha. A veces puede ser más cómodo simplemente escribir. A menudo, puede hacer una diferencia para el usuario si agrega un control numérico Up-Down vinculado a un control deslizante, o bien usa un control DateTimePicker en lugar del control de calendario.

### <a name="how-to-handle-critical-actions"></a>Cómo controlar acciones críticas

A la hora de realizar una función crítica e irrecuperable, generalmente es recomendable crear un elemento emergente del cuadro de mensaje para confirmar la acción. Vamos a realizar una muesca. En la siguiente captura de pantalla puede ver un cuadro de mensaje personalizado similar, pero con una ventaja adicional: un temporizador mostrado visualmente con la ayuda de una barra de progreso.

![captura de pantalla de un cuadro de diálogo de acción crítica.](images/humanux-08.png)

Hay algunas variaciones específicas del escenario que puede usar. Si la acción que se va a llevar a cabo es muy importante (desde la sobrecarga de una planta de energía nuclear hasta la eliminación de archivos de forma permanente), la acción predeterminada después de que se agote el temporizador debe cancelarse. El cuadro de diálogo no debería desaparecer, sino que la etiqueta de texto cambia para mostrar que se ha cancelado la acción. El usuario puede elegir confirmar el comando o la cancelación.

Asegúrese siempre de que los botones que realizan operaciones críticas estén marcados claramente; Utilice siempre texto sin cifrar que describa la acción con precisión. Si la acción es la eliminación de archivos, no escriba "quitar archivos del repositorio"; Escriba "eliminar archivos del repositorio". Al trabajar con listas de archivos, si un comando de menú eliminar elimina los archivos seleccionados del propio disco duro (en lugar de quitarse de la lista de archivos), debe sobrecargar correctamente la naturaleza crítica de este y hacer que la acción elimine los archivos de forma permanente.

Alguien dijo, "usted es tan bueno como su peor trabajo". Lo mismo se aplica a las aplicaciones de software. Una única experiencia incorrecta con la aplicación puede hacer una gran impresión negativa en el usuario. Para asegurarse de que esto no suceda, lo único que puede hacer es asegurarse de que, si la aplicación se bloquea, deja de funcionar correctamente. Si puede Agregar la recuperación de datos, o permitir que el usuario intente guardar una copia de los datos, puede ser un Big Plus. Se debe notificar correctamente al usuario si la aplicación se bloquea. Un cuadro de diálogo de error JIT-Debugger o crítico no es una buena tarea. Aunque hablaremos acerca de cómo tratar los bloqueos supera el ámbito de este artículo, se recomienda un cuadro de diálogo simple que disculpe al usuario y le informa de la situación (y, posiblemente, con un vínculo a más información sobre cómo recuperarse de este bloqueo) resultaría muy útil para el usuario.

Si desea realizar un paso más allá, puede hacer lo mismo que una de mis aplicaciones de diseño gráfico favoritas. Si se bloquea, mostrará un cuadro de diálogo de recuperación que le permitirá guardar una copia independiente del archivo en el que se está trabajando y, a continuación, le proporcionará un cuadro de diálogo de comentarios en el que puede escribir información sobre el bloqueo (información personal opcional, por supuesto) y enviarlo a los creadores.

### <a name="radiobuttons-or-comboboxes"></a>¿Botones o ComboBox?

A primera vista, el método para crear una selección de uno a varios no parece tan difícil o importante. A veces puede ser, especialmente si el escenario es una aplicación que se usa para el trabajo que depende del tiempo.

Echemos un vistazo a un ejemplo de la vida real. Microsoft publicó recientemente una versión preliminar de una aplicación de gráficos, Expression Graphics Designer (antes con el "acrílico"). Tenía unos 20 objetos gráficos a los que tuve que asignar una determinada propiedad por separado en esta aplicación. Era un proceso de Dreary. Para ello, tuve que seleccionar el objeto, hacer clic en el botón para abrir la ventana Configuración y establecer las opciones. En una de estas opciones, se tenían que elegir dos opciones de un cuadro combinado, como se puede ver en la siguiente captura de pantalla.

![captura de pantalla del cuadro de diálogo de textura de Halo para el diseñador de gráficos de expresión.](images/humanux-09.png)

Cuando tenga que desplegar la lista de cuadro combinado y seleccionar el segundo elemento (de solo 2 elementos), puede resultar irritante. Lo que normalmente no sabemos es el tiempo que tarda la lista desplegable en aparecer. Puede desperdiciar mucho tiempo y puede resultar frustrante. Esto podría resolverse fácilmente colocando un objeto GroupBox con dos RadioButtons, especialmente cuando hay mucho espacio disponible. He encontrado problemas similares en aplicaciones como CorelDRAW, Microsoft Access y otros.

Además de desperdiciar tiempo debido a la animación desplegable, también desperdicia nuestro "ancho de banda mental". Con dos botones de radioestado "siempre visible", nuestra mente subliminally saber la posición del cursor en hacer clic. Con el cuadro combinado, solo se procesará después de que se haya dibujado la lista. Aunque puede parecer demasiado importante, realmente es muy importante.

A veces es mejor utilizar RadioButtons, especialmente si tiene cuatro opciones o menos.

### <a name="never-disrupt-the-user"></a>No interrumpa nunca al usuario.

En pocas palabras, se trata de la cosa más destructiva que un desarrollador puede hacer con los usuarios. Cuando la aplicación, innecesariamente o de otro modo, interrumpe al usuario mientras está trabajando en otra aplicación con un cuadro de mensaje o un flash de la barra de tareas, gana puntos negativos del usuario.

Los destellos de la barra de tareas pueden ser útiles, por supuesto, pero solo se debe llamar cuando el proceso de la aplicación requiere la intervención del usuario para continuar, o si tiene algo crítico de transmitir al usuario. Si el usuario ha mantenido la barra de tareas en modo de ocultación automática, un botón de la barra de tareas parpadeante puede impedir que el usuario tenga acceso a la barra de estado u otros controles de límite inferior, ya que la barra de tareas estará en la parte superior y no volverá a ocultarse hasta que el usuario haga clic en el botón parpadeando.

![captura de pantalla de una ventana del sistema.](images/humanux-10.png)

Las ventanas "del sistema" (vea la figura 10), que son famosas por clientes de mensajería instantánea como MSN Messenger, son una excelente solución para informar al usuario de algo sin molestar ni interrumpir su flujo de trabajo. Hay un artículo excelente ( https://docs.microsoft.com/archive/msdn-magazine/2005/september/sprinkle-some-pizzazz-on-your-plain-vanilla-windows-forms-apps) por Bill Wagner en la creación de ventanas del sistema. Es una buena Directiva (y moda) no molestar a las notificaciones del sistema de otras aplicaciones. La obstrucción de estas ventanas puede ser molesta y desaproducción. Una solución es usar la exclusión mutua ToastSemaphore (/library/WinMessenger/winmessenger/overview/toast.asp) proporcionada por el sistema operativo para evitar colisiones del sistema.

En ocasiones, es posible que tenga que mostrar varios elementos por la notificación del sistema. En realidad, no sería aconsejable sacar 3 o más notificaciones del sistema. En su lugar, al recorrer cada una de ellas se extrae o se atenúa una notificación después de la otra. Microsoft Outlook implementa una solución similar cuando se notifica al usuario de los mensajes de correo electrónico entrantes.

### <a name="provide-progress-status"></a>Proporcionar el estado de progreso

A menudo, hay tareas que requieren que el usuario espere. Por supuesto, se trata de una de las cosas que el usuario simplemente Hates. Pero peor es cuando esperan sin saber lo que está ocurriendo. En ocasiones, es posible que la aplicación tenga que conectarse a un servicio web o a un equipo remoto, o puede que esté procesando grandes fragmentos de datos, sea cual sea el motivo, el usuario debe tener en cuenta, o al menos consciente de ello, lo que ocurre en el capó. Hay distintos métodos para hacerlo, en función de la situación.

Si se está conectando a un objeto lejano, como un servicio web o algo colocado en un servidor de red o de Internet, sería aconsejable mostrar un cuadro de diálogo de progreso simple (vea la imagen siguiente) o una barra de progreso hospedada en la barra de estado. Una etiqueta adjunta debe describir el estado actual del proceso. Por ejemplo, si se va a conectar a un servicio web para procesar algunos datos, simplemente indique "conexión al servicio Web... "o" espere, procesando... "Si este proceso es sincrónico, es aconsejable deshabilitar todos los controles a los que el usuario puede tener acceso hasta que se haya completado el proceso, o simplemente mostrar el progreso como un cuadro de diálogo modal.

![captura de pantalla de un cuadro de diálogo de barra de progreso.](images/humanux-11.png)

Es muy recomendable que establezca el estilo de barra de progreso en el modo de marquesina si usa una barra de progreso y la hora de procesamiento es desconocida, o si no tiene un valor máximo.

Otro método que se está convirtiendo es una ventana fija "del sistema" que muestra el progreso. El descargador y el actualizador de Microsoft AntiSpyware o el análisis del correo electrónico de Norton AntiVirus son buenos ejemplos de esto. Por supuesto, esto solo se debe usar para los procesos asincrónicos. De lo contrario, el usuario puede sentirse desconcertado. Estas ventanas se usan mejor para el procesamiento en segundo plano, como la descarga de una actualización o la realización de una tarea programada, y nunca deben establecerse en "siempre visible".

### <a name="simplify-complex-steps-with-wizards"></a>Simplifique los pasos complejos con los asistentes

Es seguro suponer que, si se enfrenta a una gran cantidad de controles en un único formulario, se confundirá a un usuario típico a ningún extremo. A veces, ninguna cantidad de agrupación, tamaño o espaciado puede ayudarle cuando tiene muchos controles importantes.

Un asistente es lo mejor para estos escenarios. Puede dividir los controles por tareas o categorías según corresponda y colocarlas en pasos independientes. Esto puede ayudar a que el usuario permanezca centrado y no se daunted por la tarea. Puede proporcionar ayuda específica de pasos o tareas con un botón ayuda. Puede encontrar instrucciones para la creación de asistentes en MSDN Library.

Los asistentes también son una buena manera de ayudar a configurar la configuración inicial de la aplicación. Muchas aplicaciones usan este asistente para configurar una configuración personalizada justo después de completarse la instalación o al usarse por primera vez. Este asistente inicial también debe hacerse opcional, si es posible, si el usuario cancela en cualquier momento, la configuración no especificada va a valores predeterminados. Si puede hacer que el asistente sea un gráfico de bits (consulte la sección [uso de gráficos](#use-pretty-graphics) de gran volumen), hace que la tarea de configuración sea mucho más sencilla.

### <a name="get-the-tone-of-your-text-right"></a>Obtener el tono del texto a la derecha

En las [instrucciones de interacción](/windows/apps/desktop/)de la experiencia del usuario de Windows, se ha hecho un punto muy importante sobre el "tono de texto". Esta es la impresión y la sensación de texto en la aplicación. Puede ser cualquier cosa, desde una simple información sobre herramientas, hasta un control de etiqueta de instrucción.

Anteriormente se explicó el cambio de texto en la opción de cámara web de MSN Messenger. Esto se denomina tono de texto adecuado. Cuando se trabaja con usuarios no técnicos o inexpertos, el mensaje se toma de un aspecto diferente.

Si escribe "ruta de acceso de destino" encima de un cuadro de texto en una aplicación autoextraíble, un usuario técnico podrá saber fácilmente que escribe algo como "C: \\ temp \\ myPath". Un usuario inexperto (Imagine "Mom") se puede integrar fácilmente y necesitaría consultar el manual, llamar al soporte técnico o, lo que es peor, renunciar. Una buena alternativa es especificar lo que desea que haga el usuario: "seleccione la carpeta donde desea colocar estos archivos". Puede incluso cambiar el nombre de la sección "examinar... "que se encuentra junto a ese cuadro de texto a" Seleccionar carpeta... "

Proporcionar una descripción clara de lo que desea que haga el usuario también reduce la necesidad de archivos de ayuda, o al menos reduce los detalles que necesita incluir en los archivos de ayuda.

Una buena sugerencia de las directrices de interacción de la [experiencia del usuario de Windows](/windows/apps/desktop/) se aplica a cualquier software. Indica que el escritor debe mantener el texto Conversation. Las instrucciones definen esto como, "Evite las palabras que no diría a alguien en persona".

Algunas sugerencias para escribir texto:

-   Evite hablar con el usuario de la tercera persona. Supalabras "usted" en lugar del "usuario".
-   Siempre que sea posible, use con prudencia "mi nombre:" o "mi dirección de correo electrónico:" en lugar de "nombre:" o "correo electrónico:"
-   Al ofrecer varias opciones, escriba el texto desde la perspectiva del usuario. Por ejemplo, si tiene dos RadioButtons en una etiqueta como "seleccionar permiso para \[ el nombre de usuario \] en esta red" por encima de dos RadioButtons, como "permitir" y "denegar", reemplace el texto de RadioButton por "deseo permitir el \[ nombre de usuario \] " y "deseo no permitir el \[ nombre de usuario" \] .
-   Subraye el texto solo si se utiliza para los vínculos. Confunde al usuario si el texto subrayado no es un vínculo.
-   Preste atención a la información importante con una etiqueta en negrita, pero úsela con cuidado. Demasiado texto en negrita es confuso y reduce el impacto global del formulario.
-   Al escribir el texto de una casilla, asegúrese de que es fácil saber lo que ocurrirá cuando se seleccione y cuando no se haya seleccionado o desactivado. La opción recomendada es escribir el texto directamente como resultado de la selección de la casilla. Por ejemplo, escriba "enviarme información útil de sus asociados" en lugar de "no enviarme información útil a sus asociados". Aunque puedo imaginar muchos arguing de Marketing sobre este ejemplo concreto, estoy seguro de que sabe lo que quiero decir.
-   Si tiene un control similar a un botón (normalmente un RadioButton con la apariencia de un botón de comando) que controla habilitada o deshabilitada, asegúrese de etiquetarla correctamente. Si el proceso está habilitado, escriba "habilitado" en lugar de "habilitar" o "Deshabilitar". Si escribe habilitada, se muestra el estado actual. Si se hace clic en el botón (habilitado) y el botón indica "habilitar", puede ser confuso e problemático. "Habilitar" podría pedirle al usuario que haga clic en el proceso no está activo.

### <a name="sometimes-a-listview-is-better"></a>A veces, un control ListView es mejor

A menudo nos centramos en DataGrid o ListBox o incluso en el cuadro combinado para las tareas de selección, pero con Windows XP y versiones posteriores de Windows, el uso de un control ListView puede proporcionarle opciones más grandes.

Puntos finos del control ListView:

-   Acelera el reconocimiento de elementos con iconos y mapas de bits.
-   Muestra información adicional con detalles o vistas en mosaico.
-   Con Visual Studio 2005, puede incluso tener grupos para la categorización adicional. Los grupos abarcan todas las vistas y son flexibles. Los grupos también se pueden usar para aplanar una vista de jerarquía (como una vista de árbol) donde hay más nodos secundarios que nodos primarios. Un buen ejemplo de esto es el cuadro de diálogo conexiones de red en Windows XP, cuando se ve con "Mostrar en grupos" y la vista establecida en detalles.
-   Para personalizar un control ListView, pinte manualmente estableciendo la propiedad **OwnerDraw** y usando los eventos **DrawItem** y **DrawSubItem** .
-   Admite la edición en contexto rápida de los elementos de ListView.
-   Admite fácilmente la reordenación manual.
-   Permite a los usuarios seleccionar la vista (iconos grandes, iconos pequeños, lista, etc.) con los que más se sienten más cómodos.

### <a name="simplify-navigation-with-breadcrumb-controls-and-sidebars"></a>Simplificar la navegación con controles de ruta de navegación y barras laterales

La "subnavegación" es la clave de la interfaz de usuario compleja. A veces no se puede escapar con una interfaz de usuario complicada. Lo mejor es hacerlo en esta situación es hacer que la experiencia sea lo más sencilla posible para el usuario. Una barra lateral que se compone de etiquetas de vínculo, o una vista de árbol para la navegación basada en jerarquía, sugiere una navegación de nivel relacionado para la tarea del cuadro de diálogo actual. De este modo, resulta muy fácil que el usuario salte entre los pasos del proceso y sepa dónde está.

Si va a una navegación basada en jerarquía con controles TreeView simples u otra navegación compleja similar, una buena utilidad para el usuario sería un control de ruta de navegación. Aunque Visual Studio no incluye aún un control integrado para esto, consulte [crear un control de ruta de navegación](/archive/msdn-magazine/2005/july/advanced-basics-creating-a-breadcrumb-control) para obtener información sobre la creación de uno mismo. Un control de ruta de navegación facilita la búsqueda de la ubicación actual en relación con la jerarquía.

La navegación por la ruta de navegación se puede combinar fácilmente en el encabezado si el formulario tiene uno. Vea la sección anterior sobre [encabezados](#simplify-recognition-with-headers).

### <a name="use-pretty-graphics"></a>Usar gráficos de gran uso

Todo el mundo se hace con las aplicaciones con gráficos esporádicos, la mayoría, al menos. Aunque una interfaz de usuario con gráficos no es una opción lógica para todas las aplicaciones, ayuda a realizar una buena impresión y puede ser un placer trabajar en. Por supuesto, los gráficos no deberían impedir la productividad, pero si se usan correctamente, pueden aumentar.

No es necesario que haya muchos gráficos y que no requieran mucho trabajo. Una pantalla de presentación diseñada profesionalmente o un encabezado (como el que hablamos anteriormente) realiza el truco. Si el presupuesto lo permite, puede utilizar gráficos bien diseñados para barras de herramientas, asistentes, etc. Hacen que la aplicación tenga un aspecto bastante similar y más profesional. Es un efecto sutil, pero una apariencia profesional transmite confianza y estabilidad. Si es una empresa relativamente pequeña que crea aplicaciones de venta directa, se trata de un aspecto clave que se debe tener en cuenta.

Haga siempre un punto para usar gráficos de diseño profesional. Los gráficos libres de regalías están disponibles fácilmente y son asequibles. También puede contratar a un diseñador. Pero si los gráficos no son los Forte, no los pruebe. Si no puede adquirir o usar gráficos de diseño profesional, es mejor no usarlos en absoluto.

En el caso de los gráficos pequeños, siempre puede ir a los iconos y los mapas de bits que se incluyen con Visual Studio 2005. (No se recomiendan los gráficos que se incluyen con versiones anteriores).

### <a name="provide-resizable-forms-when-possible"></a>Proporcionar formatos ajustables siempre que sea posible

Las ventanas de tamaño ajustable son similares a las ventanas independientes de la resolución. Las ventanas independientes de la resolución tienen el mismo aspecto independientemente de si se usan pantallas de 96DPI o 300DPI. Independientemente de si la interfaz de usuario de la aplicación es independiente de la resolución, se cobrará mejor si se cambia de tamaño. Por supuesto, esto no se aplicaría a muchos escenarios, pero es una buena regla de uso general.

Si su ventana trata las listas de cualquier tipo de ordenación (especialmente ListView), esto es incluso más importante. El cambio de tamaño permite al usuario examinar más datos al mismo tiempo.

Por ejemplo, tenemos una aplicación en la que el usuario tiene que seleccionar una imagen de una colección grande. El cuadro de diálogo Abrir permite seleccionar una vista en miniatura, pero el tamaño del cuadro de diálogo es fijo y la lista en miniaturas solo muestra cuatro miniaturas a la vez. Si la colección tiene cien imágenes, el desplazamiento y la apariencia (una tarea repetitiva) pueden ser bastante una tarea arduas y reducir la eficacia. Si se puede cambiar el tamaño del cuadro de diálogo, el usuario puede hacer que sea tan grande como sea más cómodo, o al menos tan grande como lo permita la pantalla, y podrá finalizar la tarea rápidamente. Si la lista tiene un desplazamiento horizontal, como un control ListView o DataGrid detallado, es aún más una tarea ardua. Las ventanas de tamaño variable son muy útiles en esta situación.

### <a name="provide-more-functionality-with-sidebarstask-panes"></a>Proporcionar más funcionalidad con barras laterales/paneles de tareas

Al igual que los encabezados que hemos hablado anteriormente, las barras laterales y los paneles de tareas son una forma maravillosa de proporcionar funciones adicionales y comandos de utilidad. Por ejemplo, los paneles de tareas de Office Word 2003 son muy cómodos, accesibles y no intrusivos. También funcionan de forma asincrónica al conectarse a recursos en línea, lo que proporciona al usuario la opción de varias tareas.

Crear un panel de tareas o barra lateral es tan sencillo como crear un panel de acoplamiento, con la opción de colocar un gráfico impecable en la parte superior para que actúe como una barra de título. Incluso puede usar un control de etiqueta coloreado. Las oportunidades para los paneles de tareas son muchas.

Si tiene funcionalidad adicional y desea proporcionarla de forma no intrusiva a su usuario, no hay ningún lugar como el panel de tareas. También puede hacer que los paneles de tareas "Ocultar automáticamente" o se contraigan como las ventanas de herramientas de Visual Studio.

### <a name="give-a-notification-choice"></a>Conceder una opción de notificación

Anteriormente vimos cómo crear un cuadro de mensaje personalizado. Si se va a mostrar un cuadro de mensaje en la aplicación a menudo para el usuario, puede ser prudente agregar una casilla que el usuario puede seleccionar para deshabilitar el cuadro de diálogo para que no se muestre en el futuro. Esta opción es especialmente adecuada para los mensajes más obvios.

Un ejemplo conocido de esto es el cuadro de diálogo de búsqueda de Visual Studio. Al buscar o reemplazar texto, Visual Studio muestra un cuadro de mensaje que indica los resultados. Pero también tiene la opción de deshabilitar ese cuadro de mensaje. Puede ser realmente molesto si tiene que presionar entrar o hacer clic en aceptar cada vez que busque.

Otra cosa que Visual Studio hace es que, incluso si el cuadro de diálogo está deshabilitado, sigue mostrando los resultados de esa operación en la barra de estado.

### <a name="provide-tooltips"></a>Proporcione información sobre herramientas.

A veces, la información sobre herramientas puede ahorrarle mucho tiempo. Los botones, las casillas y otros controles pueden ser ambiguos y es posible que el usuario no esté seguro de qué hacer. La información sobre herramientas proporciona la mejor forma de ayuda contextual en una sola línea. El usuario puede decidir rápidamente qué hacer sin buscar nada en el archivo de ayuda ni abrir otra ventana.

A menudo, las personas omiten esto en sus aplicaciones. Cree un punto para agregar información sobre herramientas a todos los controles ambiguos, o bien a todos los controles si es posible. No repita el texto de una etiqueta adjunta o el texto de ese control, sino que proporcione información adicional sobre ese control. El texto debe explicar la función del control en unas pocas palabras.

### <a name="do-not-forget-the-little-things"></a>No olvide las pocas cosas

Lo más importante es que le moleste, pero omitirlas puede afectar a la impresión que realice. Una vez que ha usado una aplicación realizada por una persona importante en la industria del software que tenía el valor de BorderStyle de su formulario establecido en gran importancia, pero los controles del lado derecho del formulario no estaban delimitados. Por esta razón, la aplicación creada por un pesado del sector tenía una sensación no profesional.

Estos tipos de "pequeñas cosas" son el núcleo de la impresión global. La interfaz de usuario y la experiencia del usuario de la aplicación son los usuarios que juzgarán la aplicación, al menos al principio. Si ve errores obvios en la interfaz de usuario, es posible que la aplicación perciba menos eficacia y eficacia.

## <a name="conclusion"></a>Conclusión

Solo hemos tocado una pequeña parte de la experiencia del usuario humano. A medida que la experiencia del usuario se vuelve más sencilla, eficaz, divertida y más fácil de utilizar, la tarea de crear esa experiencia de usuario se convierte en mucho más compleja. Pero con cierta previsión y buen planeamiento, puede crear una excelente experiencia de usuario.

La mejor manera de crear la experiencia de usuario perfecta es realizar pruebas de facilidad de uso orientadas especialmente en la interfaz de usuario, ya sea con un grupo de prueba especial o por sí mismo. Cuanto más tiempo dedique a probar la experiencia del usuario antes de lanzar la aplicación, mejor. Esto le ahorrará muchos problemas más adelante.

 

 