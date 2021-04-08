---
title: Administración de ventanas
description: En este artículo se trata la ubicación predeterminada de las ventanas cuando se muestran inicialmente en la pantalla, el orden de apilamiento con respecto a otras ventanas (orden Z), su tamaño inicial y el modo en que su pantalla afecta al foco de entrada.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dc194741713a139f643ad84b829294577d020d94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003290"
---
# <a name="window-management"></a>Administración de ventanas

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

En este artículo se trata la ubicación predeterminada de las ventanas cuando se muestran inicialmente en la pantalla, el orden de apilamiento con respecto a otras ventanas ([orden Z](glossary.md)), su tamaño inicial y el modo en que su pantalla afecta al foco de entrada.

Para las siguientes directrices:

-   Una ventana de nivel superior no tiene ventana propietaria y se muestra en la barra de tareas. Ejemplos: ventanas de la aplicación. En Windows Vista y versiones posteriores, los cuadros de diálogo sin ventanas de propietario y hojas de propiedades también se consideran de nivel superior.
-   Una ventana de propiedad tiene una ventana propietaria y no se muestra en la barra de tareas. Ejemplos: cuadros de diálogo modales, cuadros de diálogo no modales.
-   Una ventana iniciada por el usuario se muestra como el resultado directo de la acción de un usuario. De lo contrario, el programa se inicia si lo inicia un programa o si el sistema lo inicia Microsoft Windows. Por ejemplo, un cuadro de diálogo de opciones es iniciado por el usuario, pero un recordatorio de reunión es iniciado por el programa.
-   Una ventana contextual es una ventana iniciada por el usuario que tiene una relación fuerte con el objeto desde el que se inició. Por ejemplo, las ventanas que se muestran en los menús contextuales o en los iconos del área de notificación son contextuales, pero no las ventanas que se muestran por barras de menús.
-   El monitor activo es el monitor en el que se ejecuta el programa activo.
-   El monitor predeterminado es el que tiene el menú Inicio, la barra de tareas y el área de notificación.

## <a name="design-concepts"></a>Conceptos de diseño

La administración de ventanas es una de las actividades de usuario más fundamentales. Antes de Windows Vista, a menudo las ventanas tenían pequeños tamaños predeterminados y se colocaban en el centro de la pantalla. Este enfoque funciona bien para los monitores antiguos de baja resolución, pero no para el hardware de vídeo moderno.

Windows está diseñado para admitir hardware de vídeo moderno, que a menudo se ejecuta con resoluciones mucho mayores que la resolución de pantalla mínima admitida y puede tener varios monitores. Lo hace:

-   Permite a los usuarios sacar el máximo partido de su hardware avanzado.
-   Requiere menos esfuerzo por parte de los usuarios para pasar el mouse por más distancias.
-   Hace que la ubicación de las ventanas sea más predecible y, por lo tanto, es más fácil de encontrar.

### <a name="the-minimum-supported-screen-resolution"></a>La resolución de pantalla mínima admitida

La [resolución de pantalla efectiva](glossary.md) mínima admitida por Windows es de 800x600 píxeles. Esto significa que las ventanas de tamaño fijo deben mostrarse por completo en la resolución mínima (mientras se reserva espacio para la barra de tareas), pero las ventanas redimensionables se pueden optimizar para una resolución eficaz de 1024x768 píxeles siempre que sean funcionales en la resolución mínima.

A pesar de que las resoluciones de pantalla físicas más comunes para equipos Windows son de 1024x768 píxeles o más, el destino de 800x600 píxeles permite que Windows:

-   Funcione bien con todo el hardware moderno, incluidos los pequeños equipos portátiles.
-   Compatibilidad con valores altos de PPP (puntos por pulgada).
-   Admitir fuentes mayores para la accesibilidad.
-   Compatibilidad con hardware que se usa de manera global.

La elección de la resolución mínima para la compatibilidad requiere una sorprendenteción del equilibrio adecuado. El destino de una resolución mayor daría como resultado una experiencia no óptima para un porcentaje significativo del hardware moderno, mientras que si se destina a una resolución más baja, impedirá que los diseñadores aprovechen al máximo el espacio disponible de la pantalla.

