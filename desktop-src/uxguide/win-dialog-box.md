---
title: Cuadros de diálogo (conceptos básicos del diseño)
description: Un cuadro de diálogo es una ventana secundaria que permite a los usuarios realizar un comando, preguntar a los usuarios o proporcionar información sobre el progreso o los usuarios.
ms.assetid: 2ded9f30-d45f-4027-a85d-4e7d0e412793
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0db9d705cb697cdad9ed29dad86faf5f96665dd5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104561903"
---
# <a name="dialog-boxes-design-basics"></a>Cuadros de diálogo (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Un cuadro de diálogo es una ventana secundaria que permite a los usuarios realizar un comando, preguntar a los usuarios o proporcionar información sobre el progreso o los usuarios.

![captura de pantalla que identifica los elementos del cuadro de diálogo ](images/win-dialog-box-image1.png)

Cuadro de diálogo típico.

Los cuadros de diálogo se componen de una barra de título (para identificar el comando, la característica o el programa desde el que procede un cuadro de diálogo), una instrucción principal opcional (para explicar el objetivo del usuario con el cuadro de diálogo), varios controles del área de contenido (para presentar opciones) y botones de confirmación (para indicar cómo el usuario desea confirmar la tarea).

Los cuadros de diálogo tienen dos tipos fundamentales:

-   Los **cuadros de diálogo modales** requieren que los usuarios se completen y cierren antes de continuar con la ventana propietaria. Estos cuadros de diálogo son los más adecuados para las tareas de uso único críticas o poco frecuentes que requieren la finalización antes de continuar.
-   Los **cuadros de diálogo no modales** permiten a los usuarios cambiar entre el cuadro de diálogo y la ventana propietaria según sea necesario. Estos cuadros de diálogo se usan mejor para tareas frecuentes, repetitivas y continuadas.

**Un cuadro de diálogo de tarea es un cuadro de diálogo implementado mediante la interfaz de programación de aplicaciones (API) de cuadros de diálogo de tarea.** Se componen de las siguientes partes, que se pueden ensamblar en una variedad de combinaciones:

-   Una **barra de título** para identificar la aplicación o la característica del sistema de la que procede el cuadro de diálogo.
-   Una **instrucción principal**, con un icono opcional, para identificar el objetivo del usuario con el cuadro de diálogo.
-   **Área de contenido** para la información y los controles descriptivos.
-   Un **área de comandos** para botones de confirmación, incluido un botón Cancelar, y opciones más opcionales y no mostrar esta <item> los controles de nuevo.
-   Un **área de notas al pie** para obtener más explicaciones y ayuda opcionales, que normalmente se dirige a los usuarios menos experimentados.

![captura de pantalla de una tarea típica (cuadro de diálogo) ](images/win-dialog-box-image2.png)

Cuadro de diálogo de tarea típico.

**Los cuadros de diálogo de tarea se recomiendan siempre que sea adecuado, ya que son fáciles de crear y logran un aspecto coherente.** Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Microsoft Windows.

Un panel de tareas es como un cuadro de diálogo, salvo que se presenta en un panel de ventana en lugar de en una ventana independiente. Como resultado, los paneles de tareas tienen una sensación más directa y contextual que los cuadros de diálogo. Aunque técnicamente no son iguales, los **paneles de tareas son tan similares a los cuadros de diálogo que se presentan en este artículo**.

![captura de pantalla de un panel de tareas típico ](images/win-dialog-box-image3.png)

Un panel de tareas típico.

Las [ventanas de propiedades](win-property-win.md) son un tipo especializado de cuadro de diálogo que se usa para ver y cambiar las propiedades de un objeto, una colección de objetos o un programa. Además, las ventanas de propiedades suelen admitir varias tareas, mientras que los cuadros de diálogo normalmente admiten una sola tarea o paso en una tarea. Dado que su uso está especializado, las **ventanas de propiedades se describen en otro conjunto de instrucciones**.

Los cuadros de diálogo pueden tener [pestañas](ctrl-tabs.md)y, si es así, se les llama cuadros de diálogo con pestañas. Las ventanas de propiedades se determinan por su presentación de propiedades, no por el uso de pestañas.

