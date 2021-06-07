---
title: Cuadros de diálogo (conceptos básicos de diseño)
description: Un cuadro de diálogo es una ventana secundaria que permite a los usuarios realizar un comando, hacer una pregunta a los usuarios o proporcionar a los usuarios información o comentarios de progreso.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b0e0deb28a706436e4d33ece35a40c26bd7499e0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444856"
---
# <a name="dialog-boxes-design-basics"></a>Cuadros de diálogo (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Un cuadro de diálogo es una ventana secundaria que permite a los usuarios realizar un comando, hacer una pregunta a los usuarios o proporcionar a los usuarios información o comentarios de progreso.

![captura de pantalla que identifica los elementos del cuadro de diálogo ](images/win-dialog-box-image1.png)

Un cuadro de diálogo típico.

Los cuadros de diálogo constan de una barra de título (para identificar el comando, la característica o el programa de donde provenía un cuadro de diálogo), una instrucción principal opcional (para explicar el objetivo del usuario con el cuadro de diálogo), varios controles en el área de contenido (para presentar opciones) y botones de confirmación (para indicar cómo el usuario quiere confirmar en la tarea).

Los cuadros de diálogo tienen dos tipos fundamentales:

-   **Los cuadros de diálogo modales** requieren que los usuarios se completen y cierren antes de continuar con la ventana de propietario. Estos cuadros de diálogo se usan mejor para tareas críticas o poco frecuentes y únicas que requieren finalización antes de continuar.
-   **Los cuadros de diálogo no modelo** permiten a los usuarios cambiar entre el cuadro de diálogo y la ventana de propietario según sea necesario. Estos cuadros de diálogo se usan mejor para tareas frecuentes, repetitivas y en marcha.

**Un cuadro de diálogo de tarea es un cuadro de diálogo implementado mediante la interfaz de programación de aplicaciones (API) del cuadro de diálogo de tareas.** Constan de las siguientes partes, que se pueden ensamblar en una variedad de combinaciones:

-   Barra **de título para** identificar la aplicación o la característica del sistema de la que provenía el cuadro de diálogo.
-   Instrucción **principal**, con un icono opcional, para identificar el objetivo del usuario con el cuadro de diálogo.
-   Área **de contenido para** información y controles descriptivos.
-   Un **área de comandos** para los botones de confirmación, incluido un botón Cancelar, y opciones opcionales Más y No mostrar esto <item> controles de nuevo.
-   Un **área de nota al** pie para obtener explicaciones y ayuda adicionales opcionales, destinada normalmente a usuarios con menos experiencia.

![captura de pantalla de un cuadro de diálogo de tarea típico ](images/win-dialog-box-image2.png)

Cuadro de diálogo de tarea típico.

**Los diálogos de tareas se recomiendan siempre que sea necesario, ya que son fáciles de crear y logran una apariencia coherente.** Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Microsoft Windows.

Un panel de tareas es como un cuadro de diálogo, salvo que se presenta dentro de un panel de ventana en lugar de una ventana independiente. Como resultado, los paneles de tareas tienen una sensación más directa y contextual que los cuadros de diálogo. Aunque técnicamente no son iguales, los paneles de tareas son tan similares a los cuadros de diálogo que sus directrices se **presentan en este artículo**.

![captura de pantalla de un panel de tareas típico ](images/win-dialog-box-image3.png)

Panel de tareas típico.

[Las ventanas de](win-property-win.md) propiedades son un tipo especializado de cuadro de diálogo que se usa para ver y cambiar las propiedades de un objeto, una colección de objetos o un programa. Además, las ventanas de propiedades normalmente admiten varias tareas, mientras que los cuadros de diálogo normalmente admiten una sola tarea o paso en una tarea. Dado que su uso es especializado, **las ventanas de propiedades se tratan en un conjunto diferente de instrucciones**.

Los cuadros de diálogo pueden [tener pestañas](ctrl-tabs.md)y, si es así, se denominan cuadros de diálogo con pestañas. Las ventanas de propiedades están determinadas por su presentación de propiedades, no por el uso de pestañas.

**Nota:** Las instrucciones relacionadas con el [diseño,](vis-layout.md) [la](win-window-mgt.md)administración de ventanas, los cuadros [](mess-warn.md) de diálogo [comunes,](win-property-win.md)las ventanas de propiedades, los [asistentes,](win-wizards.md)las confirmaciones, los mensajes de [error](mess-error.md)y los mensajes de advertencia se presentan en [artículos](mess-confirm.md)independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirte, intenta responder a estas preguntas:

-   **¿El propósito es proporcionar a los usuarios información, hacer una pregunta a los usuarios o permitir que los usuarios seleccionen opciones para realizar un comando o una tarea?** Si no es así, use otra interfaz de usuario (UI).
-   **¿El propósito es ver y cambiar las propiedades de un objeto, una colección de objetos o un programa?** Si es así, use una ventana [de propiedades o una](win-property-win.md) barra de [herramientas](cmd-toolbars.md) en su lugar.
-   **¿El propósito es presentar una colección de comandos o herramientas?** Si es así, use una barra de herramientas o una [ventana de paleta](glossary.md).
-   **¿El propósito es comprobar que el usuario desea continuar con una acción?** ¿Hay una razón clara para no continuar y una posibilidad razonable de que a veces los usuarios no lo haga? Si es así, use una [confirmación](mess-confirm.md).
-   **¿El propósito es proporcionar un mensaje de error o advertencia?** Si es así, use un [mensaje de error o](mess-error.md) un mensaje de [advertencia](mess-warn.md).
-   Es el propósito de:
    -   Abrir archivos
    -   Guardar archivos
    -   Abrir carpetas
    -   Buscar o reemplazar texto
    -   Imprimir un documento
    -   Selección de atributos de una página impresa
    -   Selección de una fuente
    -   Elegir un color
    -   Buscar un archivo, una carpeta, un equipo o una impresora
    -   Busque usuarios, equipos o grupos en Microsoft Active Directory
    -   ¿Solicitar un nombre de usuario y una contraseña?

Si es así, use en su lugar el [cuadro de diálogo común](win-common-dlg.md) adecuado. Muchos de estos diálogos comunes son extensibles.

-   **¿El propósito es realizar una tarea de varios pasos que requiere más de una ventana?** Si es así, use un flujo [de tareas o](glossary.md) un asistente en [su](win-wizards.md) lugar.
-   **¿El propósito es informar a los usuarios de un evento del sistema o programa que no está relacionado con la actividad del usuario actual, que no requiere una acción inmediata del usuario y que los usuarios pueden omitir libremente?** Si es así, use una [notificación en](mess-notif.md) su lugar.
-   **¿El propósito es mostrar el estado del programa?** Si es así, use una [barra de estado](ctrl-status-bars.md) en su lugar.
-   **¿Sería preferible usar la interfaz de usuario local?** Los cuadros de diálogo pueden interrumpir el flujo del usuario exigiendo atención. A veces, esa interrupción en el flujo se justifica, por ejemplo, cuando el usuario debe realizar una acción que está fuera del contexto actual. En otros casos, un enfoque mejor consiste en presentar la interfaz de usuario en contexto, ya sea directamente con la interfaz de usuario local (como un panel de tareas) o a petición mediante la divulgación [progresiva](ctrl-progressive-disclosure-controls.md).
-   **¿El propósito es mostrar un problema de entrada de usuario no crítico o una condición especial?** Si es así, use un [globo en](ctrl-balloons.md) su lugar.
-   **Para los flujos de tareas, ¿sería preferible usar otra página?** Por lo general, quiere que una tarea fluya de página a página dentro de una sola ventana. Use cuadros de diálogo para confirmar los comandos locales, para obtener la entrada de los comandos locales y para realizar tareas secundarias independientes que mejor se realicen de forma independiente y fuera del flujo de tareas principal.
-   **Para seleccionar opciones, ¿es probable que los usuarios cambien las opciones?** Si no es así, considere alternativas, como:
    -   Usar las opciones predeterminadas sin preguntar, pero permitir que los usuarios realicen cambios más adelante.
    -   Proporcionar una versión con opciones (por ejemplo, **Imprimir...** en un menú) así como una versión sin opciones (por ejemplo, **Imprimir** en la barra de herramientas). Por lo general, los comandos de la barra de herramientas deben ser inmediatos y evitar mostrar cuadros de diálogo.
-   **Para seleccionar opciones, ¿hay una manera más sencilla y directa de presentar las opciones?** Si es así, considere alternativas, como:
    -   Usar un [botón de división](ctrl-command-buttons.md) para seleccionar variaciones de un comando.
    -   Usar un submenú para comandos, casillas, botones de radio y listas simples.

![Captura de pantalla que muestra un menú y un submenú.](images/win-dialog-box-image4.png)

![captura de pantalla de un menú y submenú ](images/win-dialog-box-image5.png)

En estos ejemplos, se usan submenús en lugar de cuadros de diálogo para selecciones simples.

## <a name="design-concepts"></a>Conceptos de diseño

Cuando se usan correctamente, los cuadros de diálogo son una excelente manera de proporcionar potencia y flexibilidad al programa. Cuando se usa incorrectamente, los cuadros de diálogo son una manera fácil de enojosar a los usuarios, interrumpir su flujo y hacer que el programa se sienta indirecto y tedioso de usar. **Los cuadros de diálogo modales exigen la atención de los usuarios.** Los cuadros de diálogo suelen ser más fáciles de implementar que las UI alternativas, por lo que tienden a usarse en exceso.

