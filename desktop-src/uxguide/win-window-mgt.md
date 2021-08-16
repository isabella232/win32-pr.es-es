---
title: Administración de ventanas
description: En este artículo se trata la colocación predeterminada de las ventanas cuando se muestran inicialmente en la pantalla, su orden de apilamiento con respecto a otras ventanas (orden Z), su tamaño inicial y cómo su pantalla afecta al foco de entrada.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b8dc2858b0e3cc3b2a451210a61315c610afc727ac42156d5c4fc5c112135807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212168"
---
# <a name="window-management"></a>Administración de ventanas

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

En este artículo se trata la colocación predeterminada de las ventanas cuando se muestran inicialmente en la pantalla, su orden de apilamiento con respecto a otras ventanas (orden[Z),](glossary.md)su tamaño inicial y cómo su pantalla afecta al foco de entrada.

Para obtener las siguientes directrices:

-   Una ventana de nivel superior no tiene ninguna ventana de propietario y se muestra en la barra de tareas. Ejemplos: ventanas de aplicación. En Windows Vista y versiones posteriores, los cuadros de diálogo sin ventanas de propietario y hojas de propiedades también se consideran de nivel superior.
-   Una ventana de propiedad tiene una ventana de propietario y no se muestra en la barra de tareas. Ejemplos: cuadros de diálogo modales, cuadros de diálogo modelados.
-   Se muestra una ventana iniciada por el usuario como resultado directo de la acción de un usuario. De lo contrario, se inicia el programa si lo inicia un programa o el sistema se inicia si lo inicia Microsoft Windows . Por ejemplo, un cuadro de diálogo Opciones se inicia por el usuario, pero se inicia un recordatorio de la reunión.
-   Una ventana contextual es una ventana iniciada por el usuario que tiene una relación fuerte con el objeto desde el que se inició. Por ejemplo, las ventanas mostradas por los menús contextuales o los iconos del área de notificación son contextuales, pero las ventanas mostradas por las barras de menús no lo son.
-   El monitor activo es el monitor donde se ejecuta el programa activo.
-   El monitor predeterminado es el que tiene el menú Inicio, la barra de tareas y el área de notificación.

## <a name="design-concepts"></a>Conceptos de diseño

La administración de ventanas es una de las actividades de usuario más fundamentales. Antes Windows Vista, las ventanas a menudo tenían tamaños predeterminados pequeños y se colocaban en el centro de la pantalla. Este enfoque funciona bien para los monitores individuales y de baja resolución más antiguos, pero no para el hardware de vídeo moderno.

Windows está diseñado para admitir hardware de vídeo moderno, que a menudo se ejecuta con resoluciones significativamente superiores a la resolución de pantalla mínima admitida y puede tener varios monitores. Para ello, haga lo siguiente:

-   Permite a los usuarios beneficiarse totalmente de su hardware avanzado.
-   Requiere menos esfuerzo de los usuarios para mover el mouse a través de distancias mayores.
-   Hace que la selección de ubicación de la ventana sea más predecible y, por tanto, más fácil de encontrar.

### <a name="the-minimum-supported-screen-resolution"></a>La resolución de pantalla mínima admitida

La resolución [de pantalla mínima efectiva](glossary.md) admitida por Windows es de 800 x 600 píxeles. Esto significa que las ventanas de tamaño fijo deben mostrarse completamente con la resolución mínima (mientras se reserva espacio para la barra de tareas), pero las ventanas de tamaño ajustable se pueden optimizar para una resolución efectiva de 1024 x 768 píxeles, siempre que sean funcionales con la resolución mínima.

Aunque actualmente las resoluciones de pantalla física más comunes para equipos Windows son de 1024 x 768 píxeles o superior, el destino de 800 x 600 píxeles permite Windows:

-   Trabaje bien con todo el hardware moderno, incluidos los equipos de cuadernos pequeños.
-   Admite la configuración de valores altos de ppp (puntos por pulgada).
-   Admite fuentes más grandes para la accesibilidad.
-   Compatibilidad con hardware que se usa de forma global.

Elegir la resolución mínima para admitir requiere lograr el equilibrio correcto. El destino de una resolución más alta daría lugar a una experiencia pocooptima para un porcentaje significativo de hardware moderno, mientras que el objetivo sería una resolución inferior impediría que los diseñadores aprovecharan al máximo el espacio de pantalla disponible.