**Nota:** Las instrucciones relacionadas con el [diseño](vis-layout.md), la [Administración de ventanas](win-window-mgt.md), los cuadros de diálogo comunes, las [ventanas de propiedades](win-property-win.md), los [asistentes](win-wizards.md), las [confirmaciones](mess-confirm.md), [los mensajes de error](mess-error.md)y [los mensajes de advertencia](mess-warn.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidirte, intenta responder a estas preguntas:

-   **¿Es el propósito de proporcionar información a los usuarios, formular una pregunta a los usuarios o permitir que los usuarios seleccionen opciones para realizar un comando o una tarea?** Si no es así, use otra interfaz de usuario (UI).
-   **¿Es el propósito de ver y cambiar las propiedades de un objeto, una colección de objetos o un programa?** Si es así, use una [ventana de propiedades](win-property-win.md) o una barra de [herramientas](cmd-toolbars.md) en su lugar.
-   **¿Es el propósito de presentar una colección de comandos o herramientas?** Si es así, utilice una barra de herramientas o una [ventana de paleta](glossary.md).
-   **¿Es el propósito de comprobar que el usuario desea continuar con una acción?** ¿Hay alguna razón clara de no continuar y una posibilidad razonable de que a veces los usuarios no? Si es así, use una [confirmación](mess-confirm.md).
-   **¿Es el propósito de proporcionar un mensaje de error o de advertencia?** Si es así, use un [mensaje de error](mess-error.md) o de [ADVERTENCIA](mess-warn.md).
-   Es el propósito de:
    -   Abrir archivos
    -   Guardar archivos
    -   Abrir carpetas
    -   Buscar o reemplazar texto
    -   Imprimir un documento
    -   Seleccionar atributos de una página impresa
    -   Seleccionar una fuente
    -   Elegir un color
    -   Buscar un archivo, una carpeta, un equipo o una impresora
    -   Buscar usuarios, equipos o grupos en Microsoft Active Directory
    -   ¿Solicitar un nombre de usuario y una contraseña?

Si es así, use en su lugar el [cuadro de diálogo común](win-common-dlg.md) adecuado. Muchos de estos cuadros de diálogo comunes son extensibles.

-   **¿Es el propósito de realizar una tarea con varios pasos que requiere más de una sola ventana?** En ese caso, utilice un [flujo de tareas](glossary.md) o un [Asistente](win-wizards.md) en su lugar.
-   **¿El propósito es informar a los usuarios de un evento del sistema o de un programa que no está relacionado con la actividad del usuario actual, que no requiere la intervención inmediata del usuario y que los usuarios pueden ignorar libremente?** Si es así, use una [notificación](mess-notif.md) en su lugar.
-   **¿Es el propósito de mostrar el estado del programa?** En ese caso, utilice una [barra de estado](ctrl-status-bars.md) en su lugar.
-   **¿Sería preferible usar la interfaz de usuario en contexto?** Los cuadros de diálogo pueden interrumpir el flujo del usuario exigiendo atención. A veces se justifica la interrupción en el flujo, como cuando el usuario debe realizar una acción que está fuera del contexto actual. En otros casos, un enfoque mejor es presentar la interfaz de usuario en contexto, ya sea directamente con la interfaz de usuario en contexto (por ejemplo, un panel de tareas) o a petición mediante una [divulgación progresiva](ctrl-progressive-disclosure-controls.md).
-   **¿Es el propósito de mostrar un problema de entrada de usuario no crítico o una condición especial?** Si es así, use un [globo](ctrl-balloons.md) en su lugar.
-   **En el caso de los flujos de tareas, ¿sería preferible usar otra página?** Por lo general, desea que una tarea fluya de una página a una en una sola ventana. Use los cuadros de diálogo para confirmar comandos en contexto, para obtener entradas para comandos en contexto y para realizar tareas secundarias independientes que se realizan mejor de forma independiente y fuera del flujo de tareas principal.
-   **Para seleccionar opciones, ¿es probable que los usuarios cambien las opciones?** Si no es así, considere alternativas, como:
    -   Usar las opciones predeterminadas sin preguntar, pero permitir que los usuarios realicen cambios más tarde.
    -   Proporcionar una versión con opciones (por ejemplo, **Imprimir...** en un menú), así como una versión sin opciones (por ejemplo, **Imprimir** en la barra de herramientas). Por lo general, los comandos de la barra de herramientas deberían ser inmediatos y evitar mostrar cuadros de diálogo.
-   **Para seleccionar opciones, ¿hay una forma más sencilla y directa de presentar las opciones?** Si es así, considere alternativas, como:
    -   Usar un [botón de expansión](ctrl-command-buttons.md) para seleccionar variaciones de un comando.
    -   Usar un submenú para comandos, casillas, botones de radio y listas simples.

![Captura de pantalla que muestra un menú y un submenú.](images/win-dialog-box-image4.png)

![captura de pantalla de un menú y submenú ](images/win-dialog-box-image5.png)

En estos ejemplos, se usan submenús en lugar de cuadros de diálogo para selecciones simples.

## <a name="design-concepts"></a>Conceptos de diseño

Cuando se usan correctamente, los cuadros de diálogo son una excelente manera de proporcionar eficacia y flexibilidad al programa. Cuando se usan indirectamente, los cuadros de diálogo son una forma sencilla de molestar a los usuarios, interrumpir su flujo y hacer que el programa se sienta indirecto y tedioso. **Los cuadros de diálogo modales requieren la atención de los usuarios.** Los cuadros de diálogo suelen ser más fáciles de implementar que las interfaces de usuario alternativas, por lo que tienden a estar sobreutilizados.

**Un cuadro de diálogo es más eficaz cuando sus características de diseño coinciden con su uso.** El diseño de un cuadro de diálogo está determinado en gran medida por su finalidad (para ofrecer opciones, formular preguntas, proporcionar información o comentarios), tipo (modal o no modal) e interacción del usuario (requerido, respuesta opcional o confirmación), mientras que su uso está determinado en gran medida por su contexto (usuario o programa iniciado), probabilidad de acción del usuario y frecuencia de presentación.

Para diseñar cuadros de diálogo efectivos, utilice los siguientes elementos de manera eficaz:

-   Texto del cuadro de diálogo
-   Instrucciones principales
-   No mostrar esta <item> opción de nuevo

**Si solo hace algo...**

Asegúrese de que el diseño del cuadro de diálogo (determinado por su finalidad, tipo e interacción con el usuario) coincida con su uso (determinado por su contexto, probabilidad de acción del usuario y frecuencia de presentación).

## <a name="usage-patterns"></a>Patrones de uso

Los cuadros de diálogo tienen varios patrones de uso:

-   Los cuadros de diálogo de preguntas (con botones) solicitan a los usuarios una sola pregunta o confirman un comando, y usan respuestas simples en los botones de comando dispuestos horizontalmente.
-   Los cuadros de diálogo de preguntas (mediante vínculos de comandos) solicitan a los usuarios una sola pregunta o seleccionan la tarea que se va a realizar y usan respuestas detalladas en los vínculos de comandos organizados verticalmente.
-   Los cuadros de diálogo de elección presentan a los usuarios un conjunto de opciones, normalmente para especificar un comando más completamente. A diferencia de los cuadros de diálogo de preguntas, los cuadros de diálogo de elección pueden plantear varias preguntas.
-   Los cuadros de diálogo de progreso muestran los usuarios con comentarios de progreso durante una operación larga (más de cinco segundos), junto con un comando para cancelar o detener la operación.
-   Los cuadros de diálogo informativos muestran información solicitada por el usuario.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No use cuadros de diálogo desplazables.** No use cuadros de diálogo que requieran el uso de una barra de desplazamiento para verla completamente durante el uso normal. En su lugar, rediseñe el cuadro de diálogo. Considere la posibilidad de usar [divulgación progresiva](ctrl-progressive-disclosure-controls.md) o [pestañas](ctrl-tabs.md).
-   **No tener una barra de menús o una barra de estado.** En su lugar, proporcione acceso a los comandos y al estado directamente en el propio cuadro de diálogo o mediante los menús contextuales de los controles pertinentes.

    -   **Excepción:** Las barras de menús son aceptables cuando se usa un cuadro de diálogo para implementar una ventana principal (por ejemplo, una utilidad).

    **Incorrecto:**

    ![captura de pantalla de un cuadro de diálogo con una barra de menús ](images/win-dialog-box-image6.png)

    En este ejemplo, buscar certificados es un cuadro de diálogo no modal con una barra de menús.

-   Si un cuadro de diálogo requiere atención inmediata y el programa no está activo, parpadee el botón de la **barra de tareas tres veces para atraer la atención y déjelo resaltado.** No haga nada más: no restaure ni active la ventana y no reproduzca efectos sonoros. En su lugar, respete la selección del estado de la ventana del usuario y deje que el usuario Active la ventana cuando esté listo.
-   Para obtener más instrucciones y ejemplos, vea [barra de tareas](winenv-taskbar.md).

### <a name="modal-dialog-boxes"></a>Cuadros de diálogo modales

-   **Use para tareas de uso único críticas o poco frecuentes que requieran la finalización antes de continuar.**
-   Use un [modelo de confirmación diferida](glossary.md) para que los cambios no surtan efecto hasta que se confirmen explícitamente.
-   **Implemente mediante un cuadro de diálogo de tarea siempre que sea adecuado para lograr una apariencia coherente.** Los cuadros de diálogo de tareas requieren Windows Vista o posterior, por lo que no son adecuados para versiones anteriores de Windows.

### <a name="modeless-dialog-boxes"></a>Cuadros de diálogo no modales

-   **Se usa para tareas frecuentes, repetitivas y continuas.**
-   Use un [modelo de confirmación inmediata](glossary.md) para que los cambios surtan efecto inmediatamente.
-   En los cuadros de diálogo no modales, use un botón de comando cerrar explícito en el cuadro de diálogo para cerrar la ventana. En ambos, use un botón cerrar en la barra de título para cerrar la ventana.
-   **Considere la posibilidad de crear cuadros de diálogo no modales acoplables.** Los cuadros de diálogo no modales acoplables permiten una ubicación más flexible.

![captura de pantalla de un cuadro de diálogo acoplable y no modal ](images/win-dialog-box-image7.png)

Algunos cuadros de diálogo no modales usados en Microsoft Office son acoplables.

### <a name="multiple-dialog-boxes"></a>Varios cuadros de diálogo

-   **No mostrar más de un cuadro de diálogo de opción en propiedad a la vez desde un cuadro de diálogo de elección del propietario.** Si se muestra más de una, el significado de los botones de confirmación resulta difícil para que los usuarios lo sepan. Puede mostrar otros tipos de cuadros de diálogo (como cuadros de diálogo de preguntas) según sea necesario.
-   **En el caso de una secuencia de cuadros de diálogo relacionados, considere la posibilidad de usar un cuadro de diálogo de varias páginas si es posible.** Use cuadros de diálogo individuales si no están claramente relacionados.

### <a name="multi-page-dialog-boxes"></a>Cuadros de diálogo de varias páginas

-   Use un cuadro de diálogo de varias páginas en lugar de cuadros de diálogo individuales si tiene la siguiente secuencia de páginas relacionadas:
    -   Una sola página de entrada (opcional)
    -   Página de progreso
    -   Una sola página de resultados

La página de entrada es opcional porque es posible que se haya iniciado la tarea en otro lugar. **Esto proporciona a la experiencia resultante una sensación estable, simple y ligera.**

![captura de pantalla de una barra de progreso ](images/win-dialog-box-image8.png)

![captura de pantalla del mensaje "no se encontraron problemas" ](images/win-dialog-box-image9.png)

En este ejemplo, diagnósticos de red de Windows consta de páginas de progreso y resultados.

-   **No use un cuadro de diálogo de varias páginas si la página de entrada es un cuadro de diálogo estándar.** En este caso, es más importante la coherencia del uso de un cuadro de diálogo estándar.
-   **No use los botones siguiente o atrás y no tenga más de tres páginas.** Los cuadros de diálogo de varias páginas son para tareas de un solo paso con comentarios. No son [asistentes](win-wizards.md), que se usan para tareas de varios pasos. Los asistentes tienen una sensación intensa e indirecta en comparación con los cuadros de diálogo de varias páginas.
-   **En la página entrada, use botones de comando específicos o vínculos de comandos para iniciar la tarea.**
-   **Use un botón Cancelar en las páginas de entrada y progreso, y un botón cerrar en la página resultados.**

**Desarrolladores:** Puede crear cuadros de diálogo de tareas de varias páginas mediante el mensaje de [ \_ \_ Página de navegación TDM](../controls/tdm-navigate-page.md) .

### <a name="presentation"></a>Presentación

Para facilitar la búsqueda y el acceso a los cuadros de diálogo, asocie claramente el cuadro de diálogo a su origen y trabaje bien con varios monitores:

-   **Muestre inicialmente los cuadros de diálogo "centrados" en la parte superior de la ventana propietaria.** En el caso de las pantallas posteriores, considere la posibilidad de mostrarla en su última ubicación (relativa a la ventana propietaria) si es probable que sea más conveniente.

![diagrama del cuadro de diálogo centrado en la ventana detrás de él ](images/win-dialog-box-image10.png)

Los cuadros de diálogo se centran inicialmente en la parte superior de la ventana propietaria.

-   **Si un cuadro de diálogo es contextual, mostrarlo cerca del objeto desde el que se inició.** Sin embargo, colóquelo fuera del camino (preferiblemente desplazarse hacia abajo y a la derecha) para que el objeto no esté incluido en el cuadro de diálogo.

![diagrama de desplazamiento hacia abajo y a la derecha del cuadro de diálogo ](images/win-dialog-box-image11.png)

Las propiedades de un objeto se muestran cerca del objeto.

-   **En los cuadros de diálogo no modales, se muestra inicialmente en la parte superior de la ventana propietaria para facilitar su búsqueda.** Si el usuario activa la ventana propietaria, puede ocultar el cuadro de diálogo no modal.
-   **Si es necesario, ajuste la ubicación inicial para que todo el cuadro de diálogo esté visible dentro del monitor de destino.** Si una ventana de tamaño superior es mayor que el monitor de destino, reduzca su tamaño.
-   **Cuando se vuelva a mostrar un cuadro de diálogo, considere la posibilidad de mostrarlo en el mismo estado en el que se ha tenido acceso por última vez.** Al cerrar, guarde el monitor usado, el tamaño de la ventana, la ubicación y el estado (maximizado frente a restauración). Al volver a mostrar, restaure el tamaño, la ubicación y el estado del cuadro de diálogo guardado con el monitor adecuado. Además, considere la posibilidad de hacer que estos atributos persistan entre instancias de programa por usuario.
-   **En el caso de ventanas redimensionables, establezca un tamaño de ventana mínimo si hay un tamaño por debajo del cual ya no se puede usar el contenido.** Considere la posibilidad de modificar la presentación para que el contenido se pueda usar en tamaños menores.

![captura de pantalla de los botones del reproductor de media centrado ](images/win-dialog-box-image12.png)

En este ejemplo, Windows Media Player cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

-   **No use el atributo Top de AlwaysOn.**
    -   **Excepción:** Use solo cuando un cuadro de diálogo implementa una operación esencialmente modal, pero debe suspenderse brevemente para tener acceso a la ventana propietaria. Por ejemplo, al comprobar la ortografía de un documento, los usuarios pueden dejar ocasionalmente el cuadro de diálogo Ortografía y acceder al documento para corregir los errores.

Para obtener más información y ejemplos, vea [Administración de ventanas](win-window-mgt.md).

### <a name="title-bars"></a>Barras de título

-   **Los cuadros de diálogo no tienen iconos de barra de título.** Los iconos de la barra de título se usan como una distinción visual entre las ventanas [principales](glossary.md) y [secundarias](glossary.md).
    -   **Excepción:** Si se usa un cuadro de diálogo para implementar una ventana principal (por ejemplo, una utilidad) y, por tanto, aparece en la barra de tareas, tiene un icono de barra de título. En este caso, para optimizar el título que se va a mostrar en la barra de tareas, coloque primero la información distintiva.
-   **Los cuadros de diálogo siempre tienen un botón Cerrar.** Los cuadros de diálogo no modales también pueden tener un botón minimizar. Los cuadros de diálogo de tamaño variable pueden tener un botón maximizar.
-   **No deshabilite el botón Cerrar.** Tener un botón Cerrar ayuda a los usuarios a permanecer en el control permitiéndoles cerrar las ventanas que no desean.
    -   **Excepción:** En el caso de los cuadros de diálogo de progreso, puede deshabilitar el botón Cerrar si la tarea debe ejecutarse hasta su finalización para lograr un estado válido o evitar la pérdida de datos.
-   **El botón cerrar de la barra de título debe tener el mismo efecto que el botón Cancelar o cerrar** del cuadro de diálogo. Nunca asígnele el mismo efecto que aceptar.
-   Si el título y el icono de la barra de título ya se muestran de forma destacada cerca de la parte superior de la ventana, puede ocultar el título y el icono de la barra de título para evitar la redundancia. Sin embargo, todavía tiene que establecer un título adecuado internamente para su uso por parte de Windows.

### <a name="interaction"></a>Interacción

-   **Cuando se muestra, los cuadros de diálogo iniciados por el usuario siempre deben tomar el foco de entrada.** Los cuadros de diálogo iniciados por el programa no deben tener el foco de entrada porque es posible que el usuario interactúe con otra ventana. Tal interacción errónea en el cuadro de diálogo puede tener consecuencias imprevistas.
-   **Asigne el foco de entrada inicial al control con el que es más probable que los usuarios interactúen primero**, lo que suele ser (pero no siempre) el primer control interactivo. Evite asignar el foco de entrada inicial a un vínculo de ayuda.
-   **En la navegación con el teclado, el orden de tabulación debe fluir en un orden lógico, generalmente de izquierda a derecha, de arriba abajo.** Normalmente, el orden de tabulación sigue el orden de lectura, pero puede realizar estas excepciones:

    -   Coloque los controles que se usan con más frecuencia en el orden de tabulación.
    -   Coloque los vínculos de ayuda en la parte inferior de un cuadro de diálogo, después de los botones de confirmación en el orden de tabulación.

    Al asignar el orden, supongamos que los usuarios muestran cuadros de diálogo para su finalidad prevista; por lo tanto, por ejemplo, los usuarios muestran cuadros de diálogo de opciones para hacer elecciones, no revisar y hacer clic en Cancelar.

-   **Al presionar la tecla ESC, siempre se cierra un cuadro de diálogo activo.** Esto se aplica a los cuadros de diálogo con cancelar o cerrar, e incluso si se ha cambiado el nombre de la cancelación a cerrado porque los resultados ya no se pueden deshacer.

**Claves de acceso**

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o a sus etiquetas.** Los [cuadros de texto de solo lectura](ctrl-text-boxes.md) son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto) para que se beneficien de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones aceptar, cancelar y cerrar.** ENTER y ESC se usan para sus claves de acceso. Sin embargo, asigne siempre una tecla de acceso a un control que signifique aceptar o cancelar, pero que tenga una etiqueta diferente.

        ![captura de pantalla del cuadro de diálogo Eliminar archivo ](images/win-dialog-box-image13.png)

        En este ejemplo, el botón confirmación positivo tiene asignada una clave de acceso.

    -   **Etiquetas de grupo.** Normalmente, los controles individuales dentro de un grupo tienen asignadas claves de acceso, por lo que la etiqueta de grupo no necesita una. Sin embargo, si hay una escasez de claves de acceso, asigne una clave de acceso a la etiqueta del grupo y no a los controles individuales.
    -   **Botones de ayuda genéricos,** a los que se tiene acceso con F1.
    -   **Etiquetas de vínculo.** A menudo hay demasiados vínculos para asignar claves de acceso únicas y los guiones bajos que se usan a menudo para indicar que los vínculos ocultan los guiones bajos de la tecla de acceso. En su lugar, tiene acceso a los vínculos con la tecla TAB.
    -   **Nombres de pestaña.** Las pestañas se recorren con Ctrl + Tab y Ctrl + Mayús + Tab.
    -   **Botones examinar etiquetados como "...".** No se puede asignar a estos botones de exploración de forma exclusiva.
    -   **Controles sin etiqueta,** como controles de número, botones de comando gráficos y controles de divulgación progresiva sin etiquetar.
    -   **Etiquetas o texto estático sin etiqueta para los controles que no son interactivos,** como las barras de progreso.