**Un cuadro de diálogo es más eficaz cuando sus características de diseño coinciden con su uso.** El diseño de un cuadro de diálogo viene determinado en gran medida por su propósito (ofrecer opciones, realizar preguntas, proporcionar información o comentarios), el tipo (modal o modeless) y la interacción del usuario (necesaria, respuesta opcional o confirmación), mientras que su uso se determina en gran medida por su contexto (iniciado por el usuario o programa), la probabilidad de acción del usuario y la frecuencia de presentación.

Para diseñar cuadros de diálogo efectivos, use los siguientes elementos de forma eficaz:

-   Texto del cuadro de diálogo
-   Instrucciones principales
-   No mostrar esto <item> opción again

**Si solo hace una cosa...**

Asegúrese de que el diseño del cuadro de diálogo (determinado por su propósito, tipo e interacción del usuario) coincide con su uso (determinado por su contexto, probabilidad de acción del usuario y frecuencia de presentación).

## <a name="usage-patterns"></a>Patrones de uso

Los cuadros de diálogo tienen varios patrones de uso:

-   Los diálogos de pregunta (mediante botones) preguntan a los usuarios una sola pregunta o para confirmar un comando, y usan respuestas sencillas en botones de comandos organizados horizontalmente.
-   Los diálogos de preguntas (mediante vínculos de comandos) preguntan a los usuarios una sola pregunta o seleccionan una tarea que realizar y usan respuestas detalladas en vínculos de comandos organizados verticalmente.
-   Los cuadros de diálogo de opción presentan a los usuarios un conjunto de opciones, normalmente para especificar un comando más por completo. A diferencia de los diálogos de preguntas, los diálogos de elección pueden hacer varias preguntas.
-   Los diálogos de progreso presentan a los usuarios comentarios sobre el progreso durante una operación larga (más de cinco segundos), junto con un comando para cancelar o detener la operación.
-   Los cuadros de diálogo informativos muestran la información solicitada por el usuario.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No use cuadros de diálogo desplazables.** No use cuadros de diálogo que requieran que el uso de una barra de desplazamiento se vea completamente durante el uso normal. Rediseñar el cuadro de diálogo en su lugar. Considere la posibilidad [de usar la divulgación](ctrl-progressive-disclosure-controls.md) progresiva [o las pestañas](ctrl-tabs.md).
-   **No tiene una barra de menús ni una barra de estado.** En su lugar, proporcione acceso a los comandos y el estado directamente en el propio cuadro de diálogo o mediante menús contextuales en los controles pertinentes.

    -   **Excepción:** Las barras de menús son aceptables cuando se usa un cuadro de diálogo para implementar una ventana principal (como una utilidad).

    **Incorrecto:**

    ![captura de pantalla de un cuadro de diálogo con una barra de menús ](images/win-dialog-box-image6.png)

    En este ejemplo, Buscar certificados es un cuadro de diálogo no modelo con una barra de menús.

-   Si un cuadro de diálogo requiere atención inmediata y el programa no está activo, flashee el botón de la barra de tareas tres veces para llamar la atención y **déjelo resaltado.** No haga nada más: no restaure ni active la ventana y no haga ningún efecto de sonido. En su lugar, respeta la selección del estado de la ventana del usuario y deja que el usuario active la ventana cuando esté listo.
-   Para obtener más instrucciones y ejemplos, vea [Taskbar](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Cuadros de diálogo modales

-   **Se usa para tareas críticas o poco frecuentes y únicas que requieren finalización antes de continuar.**
-   Use un [modelo de confirmación retrasada](glossary.md) para que los cambios no se atentan hasta que se confirmen explícitamente.
-   **Implemente mediante un cuadro de diálogo de tarea siempre que sea necesario para lograr una apariencia coherente.** Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows.

### <a name="modeless-dialog-boxes"></a>Cuadros de diálogo de modeless

-   **Se usa para tareas frecuentes, repetitivas y continuas.**
-   Use un [modelo de confirmación inmediata](glossary.md) para que los cambios sumen efecto inmediatamente.
-   Para los diálogos no modelo, use un botón de comando Cerrar explícito en el cuadro de diálogo para cerrar la ventana. Para ambos, use un botón Cerrar en la barra de título para cerrar la ventana.
-   **Considere la posibilidad de acoplar cuadros de diálogo no modelo.** Los cuadros de diálogo de modeless acoplables permiten una selección de ubicación más flexible.

![captura de pantalla de un cuadro de diálogo acoplable y no modelo ](images/win-dialog-box-image7.png)

Algunos cuadros de diálogo modelados que se usan Microsoft Office son acoplables.

### <a name="multiple-dialog-boxes"></a>Varios cuadros de diálogo

-   **No muestre más de un cuadro de diálogo de elección de propiedad a la vez desde un diálogo de elección de propietario.** Mostrar más de uno hace que el significado de los botones de confirmación sea difícil de entender para los usuarios. Puede mostrar otros tipos de cuadros de diálogo (como diálogos de pregunta) según sea necesario.
-   **Para una secuencia de diálogos relacionados, considere la posibilidad de usar un diálogo de varias páginas si es posible.** Use diálogos individuales si no están claramente relacionados.

### <a name="multi-page-dialog-boxes"></a>Cuadros de diálogo de varias páginas

-   Use un cuadro de diálogo de varias páginas en lugar de cuadros de diálogo individuales cuando tenga la siguiente secuencia de páginas relacionadas:
    -   Una sola página de entrada (opcional)
    -   Una página de progreso
    -   Una sola página de resultados

La página de entrada es opcional porque es posible que la tarea se haya iniciado en otro lugar. **Esto proporciona a la experiencia resultante una sensación estable, sencilla y ligera.**

![captura de pantalla de una barra de progreso ](images/win-dialog-box-image8.png)

![captura de pantalla del mensaje "no se encontraron problemas" ](images/win-dialog-box-image9.png)

En este ejemplo, Diagnósticos de red de Windows consta de páginas de progreso y resultados.

-   **No use un cuadro de diálogo de varias páginas si la página de entrada es un diálogo estándar.** En este caso, la coherencia del uso de un diálogo estándar es más importante.
-   **No use los botones Siguiente o Atrás y no tenga más de tres páginas.** Los cuadros de diálogo de varias páginas son para tareas de un solo paso con comentarios. No son [asistentes, que](win-wizards.md)se usan para tareas de varios pasos. Los asistentes tienen una gran sensación indirecta en comparación con los cuadros de diálogo de varias páginas.
-   **En la página de entrada, use botones de comando específicos o vínculos de comando para iniciar la tarea.**
-   **Use un botón Cancelar en las páginas de entrada y progreso y un botón Cerrar en la página de resultados.**

**Desarrolladores:** Puede crear diálogos de tareas de varias páginas mediante el [mensaje TDM \_ NAVIGATE \_ PAGE.](../controls/tdm-navigate-page.md)

### <a name="presentation"></a>Presentación

Para facilitar la búsqueda y el acceso a los cuadros de diálogo, asocie claramente el diálogo a su origen y trabaje bien con varios monitores:

-   **Inicialmente, se muestran los cuadros de diálogo "centrados" en la parte superior de la ventana de propietario.** Para su posterior visualización, considere la posibilidad de mostrarla en su última ubicación (en relación con la ventana de propietario) si es probable que sea más conveniente.

![diagrama del cuadro de diálogo centrado en la ventana detrás de él ](images/win-dialog-box-image10.png)

Inicialmente, centra los diálogos en la parte superior de la ventana de propietario.

-   **Si un cuadro de diálogo es contextual, se muestra cerca del objeto desde el que se inició.** Sin embargo, colómela fuera del camino (preferiblemente desplazamiento hacia abajo y hacia la derecha) para que el objeto no esté cubierto por el cuadro de diálogo.

![diagrama de desplazamiento hacia abajo y hacia la derecha del cuadro de diálogo ](images/win-dialog-box-image11.png)

Las propiedades de un objeto se muestran cerca del objeto .

-   **En el caso de los diálogos de modeless, se muestra inicialmente en la parte superior de la ventana del propietario para que sea fácil de encontrar.** Si el usuario activa la ventana de propietario, puede ocultar el cuadro de diálogo de modeless.
-   **Si es necesario, ajuste la ubicación inicial para que todo el cuadro de diálogo esté visible dentro del monitor de destino.** Si una ventana de tamaño ajustable es mayor que el monitor de destino, reduzca para ajustarla.
-   **Cuando se vuelva a mostrar un cuadro de diálogo, considere la posibilidad de mostrarlo en el mismo estado que el último al que se ha accedido.** Al cerrar, guarde el monitor usado, el tamaño de la ventana, la ubicación y el estado (maximizado frente a restauración). Al volver a mostrar, restaure el tamaño, la ubicación y el estado del cuadro de diálogo guardado mediante el monitor adecuado. Además, considere la posibilidad de hacer que estos atributos se conserven en todas las instancias del programa por usuario.
-   **Para ventanas de tamaño ajustable, establezca un tamaño mínimo de ventana si hay un tamaño por debajo del cual el contenido ya no se puede utilizar.** Considere la posibilidad de modificar la presentación para que el contenido se pueda usar en tamaños más pequeños.

![captura de pantalla de los botones del reproductor multimedia centrado ](images/win-dialog-box-image12.png)

En este ejemplo, Reproductor de Windows Media cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

-   **No use el atributo Always On Top.**
    -   **Excepción:** Se usa solo cuando un cuadro de diálogo implementa una operación esencialmente modal, pero debe suspenderse brevemente para acceder a la ventana de propietario. Por ejemplo, al revisar la ortografía de un documento, los usuarios pueden salir ocasionalmente del cuadro de diálogo de revisión ortográfica y acceder al documento para corregir errores.

Para obtener más información y ejemplos, vea [Administración de ventanas.](win-window-mgt.md)

### <a name="title-bars"></a>Barras de título

-   **Los cuadros de diálogo no tienen iconos de barra de título.** Los iconos de la barra de título se usan como una distinción visual entre [las ventanas principales y](glossary.md) las [secundarias.](glossary.md)
    -   **Excepción:** Si se usa un cuadro de diálogo para implementar una ventana principal (como una utilidad) y, por tanto, aparece en la barra de tareas, tiene un icono de barra de título. En este caso, optimice el título para mostrarlo en la barra de tareas colocando primero la información distintiva de forma concisa.
-   **Los cuadros de diálogo siempre tienen un botón Cerrar.** Los diálogos de modeless también pueden tener un botón Minimizar. Los cuadros de diálogo que se pueden cambiar de tamaño pueden tener un botón Maximizar.
-   **No deshabilite el botón Cerrar.** Tener un botón Cerrar ayuda a los usuarios a mantener el control, ya que les permite cerrar las ventanas que no desean.
    -   **Excepción:** Para los diálogos de progreso, puede deshabilitar el botón Cerrar si la tarea debe ejecutarse hasta completarse para lograr un estado válido o evitar la pérdida de datos.
-   **El botón Cerrar de la barra de título debe tener el mismo** efecto que el botón Cancelar o Cerrar del cuadro de diálogo. No le dé nunca el mismo efecto que Aceptar.
-   Si el título y el icono de la barra de título ya se muestran de forma destacada cerca de la parte superior de la ventana, puede ocultar el título y el icono de la barra de título para evitar redundancia. Sin embargo, todavía tiene que establecer un título adecuado internamente para su uso por Parte de Windows.

### <a name="interaction"></a>Interacción

-   **Cuando se muestra, los cuadros de diálogo iniciados por el usuario siempre deben tener el foco de entrada.** Los cuadros de diálogo iniciados por el programa no deben tener el foco de entrada porque el usuario puede estar interactuando con otra ventana. Esta interacción mal dirigida en el cuadro de diálogo puede tener consecuencias no deseadas.
-   **Asigne el foco de entrada inicial al control** con el que es más probable que los usuarios interactúen con el primero, que suele ser (pero no siempre) el primer control interactivo. Evite asignar el foco de entrada inicial a un vínculo de Ayuda.
-   **Para la navegación con el teclado, el orden de tabulación debe fluir en un orden lógico, generalmente de izquierda a derecha, de arriba abajo.** Normalmente, el orden de tabulación sigue el orden de lectura, pero considere la posibilidad de realizar estas excepciones:

    -   Coloque los controles más usados anteriormente en orden de tabulación.
    -   Coloque los vínculos de Ayuda en la parte inferior de un cuadro de diálogo, después de los botones de confirmación en orden de tabulación.

    Al asignar el pedido, suponga que los usuarios muestran cuadros de diálogo para su propósito previsto; Por lo tanto, por ejemplo, los usuarios muestran cuadros de diálogo de elección para tomar decisiones, no para revisar y hacer clic en Cancelar.

-   **Al presionar la tecla Esc siempre se cierra un cuadro de diálogo activo.** Esto es así para los cuadros de diálogo con Cancelar o Cerrar, e incluso si se ha cambiado el nombre de Cancelar a Cerrar porque los resultados ya no se pueden deshacer.

**Claves de acceso**

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o sus etiquetas.** [Los cuadros de texto de solo](ctrl-text-boxes.md) lectura son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto) para que se beneficien de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones Aceptar, Cancelar y Cerrar.** Escriba y Esc se usan para sus claves de acceso. Sin embargo, asigne siempre una clave de acceso a un control que significa Aceptar o Cancelar, pero tiene una etiqueta diferente.

        ![captura de pantalla del cuadro de diálogo Eliminar archivo ](images/win-dialog-box-image13.png)

        En este ejemplo, el botón de confirmación positiva tiene asignada una clave de acceso.

    -   **Etiquetas de grupo.** Normalmente, a los controles individuales de un grupo se les asignan claves de acceso, por lo que la etiqueta de grupo no necesita ninguna. Sin embargo, si hay escasez de claves de acceso, asigne una clave de acceso a la etiqueta de grupo y no a los controles individuales.
    -   **Botones genéricos de Ayuda,** a los que se accede con F1.
    -   **Vincular etiquetas.** A menudo hay demasiados vínculos para asignar claves de acceso únicas y los caracteres de subrayado que se usan a menudo para indicar vínculos ocultan los caracteres de subrayado de la clave de acceso. En su lugar, acceda a los vínculos con la tecla Tab.
    -   **Nombres de tabulación.** Las pestañas se ciclon mediante Ctrl+Tab y Ctrl+Mayús+Tab.
    -   **Botones de exploración etiquetados como "...".** Estos botones Examinar no se pueden asignar de forma única a las claves de acceso.
    -   **Controles sin etiquetar, como** controles de giro, botones de comandos gráficos y controles de divulgación progresiva sin etiquetar.
    -   **Texto estático sin etiqueta o etiquetas para controles que no son interactivos,** como barras de progreso.