Si cree que los usuarios de destino usan resoluciones significativamente más altas que el mínimo de Windows, puede diseñar el programa para aprovechar al máximo el espacio de pantalla adicional mediante ventanas que se pueden cambiar de tamaño y escalar bien.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Admite la resolución Windows una resolución efectiva de 800 x 600 píxeles.** En el caso de las interfaces de usuario críticas (UI) que deben funcionar en modo seguro, admiten una resolución efectiva de 640 x 480 píxeles. Asegúrese de tener en cuenta el espacio utilizado por la barra de tareas reservando 48 píxeles [relativos](glossary.md) verticales para las ventanas mostradas con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño ajustable para una resolución efectiva de 1024 x 768 píxeles.** Cambie automáticamente el tamaño de estas ventanas para obtener resoluciones de pantalla inferiores de forma que todavía sea funcional.
-   **Asegúrese de probar las ventanas en 96 ppp (100 por ciento) a 800 x 600 píxeles, 120 ppp (125 por ciento) a 1024 x 768 píxeles y 144 ppp (150 por ciento) a 1200 x 900 píxeles.** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y la extensión de iconos y mapas de bits.
-   **Para los programas con escenarios de uso táctil y móvil, optimice para 120 ppp.** Actualmente, las pantallas de valores altos de ppp son frecuentes en equipos táctiles y móviles.
-   **Las ventanas que se pueden** cambiar de tamaño ya no deben mostrar el glifo de cambio de tamaño en la esquina inferior derecha, porque:
    -   Todos los lados y bordes de una ventana son ajustables, no solo la esquina inferior derecha.
    -   El glifo requiere que se muestre una barra de estado, pero muchas ventanas de tamaño ajustable no proporcionan barras de estado.
    -   Los bordes de ventana y los punteros de cambio de tamaño que se pueden cambiar de tamaño son más eficaces para comunicar que una ventana se puede cambiar de tamaño que el glifo de cambio de tamaño.

### <a name="title-bar-controls"></a>Controles de la barra de título

Use los controles de la barra de título como se muestra a continuación:

-   **Cerca.** Todas las ventanas principales y secundarias con un marco de ventana estándar deben tener un botón Cerrar en la barra de título. Hacer clic en Cerrar tiene el efecto de cancelar o cerrar la ventana.

![captura de pantalla del cuadro de diálogo sin botón Cerrar ](images/win-window-mgt-image1.png)

En este ejemplo, el cuadro de diálogo no tiene un botón Cerrar en la barra de título.

-   **Minimizar.** Todas las ventanas principales y las ventanas secundarias modeleses de ejecución larga (como los diálogos de progreso) deben tener un botón Minimizar. Al hacer clic en Minimizar, se reduce la ventana a su botón de la barra de tareas. Por lo tanto, las ventanas que se pueden minimizar requieren un icono de barra de título.
-   **Maximizar o restaurar hacia abajo.** Todas las ventanas de tamaño ajustable deben tener un botón Maximizar o restaurar hacia abajo. Al hacer clic en Maximizar se muestra la ventana en su tamaño más grande, que para la mayoría de las ventanas es de pantalla completa. mientras que al hacer clic en Restaurar hacia abajo se muestra la ventana en su tamaño anterior. Sin embargo, algunas ventanas no se benefician del uso de una pantalla completa, por lo que estas ventanas deben maximizar su tamaño útil más grande.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No tenga miedo de usar tamaños de ventana iniciales mayores si puede usar el espacio de forma eficaz.
-   **Use ventanas de tamaño ajustable siempre que sea práctico para evitar barras de desplazamiento y datos truncados.** Windows con contenido dinámico y listas se benefician al máximo de las ventanas de tamaño ajustable.
-   **En el caso de los documentos de texto,** considere la posibilidad de una longitud de línea máxima de 65 caracteres para facilitar la lectura del texto. (Los caracteres incluyen letras, signos de puntuación y espacios).
-   Ventanas de tamaño fijo:
    -   **Debe ser completamente visible y ajustarse al tamaño del área de trabajo.**