-   **Siempre que sea posible, asigne claves de acceso para comandos de uso frecuente según las asignaciones de teclas de acceso estándar**. Aunque las asignaciones de claves de acceso coherentes no siempre son posibles, se prefieren especialmente en los cuadros de diálogo que se usan con frecuencia.
-   **Asigne las claves de acceso del botón confirmar primero para asegurarse de que tienen las asignaciones de clave estándar.** Si no hay ninguna asignación de clave estándar, utilice la primera letra de la primera palabra. Por ejemplo, la tecla de acceso para los botones sí y no confirmar siempre debe ser "Y" y "N", independientemente de los otros controles del cuadro de diálogo.
-   Para facilitar la búsqueda de las **claves de acceso, asigne las teclas de acceso a un carácter que aparece al principio de la etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.
-   **Prefiere caracteres con ancho ancho,** como w, m y mayúsculas.
-   **Prefiere una consonante distintiva o una vocal,** como "x" en la salida.
-   **Evite el uso de caracteres que hagan que el subrayado sea difícil de ver,** como (desde la mayoría de los problemas a los menos problemáticos):
    -   Letras que solo tienen un píxel de ancho, como i y l.
    -   Letras con descendentes, como g, j, p, q e y.
    -   Letras situadas junto a una letra con un descendiente.

Para obtener más instrucciones y ejemplos, consulte [teclado](inter-keyboard.md).

### <a name="progress-dialogs"></a>Cuadros de diálogo de progreso

En el caso de las tareas de ejecución prolongada, **Supongamos que los usuarios realizarán otra acción mientras se completa la tarea**. Diseñe la tarea para que se ejecute en modo desatendido.

-   **Presente el cuadro de diálogo comentarios de progreso si una operación tarda más de cinco segundos en completarse**, junto con un comando para cancelar o detener la operación.
    -   **Excepción:** En el caso de los asistentes y los flujos de tareas, use un cuadro de diálogo modal para el progreso solo si la tarea permanece en la misma página (en lugar de avanzar hasta otra página) y los usuarios no pueden hacer nada mientras esperan. De lo contrario, use una página de progreso o un progreso en contexto.
-   Si la operación es una tarea de ejecución prolongada (más de 30 segundos) y se puede realizar en segundo plano, use un cuadro de diálogo de progreso no modal para que los usuarios puedan continuar usando el programa mientras esperan.
-   Cuadros de diálogo de progreso no modal:
    -   Tenga un botón minimizar en la barra de título.
    -   Se muestran en la barra de tareas.
-   Implemente los cuadros de diálogo de progreso no modal para que sigan ejecutándose incluso si la ventana propietaria está cerrada.

![captura de pantalla del cuadro de diálogo copiar con barra de progreso ](images/win-dialog-box-image14.png)

En este ejemplo, la copia del archivo continúa incluso si se cierra la ventana propietaria.

-   **Proporcione un botón de comando para detener la operación si se tardan más de unos segundos en completarse, o si tiene la posibilidad de que nunca se complete.** Etiquete el botón Cancelar si la cancelación devuelve el entorno a su estado anterior (sin dejar efectos secundarios). de lo contrario, etiquete el botón detener para indicar que deja intacta la operación parcialmente completada. Puede cambiar la etiqueta del botón de cancelar para detenerla en medio de la operación, si en algún momento no es posible devolver el entorno a su estado anterior.

![captura de pantalla del cuadro de diálogo con el botón Cancelar ](images/win-dialog-box-image15.png)

En este ejemplo, detener el diagnóstico del problema no tiene ningún efecto secundario.

-   **Proporcione un botón de comando para pausar la operación si tarda más de unos minutos en completarse, y puede dificultar la capacidad de los usuarios para realizar el trabajo.** Al hacerlo, no se obliga al usuario a elegir entre completar la tarea y realizar su trabajo.
-   **Recopile toda la información que pueda antes de iniciar la tarea.**
-   **Si se detectan problemas recuperables, pida a los usuarios que traten todos los problemas detectados al final de la tarea.** Si eso no es práctico, tenga en cuenta que los usuarios tienen problemas a medida que se producen.
-   **No abandone las tareas como resultado de errores recuperables.**