-   **Siempre que sea posible, asigne claves de acceso para los** comandos usados habitualmente según las asignaciones de claves de acceso estándar . Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, ciertamente se prefieren especialmente para los cuadros de diálogo usados con frecuencia.
-   **Asigne primero las claves de acceso del botón de confirmación para asegurarse de que tienen las asignaciones de claves estándar.** Si no hay una asignación de clave estándar, use la primera letra de la primera palabra. Por ejemplo, la clave de acceso para los botones de confirmación Sí y No siempre debe ser "Y" y "N", independientemente de los demás controles del cuadro de diálogo.
-   Para facilitar la búsqueda de claves de acceso, asigne las claves de acceso a un carácter que aparezca al principio de la **etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.
-   **Prefiere caracteres con anchos anchos anchos,** como w, m y letras mayúsculas.
-   **Prefiere una consonante distintiva o una voto,** como "x" en Salir.
-   **Evite usar caracteres que hagan que el subrayado** sea difícil de ver, como (de más problemático a menos problemático):
    -   Letras que solo tienen un píxel de ancho, como i y l.
    -   Letras con descendientes, como g, j, p, q e y.
    -   Letras junto a una letra con un descendiente.

Para obtener más instrucciones y ejemplos, vea [Teclado](inter-keyboard.md).

### <a name="progress-dialogs"></a>Cuadros de diálogo de progreso

En el caso de las tareas de ejecución larga, suponga que los usuarios harán otra **cosa mientras la tarea está completando**. Diseñe la tarea para que se ejecute desatendida.

-   **Presente a los usuarios el cuadro de** diálogo de comentarios de progreso si una operación tarda más de cinco segundos en completarse, junto con un comando para cancelar o detener la operación.
    -   **Excepción:** Para los asistentes y flujos de tareas, use un cuadro de diálogo modal para el progreso solo si la tarea permanece en la misma página (en lugar de avanzar a otra página) y los usuarios no pueden hacer nada mientras esperan. De lo contrario, use una página de progreso o un progreso local.
-   Si la operación es una tarea de ejecución larga (más de 30 segundos) y se puede realizar en segundo plano, use un cuadro de diálogo de progreso de modelado para que los usuarios puedan seguir usando el programa mientras esperan.
-   Cuadros de diálogo de progreso de modeless:
    -   Tiene un botón Minimizar en la barra de título.
    -   Se muestran en la barra de tareas.
-   Implemente diálogos de progreso de modeless para que sigan en ejecución incluso si se cierra la ventana de propietario.

![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/win-dialog-box-image14.png)

En este ejemplo, la copia de archivos continúa incluso si se cierra la ventana de propietario.

-   **Proporcione un botón de comando para detener la operación si tarda más de unos segundos en completarse o tiene la posibilidad de que nunca se complete.** Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin efectos secundarios); De lo contrario, etiquete el botón Detener para indicar que deja intacta la operación parcialmente completada. Puede cambiar la etiqueta del botón de Cancelar a Detener en medio de la operación, si en algún momento no es posible devolver el entorno a su estado anterior.

![captura de pantalla del cuadro de diálogo con el botón Cancelar ](images/win-dialog-box-image15.png)

En este ejemplo, detener el diagnóstico del problema no tiene ningún efecto secundario.

-   **Proporcione un botón de comando para pausar la operación si tarda más de varios minutos en completarse y afecta a la capacidad de los usuarios de realizar el trabajo.** Esto no obliga al usuario a elegir entre completar la tarea y realizar su trabajo.
-   **Recopila toda la información que pueda antes de iniciar la tarea.**
-   **Si se detectan problemas recuperables, haga que los usuarios ata con todos los problemas encontrados al final de la tarea.** Si esto no es práctico, haga que los usuarios se des frente a problemas a medida que se suceden.
-   **No abandone las tareas como resultado de errores recuperables.**

![captura de pantalla del cuadro de diálogo con el botón Intentarlo de nuevo ](images/win-dialog-box-image16.png)

En este ejemplo, Explorador de Windows permite a los usuarios continuar con la tarea después de un error recuperable.