Si cree que los usuarios de destino usan resoluciones significativamente mayores que el mínimo de Windows, puede diseñar el programa para sacar el máximo partido del espacio de pantalla adicional mediante ventanas de tamaño variable que se escalan bien.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Admitir la resolución efectiva mínima de Windows de 800x600 píxeles.** En el caso de las interfaces de usuario (IUS) críticas que deben funcionar en modo seguro, admiten una resolución efectiva de 640x480 píxeles. Asegúrese de tener en cuenta el espacio que usa la barra de tareas mediante la reserva de 48 [píxeles relativos](glossary.md) verticales para las ventanas que se muestran con la barra de tareas.
-   **Optimice los diseños de ventana de tamaño variable para una resolución efectiva de 1024x768 píxeles.** Cambiar automáticamente el tamaño de estas ventanas para resoluciones de pantalla inferiores de una forma que sigue siendo funcional.
-   **Asegúrese de probar las ventanas en 96 PPP (100 por ciento) a 800x600 píxeles, 120 ppp (125 por ciento) a 1024x768 píxeles y 144 ppp (150 por ciento) en 1200x900 píxeles.** Compruebe si hay problemas de diseño, como el recorte de controles, texto y ventanas, y ajuste de iconos y mapas de bits.
-   **En el caso de los programas con escenarios táctiles y de uso móvil, optimice para 120 ppp.** Actualmente, las pantallas con un alto nivel de PPP están predominantes en PC táctiles y móviles.
-   Las **ventanas de tamaño variable ya no deben mostrar el glifo de redimensionamiento** en la esquina inferior derecha, ya que:
    -   Todos los lados y bordes de una ventana se pueden cambiar de tamaño, no solo la esquina inferior derecha.
    -   El glifo requiere que se muestre una barra de estado, pero muchas ventanas de tamaño variable no proporcionan barras de estado.
    -   Los bordes de ventana de tamaño variable y los punteros de redimensionamiento son más eficaces en la comunicación de que una ventana es de tamaño ajustable que el glifo de redimensionamiento.

### <a name="title-bar-controls"></a>Controles de barra de título

Use los controles de la barra de título de la siguiente manera:

-   **Cercanos.** Todas las ventanas principales y secundarias con un marco de ventana estándar deben tener un botón cerrar en la barra de título. Al hacer clic en cerrar, se cancela o se cierra la ventana.

![captura de pantalla del cuadro de diálogo sin botón cerrar ](images/win-window-mgt-image1.png)

En este ejemplo, el cuadro de diálogo no tiene un botón cerrar en la barra de título.

-   **MiniMIZE.** Todas las ventanas principales y no modales de ejecución prolongada (como los cuadros de diálogo de progreso) deben tener un botón minimizar. Al hacer clic en minimizar, se reduce la ventana a su botón de la barra de tareas. Por lo tanto, las ventanas que se pueden minimizar requieren un icono de barra de título.
-   **Maximizar o restaurar.** Todas las ventanas de tamaño variable deben tener un botón para maximizar o restaurar. Al hacer clic en maximizar, se muestra la ventana en su tamaño más grande, que para la mayoría de las ventanas es pantalla completa. mientras que al hacer clic en restaurar abajo, se muestra la ventana en su tamaño anterior. Sin embargo, algunas ventanas no se benefician del uso de una pantalla completa, por lo que estas ventanas deben maximizar su tamaño más útil.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana predeterminado adecuado para su contenido.** No dude en usar tamaños de ventana iniciales más grandes si puede utilizar el espacio con eficacia.
-   **Use ventanas redimensionables siempre que sea práctico para evitar las barras de desplazamiento y los datos truncados.** Las ventanas con contenido dinámico y listas sacan el máximo partido de las ventanas redimensionables.
-   En el **caso de los documentos de texto, considere una longitud de línea máxima de 65 caracteres** para facilitar la lectura del texto. (Entre los caracteres se incluyen letras, signos de puntuación y espacios).
-   Ventanas de tamaño fijo:
    -   **Debe ser totalmente visible y ajustarse al área de trabajo.**
-   Ventanas redimensionables:
    -   **Puede estar optimizado para resoluciones más altas, pero debe reducirse según sea necesario en el momento de la presentación en la resolución de pantalla real.**
    -   **En el caso de tamaños de ventana progresivamente mayores, debe mostrar progresivamente más información.** Asegúrese de que al menos una parte o un control de la ventana tenga contenido de tamaño variable.
    -   **Debe evitar los tamaños de restauración predeterminados maximizados o casi maximizados.** En su lugar, elija un tamaño predeterminado que normalmente sea el más útil sin tener una pantalla completa. Supongamos que los usuarios maximizarán la ventana en lugar de cambiar el tamaño para que esté en pantalla completa.
    -   **Debe establecer un tamaño de ventana mínimo si hay un tamaño por debajo del cual ya no se puede usar el contenido.** En el caso de los controles de tamaño variable, establezca tamaños de elementos de tamaño mínimo ajustables en sus tamaños funcionales más pequeños, como el ancho mínimo de las columnas funcionales en las vistas de lista.
    -   **Debe cambiar la presentación si esto hace que el contenido se pueda usar en tamaños más pequeños.**