![captura de pantalla del cuadro de diálogo con el botón reintentar ](images/win-dialog-box-image16.png)

En este ejemplo, el explorador de Windows permite a los usuarios continuar con la tarea después de un error recuperable.

-   **Para indicar problemas, desactive la barra de progreso en rojo.**

![captura de pantalla de la barra de progreso y botón volver a intentarlo ](images/win-dialog-box-image17.png)

En este ejemplo, se ha quitado un disco extraíble durante una copia de archivos.

-   **Si los resultados son claramente evidentes para los usuarios, cierre el cuadro de diálogo de progreso automáticamente cuando se complete correctamente.** De lo contrario, use los comentarios solo para notificar problemas:
    -   Para mostrar comentarios sencillos, muestre los comentarios en el cuadro de diálogo de progreso y cambie el botón Cancelar a cerrar.
    -   Para mostrar comentarios detallados, cierre el cuadro de diálogo de progreso y muestre un cuadro de diálogo informativo.

**No use una notificación para los comentarios de finalización.** Use un cuadro de diálogo de progreso o una [notificación de acción correcta](mess-notif.md), pero no ambos.

**Tiempo restante**

-   **Use los siguientes formatos de hora.** Comience con el primero de los siguientes formatos en los que la unidad de tiempo más grande no sea cero y, a continuación, cambie al formato siguiente una vez que la unidad de tiempo más grande sea cero.

**Para barras de progreso:**

**Si la información relacionada se muestra en un formato de dos puntos:**

Tiempo restante: h horas, m minutos

Tiempo restante: m minutos, s segundos

Tiempo restante: s segundos

**Si el espacio de la pantalla es Premium:**

horas h, m min.

m min, s segundos restantes

s segundos restantes

**Casos**

h horas, m minutos restantes

m minutos, s segundos restantes

s segundos restantes

**Para las barras de título:**

HH: mm restantes

mm: SS restante

0: SS restante

Este formato compacto muestra la información más importante en primer lugar para que no se trunque en la barra de tareas.

-   **Realizar estimaciones precisas, pero no proporcionar una precisión falsa.** Si la unidad más grande es horas, dé unos minutos (si es significativo) pero no los segundos.

**Incorrecto:**

HH horas, mm minutos, SS segundos

-   **Mantenga la estimación actualizada.** Las estimaciones restantes de tiempo de actualización al menos cada 5 segundos.
-   **Céntrese en el tiempo restante** , ya que es la información que los usuarios más le interesan. Proporcione el tiempo total transcurrido solo cuando haya escenarios en los que el tiempo transcurrido sea útil (por ejemplo, cuando sea probable que se repita la tarea). Si la estimación de tiempo restante está asociada a una barra de progreso, no hay ningún texto de porcentaje completo porque esa información se transmite por la barra de progreso.
-   **Ser gramaticalmente correcto.** Use unidades singulares cuando el número sea uno.

**Incorrecto:**

1 minutos, 1 segundo

-   **Use mayúsculas de estilo de frase.**

Para obtener más información y ejemplos, vea [barras de progreso](progress-bars.md).

### <a name="icons-and-graphics"></a>Iconos y gráficos

**Elementos gráficos**

-   **No use gráficos de gran tamaño que no sirvan de nada más allá de llenar el espacio con golosinas.** En su lugar, conserve la apariencia simple.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con un gráfico grande ](images/win-dialog-box-image18.png)

En este ejemplo, el gráfico grande no sirve para ningún propósito.

**Iconos de la barra de título**

-   **Los cuadros de diálogo no tienen iconos de barra de título.**
    -   **Excepción:** Si se usa un cuadro de diálogo para implementar una ventana principal (por ejemplo, una utilidad) y, por tanto, aparece en la barra de tareas, tiene un icono de barra de título.

**Iconos de cuerpo**

-   **Elija el icono de cuerpo en función del patrón de diseño:**



|                                      |                                                                                                                            |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Patrón**<br/>               | **Icono de cuerpo**<br/>                                                                                                   |
| **Cuadros de diálogo de preguntas**<br/>      | Programa, característica, objeto, icono de advertencia (si la pérdida potencial de datos o acceso al sistema), advertencia de seguridad o ninguno.<br/> |
| **Cuadros de diálogo de elección**<br/>        | Ninguno.<br/>                                                                                                           |
| **Cuadros de diálogo de progreso**<br/>      | Ninguno (pero puede tener una animación).<br/>                                                                               |
| **Cuadros de diálogo informativos**<br/> | Ninguno.<br/>                                                                                                           |



 

-   **Incorrecto:**

![captura de pantalla del cuadro de diálogo con el icono de advertencia ](images/win-dialog-box-image19.png)

En este ejemplo, un icono de advertencia se usa incorrectamente para una pregunta que no implica la pérdida potencial de datos o el acceso al sistema.

- **Considere la posibilidad de usar iconos para ayudar a los usuarios a reconocer visualmente las características de su programa.** Esta técnica es más eficaz cuando los iconos se pueden reconocer y usar fácilmente en varias ubicaciones dentro de su programa.

![captura de pantalla del cuadro de diálogo favoritos con icono de estrella ](images/win-dialog-box-image20.png)

En este ejemplo, el icono de estrella amarilla representa los favoritos. El icono es fácilmente reconocible y se utiliza de forma coherente en todas las ventanas para representar los favoritos.

-   **Use iconos para ayudar a los usuarios a reconocer el objeto en cuestión.**

![captura de pantalla del cuadro de diálogo con el icono de PowerPoint ](images/win-dialog-box-image21.png)

En este ejemplo, el icono del objeto ayuda a los usuarios a reconocer el tipo de archivo que se va a abrir o guardar.

-   **Considere la posibilidad de usar iconos para facilitar la explicación de las características.**

![imágenes de flechas que muestran cómo colocar el monitor ](images/win-dialog-box-image22.png)

En este ejemplo, estos iconos ayudan a los usuarios a visualizar el efecto de sus características.

-   **Use un icono en los cuadros de diálogo de cuadro acerca de la personalización de marca de la aplicación.**

![captura de pantalla del cuadro de diálogo acerca de con el logotipo de Windows ](images/win-dialog-box-image23.png)

En este ejemplo, se usa un mapa de bits en el cuadro acerca de para identificar y personalizar la aplicación.

**Iconos de nota al pie**

-   **Si tiene una nota al pie, considere la posibilidad de usar un icono de nota al pie para resumir el asunto de la nota al pie.**

![captura de pantalla del cuadro de diálogo con el icono de nota al pie ](images/win-dialog-box-image24.png)

En este ejemplo, el icono de nota al pie indica que la pregunta tiene implicaciones de seguridad.

-   **No use un icono de nota al pie que repite el icono del cuerpo.**
-   **No use los iconos de error o de información estándar.** Las condiciones de error se deben transmitir a través del icono de cuerpo y las notas a pie siempre son para obtener información, lo que permite que el icono de información sea redundante. Sin embargo, puede usar el icono de advertencia estándar y el escudo de seguridad amarillo para alertar a los usuarios de las consecuencias peligrosas.

Para obtener más información y ejemplos, vea [iconos](vis-icons.md).

### <a name="commit-buttons"></a>Botones de confirmación

**Notas:**

-   Estas instrucciones no se aplican a los cuadros de diálogo de preguntas mediante vínculos de comandos, ya que ese patrón usa vínculos de comandos en lugar de botones.
-   \[Hágalo \] y \[ no \] se requieran respuestas positivas y negativas, respectivamente, a la instrucción principal.

**General**

-   **Elija los botones de confirmación según el modelo de diseño:**

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
    <td><strong>Cuadros de diálogo de preguntas (con botones)</strong><br/></td>
    <td>Uno de los siguientes conjuntos de comandos concisos: sí/no, sí/no/cancelar, [hágalo]/CANCEL, [hágalo]/[no lo haga], [hágalo]/[no lo haga]/CANCEL.<br/></td>
    </tr>
    <tr class="odd">
    <td><strong>Cuadros de diálogo de preguntas (mediante vínculos)</strong><br/></td>
    <td>Cancel (Cancelar)<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Cuadros de diálogo de elección</strong><br/></td>
    <td><ul>
    <li>Cuadros de diálogo modales: aceptar/cancelar o [hacer]/CANCEL</li>
    <li>Cuadros de diálogo no modales: botón cerrar en el cuadro de diálogo y en la barra de título</li>
    <li>Panel de tareas: botón cerrar en la barra de título</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><strong>Cuadros de diálogo de progreso</strong><br/></td>
    <td>Usar cancelar si devuelve el entorno a su estado anterior (no se deja ningún efecto secundario); de lo contrario, utilice STOP.<br/></td>
    </tr>
    <tr class="even">
    <td><strong>Cuadros de diálogo informativos</strong><br/></td>
    <td>Casi.<br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   **Todos los botones de confirmación excepto aplicar dan como resultado el cierre de la ventana de cuadro de diálogo.**
-   **No confirme los botones de confirmación.** Hacerlo innecesariamente puede ser muy molesto. **Excepciones:**

    -   La acción es potencialmente catastrófica.
    -   La acción es claramente incoherente con otras acciones.
    -   Si es incorrecto, la acción puede provocar una pérdida significativa de datos, tiempo o esfuerzo en nombre del usuario.

    Para obtener más instrucciones y ejemplos, consulte [confirmaciones](mess-confirm.md).