-   **Indique los problemas si la barra de progreso se muestra en rojo.**

![captura de pantalla de la barra de progreso e intentarlo de nuevo ](images/win-dialog-box-image17.png)

En este ejemplo, se quitó un disco extraíble durante una copia de archivos.

-   **Si los resultados son claramente evidentes para los usuarios, cierre automáticamente el cuadro de diálogo de progreso al finalizar correctamente.** De lo contrario, use comentarios solo para notificar problemas:
    -   Para mostrar comentarios simples, muestre los comentarios en el cuadro de diálogo de progreso y cambie el botón Cancelar a Cerrar.
    -   Para mostrar comentarios detallados, cierre el cuadro de diálogo progreso y muestre un cuadro de diálogo informativo.

**No use una notificación para los comentarios de finalización.** Use un cuadro de diálogo de progreso o una [notificación de acción correcta,](mess-notif.md)pero no ambos.

**Tiempo restante**

-   **Use los siguientes formatos de hora.** Comience con el primero de los siguientes formatos, donde la unidad de tiempo más grande no es cero y, después, cambie al siguiente formato una vez que la unidad de tiempo más grande se convierta en cero.

**Para las barras de progreso:**

**Si la información relacionada se muestra en formato de dos puntos:**

Tiempo restante: h horas, m minutos

Tiempo restante: m minutos, s segundos

Tiempo restante: s segundos

**Si el espacio de pantalla es premium:**

h hrs, m mins remaining

m mins, s secs restantes

s segundos restantes

**De lo contrario:**

h hours, m minutes remaining

m minutes, s seconds remaining

s segundos restantes

**Para las barras de título:**

hh:mm restante

mm:ss restante

0:ss restantes

Este formato compacto muestra primero la información más importante para que no se trunca en la barra de tareas.

-   **Realice estimaciones precisas, pero no dé una precisión falsa.** Si la unidad más grande es horas, dé minutos (si es significativo), pero no segundos.

**Incorrecto:**

hh hours, mm minutes, ss seconds

-   **Mantenga actualizada la estimación.** El tiempo de actualización restante calcula al menos cada 5 segundos.
-   **Céntrate en el tiempo restante,** ya que es la información que más preocupa a los usuarios. Proporcionar tiempo total transcurrido solo cuando haya escenarios en los que el tiempo transcurrido sea útil (por ejemplo, cuando es probable que se repita la tarea). Si la estimación de tiempo restante está asociada a una barra de progreso, no tiene el porcentaje de texto completo porque esa información la transmite la propia barra de progreso.
-   **Ser gramaticalmente correcto.** Use unidades singulares cuando el número sea uno.

**Incorrecto:**

1 minuto, 1 segundo

-   **Use mayúsculas de estilo de frase.**

Para obtener más información y ejemplos, vea [Barras de progreso](progress-bars.md).

### <a name="icons-and-graphics"></a>Iconos y gráficos

**Elementos gráficos**

-   **No use gráficos grandes que no sirvan para nada más que llenar el espacio con los ojos.** En su lugar, mantenga la apariencia sencilla.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con un gráfico grande ](images/win-dialog-box-image18.png)

En este ejemplo, el gráfico grande no sirve para nada.

**Iconos de la barra de título**

-   **Los cuadros de diálogo no tienen iconos de barra de título.**
    -   **Excepción:** Si se usa un cuadro de diálogo para implementar una ventana principal (como una utilidad) y, por tanto, aparece en la barra de tareas, tiene un icono de barra de título.

**Iconos de cuerpo**

-   **Elija el icono de cuerpo en función del patrón de diseño:**



| Patrón | Icono de cuerpo |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Diálogos de preguntas**<br/>      | Icono de programa, característica, objeto, advertencia (si se puede perder datos o acceso al sistema), advertencia de seguridad o ninguno.<br/> |
| **Cuadros de diálogo de elección**<br/>        | Ninguno.<br/>                                                                                                           |
| **Cuadros de diálogo de progreso**<br/>      | Ninguno (pero puede tener una animación).<br/>                                                                               |
| **Cuadros de diálogo informativos**<br/> | Ninguno.<br/>                                                                                                           |



 

-   **Incorrecto:**

![captura de pantalla del cuadro de diálogo con el icono de advertencia ](images/win-dialog-box-image19.png)

En este ejemplo, se usa incorrectamente un icono de advertencia para una pregunta que no implica una posible pérdida de datos o acceso al sistema.

- **Considere la posibilidad de usar iconos para ayudar a los usuarios a reconocer visualmente las características del programa.** Esta técnica es más eficaz cuando los iconos son fácilmente reconocibles y se usan en varias ubicaciones dentro del programa.

![captura de pantalla del cuadro de diálogo favoritos con icono de estrella ](images/win-dialog-box-image20.png)

En este ejemplo, el icono de estrella amarilla representa Favoritos. El icono es fácilmente reconocible y se usa de forma coherente en Windows para representar Favoritos.

-   **Use iconos para ayudar a los usuarios a reconocer el objeto en cuestión.**

![captura de pantalla del cuadro de diálogo con el icono de PowerPoint ](images/win-dialog-box-image21.png)

En este ejemplo, el icono del objeto ayuda a los usuarios a reconocer el tipo de archivo que se abre o guarda.

-   **Considere la posibilidad de usar iconos para ayudar a que las características se puedan explicar por sí solas.**

![imágenes de flechas que muestran cómo colocar el monitor ](images/win-dialog-box-image22.png)

En este ejemplo, estos iconos ayudan a los usuarios a visualizar el efecto de sus características.

-   **Use un icono en los cuadros de diálogo About Box para la personal de marca de la aplicación.**

![captura de pantalla del cuadro de diálogo Acerca de con el logotipo de Windows ](images/win-dialog-box-image23.png)

En este ejemplo, se usa un mapa de bits en about box para identificar y marcar la aplicación.

**Iconos de nota al pie**

-   **Si tiene una nota al pie, considere la posibilidad de usar un icono de nota al pie para resumir el asunto de la nota al pie.**

![captura de pantalla del cuadro de diálogo con el icono de nota al pie ](images/win-dialog-box-image24.png)

En este ejemplo, el icono de nota al pie indica que la pregunta tiene implicaciones de seguridad.

-   **No use un icono de nota al pie que repita el icono de cuerpo.**
-   **No use los iconos estándar de error o de información.** Las condiciones de error se deben transmitir a través del icono del cuerpo y las notas al pie siempre son para obtener información, lo que hace que el icono de información sea redundante. Sin embargo, puede usar el icono de advertencia estándar y el escudo de seguridad amarillo para alertar a los usuarios de consecuencias de riesgo.

Para obtener más información y ejemplos, vea [Iconos](vis-icons.md).

### <a name="commit-buttons"></a>Botones de confirmación

**Notas:**

-   Estas directrices no se aplican a los diálogos de pregunta mediante vínculos de comandos, porque ese patrón usa vínculos de comandos en lugar de botones.
-   \[Hacerlo y No hacerlo son respuestas afirmativas y \] \[ \] negativas, respectivamente, a la instrucción principal.

**General**

-   **Elija los botones de confirmación según el patrón de diseño:**

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>Patrón</strong><br/></td>
    <td><strong>Botones de confirmación</strong><br/></td>
    </tr>
    <tr class="even">
    <td><strong>Diálogos de pregunta (mediante botones)</strong><br/></td>
    <td>Uno de los siguientes conjuntos de comandos concisos: Yes/No, Yes/No/Cancel, [Do it]/Cancel, [Do it]/[Don't do it], [Do it]/[Don't do it]/Cancel.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Diálogos de pregunta (mediante vínculos)</strong><br/></td>
    <td>Cancel (Cancelar)<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Cuadros de diálogo de elección</strong><br/></td>
    <td><ul>
    <li>Diálogos modales: Aceptar/Cancelar o [Hacerlo]/Cancelar</li>
    <li>Diálogos de modeless: Botón Cerrar en el cuadro de diálogo y la barra de título</li>
    <li>Panel de tareas: botón Cerrar de la barra de título</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Cuadros de diálogo de progreso</strong><br/></td>
    <td>Use Cancelar si devuelve el entorno a su estado anterior (sin ningún efecto secundario); De lo contrario, use Detener.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Cuadros de diálogo informativos</strong><br/></td>
    <td>Casi.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Todos los botones de confirmación, excepto Aplicar, cierran la ventana del cuadro de diálogo.**
-   **No confirme los botones de confirmación.** Hacerlo innecesariamente puede ser muy molesto. **Excepciones:**

    -   La acción es potencialmente catastrófica.
    -   La acción es claramente incoherente con otras acciones.
    -   Si no es correcta, la acción puede provocar una pérdida significativa de datos, tiempo o esfuerzo en nombre del usuario.

    Para obtener más instrucciones y ejemplos, vea [Confirmaciones](mess-confirm.md).