-   Ventanas de tamaño ajustable:
    -   **Se puede optimizar para resoluciones más altas, pero se puede cambiar el tamaño según sea necesario en el momento de la presentación a la resolución de pantalla real.**
    -   **Para tamaños de ventana cada vez mayores, debe mostrar más información progresivamente.** Asegúrese de que al menos una parte o control de la ventana tiene contenido que se puede tamaño.
    -   **Debe evitar los tamaños restaurados predeterminados que estén maximizados o casi maximizados.** En su lugar, elija un tamaño predeterminado que normalmente sea el más útil sin tener que estar en pantalla completa. Suponga que los usuarios maximizarán la ventana en lugar de cambiar el tamaño para que sea de pantalla completa.
    -   **Debe establecer un tamaño mínimo de ventana si hay un tamaño por debajo del cual el contenido ya no se puede usar.** Para los controles que se pueden cambiar de tamaño, establezca los tamaños mínimos de elementos que se pueden cambiar de tamaño en sus tamaños funcionales más pequeños, como los anchos de columna funcionales mínimos en las vistas de lista.
    -   **Debe cambiar la presentación si lo hace para que el contenido se puede usar en tamaños más pequeños.**

![captura de pantalla de los botones del reproductor multimedia ](images/win-window-mgt-image2.png)

En este ejemplo, Reproductor de Windows Media cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="window-location"></a>Ubicación de la ventana

-   **Para las siguientes directrices, "centrar" significa sesgo de la posición vertical ligeramente hacia la parte superior del monitor, en lugar de colocarse exactamente en el centro.** Coloque el 45 por ciento del espacio entre la parte superior del monitor o propietario y la parte superior de la ventana, y el 55 por ciento entre la parte inferior del monitor o propietario y la parte inferior de la ventana. Haga esto porque el ojo está sesgado de forma natural hacia la parte superior de la pantalla.

    ![figura de ventana situada ligeramente por encima del centro ](images/win-window-mgt-image3.png)

    "Centrar" significa sesgo de la posición vertical ligeramente hacia la parte superior del monitor.

-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Colómelo fuera del camino para que la ventana no cubre el objeto de origen.

    -   Si se muestra con el mouse, cuando sea posible, coloque el desplazamiento hacia abajo y hacia la derecha.

    ![figura de la ventana contextual situada a la derecha del objeto ](images/win-window-mgt-image4.png)

    Mostrar ventanas contextuales cerca del objeto desde el que se inició.

    ![figura de la ventana del área de notificación ](images/win-window-mgt-image5.png)

    Windows se inician desde iconos de área de notificación que se muestran cerca del área de notificación.

-   Si se muestra con un lápiz, cuando sea posible, colómelo para que no esté cubierto por la mano del usuario. Para los usuarios con la derecha, se muestra a la izquierda; de lo contrario, se muestra a la derecha.

    ![figura de la ventana contextual situada a la izquierda del objeto ](images/win-window-mgt-image6.png)

    Cuando se usa un lápiz, también se muestran las ventanas contextuales para que no se cubren con la mano del usuario.

-   **Desarrolladores:** Puede distinguir entre eventos del mouse y eventos de lápiz mediante la API [GetMessageExtraInfo.](../tablet/system-events-and-mouse-messages.md) Puede determinar la entrega del [usuario](/previous-versions/ms819495(v=msdn.10)) mediante la API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.
-   **Coloque los diálogos de progreso fuera del camino en la esquina inferior derecha del monitor activo.**

    ![figura de la barra de progreso en la esquina inferior derecha ](images/win-window-mgt-image7.png)

    Coloque los cuadros de diálogo de progreso en la esquina inferior derecha.

-   **Si una ventana no está relacionada con el contexto actual o la acción del usuario, colómela fuera de la ubicación actual del puntero.** Si lo hace, se evita la interacción accidental.
-   **Si una ventana es una aplicación o documento de nivel superior, siempre debe poner en cascada su origen desde la esquina superior izquierda del monitor.** Si lo crea el programa activo, use el monitor activo; De lo contrario, use el monitor predeterminado.

    ![ilustración de tres ventanas en cascada desde la parte superior izquierda ](images/win-window-mgt-image8.png)

    Ventanas de documento o aplicación de nivel superior en cascada en la esquina superior izquierda del monitor.

-   **Si una ventana es una utilidad de nivel superior, siempre debe mostrarla "centrada" en el monitor.** Si lo crea el programa activo, use el monitor activo; De lo contrario, use el monitor predeterminado.

    ![figura de la ventana de utilidad centrada en el monitor ](images/win-window-mgt-image9.png)

    Ventanas de utilidad de nivel superior central.

-   **Si una ventana es de propiedad, inicialmente se muestra "centrada" en la parte superior de la ventana del propietario.** Para su posterior visualización, considere la posibilidad de mostrarla en su última ubicación (con respecto a la ventana de propietario) si es probable que sea más conveniente.

    ![figura de la ventana de propiedad centrada en la ventana de propietario ](images/win-window-mgt-image10.png)

    Inicialmente, centra las ventanas propiedad de en la parte superior de la ventana del propietario.