-   **No deshabilite los botones de confirmación. Excepciones**
    -   **Si los usuarios deben elevar para realizar un cambio, deshabilite los botones de confirmación positivos hasta que el usuario realice un cambio.** Al hacerlo, se impide que los usuarios Eleven solo para cerrar una ventana, para lo que deben hacer clic en Cancelar.
    -   Para obtener más excepciones, vea [deshabilitar o quitar controles en lugar de asignar mensajes de error](#disabling-or-removing-controls-vs-giving-error-messages).
-   **Alinear a la derecha los botones de confirmación en una única fila en la parte inferior del cuadro de diálogo,** pero encima del área de la nota al pie. Haga esto incluso si hay un solo botón de confirmación (como aceptar).

    **Incorrecto:**

    ![captura de pantalla del mensaje con el botón Aceptar centrado ](images/win-dialog-box-image25.png)

    En este ejemplo, el botón Aceptar no está correctamente centrado.

-   **Presente los botones de confirmación en el orden siguiente:**
    1.  Aceptar o \[ hacerlo \] /yes
    2.  \[No lo haga \] /no
    3.  Cancelar
    4.  Aplicar (si existe)
    5.  Ayuda (si existe)
-   **Si tiene muchos botones de confirmación relacionados, consolidelos con los botones de expansión**.
-   **Tenga una separación clara de los botones de confirmación (que cierran la ventana) y de todos los demás botones de comando (como avanzado).**

**Responder a las instrucciones principales**

-   **Use botones de confirmación positivos que son respuestas específicas a la instrucción principal, en lugar de etiquetas genéricas como aceptar o sí/no.** Los usuarios deben poder comprender las opciones leyendo solo el texto del botón. **Excepciones:**
    -   Use cerrar para los cuadros de diálogo que no tienen configuración, como los cuadros de diálogo informativos. No use nunca cerrar para los cuadros de diálogo que tienen configuración.
    -   Use aceptar cuando las respuestas "específicas" sigan siendo genéricas, como guardar, seleccionar o elegir. Use aceptar cuando cambie una configuración específica o una colección de valores de configuración.
    -   **En el caso de los cuadros de diálogo heredados sin una instrucción principal, puede usar etiquetas genéricas como aceptar.** A menudo, estos cuadros de diálogo no están diseñados para realizar una tarea específica, lo que impide respuestas más específicas.
    -   Ciertas tareas requieren más pensamiento y una lectura cuidadosa para que los usuarios tomen decisiones informadas. Esto suele ser el caso de las [confirmaciones](mess-confirm.md). **En tales casos, puede usar de forma intencionada etiquetas de botón de confirmación genéricas para obligar a los usuarios a leer las instrucciones principales y evitar las decisiones de prisa.**

        **Correcto:**

        ![captura de pantalla del mensaje con los botones sí y no](images/win-dialog-box-image26.png)

        En este ejemplo, el uso de botones de confirmación sí/no obliga a los usuarios a leer la instrucción principal al menos.

-   **Como alternativa, puede Agregar la palabra "de todos modos" a la etiqueta del botón de confirmación positiva para indicar que el cuadro de diálogo presenta un motivo para no continuar** y que los usuarios deberían leer el cuadro de diálogo detenidamente antes de continuar.

    **Correcto:**

    ![captura de pantalla del mensaje y desinstalación de cualquier botón ](images/win-dialog-box-image27.png)

    En este ejemplo, se agrega "de todos modos" a la etiqueta del botón de confirmación para indicar que los usuarios deben continuar cuidadosamente.

-   **Use cancelar o cerrar para los botones de confirmación negativos en lugar de respuestas específicas a la instrucción principal.** Con bastante frecuencia, los usuarios saben que no quieren realizar una tarea una vez que ven un cuadro de diálogo. Si la cancelación o el cierre se cambiaron de etiqueta a respuestas específicas, los usuarios tendrían que leer atentamente todos los botones de confirmación para determinar cómo cancelar. **La etiqueta de cancelación y cierre de forma coherente facilita su búsqueda. Excepciones**
    -   **No use sí/cancelar.** Use siempre sí/no como un par.
    -   **Use una respuesta concreta cuando CANCEL sea ambiguo.**
-   **No asigne etiquetas genéricas a su significado específico con texto en el área de contenido.** En su lugar, use etiquetas de botón de confirmación específicas o un cuadro de diálogo de preguntas con vínculos si las etiquetas son largas.

    **Incorrecto:**

    ![captura de pantalla del mensaje con uso no claro de botones ](images/win-dialog-box-image28.png)

    En este ejemplo, aceptar está asignado para continuar, la cancelación se asigna para permanecer en la página.

**Botones sí y no**

-   **Prefiere respuestas específicas a los botones sí y no.** Aunque no hay ningún problema con el uso de sí y no, las respuestas específicas se pueden entender más rápidamente, lo que da lugar a una toma de decisiones eficaz. Sin embargo, las [confirmaciones](mess-confirm.md) suelen tener botones sí y no para que los usuarios no tengan que realizar [la confirmación antes](mess-confirm.md) de responder.
-   **Use los botones sí y no solo para responder a preguntas sí o no.** La instrucción principal debe expresarse naturalmente como una pregunta sí o no. Nunca use aceptar y Cancelar para responder a preguntas o respuestas.

    **Incorrecto:**

    ![Captura de pantalla que muestra un mensaje con un "OK" para una pregunta sí.](images/win-dialog-box-image29.png)

    **Correcto:**

    ![captura de pantalla del mensaje con sí para la misma pregunta ](images/win-dialog-box-image30.png)

    **Manera**

    ![captura de pantalla del mensaje con la ejecución de la misma pregunta ](images/win-dialog-box-image31.png)

    En estos ejemplos, sí y no son buenas respuestas a sí y sin preguntas, pero las respuestas específicas son incluso mejores.

-   **Considere la formulación de la instrucción principal como una pregunta sí o no si los botones de confirmación con frases específicas se convierten en largos o extraños.** Como alternativa, puede usar vínculos de comandos para respuestas más largas (cinco palabras o más) a la instrucción principal.

    **Incorrecto:**

    ![captura de pantalla del mensaje con etiquetas de botón de palabra ](images/win-dialog-box-image32.png)

    **Correcto:**

    ![captura de pantalla del mensaje con etiquetas de botón sí/no ](images/win-dialog-box-image33.png)

    La formulación específica en el ejemplo incorrecto es demasiado larga, por lo que el ejemplo correcto utiliza yes y no.

-   **No use los botones sí y no si el significado de la respuesta no es claro.** Si es así, use respuestas específicas en su lugar.

**Botones aceptar**

-   **En los cuadros de diálogo modales, al hacer clic en aceptar, se aplican los valores, se realiza la tarea y se cierra la ventana.**
-   **No use los botones Aceptar para responder a preguntas.**
-   **No asigne claves de acceso a correcto, porque ENTER es la tecla de acceso del botón predeterminado.** Esto hace que las demás claves de acceso sean más fáciles de asignar.
-   **Etiquete los botones aceptar correctamente.** El botón Aceptar se debe etiquetar como correcto, no correcto o correcto.
-   **No use los botones Aceptar para errores o advertencias.** Los problemas nunca son correctos. Utilice Close en su lugar.

    **Incorrecto:**

    ![captura de pantalla del mensaje con el botón Aceptar ](images/win-dialog-box-image34.png)

    En este ejemplo, se debe usar Close en lugar de OK.

-   **No use los botones aceptar en los cuadros de diálogo no modales.** En su lugar, los cuadros de diálogo no modales deben usar botones de confirmación específicos de la tarea (por ejemplo, buscar). Sin embargo, algunos cuadros de diálogo no modales solo requieren un botón Cerrar.

**Cancelar botones**

-   **Al hacer clic en cancelar, se abandonan todos los cambios, se cancela la tarea, se cierra la ventana y se devuelve el entorno a su estado anterior, sin dejar ningún efecto secundario.** En el caso de los cuadros de diálogo de elección anidada, al hacer clic en Cancelar en el cuadro de diálogo elección del propietario, también se abandonan los cambios realizados por los cuadros de diálogo de elección.
-   **Proporcione un botón Cancelar para permitir que los usuarios abandonen los cambios explícitamente.** Los cuadros de diálogo necesitan un punto de salida claro. No dependa de que los usuarios busquen el botón cerrar en la barra de título.

    -   **Excepción:** No proporcione un botón Cancelar para los cuadros de diálogo sin configuración. Los botones aceptar y cerrar tienen el mismo efecto que cancelar en este caso.

    **Incorrecto:**

    ![captura de pantalla del mensaje con el botón aceptar únicamente ](images/win-dialog-box-image35.png)

    En este ejemplo, tener solo un botón cerrar en la barra de título hace que aparezca como si los usuarios no tienen una opción.

-   **No use los botones Cancelar para responder a preguntas.**

    **Incorrecto:**

    ![captura de pantalla del mensaje con la respuesta correcta para sí. ](images/win-dialog-box-image36.png)

    En este ejemplo, aceptar y cancelar se usan incorrectamente para responder a una pregunta sí o no.

-   **No asigne claves de acceso para cancelar, porque ESC es la tecla de acceso.** Esto hace que las demás claves de acceso sean más fáciles de asignar.
-   **No utilice los botones cancelar en los cuadros de diálogo no modales.** En su lugar, utilice Close en su lugar.
-   **No deshabilite el botón Cancelar.** Los usuarios siempre deben poder cancelar los cuadros de diálogo.
    -   **Excepción:** Puede deshabilitar el botón Cancelar en un cuadro de diálogo de progreso si hay un período durante el cual la operación no se puede cancelar. Sin embargo, una mejor solución consiste en diseñar dichas operaciones para que siempre se puedan cancelar.

**Botones cerrar**

-   **Use botones cerrar para los cuadros de diálogo no modales, así como cuadros de diálogo modales que no se pueden cancelar.**
-   **Al hacer clic en cerrar, se cierra la ventana del cuadro de diálogo y se dejan los efectos secundarios existentes.** No utilice Done, ya que no es una construcción imperativa. En el caso de los cuadros de diálogo de elección anidada, al hacer clic en cerrar en el cuadro de diálogo elección del propietario se conservan los cambios realizados por los cuadros de diálogo de elección de propiedad.
-   **Coloque un botón Cerrar explícito en el cuerpo del cuadro de diálogo.** Los cuadros de diálogo necesitan un punto de salida claro. No dependa de que los usuarios busquen el botón cerrar en la barra de título.
-   **Asegúrese de que el botón cerrar de la barra de título tiene el mismo efecto que cancelar o cerrar.**
-   **No asigne teclas de acceso a Close, porque ESC es la tecla de acceso.** Esto hace que las demás claves de acceso sean más fáciles de asignar.

**Aplicar botones**

-   **No utilice los botones aplicar en los cuadros de diálogo que no son hojas de propiedades ni paneles de control.** El botón aplicar significa aplicar los cambios pendientes, pero dejar la ventana abierta. Esto permite a los usuarios evaluar los cambios antes de cerrar la ventana. Sin embargo, solo las hojas de propiedades y los paneles de control tienen esta necesidad.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con el botón aplicar ](images/win-dialog-box-image37.png)

    En este ejemplo, un cuadro de diálogo de elección tiene innecesariamente un botón aplicar.