-   **No deshabilite los botones de confirmación. Excepciones:**
    -   **Si los usuarios deben elevar para realizar un cambio, deshabilite los botones de confirmación positiva hasta que el usuario realice un cambio.** Si lo hace, impide que los usuarios eleven solo para cerrar una ventana, forzándolos a hacer clic en Cancelar.
    -   Para obtener más excepciones, vea Deshabilitar o quitar controles frente a [dar mensajes de error.](#disabling-or-removing-controls-vs-giving-error-messages)
-   **Alinear a la derecha los botones de confirmación en una sola fila en** la parte inferior del cuadro de diálogo, pero encima del área de nota al pie. Haga esto incluso si hay un solo botón de confirmación (por ejemplo, Aceptar).

    **Incorrecto:**

    ![captura de pantalla del mensaje con el botón Aceptar centrado ](images/win-dialog-box-image25.png)

    En este ejemplo, el botón Aceptar se centra incorrectamente.

-   **Presente los botones de confirmación en el orden siguiente:**
    1.  Ok/ \[ Do it \] /Yes
    2.  \[No lo haga \] /No
    3.  Cancelar
    4.  Aplicar (si está presente)
    5.  Ayuda (si está presente)
-   **Si tiene muchos botones de confirmación relacionados, consolidelos mediante los botones de división**.
-   **Tener una separación clara de los botones de confirmación (que cierran la ventana) y todos los demás botones de comando (como Avanzado).**

**Respuesta a las instrucciones principales**

-   **Use botones de confirmación positivos que sean respuestas específicas a la instrucción principal, en lugar de etiquetas genéricas como Aceptar o Sí/No.** Los usuarios deben poder comprender las opciones leyendo solo el texto del botón. **Excepciones:**
    -   Use Cerrar para los diálogos que no tienen configuración, como los diálogos informativos. Nunca use Cerrar para los cuadros de diálogo que tengan configuración.
    -   Use Aceptar cuando las respuestas "específicas" sean todavía genéricas, como Guardar, Seleccionar o Elegir. Use Aceptar al cambiar una configuración específica o una colección de configuraciones.
    -   **Para los cuadros de diálogo heredados sin una instrucción principal, puede usar etiquetas genéricas como Aceptar.** A menudo, estos cuadros de diálogo no están diseñados para realizar una tarea específica, lo que impide respuestas más específicas.
    -   Ciertas tareas requieren una lectura más cuidadosa y reflexión para que los usuarios puedan tomar decisiones informadas. Este suele ser el caso de [las confirmaciones](mess-confirm.md). **En tales casos, puede usar etiquetas de botón de confirmación genéricas para obligar a los usuarios a leer las instrucciones principales y evitar decisiones desatensadas.**

        **Correcto:**

        ![captura de pantalla del mensaje con botones sí y no](images/win-dialog-box-image26.png)

        En este ejemplo, el uso de botones de confirmación Sí/No obliga a los usuarios a leer al menos la instrucción principal.

-   **Como alternativa,** puede agregar la palabra "de todos modos" a la etiqueta del botón de confirmación positiva para indicar que el cuadro de diálogo presenta una razón para no continuar y que los usuarios deben leer el cuadro de diálogo cuidadosamente antes de continuar.

    **Correcto:**

    ![captura de pantalla del mensaje y botón desinstalar de todos modos ](images/win-dialog-box-image27.png)

    En este ejemplo, "de todos modos" se agrega a la etiqueta del botón de confirmación para indicar que los usuarios deben continuar con cuidado.

-   **Use Cancelar o Cerrar para botones de confirmación negativos en lugar de respuestas específicas a la instrucción principal.** A menudo, los usuarios se dan cuenta de que no quieren realizar una tarea una vez que ven un cuadro de diálogo. Si Cancel o Close se vuelven a etiquetar para respuestas específicas, los usuarios tendrían que leer cuidadosamente todos los botones de confirmación para determinar cómo cancelar. **Al etiquetar Cancel y Close de forma coherente, resulta fácil encontrarlos. Excepciones:**
    -   **No use Sí/Cancelar.** Use siempre Sí/No como par.
    -   **Use una respuesta específica cuando Cancelar sea ambiguo.**
-   **No asigne etiquetas genéricas a su significado específico con texto en el área de contenido.** En su lugar, use etiquetas de botón de confirmación específicas o un cuadro de diálogo de pregunta mediante vínculos si las etiquetas son largas.

    **Incorrecto:**

    ![captura de pantalla del mensaje con un uso poco claro de botones ](images/win-dialog-box-image28.png)

    En este ejemplo, Aceptar se asigna a Continuar, Cancelar se asigna a Permanecer en la página.

**Botones Sí y No**

-   **Prefiere respuestas específicas a los botones Sí y No.** Aunque no hay ningún problema con el uso de Sí y No, las respuestas específicas se pueden entender más rápidamente, lo que da lugar a una toma de decisiones eficaz. Sin embargo, [las confirmaciones](mess-confirm.md) suelen tener botones Sí y No para hacer que los usuarios tengan en cuenta la [confirmación antes](mess-confirm.md) de responder.
-   **Use los botones Sí y No solo para responder a preguntas sí o ninguna.** La instrucción principal debe expresarse de forma natural como una pregunta sí o ninguna. No use nunca Ok (Aceptar) y Cancel (Cancelar) para preguntas sí o ninguna.

    **Incorrecto:**

    ![Captura de pantalla que muestra un mensaje con un "Ok" para una pregunta sí-no.](images/win-dialog-box-image29.png)

    **Correcto:**

    ![captura de pantalla del mensaje con sí para la misma pregunta ](images/win-dialog-box-image30.png)

    **Mejor:**

    ![captura de pantalla del mensaje con la ejecución de la misma pregunta ](images/win-dialog-box-image31.png)

    En estos ejemplos, Sí y No son buenas respuestas a preguntas sí y ninguna, pero las respuestas específicas son incluso mejores.

-   **Considere la posibilidad de decir la instrucción principal como una pregunta sí o ninguna si los botones de confirmación con expresiones específicas son largos o difíciles.** Como alternativa, puede usar vínculos de comandos para respuestas más largas (cinco palabras o más) a la instrucción principal.

    **Incorrecto:**

    ![captura de pantalla del mensaje con etiquetas de botón wordy ](images/win-dialog-box-image32.png)

    **Correcto:**

    ![captura de pantalla del mensaje con etiquetas de botón Sí/No ](images/win-dialog-box-image33.png)

    La expresión específica del ejemplo incorrecto es demasiado larga, por lo que el ejemplo correcto usa Sí y No.

-   **No use los botones Sí y No si el significado de la respuesta No es claro.** Si es así, use respuestas específicas en su lugar.

**Botones aceptar**

-   **En los diálogos modales, hacer clic en Aceptar significa aplicar los valores, realizar la tarea y cerrar la ventana.**
-   **No use los botones Aceptar para responder a preguntas.**
-   **No asigne claves de acceso a Aceptar, porque Entrar es la clave de acceso del botón predeterminado.** Esto facilita la asignación de las demás claves de acceso.
-   **Etiquetar correctamente los botones Aceptar.** El botón Aceptar debe tener la etiqueta Aceptar, no Aceptar o Aceptar.
-   **No use los botones Aceptar para errores o advertencias.** Los problemas nunca son correctos. Use Cerrar en su lugar.

    **Incorrecto:**

    ![captura de pantalla del mensaje con el botón Aceptar ](images/win-dialog-box-image34.png)

    En este ejemplo, se debe usar Close en lugar de Aceptar.

-   **No use los botones Aceptar en los cuadros de diálogo de modeless.** En su lugar, los diálogos no modelo deben usar botones de confirmación específicos de la tarea (por ejemplo, Buscar). Sin embargo, algunos cuadros de diálogo no modelo solo requieren un botón Cerrar.

**Botones cancelar**

-   **Hacer clic en Cancelar significa abandonar todos los cambios, cancelar la tarea, cerrar la ventana y devolver el entorno a su estado anterior, sin ningún efecto secundario.** En el caso de los cuadros de diálogo de elección anidados, al hacer clic en Cancelar en el cuadro de diálogo de elección de propietario, también se abandonan los cambios realizados por los diálogos de elección de propiedad.
-   **Proporcione un botón Cancelar para permitir que los usuarios abandonen explícitamente los cambios.** Los cuadros de diálogo necesitan un punto de salida sin borrar. No dependa de que los usuarios encuentran el botón Cerrar en la barra de título.

    -   **Excepción:** No proporcione un botón Cancelar para cuadros de diálogo sin configuración. Los botones Aceptar y Cerrar tienen el mismo efecto que Cancelar en este caso.

    **Incorrecto:**

    ![captura de pantalla del mensaje solo con el botón Aceptar ](images/win-dialog-box-image35.png)

    En este ejemplo, tener solo un botón Cerrar en la barra de título hace que parezca que los usuarios no tienen otra opción.

-   **No use los botones Cancelar para responder a preguntas.**

    **Incorrecto:**

    ![captura de pantalla del mensaje con ok for yes-no question ](images/win-dialog-box-image36.png)

    En este ejemplo, OK y Cancel se usan incorrectamente para responder a una pregunta Sí o No.

-   **No asigne claves de acceso a Cancel, porque Esc es la clave de acceso.** Esto facilita la asignación de las demás claves de acceso.
-   **No use los botones Cancelar en los cuadros de diálogo de modeless.** En su lugar, use Cerrar en su lugar.
-   **No deshabilite el botón Cancelar.** Los usuarios siempre deben poder cancelar los cuadros de diálogo.
    -   **Excepción:** Puede deshabilitar el botón Cancelar en un cuadro de diálogo de progreso si hay un período durante el cual no se puede cancelar la operación. Sin embargo, una mejor solución es diseñar estas operaciones para que siempre se puedan cancelar.

**Botones cerrar**

-   **Use los botones Cerrar para los cuadros de diálogo no modales, así como los diálogos modales que no se pueden cancelar.**
-   **Al hacer clic en Cerrar, se cierra la ventana del cuadro de diálogo y se dejan los efectos secundarios existentes.** No use Listo, porque no es una construcción imperativa. En el caso de los cuadros de diálogo de elección anidados, al hacer clic en Cerrar en el cuadro de diálogo de elección de propietario, se conservan los cambios realizados por los diálogos de elección de propiedad.
-   **Coloque un botón Cerrar explícito en el cuerpo del cuadro de diálogo.** Los cuadros de diálogo necesitan un punto de salida sin borrar. No dependa de que los usuarios encuentran el botón Cerrar en la barra de título.
-   **Asegúrese de que el botón Cerrar de la barra de título tiene el mismo efecto que Cancelar o Cerrar.**
-   **No asigne claves de acceso a Close, porque Esc es la clave de acceso.** Esto facilita la asignación de las demás claves de acceso.

**Aplicar botones**

-   **No use los botones Aplicar en cuadros de diálogo que no sean hojas de propiedades ni paneles de control.** El botón Aplicar significa aplicar los cambios pendientes, pero dejar la ventana abierta. Esto permite a los usuarios evaluar los cambios antes de cerrar la ventana. Sin embargo, solo la hoja de propiedades y los paneles de control tienen esta necesidad.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con el botón Aplicar ](images/win-dialog-box-image37.png)

    En este ejemplo, un cuadro de diálogo de opción tiene un botón Aplicar.