![captura de pantalla de los botones del reproductor de media ](images/win-window-mgt-image2.png)

En este ejemplo, Windows Media Player cambia su formato cuando la ventana se vuelve demasiado pequeña para el formato estándar.

### <a name="window-location"></a>Ubicación de la ventana

-   **En el caso de las siguientes directrices, "centrando" significa que se debe sesgar la posición vertical ligeramente hacia la parte superior del monitor, en lugar de colocarla exactamente en el centro.** Coloque el 45 por ciento del espacio entre la parte superior del monitor/propietario y la parte superior de la ventana, y 55 por ciento entre la parte inferior del monitor/propietario y la parte inferior de la ventana. Haga esto porque el ojo está orientado naturalmente hacia la parte superior de la pantalla.

    ![figura de la ventana colocada ligeramente por encima del centro ](images/win-window-mgt-image3.png)

    "Centrar" significa sesgar la posición vertical ligeramente hacia la parte superior del monitor.

-   **Si una ventana es contextual, mostrarla siempre cerca del objeto desde el que se inició.** Colóquelo fuera del camino para que el objeto de origen no esté incluido en la ventana.

    -   Si se muestra con el mouse, cuando sea posible, colóquelo hacia abajo y hacia la derecha.

    ![figura de la ventana contextual situada a la derecha del objeto ](images/win-window-mgt-image4.png)

    Mostrar las ventanas contextuales cerca del objeto desde el que se inició.

    ![figura de la ventana del área de notificación ](images/win-window-mgt-image5.png)

    Las ventanas iniciadas desde los iconos del área de notificación se muestran cerca del área de notificación.

-   Si se muestra con un lápiz, siempre que sea posible colóquelo de modo que no esté incluido en la mano del usuario. En el caso de los usuarios que se entregan a la derecha, se muestran a la izquierda; de lo contrario, se muestra a la derecha.

    ![figura de la ventana contextual colocada a la izquierda del objeto ](images/win-window-mgt-image6.png)

    Al usar un lápiz, muestre también ventanas contextuales para que no estén incluidas en la mano del usuario.