**Botones de confirmación para cuadros de diálogo indirectos**

**Nota:** Los cuadros de diálogo indirectos se muestran fuera del contexto, ya sea como resultado indirecto de una tarea o el resultado de un problema con un sistema o un proceso en segundo plano. Para los cuadros de diálogo indirectos, el botón Cancelar es ambiguo porque podría significar cancelar el cuadro de diálogo o cancelar toda la tarea.

-   **Si los usuarios deben cancelar el cuadro de diálogo y la tarea, dé a los botones de confirmación para hacerlo.** Etiquete el botón que cancela el cuadro de diálogo con una respuesta negativa a la instrucción principal. Etiquete el botón que cancela la tarea completa con cancelar. El uso de CANCEL permite usar el cuadro de diálogo en muchos contextos.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo con guardar/no guardar ](images/win-dialog-box-image38.png)

    En este ejemplo, Windows Paint muestra este cuadro de diálogo como resultado de un comando nuevo o salir cuando el gráfico no se ha guardado. No guardar cierra el cuadro de diálogo sin guardar, mientras que cancelar cancela el comando nuevo o salir.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo con botones sí/no ](images/win-dialog-box-image39.png)

    En este ejemplo, no hay ninguna manera de cancelar la tarea (cerrar la barra de acceso directo de Office) que condujo a mostrar este cuadro de diálogo. Este cuadro de diálogo necesita un botón Cancelar.

-   **Si los usuarios solo necesitan cancelar el cuadro de diálogo pero no la tarea, use un botón con una respuesta negativa y determinada a la instrucción principal** y no tenga un botón Cancelar.

    ![captura de pantalla del cuadro de diálogo con ejecutar/no ejecutar ](images/win-dialog-box-image24.png)

    En este ejemplo, este cuadro de diálogo se muestra indirectamente como resultado de desplazarse a una página web que instala un control ActiveX. El uso de CANCEL sería ambiguo aquí, por lo que no se usa en su lugar la ejecución.

Para obtener más información y ejemplos, vea [botones de comando](ctrl-command-buttons.md).

### <a name="command-links"></a>Vínculos de comandos

-   **Presente un conjunto de comandos largos mediante vínculos de comandos, en lugar de botones de comando o una combinación de botones de radio y un botón Aceptar.** Esto permite a los usuarios responder con un solo clic. Sin embargo, este enfoque solo funciona para una sola pregunta.
-   **Presente primero los vínculos de comandos que se usan con más frecuencia.** El orden resultante debe seguir aproximadamente la probabilidad de uso, pero también tiene un flujo lógico.
    -   **Excepción:** Los vínculos de comandos que dan lugar a hacer todo deben colocarse en primer lugar.
-   Si un vínculo de comando requiere una explicación más detallada, **proporcione una explicación complementaria.** Las explicaciones complementarias describen el motivo por el que los usuarios pueden elegir el comando o lo que sucede si se elige el comando.
-   **No use explicaciones complementarias que son las reinstrucciones de texto del vínculo de comandos.** Use una explicación complementaria solo si no puede hacer que un vínculo de comando sea autoexplicativo. Proporcionar una explicación complementaria para un vínculo de comando no significa que tenga que proporcionarlos para todos los comandos.

![captura de pantalla del cuadro de diálogo con opciones de anotaciones de texto ](images/win-dialog-box-image40.png)

En este ejemplo, la explicación complementaria describe las implicaciones de una de las opciones.

-   **Usar frases que comienzan con un verbo, sin puntuación final.**
-   **Si se recomienda encarecidamente un comando, considere la posibilidad de agregar "(recomendado)" a la etiqueta.** Asegúrese de agregar a la etiqueta de vínculo, no la explicación complementaria.
-   **Si un comando está pensado únicamente para usuarios avanzados, considere la posibilidad de agregar "(avanzado)" a la etiqueta.** Asegúrese de agregar a la etiqueta de vínculo, no la explicación complementaria.
-   **Proporcione siempre un botón Cancelar explícito**. No utilice un vínculo de comando con este fin.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con el vínculo no salir ](images/win-dialog-box-image41.png)

En este ejemplo, el cuadro de diálogo usa un vínculo de comando en lugar de un botón Cancelar.

Para obtener más información y ejemplos, vea [vínculos de comandos](ctrl-command-links.md).

### <a name="dont-show-this-item-again"></a>No mostrar esta <item> nuevo

-   **Considere la posibilidad de usar una <item> opción no volver a mostrar esto para permitir que los usuarios supriman un cuadro de diálogo recurrente, solo si no hay una alternativa mejor.** Es mejor Mostrar siempre el cuadro de diálogo si los usuarios lo necesitan realmente o simplemente eliminarlo si no lo necesitan.
-   **Use esta frase específica reemplazar <item> por el elemento específico.** Por ejemplo, no vuelva a mostrar este aviso. Al hacer referencia a un cuadro de diálogo en general, use no volver a mostrar este mensaje.
-   **Indique claramente cuándo se usarán los datos proporcionados por el usuario para los valores predeterminados futuros** agregando la siguiente frase en la opción: las selecciones se usarán de forma predeterminada en el futuro.
-   **No seleccione la opción de forma predeterminada. Si el cuadro de diálogo realmente debe mostrarse solo una vez, hágalo sin preguntar.** No use esta opción como excusa para molestar a los usuarios. Asegúrese de que el comportamiento predeterminado no sea molesto.

**Incorrecto:**

![captura de pantalla del mensaje en el que se pide una pregunta innecesaria ](images/win-dialog-box-image42.png)

En este ejemplo, el mensaje se debería mostrar solo una vez. No es necesario realizar ninguna pregunta.

-   **Haga que la configuración se mantenga por usuario.**
-   **Si los usuarios seleccionan la opción y hacen clic en cancelar, esta opción surte efecto.** Esta opción es una meta, por lo que no sigue el comportamiento de cancelación estándar de no tener ningún efecto secundario. Tenga en cuenta que si los usuarios no quieren ver el cuadro de diálogo en el futuro, lo más probable es que deseen cancelarlo también.
-   Si los usuarios pueden necesitar restaurar estos cuadros de diálogo, proporcione un comando **restore messages** en el cuadro de diálogo Opciones del programa.

### <a name="ask-me-later"></a>Preguntarme más tarde

-   Proporcione esta opción para descartar un cuadro de diálogo solo cuando:
    -   **El cuadro de diálogo es indirecto**, por lo que es probable que los usuarios se centren en otra tarea.
    -   **Los usuarios deben responder pero no inmediatamente** para que puedan continuar con su trabajo.
    -   **La pregunta requiere una idea o un esfuerzo suficientes** para que los usuarios puedan tomar mejores decisiones si se le proporciona más tiempo.
    -   **La opción o el cuadro de diálogo se presentarán automáticamente más adelante** (de modo que los usuarios se pregunten más tarde).
-   **Incorrecto:**
-   ![captura de pantalla del mensaje con la opción preguntar más tarde ](images/win-dialog-box-image43.png)
-   En este ejemplo, la pregunta es lo suficientemente sencilla como para agregar una opción preguntar más tarde.
-   En caso contrario, se espera que los usuarios respondan ahora, pero que puedan cerrar el cuadro de diálogo normalmente con cancelar o cerrar. Cuando se usa correctamente, esta opción no es habitual.

### <a name="morefewer"></a>Más o menos

-   **Use más o menos botones de divulgación progresiva para mostrar u ocultar las opciones, los comandos o las opciones avanzadas o con poca utilización que los usuarios de destino no suelen necesitar.** Al hacerlo, se simplifica el cuadro de diálogo para el uso típico. No oculte opciones, comandos o información de uso común, ya que es posible que los usuarios no las encuentren.

![captura de pantalla del cuadro de diálogo con el botón más opciones ](images/win-dialog-box-image24.png)

En este ejemplo, las opciones que rara vez se usan están ocultas de forma predeterminada.