**Botones de confirmación para cuadros de diálogo indirectos**

**Nota:** Los cuadros de diálogo indirectos se muestran fuera de contexto, ya sea como resultado indirecto de una tarea o como resultado de un problema con un sistema o proceso en segundo plano. Para los diálogos indirectos, el botón Cancelar es ambiguo porque podría significar cancelar el diálogo o cancelar toda la tarea.

-   **Si los usuarios necesitan cancelar el cuadro de diálogo y la tarea, dé botones de confirmación para realizar ambas tareas.** Etiquete el botón que cancela el cuadro de diálogo con una respuesta negativa a la instrucción principal. Etiquete el botón que cancela toda la tarea con Cancelar. El uso de Cancelar permite usar el cuadro de diálogo en muchos contextos.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo con guardar o no guardar ](images/win-dialog-box-image38.png)

    En este ejemplo, Windows Paint muestra este cuadro de diálogo como resultado de un comando New o Exit cuando el gráfico no se ha guardado. No guardar cierra el cuadro de diálogo sin guardar, mientras que Cancelar cancela el comando New o Exit.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con botones Sí/No ](images/win-dialog-box-image39.png)

    En este ejemplo, no hay ninguna manera de cancelar la tarea (cerrar la barra de accesos directos de Office) que condujo a mostrar este cuadro de diálogo. Este cuadro de diálogo necesita un botón Cancelar.

-   **Si los usuarios solo** necesitan cancelar el cuadro de diálogo, pero no la tarea, use un botón con una respuesta específica negativa a la instrucción principal y no tenga un botón Cancelar.

    ![captura de pantalla del cuadro de diálogo con run/don't run ](images/win-dialog-box-image24.png)

    En este ejemplo, este cuadro de diálogo se muestra indirectamente como resultado de navegar a una página web que instala un control ActiveX. El uso de Cancelar sería ambiguo aquí, por lo que no se usa No ejecutar en su lugar.

Para obtener más información y ejemplos, vea [Botones de comando](ctrl-command-buttons.md).

### <a name="command-links"></a>Vínculos de comandos

-   **Presente un conjunto de comandos largos mediante vínculos de comandos, en lugar de botones de comando o una combinación de botones de radio y un botón Aceptar.** Esto permite a los usuarios responder con un solo clic. Sin embargo, este enfoque solo funciona para una sola pregunta.
-   **Presente primero los vínculos de comandos más usados.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tener un flujo lógico.
    -   **Excepción:** Los vínculos de comandos que hacen que todo se haga primero deben colocarse en primer lugar.
-   Si un vínculo de comando requiere una explicación adicional, **proporcione una explicación complementaria.** Las explicaciones adicionales describen por qué es posible que los usuarios quieran elegir el comando o qué ocurre si se elige el comando.
-   **No use explicaciones complementarias que sean instrucciones de texto del vínculo de comando.** Use una explicación complementaria solo cuando no pueda hacer que un vínculo de comando se explique por sí mismo. Proporcionar una explicación complementaria para un vínculo de comando no significa que tenga que proporcionarlos para todos los comandos.

![captura de pantalla del cuadro de diálogo con opciones de notación de texto ](images/win-dialog-box-image40.png)

En este ejemplo, la explicación complementaria describe las implicaciones de una de las opciones.

-   **Use frases que empiecen por un verbo, sin finalizar la puntuación.**
-   **Si se recomienda encarecidamente un comando, considere la posibilidad de agregar "(recommended)" a la etiqueta.** Asegúrese de agregar a la etiqueta de vínculo, no a la explicación complementaria.
-   **Si un comando está pensado solo para usuarios avanzados, considere la posibilidad de agregar "(advanced)" a la etiqueta.** Asegúrese de agregar a la etiqueta de vínculo, no a la explicación complementaria.
-   **Proporcione siempre un botón Cancelar explícito.** No use un vínculo de comando para este propósito.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con el vínculo No salir ](images/win-dialog-box-image41.png)

En este ejemplo, el cuadro de diálogo usa un vínculo de comando en lugar de un botón Cancelar.

Para obtener más información y ejemplos, vea [Vínculos de comandos](ctrl-command-links.md).

### <a name="dont-show-this-item-again"></a>No mostrar esto <item> Otra vez

-   **Considere la posibilidad de usar una opción No volver a mostrar esta opción para permitir a los usuarios suprimir un cuadro de diálogo periódico, solo si no <item> hay una alternativa mejor.** Es mejor mostrar siempre el cuadro de diálogo si los usuarios realmente lo necesitan, o simplemente eliminarlo si no lo necesitan.
-   **Use esta expresión específica para reemplazar <item> por el elemento específico.** Por ejemplo, no vuelva a mostrar este recordatorio. Al hacer referencia a un cuadro de diálogo en general, use No volver a mostrar este mensaje.
-   **Indique claramente cuándo se usará** la entrada del usuario para los valores predeterminados futuros agregando la siguiente frase bajo la opción : Las selecciones se usarán de forma predeterminada en el futuro.
-   **No seleccione la opción de forma predeterminada. Si el cuadro de diálogo debe mostrarse solo una vez, debe hacerlo sin preguntar.** No use esta opción como medida para fastidiar a los usuarios, asegúrese de que el comportamiento predeterminado no sea molesto.

**Incorrecto:**

![captura de pantalla del mensaje que hace preguntas innecesarias ](images/win-dialog-box-image42.png)

En este ejemplo, el mensaje solo debe mostrarse una vez. No es necesario preguntar.

-   **Haga que la configuración se conserve por usuario.**
-   **Si los usuarios seleccionan la opción y hacen clic en Cancelar, esta opción se hace efectiva.** Esta configuración es una meta-opción, por lo que no sigue el comportamiento de cancelación estándar de no dejar ningún efecto secundario. Tenga en cuenta que si los usuarios no quieren ver el cuadro de diálogo en el futuro, lo más probable es que también quieran cancelarlo.
-   Si es posible que los usuarios necesiten restaurar estos cuadros de diálogo, proporcione un comando **Restaurar** mensajes en el cuadro de diálogo Opciones del programa.

### <a name="ask-me-later"></a>Preguntarme más tarde

-   Proporcione esta opción para descartar un cuadro de diálogo solo cuando:
    -   **El cuadro de diálogo es indirecto,** por lo que es probable que los usuarios se centren en otra tarea.
    -   **Los usuarios deben responder, pero no inmediatamente,** para que puedan continuar con su trabajo.
    -   **La pregunta requiere suficiente reflexión o esfuerzo para** que los usuarios puedan tomar mejores decisiones si se les da más tiempo.
    -   **El cuadro de diálogo o la opción se mostrará automáticamente más adelante** (para que los usuarios realmente se pregunten más adelante).
-   **Incorrecto:**
-   ![captura de pantalla del mensaje con la opción preguntarme más adelante ](images/win-dialog-box-image43.png)
-   En este ejemplo, la pregunta es lo suficientemente sencilla como para que agregar una opción Pregúnteme más adelante solo la complica.
-   De lo contrario, espere que los usuarios respondan ahora, pero permita que cierren el cuadro de diálogo normalmente con Cancelar o Cerrar. Cuando se usa correctamente, esta opción debe ser poco frecuente.

### <a name="morefewer"></a>Más o menos

-   **Use más o menos botones de divulgación progresiva para mostrar u ocultar opciones, comandos o detalles avanzados o poco usados que los usuarios de destino normalmente no necesitan.** Esto simplifica el cuadro de diálogo para un uso típico. No oculte las opciones, los comandos o la información que se usan habitualmente porque es posible que los usuarios no las encuentren.

![captura de pantalla del cuadro de diálogo con el botón más opciones ](images/win-dialog-box-image24.png)

En este ejemplo, las opciones que se usan con menos frecuencia se ocultan de forma predeterminada.