-   **Desarrolladores:** Puede distinguir entre eventos del mouse y eventos del lápiz mediante la API de [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Puede determinar la [mano](/previous-versions/ms819495(v=msdn.10)) del usuario mediante la API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ GETMENUDROPALIGNMENT.
-   **Coloque los cuadros de diálogo de progreso fuera del camino en la esquina inferior derecha del monitor activo.**

    ![figura de la barra de progreso en la esquina inferior derecha ](images/win-window-mgt-image7.png)

    Coloque los cuadros de diálogo de progreso en la esquina inferior derecha.

-   **Si una ventana no está relacionada con el contexto o la acción del usuario actual, colóquela fuera de la ubicación actual del puntero.** De este modo, se evita la interacción accidental.
-   **Si una ventana es una aplicación de nivel superior o un documento, siempre debe poner en cascada su origen en la esquina superior izquierda del monitor.** Si el programa activo lo crea, use el monitor activo; de lo contrario, use el monitor predeterminado.

    ![figura de tres ventanas en cascada de la parte superior izquierda ](images/win-window-mgt-image8.png)

    Las ventanas de documento o de aplicación de nivel superior en cascada se desconectan de la esquina superior izquierda del monitor.

-   **Si una ventana es una utilidad de nivel superior, mostrarla siempre "centrada" en el monitor.** Si el programa activo lo crea, use el monitor activo; de lo contrario, use el monitor predeterminado.

    ![figura de la ventana de la utilidad centrada en el monitor ](images/win-window-mgt-image9.png)

    Centrar las ventanas de la utilidad de nivel superior.

-   **Si una ventana es propiedad, se muestra inicialmente "centrada" en la parte superior de la ventana propietaria.** En el caso de las pantallas posteriores, considere la posibilidad de mostrarla en su última ubicación (relativa a la ventana propietaria) si es probable que sea más conveniente.

    ![figura de la ventana de propiedad centrada en la ventana propietaria ](images/win-window-mgt-image10.png)

    Centrar las ventanas de la propiedad en la parte superior de la ventana propietaria.

-   **En los cuadros de diálogo no modales, siempre se muestra inicialmente en la parte superior de la ventana propietaria para facilitar su búsqueda.** Sin embargo, si el usuario activa la ventana propietaria, puede ocultar el cuadro de diálogo no modal.

    ![figura del cuadro de diálogo no modal en la ventana propietaria ](images/win-window-mgt-image11.png)

    Muestre cuadros de diálogo no modales inicialmente en la parte superior de la ventana propietaria para que sean fáciles de encontrar.

-   **Si es necesario, ajuste la ubicación inicial para que toda la ventana esté visible dentro del monitor de destino.** Si una ventana de tamaño superior es mayor que el monitor de destino, reduzca su tamaño.

### <a name="window-order-z-order"></a>Orden de ventana (orden Z)

-   **Coloque las ventanas de propiedad siempre en la parte superior de la ventana propietaria.** No coloque nunca las ventanas de propiedad bajo sus ventanas propietarias, ya que los usuarios más probables no las verán.
-   **Respetar la selección del orden Z de los usuarios. Cuando los usuarios seleccionan una ventana, solo tiene que hacer que las ventanas asociadas a esa instancia del programa (la ventana más cualquier propietario o ventanas pertenecientes) se coloquen en la parte superior del orden Z.** No cambie el orden de ninguna otra ventana, como las instancias independientes del mismo programa.

### <a name="window-activation"></a>Activación de ventanas

-   **Respetar la selección del estado de la ventana de los usuarios. Si una ventana existente necesita atención, parpadee el botón de la barra de tareas tres veces para atraer la atención y dejarla resaltada, pero no haga nada más.** No restaure ni active la ventana. No utilice efectos sonoros. En su lugar, permita a los usuarios activar la ventana cuando estén listas.
    -   **Excepción:** Si la ventana no aparece en la barra de tareas, póngalo en la parte superior de todas las demás ventanas y, en su lugar, en la barra de título.
-   **La restauración de una ventana principal también debe restaurar todas las ventanas secundarias**, incluso si esas ventanas secundarias tienen su propio botón de la barra de tareas. Al restaurar, coloque las ventanas secundarias en la parte superior de la ventana principal.

### <a name="input-focus"></a>Foco de entrada

-   Las **ventanas que se muestran mediante acciones iniciadas por el usuario deben tomar el foco de entrada, pero solo si la ventana se representa inmediatamente** (en menos de 5 segundos). Una vez que se representa la ventana, puede tomar el foco de entrada una vez.
    -   Si una ventana se representa lentamente (más de 5 segundos), es probable que los usuarios realicen otra tarea mientras esperan. Tomar el foco en este punto sería una molestia, especialmente si se realiza más de una vez.
-   **Las ventanas que no se muestran ni muestran inmediatamente en una acción iniciada por el sistema no deben tener el foco de entrada.** En su lugar, se muestra en la parte superior sin foco y permite que los usuarios los activen cuando estén listos.
    -   **Excepción:** Administrador de credenciales.

### <a name="persistence"></a>Persistencia

-   **Cuando se vuelva a mostrar una ventana, considere la posibilidad de mostrarla en el mismo estado en el que se ha tenido acceso por última vez.** Al cerrar, guarde el monitor usado, el tamaño de la ventana, la ubicación y el estado (maximizado frente a restauración). Al volver a mostrar, restaure el tamaño, la ubicación y el estado de la ventana guardada con el monitor adecuado. Además, considere la posibilidad de hacer que estos atributos persistan entre instancias de programa por usuario. **Excepciones:**
    -   No guarde o haga que estos atributos se conserven para Windows cuando su uso sea tal que los usuarios tengan mucho más probabilidades de comenzar a usarse por completo.
    -   En el caso de los programas que puedan usarse en equipos con tecnología táctil y de tabletas de Windows, guarde dos Estados de Windows para los modos horizontal y vertical. Para obtener más información, vea [diseñar para tamaños de pantalla diferentes](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Si la configuración del monitor actual impide que se muestre una ventana con su último estado:**
    -   Intente Mostrar la ventana con el último monitor.
    -   Si la ventana es mayor que el monitor, cambie el tamaño de la ventana según sea necesario.
    -   Mueva la ubicación hacia la esquina superior izquierda para que quepa en el monitor según sea necesario.
    -   Si los pasos anteriores no solucionan el problema, vuelva a las instrucciones de selección de ubicación de la ventana predeterminada. Considere la posibilidad de restaurar el tamaño anterior, si es posible.

 

 