-   **No use más o menos controles a menos que haya realmente más detalles que mostrar.** No solo tiene que volver a indicar la misma información en un formato diferente.
-   **No use más o menos controles para mostrar la ayuda.** En su lugar, use vínculos de ayuda o notas al pie.
-   **Con los cuadros de diálogo de tarea, evite combinar más o menos controles con no <item> volver a mostrar esto.** Esta combinación tiene un aspecto extraño.
-   Para obtener instrucciones de etiquetado, vea [divulgación progresiva](ctrl-progressive-disclosure-controls.md).

### <a name="footnotes"></a>Notas al pie

-   **Use notas a pie de página para obtener información que no es esencial para el propósito de un cuadro de diálogo, pero que los usuarios pueden resultar útiles para tomar decisiones.** La mayoría de los usuarios deberían poder omitir las notas a pie de página y seguir realizando decisiones informadas en su respuesta al cuadro de diálogo.

![captura de pantalla del cuadro de diálogo con la nota al pie de página clarificada ](images/win-dialog-box-image44.png)

En este ejemplo, la información de la nota al pie es complementaria, no esencial.

### <a name="disabling-or-removing-controls-vs-giving-error-messages"></a>Deshabilitar o quitar controles en lugar de asignar mensajes de error

-   Cuando un control no se aplique en el contexto actual, tenga en cuenta las siguientes opciones:
    -   **Quitar el control cuando no hay ninguna manera de que los usuarios lo habiliten, o los usuarios no esperan que se apliquen y su estado no cambia con frecuencia.** Al hacerlo, se simplifica el cuadro de diálogo y los usuarios no lo pierden. El hecho de que aparezca un control y desaparezca con frecuencia es molesto.
    -   **Deshabilite el control cuando los usuarios esperan que se aplique o su estado cambie con frecuencia, y los usuarios pueden deducir fácilmente por qué está deshabilitado el control.** Un ejemplo de deducción sencilla es deshabilitar un botón de confirmación cuando hay un solo cuadro de texto vacío que requiere una entrada. Puede usar [globos](ctrl-balloons.md) para mostrar los problemas de los datos de los usuarios no críticos con cuadros de texto y listas desplegables editables. Sin embargo, si el problema no se puede explicar con un globo o implica varios controles, la deducción dejará de ser fácil.
    -   **De lo contrario, deje el control habilitado, pero proporcione un mensaje de error cuando se use incorrectamente.** Deshabilitar en este caso dificultaría a los usuarios comprender por qué está deshabilitado el control. Los usuarios se verán obligados a determinar el problema a través de la lógica de experimentación y deducción. Es mejor proporcionar un mensaje de error útil para explicar el problema explícitamente.
-   **Sugerencia:** Si no está seguro de si debe deshabilitar un control o enviar un mensaje de error, empiece por redactar el mensaje de error que puede proporcionar. Si el mensaje de error contiene información útil que no es probable que los usuarios de destino deduzcan rápidamente, deje habilitado el control y proporcione el error. De lo contrario, deshabilite el control.
-   **Si deshabilita un control, también deshabilitará todos los controles asociados**, como su etiqueta, las explicaciones complementarias o los botones de comando. Sin embargo, no deshabilite los [cuadros de grupo](ctrl-group-boxes.md), las etiquetas de grupo o las explicaciones de grupo si es que hay alguno.

![captura de pantalla del cuadro de diálogo con controles atenuados ](images/win-dialog-box-image45.png)

En este ejemplo, las etiquetas del cuadro de texto deshabilitado también están deshabilitadas, pero la etiqueta de grupo y la explicación de grupo no lo están.

### <a name="required-input"></a>Entrada necesaria

-   Para indicar que los usuarios deben proporcionar información en un control, tenga en cuenta las siguientes opciones:
    -   **No indique nada, pero controle la entrada necesaria que falta con mensajes de error.** Este enfoque reduce el desorden y funciona bien si la mayoría de las entradas es opcional o no es probable que los usuarios omitan los controles, con lo que el número de mensajes de error se mantiene bajo.
    -   **Indicar la entrada necesaria mediante un asterisco al principio de la etiqueta.** Explique el asterisco con cualquiera de las siguientes opciones:

        -   Una nota al pie en la parte inferior del área de contenido que indica la \* entrada necesaria.
        -   Información sobre herramientas en el asterisco que indica la entrada necesaria.

        Este enfoque funciona bien si no hay muchos controles necesarios, pero es deficiente si la mayoría de los controles son necesarios.

        ![captura de pantalla de etiquetas de cuadro de texto con asteriscos ](images/win-dialog-box-image46.png)

        En este ejemplo, se usan asteriscos para indicar la entrada necesaria.

    -   **Si todos los controles requieren una entrada, el estado "todas las entradas necesarias" se encuentra en un lugar adecuado en la parte superior del área de contenido.** Este enfoque reduce la aglomeración en este caso específico.
    -   **Indica entradas opcionales con "(opcional)" después de la etiqueta.** Este enfoque funciona bien si la mayoría de las entradas es necesaria, pero en caso contrario, es deficiente.

-   **Por coherencia, intente usar el mismo método para indicar la entrada necesaria en todo el programa.** En concreto, indique la entrada obligatoria u opcional según sea necesario, pero evite usar ambos en el mismo programa.

### <a name="error-handling"></a>Control de errores

-   Evite los errores mediante el uso de controles que están restringidos a entradas de usuario válidas. También puede ayudar a reducir el número de errores proporcionando valores predeterminados razonables.
-   Valide la entrada del usuario tan pronto como sea posible y muestre los errores lo más cerca posible del punto de entrada.
-   **Utilice el control de errores no modal (errores o globos en contexto) para los problemas de los datos proporcionados por el usuario.**
    -   **Usar globos para problemas de entrada de usuario de punto único no críticos detectados en un cuadro de texto o inmediatamente después de que un cuadro de texto pierda el foco.** Los globos no requieren espacio de pantalla disponible ni el diseño dinámico necesario para mostrar los mensajes en contexto. Muestra un solo globo a la vez. Dado que el problema no es crítico, no es necesario ningún icono de error. Los globos desaparecen cuando se hace clic en él, cuando se resuelve el problema o después de un tiempo de espera.

        ![captura de pantalla del mensaje ' carácter incorrecto ' ](images/win-dialog-box-image47.png)

        En este ejemplo, un globo indica un problema de entrada mientras sigue en el control.

-   **Use errores en contexto para la detección diferida de errores**, normalmente errores detectados al hacer clic en el botón confirmar. (No use errores en contexto para la configuración que se confirma inmediatamente). Puede haber varios errores en contexto a la vez. Use el texto normal y un icono de error de 16x16 píxeles, y colóquelos directamente junto al problema siempre que sea posible. Los errores en contexto no desaparecen a menos que el usuario confirme y no se encuentren otros errores.

    ![captura de pantalla del cuadro de diálogo con dos mensajes de error ](images/win-dialog-box-image48.png)

    En este ejemplo, se usa un error en contexto para un error encontrado al hacer clic en el botón confirmar.

-   **Utilice el control de errores modal (cuadros de diálogo o cuadros de mensajes) para todos los demás problemas, incluidos los** errores que impliquen varios controles o que se encuentren con errores no contextuales o no de entrada al hacer clic en un botón de confirmación.
-   **Cuando se detecta y se detecta un problema de entrada, establezca el foco de entrada en el primer control con los datos incorrectos.** Desplácese por el control en la vista si es necesario.

Para obtener más información y ejemplos, vea [mensajes de error](mess-error.md) y [globos](ctrl-balloons.md).

### <a name="help"></a>Ayuda

-   Al proporcionar asistencia al usuario, tenga en cuenta las siguientes opciones (en orden de preferencia):
    -   Proporcione a los controles interactivos etiquetas autoexplicativas. Los usuarios tienen más probabilidades de leer las etiquetas en los controles interactivos que cualquier otro texto.
    -   Proporcionar explicaciones en contexto mediante etiquetas de [texto estático](text-ui.md).
    -   Proporcione un vínculo de ayuda específico a un tema de ayuda relevante.
-   **Busque vínculos de ayuda en la parte inferior del área de contenido del cuadro de diálogo.** Si el cuadro de diálogo tiene una nota al pie y el vínculo de ayuda está relacionado con él, coloque el vínculo de ayuda en la nota al pie.

    ![captura de pantalla del cuadro de diálogo con el vínculo de ayuda ](images/win-dialog-box-image40.png)

    En este ejemplo, el vínculo de ayuda se aplica a todo el cuadro de diálogo.

    -   **Excepción:** Si un cuadro de diálogo tiene varios grupos de valores de configuración distintos que tienen temas de ayuda independientes (quizás dentro de los cuadros de grupo), busque los vínculos de ayuda en la parte inferior de los grupos.

-   **No use vínculos a temas de ayuda generales ni imprecisos ni botones de ayuda genérica.** Los usuarios a menudo omiten la ayuda genérica.

Para obtener más información y ejemplos, vea la [ayuda](winenv-help.md)de.

### <a name="default-values"></a>Valores predeterminados

-   Incluir un botón de confirmación predeterminado en cada cuadro de diálogo.
-   Para los cuadros de diálogo de preguntas:
    -   **Seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema), la respuesta más segura es el valor predeterminado.** Si seguridad y seguridad no son factores, seleccione la respuesta más probable o cómoda.
        -   **Excepción:** No convierta una respuesta destructiva en la predeterminada, a menos que haya una manera fácil y obvia de deshacer el comando.