-   **No use más o menos controles a menos que realmente haya más detalles para mostrar.** No solo vuelva a establecer la misma información en un formato diferente.
-   **No use más o menos controles para mostrar la Ayuda.** En su lugar, use vínculos de Ayuda o notas al pie.
-   **Con los cuadros de diálogo de tareas, evite combinar más o menos controles con No volver a <item> mostrar esto.** Esta combinación tiene un aspecto extraño.
-   Para obtener instrucciones de etiquetado, vea [Divulgación progresiva.](ctrl-progressive-disclosure-controls.md)

### <a name="footnotes"></a>Notas al pie

-   **Use notas al pie para obtener información que no es esencial para el propósito de un cuadro de diálogo, pero que los usuarios pueden resultar útiles para tomar decisiones.** La mayoría de los usuarios deben poder omitir las notas al pie y seguir tomando decisiones informadas en su respuesta al cuadro de diálogo.

![captura de pantalla del cuadro de diálogo con la nota al pie aclarada ](images/win-dialog-box-image44.png)

En este ejemplo, la información de nota al pie es complementaria, no esencial.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Deshabilitar o quitar controles frente a dar mensajes de error

-   Cuando un control no se aplica en el contexto actual, tenga en cuenta las siguientes opciones:
    -   **Quite el control cuando los usuarios no puedan habilitarlo o cuando los usuarios no esperen que se aplique y su estado no cambie con frecuencia.** Esto simplifica el cuadro de diálogo y los usuarios no lo perderán. Hacer que un control aparezca y desaparezca con frecuencia resulta molesto.
    -   **Deshabilite el control cuando los usuarios esperen que se aplique o su estado cambie con frecuencia, y los usuarios pueden deducir fácilmente por qué el control está deshabilitado.** Un ejemplo de deducción sencilla es deshabilitar un botón de confirmación cuando hay un único cuadro de texto vacío que requiere cualquier entrada. Puede usar [globos para mostrar](ctrl-balloons.md) problemas de entrada de usuario no críticos con cuadros de texto y listas desplegables editables. Sin embargo, si el problema no se puede explicar con un globo o implica varios controles, la deducción ya no sería fácil.
    -   **De lo contrario, deje el control habilitado, pero dé un mensaje de error cuando se utilice incorrectamente.** Deshabilitar en este caso dificultaría a los usuarios comprender por qué el control está deshabilitado. Los usuarios se verían obligados a determinar el problema a través de la experimentación y la lógica de desasoción. Es mejor proporcionar un mensaje de error útil para explicar el problema explícitamente.
-   **Sugerencia:** Si no está seguro de si debe deshabilitar un control o proporcionar un mensaje de error, empiece por crear el mensaje de error que podría proporcionar. Si el mensaje de error contiene información útil que es probable que los usuarios de destino no deduzcan rápidamente, deje el control habilitado y dé el error. De lo contrario, deshabilite el control .
-   **Si deshabilita un control, deshabilite también** todos los controles asociados, como su etiqueta, explicaciones complementarias o botones de comando. Sin embargo, no deshabilite sus cuadros [de grupo,](ctrl-group-boxes.md)etiqueta de grupo o explicación de grupo si los hay.

![captura de pantalla del cuadro de diálogo con controles atenuados ](images/win-dialog-box-image45.png)

En este ejemplo, las etiquetas de cuadro de texto deshabilitadas también están deshabilitadas, pero su explicación de grupo y etiqueta de grupo no.

### <a name="required-input"></a>Entrada necesaria

-   Para indicar que los usuarios deben proporcionar información en un control, tenga en cuenta las siguientes opciones:
    -   **No indique nada, pero controle la entrada necesaria que falta con mensajes de error.** Este enfoque reduce el desorden y funciona bien si la mayoría de la entrada es opcional o es probable que los usuarios no omitan controles, lo que mantiene el número de mensajes de error bajo.
    -   **Indique la entrada necesaria mediante un asterisco al principio de la etiqueta.** Explique el asterisco mediante:

        -   Una nota al pie en la parte inferior del área de contenido que dice \* Entrada necesaria.
        -   Información sobre herramientas en el asterisco que indica Entrada requerida.

        Este enfoque funciona bien si no hay muchos controles necesarios, pero es deficiente si se requieren la mayoría de los controles.

        ![captura de pantalla de etiquetas de cuadro de texto con asteriscos ](images/win-dialog-box-image46.png)

        En este ejemplo, se usan asteriscos para indicar la entrada necesaria.

    -   **Si todos los controles requieren entrada, estado "All input required" (Todas las entradas necesarias) en un lugar adecuado en la parte superior del área de contenido.** Este enfoque reduce el desorden en este caso específico.
    -   **Indique entradas opcionales con "(opcional)" después de la etiqueta.** Este enfoque funciona bien si se requiere la mayoría de las entradas, pero en caso contrario, es deficiente.

-   **Para mantener la coherencia, intente usar el mismo método para indicar la entrada necesaria en todo el programa.** En concreto, indique la entrada obligatoria u opcional según sea necesario, pero evite usar ambas dentro del mismo programa.

### <a name="error-handling"></a>Control de errores

-   Evite errores mediante el uso de controles restringidos a la entrada de usuario válida. También puede ayudar a reducir el número de errores proporcionando valores predeterminados razonables.
-   Valide la entrada del usuario lo antes posible y muestre los errores lo más cerca posible del punto de entrada.
-   **Use el control de errores modelados (errores en el lugar o globos) para problemas de entrada del usuario.**
    -   **Use globos para problemas de entrada de usuario de un solo punto no críticos detectados en un cuadro de texto o inmediatamente después de que un cuadro de texto pierda el foco.** Los globos no requieren espacio de pantalla disponible ni el diseño dinámico necesario para mostrar los mensajes en su lugar. Mostrar solo un globo a la vez. Dado que el problema no es crítico, no es necesario ningún icono de error. Los globos desaparecen cuando se hace clic en él, cuando se resuelve el problema o después de un tiempo de espera.

        ![captura de pantalla del mensaje "carácter incorrecto" ](images/win-dialog-box-image47.png)

        En este ejemplo, un globo indica un problema de entrada mientras sigue en el control .

-   **Use errores en el lugar para la detección de errores retrasada;** normalmente, los errores encontrados al hacer clic en un botón de confirmación. (No use errores en el lugar para las configuraciones que se confirman inmediatamente). Puede haber varios errores en el lugar a la vez. Use texto normal y un icono de error de 16 x 16 píxeles, colocándolos directamente junto al problema siempre que sea posible. Los errores locales no desaparecen a menos que el usuario se confirme y no se haya encontrado ningún otro error.

    ![captura de pantalla del cuadro de diálogo con dos mensajes de error ](images/win-dialog-box-image48.png)

    En este ejemplo, se usa un error local para un error encontrado al hacer clic en el botón confirmar.

-   Use el control modal de **errores (cuadros** de diálogo de tareas o cuadros de mensaje) para todos los demás problemas, incluidos los errores que implican varios controles, o bien los errores no contextuales o que no son de entrada encontrados al hacer clic en un botón de confirmación.
-   **Cuando se encuentra y notifica un problema de entrada, establezca el foco de entrada en el primer control con los datos incorrectos.** Si es necesario, desplácese hasta la vista del control.

Para obtener más información y ejemplos, vea [Mensajes de error](mess-error.md) y [globos](ctrl-balloons.md).

### <a name="help"></a>Ayuda

-   Al proporcionar asistencia al usuario, tenga en cuenta las siguientes opciones (enumeradas en su orden de preferencia):
    -   Proporcionar etiquetas autoexplicativas a los controles interactivos. Es más probable que los usuarios lean las etiquetas en controles interactivos que cualquier otro texto.
    -   Proporcione explicaciones en contexto mediante etiquetas [de texto estático](text-ui.md).
    -   Proporcione un vínculo de Ayuda específico a un tema de Ayuda pertinente.
-   **Busque vínculos de Ayuda en la parte inferior del área de contenido del cuadro de diálogo.** Si el cuadro de diálogo tiene una nota al pie y el vínculo ayuda está relacionado con ella, coloque el vínculo Ayuda dentro de la nota al pie.

    ![captura de pantalla del cuadro de diálogo con el vínculo de ayuda ](images/win-dialog-box-image40.png)

    En este ejemplo, el vínculo ayuda se aplica a todo el cuadro de diálogo.

    -   **Excepción:** Si un cuadro de diálogo tiene varios grupos distintos de configuraciones que tienen temas de Ayuda independientes (quizás dentro de cuadros de grupo), busque los vínculos de Ayuda en la parte inferior de los grupos.

-   **No use vínculos de temas de Ayuda generales o imprecisos ni botones genéricos de Ayuda.** A menudo, los usuarios omiten la Ayuda genérica.

Para obtener más información y ejemplos, vea [Ayuda de](winenv-help.md).

### <a name="default-values"></a>Valores predeterminados

-   Incluya un botón de confirmación predeterminado en cada cuadro de diálogo.
-   Para los diálogos de preguntas:
    -   **Seleccione la respuesta más segura (para evitar la pérdida de datos o el acceso del sistema), la respuesta más segura será la predeterminada.** Si la seguridad y la seguridad no son factores, seleccione la respuesta más probable o conveniente.
        -   **Excepción:** No haga que una respuesta destructiva sea la predeterminada a menos que haya una manera sencilla y obvia de deshacer el comando.
-   Para los cuadros de diálogo de elección:
    -   Para los valores predeterminados iniciales, seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema) y los valores más **seguros para cada control.** Si la seguridad y la seguridad no son factores, seleccione las opciones más probables o prácticas.
    -   Para los valores predeterminados posteriores, vuelva a seleccionar las opciones seleccionadas anteriormente si es probable que esos valores se repitan y hacerlo **es seguro y seguro.** De lo contrario, seleccione los valores predeterminados iniciales.