-   **En el caso de los cuadros de diálogo de modelado, siempre se muestran inicialmente en la parte superior de la ventana del propietario para facilitar su búsqueda.** Sin embargo, si el usuario activa la ventana de propietario, esto puede ocultar el cuadro de diálogo de modeless.

    ![figura del cuadro de diálogo modeless sobre la ventana de propietario ](images/win-window-mgt-image11.png)

    Mostrar diálogos de modelado inicialmente en la parte superior de la ventana del propietario para facilitar su búsqueda.

-   **Si es necesario, ajuste la ubicación inicial para que toda la ventana esté visible en el monitor de destino.** Si una ventana que se puede cambiar de tamaño es mayor que el monitor de destino, reduzca para que quepa.

### <a name="window-order-z-order"></a>Orden de ventana (orden Z)

-   **Coloque siempre las ventanas de propiedad encima de su ventana de propietario.** Nunca coloque las ventanas de propiedad en sus ventanas de propietario, ya que lo más probable es que los usuarios no las vean.
-   **Respetar la selección del pedido Z de los usuarios. Cuando los usuarios seleccionen una ventana, lleve solo las ventanas asociadas a esa instancia del programa (la ventana más cualquier ventana propietaria o de propiedad) al principio del pedido Z.** No cambie el orden de ninguna otra ventana, como instancias independientes del mismo programa.

### <a name="window-activation"></a>Activación de ventanas

-   **Respetar la selección de estado de ventana de los usuarios. Si una ventana existente necesita atención, flashee el botón de la barra de tareas tres veces para llamar la atención y dejarla resaltada, pero no haga nada más.** No restaure ni active la ventana. No use ningún efecto de sonido. En su lugar, permita que los usuarios activen la ventana cuando estén listos.
    -   **Excepción:** Si la ventana no aparece en la barra de tareas, colómela en la parte superior de todas las demás ventanas y, en su lugar, flashee su barra de título.
-   **La restauración de una ventana principal también debe restaurar** todas sus ventanas secundarias, incluso si esas ventanas secundarias tienen su propio botón de barra de tareas. Al restaurar, coloque las ventanas secundarias encima de la ventana principal.

### <a name="input-focus"></a>Foco de entrada

-   **Windows que muestran las acciones** iniciadas por el usuario deben tener el foco de entrada, pero solo si la ventana se representa inmediatamente (en un plazo de 5 segundos). Una vez que se representa la ventana, puede tomar el foco de entrada una vez.
    -   Si una ventana se representa lentamente (más de 5 segundos), es probable que los usuarios realicen otra tarea mientras esperan. Centrarse en este punto sería una molestia, especialmente si se hace más de una vez.
-   **Windows que una acción iniciada por el sistema no muestra o no se muestra inmediatamente, no debe centrarse en la entrada.** En su lugar, se muestra en la parte superior sin el foco y permite que los usuarios los activen cuando estén listos.
    -   **Excepción:** Administrador de credenciales.

### <a name="persistence"></a>Persistencia

-   **Cuando se vuelva a mostrar una ventana, considere la posibilidad de mostrarla en el mismo estado al que se ha accedido por última vez.** Al cerrar, guarde el monitor usado, el tamaño de la ventana, la ubicación y el estado (maximizado frente a restauración). Al volver a mostrar, restaure el tamaño, la ubicación y el estado de la ventana guardados mediante el monitor adecuado. Además, considere la posibilidad de hacer que estos atributos se conserven en todas las instancias del programa por usuario. **Excepciones:**
    -   No guarde ni haga que estos atributos se conserven para las ventanas cuando su uso sea tal que es mucho más probable que los usuarios quieran volver a empezar por completo.
    -   En el caso de los programas que probablemente se usarán Tecnología táctil y Tablet PC de Windows equipos, guarde dos estados de windows para los modos horizontal y vertical. Para obtener más información, [vea Designing for Varying Display Sizes](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Si la configuración actual del monitor impide mostrar una ventana con su último estado:**
    -   Intente mostrar la ventana con su último monitor.
    -   Si la ventana es mayor que el monitor, cambie el tamaño de la ventana según sea necesario.
    -   Mueva la ubicación hacia la esquina superior izquierda para que quepa dentro del monitor según sea necesario.
    -   Si los pasos anteriores no resuelven el problema, vuelva a las directrices de selección de ubicación de ventana predeterminadas. Considere la posibilidad de restaurar el tamaño anterior, si es posible.

 

 