-   Para los cuadros de diálogo de elección:
    -   Para los valores predeterminados iniciales, **Seleccione el más seguro (para evitar la pérdida de datos o el acceso al sistema) y los valores más seguros de cada control.** Si seguridad y seguridad no son factores, seleccione las opciones más probables o convenientes.
    -   En el caso de los valores predeterminados posteriores, **vuelva a seleccionar las opciones seleccionadas anteriormente si es probable que estos valores se repitan y, de este modo, sea seguro y seguro.** En caso contrario, seleccione los valores predeterminados iniciales.

![captura de pantalla del cuadro de diálogo Imprimir ](images/win-dialog-box-image49.png)

En este ejemplo, lo más probable es que los usuarios elijan la misma configuración de impresión que tenían la última vez. Sin embargo, es probable que el número de copias que desee cambiar, por lo que esta configuración no se reselecciona.

## <a name="recommended-sizing-and-spacing&quot;></a>Ajuste de tamaño y espaciado recomendados

-   **Admite la resolución de pantalla mínima de Windows Vista de 800 x 600 píxeles.** Los diseños se pueden optimizar para ventanas redimensionables con una resolución de pantalla de 1024 x 768 píxeles.
-   **Use ventanas redimensionables siempre que sea práctico para evitar las barras de desplazamiento y los datos truncados.** Las ventanas con contenido dinámico y listas sacan el máximo partido de las ventanas redimensionables.
-   **Las ventanas de tamaño fijo deben ser totalmente visibles y ajustarse al área de trabajo.**
-   **Las ventanas de tamaño variable pueden estar optimizadas para resoluciones más altas, pero se reduce el tamaño según sea necesario en el momento de la presentación en la resolución de pantalla real.**
-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No dude en usar tamaños de ventana iniciales más grandes si puede utilizar el espacio con eficacia.

## <a name=&quot;text&quot;></a>Texto

### <a name=&quot;general&quot;></a>General

-   **Quite el texto redundante.** Busque texto redundante en títulos, instrucciones principales, instrucciones adicionales, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en las instrucciones y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **Usar frases positivas.** La formulación positiva es más fácil de entender para los usuarios.

**Correcto:**

¿Desea habilitar el uso compartido de archivos e impresoras?

**Incorrecto:**

¿Desea deshabilitar el uso compartido de archivos e impresoras?

Sin embargo, la formulación debe coincidir con el comando asociado, aunque el comando tenga frase negativa. por lo tanto, por ejemplo, use Disable para confirmar un comando DISABLE.

-   **Si es necesario, use la palabra &quot;ventana&quot; para hacer referencia al propio cuadro de diálogo.**
-   **Use la segunda persona (&quot;usted/su") para indicar a los usuarios qué hacer** en la instrucción principal y en el área de contenido. A menudo, la segunda persona está implícita.

**Ejemplos:**

Elegir las imágenes que desea imprimir

Elija una cuenta.

-   **Use la primera persona ("I/me/My") para que los usuarios puedan indicar al programa qué hacer** en los controles del área de contenido que responden a la instrucción principal.

**Ejemplo:** Imprimir las fotos en la cámara.

### <a name="dialog-box-titles"></a>Títulos del cuadro de diálogo

-   **Use el título para identificar el comando, la característica o el programa desde el que procede un cuadro de diálogo.**
    -   Si el cuadro de diálogo es iniciado por el usuario, se identifica mediante el comando o el nombre de la característica. **Excepciones:**
        -   Si un cuadro de diálogo se muestra en muchos comandos diferentes, considere la posibilidad de usar el nombre del programa en su lugar.
        -   Si ese título sería redundante con la instrucción principal, utilice en su lugar el nombre del programa.
    -   Si se inicia un programa o sistema (y, por tanto, fuera de contexto), debe identificarlo mediante el nombre del programa o de la característica para asignar el contexto.
    -   No use el título para explicar qué hacer en el cuadro de diálogo que es el propósito de la instrucción principal.
-   Use el nombre de comando exacto para los nombres basados en comandos, pero no incluya los puntos suspensivos si hay alguno. Puede incluir el título de menú del comando si es necesario para redactar un buen título. Ejemplo: para un objeto... en un menú Insertar, use el título Insertar objeto.
-   **Si aparece un cuadro de diálogo no modal en la barra de tareas, optimice el título para que se muestre en la barra de tareas** ; para ello, coloque primero la información distintiva. Ejemplos: "66% completed" y "3 recordatorios".
-   **No incluya las palabras "Dialog" o "Progress" en el título.** Esto es implícito y, si se deja desactivado, facilita la exploración de los usuarios.
-   Usar [mayúsculas y minúsculas de estilo de título](glossary.md), sin puntuación final.

### <a name="main-instructions"></a>Instrucciones principales

-   **Use la instrucción principal para explicar brevemente qué hacer en el cuadro de diálogo.** La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. Las buenas instrucciones comunican el objetivo del usuario con el cuadro de diálogo en lugar de centrarse exclusivamente en el mecanismo de manipulación.
-   **Omita la instrucción principal cuando lo único que puede decir es obvio.** En tales casos, el contenido del cuadro de diálogo se explica por sí mismo. Por ejemplo, los cuadros de diálogo comunes abrir archivo y guardar archivo no necesitan una instrucción principal porque su contexto y diseño hacen que su finalidad sea obvia.
-   **Omita las etiquetas de control que representen la instrucción principal.** En este caso, la instrucción principal toma la clave de acceso.

**Aceptable:**

![captura de pantalla del cuadro de texto con etiqueta redundante ](images/win-dialog-box-image50.png)

En este ejemplo, la etiqueta del cuadro de texto es simplemente una resituación de la instrucción principal.

**Manera**

![captura de pantalla del mismo cuadro de texto con una etiqueta ](images/win-dialog-box-image51.png)

En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma la clave de acceso.

-   **Sea conciso usar una sola oración completa.** Reduzca la instrucción principal a la información esencial. Si debe explicar algo más, use la instrucción complementaria.
-   **Use verbos específicos siempre que sea posible.** Los verbos específicos (ejemplos: Connect, Save, install) son más significativos para los usuarios que los genéricos (por ejemplo: configurar, administrar, establecer).
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   **No incluya los períodos finales si la instrucción es una instrucción.** Si la instrucción es una pregunta, incluya un signo de interrogación final.
-   **En el caso de los cuadros de diálogo de progreso, utilice una frase de gerundio que explique brevemente la operación en curso y** termine con puntos suspensivos. Ejemplo: imprimir imágenes...
-   **Sugerencia:** Puede evaluar una instrucción principal deimaginando lo que diría a un amigo. Si responder con la instrucción principal sería no natural, no práctico o complicado, retrabaje la instrucción.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   **Cuando sea necesario, use una instrucción complementaria opcional para presentar información adicional útil para entender o usar la página.** Puede proporcionar información más detallada y definir la terminología.
-   **Si la apariencia del cuadro de diálogo es iniciado por el sistema o por el sistema (y, por tanto, fuera de contexto), use la instrucción complementaria para explicar por qué ha aparecido el cuadro de diálogo.** Para estos cuadros de diálogo, el contexto normalmente no es obvio.
-   **No repita la instrucción principal con un texto ligeramente diferente.** En su lugar, omita la instrucción complementaria Si no hay más que agregar.
-   Use frases completas, uso de mayúsculas y minúsculas y puntuación final.

### <a name="command-links"></a>Vínculos de comandos

-   **Elija texto de vínculo conciso que se comunique claramente y diferencie el vínculo del comando.** Debe ser autoexplicativo y corresponder a la instrucción principal. Los usuarios no deben tener que averiguar qué significa realmente el vínculo o cómo se diferencia de otros vínculos.
-   **Inicie siempre los vínculos de comandos con un verbo.**
-   Use mayúsculas de estilo de frase.
-   No uses puntuación final.
-   **Si es necesario, proporcione cualquier explicación adicional mediante oraciones completos y puntuación final.** Sin embargo, agregue estas explicaciones solo cuando sea necesario no agregue explicaciones a todos los vínculos de comandos solo porque un vínculo de comando necesita uno.

Para obtener más información y ejemplos, vea instrucciones de [vínculo de comandos](ctrl-command-links.md) .

### <a name="commit-buttons"></a>Botones de confirmación

-   **Use etiquetas de botón de confirmación específicas que tengan sentido por sí mismas y que sean una respuesta a la instrucción principal.** Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta. Es mucho más probable que los usuarios lean etiquetas de botón de comando que el texto estático.
-   **Iniciar las etiquetas del botón confirmar con un verbo. Las excepciones son OK, yes y no.**
-   Use mayúsculas de estilo de frase.
-   No uses puntuación final.
-   Asigne una [clave de acceso](glossary.md)única.
    -   **Excepción:** No asigne claves de acceso a los botones aceptar y cancelar porque ENTER y ESC son sus claves de acceso. Esto hace que las demás claves de acceso sean más fáciles de asignar.

## <a name="documentation"></a>Documentación

Al hacer referencia a los cuadros de diálogo:

-   En programación y otra documentación técnica, consulte cuadros de diálogo como cuadros de diálogo. En cualquier otro lugar, haga referencia a los cuadros de diálogo por su título. Si la barra de título está oculta, consulte el cuadro de diálogo con la instrucción principal.
-   Si debe hacer referencia a un cuadro de diálogo en general, use la ventana de la documentación del usuario. Puede hacer referencia a un cuadro de diálogo de pregunta simple o a una confirmación como un mensaje.
-   Use el título exacto o el texto de la instrucción principal, incluido el uso de mayúsculas.
-   Siempre que sea posible, dé formato al título usando texto en negrita. De lo contrario, coloque el título entre comillas solo si es necesario para evitar confusiones.

Ejemplo: en **seguridad de Windows**, haga clic en **más opciones**.