![captura de pantalla del cuadro de diálogo de impresión ](images/win-dialog-box-image49.png)

En este ejemplo, es más probable que los usuarios elijan la misma configuración de impresión que la última vez. Sin embargo, es probable que el número de copias deseadas cambie, por lo que esta configuración no se vuelve a elegir.

## <a name="recommended-sizing-and-spacing&quot;></a>Tamaño y espaciado recomendados

-   **Admite la resolución de pantalla mínima de Windows Vista de 800 x 600 píxeles.** Los diseños se pueden optimizar para ventanas de tamaño ajustable mediante una resolución de pantalla de 1024 x 768 píxeles.
-   **Use ventanas de tamaño ajustable siempre que sea práctico para evitar barras de desplazamiento y datos truncados.** Las ventanas con contenido dinámico y listas son las que más se benefician de las ventanas de tamaño ajustable.
-   **Las ventanas de tamaño fijo deben ser totalmente visibles y ajustarse al área de trabajo.**
-   **Las ventanas que se pueden cambiar de tamaño se pueden optimizar para resoluciones más altas, pero se puede cambiar el tamaño según sea necesario en tiempo de presentación a la resolución de pantalla real.**
-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No tenga miedo de usar tamaños de ventana iniciales mayores si puede usar el espacio de forma eficaz.

## <a name=&quot;text&quot;></a>Texto

### <a name=&quot;general&quot;></a>General

-   **Quite el texto redundante.** Busque texto redundante en títulos, instrucciones principales, instrucciones complementarias, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en instrucciones y controles interactivos y quite cualquier redundancia de los demás lugares.
-   **Use expresiones positivas.** Las expresiones positivas son más fáciles de entender para los usuarios.

**Correcto:**

¿Desea habilitar el uso compartido de archivos e impresoras?

**Incorrecto:**

¿Desea deshabilitar el uso compartido de archivos e impresoras?

Sin embargo, las expresiones deben coincidir con el comando asociado, incluso si el comando está con frases negativas; por ejemplo, use disable para confirmar un comando Disable.

-   **Si es necesario, use la palabra &quot;ventana&quot; para hacer referencia al propio cuadro de diálogo.**
-   **Use la segunda persona (&quot;usted/su")** para decir a los usuarios qué hacer en el área principal de instrucción y contenido. A menudo, la segunda persona está implícita.

**Ejemplos:**

Elija las imágenes que desea imprimir.

Elija una cuenta.

-   **Use la primera persona ("I/me/my")** para permitir que los usuarios digan al programa qué hacer en los controles del área de contenido que responden a la instrucción principal.

**Ejemplo:** Imprima las fotos en mi cámara.

### <a name="dialog-box-titles"></a>Títulos del cuadro de diálogo

-   **Use el título para identificar el comando, la característica o el programa de donde provenía un cuadro de diálogo.**
    -   Si el usuario inicia el cuadro de diálogo, puede identificarlo con el nombre de la característica o el comando. **Excepciones:**
        -   Si muchos comandos diferentes muestran un cuadro de diálogo, considere la posibilidad de usar el nombre del programa en su lugar.
        -   Si ese título sería redundante con la instrucción principal, use el nombre del programa en su lugar.
    -   Si se ha iniciado el programa o el sistema (y, por lo tanto, está fuera de contexto), debe identificarlo mediante el nombre del programa o la característica para dar contexto.
    -   No use el título para explicar qué hacer en el cuadro de diálogo que es el propósito de la instrucción principal.
-   Use el nombre exacto del comando para los nombres basados en comandos, pero no incluya los puntos suspensivos si los hay. Puede incluir el título del menú del comando si es necesario para crear un buen título. Ejemplo: para un objeto... En un menú Insertar, use el título Insertar objeto.
-   **Si aparece un cuadro de diálogo** de modelado en la barra de tareas, optimice el título para mostrarlo en la barra de tareas colocando primero la información distintiva de forma concisa. Ejemplos: "66 % completado" y "3 recordatorios".
-   **No incluya las palabras "dialog" o "progress" en el título.** Esto está implícito y dejarla desactivada facilita el examen de los usuarios.
-   Use [el uso de mayúsculas de estilo de](glossary.md)título, sin finalizar los signos de puntuación.

### <a name="main-instructions"></a>Instrucciones principales

-   **Use la instrucción principal para explicar concisamente qué hacer en el cuadro de diálogo.** La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. Las instrucciones correctas comunican el objetivo del usuario con el diálogo en lugar de centrarse exclusivamente en la mecánica de su manipulación.
-   **Omita la instrucción principal cuando lo único que puede decir sea obvio.** En tales casos, el contenido del cuadro de diálogo se explica por sí mismo. Por ejemplo, los cuadros de diálogo comunes Abrir archivo y Guardar archivos no necesitan una instrucción principal porque su contexto y diseño hacen que su propósito sea obvio.
-   **Omita las etiquetas de control que vuelvan a restablecer la instrucción principal.** En este caso, la instrucción principal toma la clave de acceso.

**Aceptable:**

![captura de pantalla del cuadro de texto con etiqueta redundante ](images/win-dialog-box-image50.png)

En este ejemplo, la etiqueta del cuadro de texto es simplemente una nueva instrucción de la instrucción principal.

**Mejor:**

![captura de pantalla del mismo cuadro de texto con una etiqueta ](images/win-dialog-box-image51.png)

En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma la clave de acceso.

-   **Sea conciso y use solo una sola oración completa.** Pare la instrucción principal hasta la información esencial. Si tiene que explicar algo más, use instrucciones complementarias.
-   **Use verbos específicos siempre que sea posible.** Los verbos específicos (ejemplos: conectar, guardar, instalar) son más significativos para los usuarios que los genéricos (ejemplos: configurar, administrar, establecer).
-   Use [mayúsculas de estilo oración.](glossary.md)
-   **No incluya períodos finales si la instrucción es una instrucción .** Si la instrucción es una pregunta, incluya un signo de interrogación final.
-   **En el caso de los diálogos de progreso, use** una frase de error que explique brevemente la operación en curso y termine con puntos suspensivos. Ejemplo: Imprimir las imágenes...
-   **Sugerencia:** Puede evaluar una instrucción principal mediante la lectura de lo que podría decir a un amigo. Si responder con la instrucción principal sería poco natural, poco útil o difícil, vuelva a trabajar la instrucción.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **Cuando sea necesario, use una instrucción complementaria opcional para presentar información adicional útil para comprender o usar la página.** Puede proporcionar información más detallada y definir terminología.
-   **Si la apariencia del cuadro de diálogo está iniciada por el programa o el sistema (y, por tanto, fuera de contexto), use la instrucción complementaria para explicar por qué ha aparecido el diálogo.** Para estos diálogos, el contexto no suele ser obvio.
-   **No repita la instrucción principal con una redacción ligeramente diferente.** En su lugar, omita la instrucción complementaria si no hay más que agregar.
-   Use oraciones completas, mayúsculas de estilo oración y signos de puntuación finales.

### <a name="command-links"></a>Vínculos de comandos

-   **Elija texto de vínculo conciso que comunique claramente y diferencie lo que hace el vínculo de comando.** Debe ser autoexplicativo y corresponder a la instrucción principal. Los usuarios no deben tener que averiguar qué significa realmente el vínculo ni cómo difiere de otros vínculos.
-   **Inicie siempre los vínculos de comando con un verbo.**
-   Use mayúsculas de estilo de frase.
-   No uses puntuación final.
-   **Si es necesario, proporcione una explicación adicional mediante oraciones completas y signos de puntuación finales.** Sin embargo, agregue estas explicaciones solo cuando sea necesario no agregue explicaciones a todos los vínculos de comandos solo porque un vínculo de comando necesita uno.

Para obtener más información y ejemplos, vea [Instrucciones de vínculo de](ctrl-command-links.md) comandos.

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use etiquetas de botón de confirmación específicas que tienen sentido por sí solas y son una respuesta a la instrucción principal.** Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta. Es mucho más probable que los usuarios lean las etiquetas de los botones de comando que el texto estático.
-   **Inicie las etiquetas de botón de confirmación con un verbo. Las excepciones son Ok, Yes y No.**
-   Use mayúsculas de estilo de frase.
-   No uses puntuación final.
-   Asigne una clave [de acceso única.](glossary.md)
    -   **Excepción:** No asigne claves de acceso a los botones Aceptar y Cancelar porque Enter y Esc son sus claves de acceso. Esto facilita la asignación de las demás claves de acceso.

## <a name="documentation"></a>Documentación

Al hacer referencia a cuadros de diálogo:

-   En programación y otra documentación técnica, consulte los cuadros de diálogo como cuadros de diálogo. En cualquier otro lugar, consulte los cuadros de diálogo por su título. Si la barra de título está oculta, consulte el cuadro de diálogo con la instrucción principal.
-   Si debe hacer referencia a un cuadro de diálogo en general, use la ventana de la documentación del usuario. Puede hacer referencia a un cuadro de diálogo de pregunta simple o a una confirmación como un mensaje.
-   Use el título exacto o el texto de la instrucción principal, incluida su mayúscula.
-   Cuando sea posible, formatee el título con texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Ejemplo: **en** Seguridad de Windows , haga clic **en Más opciones**.

