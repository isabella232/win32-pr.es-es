---
description: En esta información general se describen las características de Windows, como los tipos de ventana, los Estados, el tamaño y la posición.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Características de las ventanas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228c6b4ab59102cae38a248935fbbad32198f2e0
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105661418"
---
# <a name="window-features"></a>Características de las ventanas

En esta información general se describen las características de Windows, como los tipos de ventana, los Estados, el tamaño y la posición.

-   [Tipos de ventana](#window-types)
    -   [Ventanas superpuestas](#overlapped-windows)
    -   [Ventanas emergentes](#pop-up-windows)
    -   [Ventanas secundarias](#child-windows)
        -   [Posición](#positioning)
        -   [Recorte](#clipping)
        -   [Relación con la ventana primaria](#relationship-to-parent-window)
        -   [Mensajes](#size-and-position-messages)
    -   [Ventanas superpuestas](#layered-windows)
    -   [Solo mensajes de Windows](#message-only-windows)
-   [Relaciones de ventanas](#window-relationships)
    -   [Ventanas de primer y segundo plano](#foreground-and-background-windows)
    -   [Ventanas de propiedad](#owned-windows)
    -   [Orden Z](#z-order)
-   [Estado de la ventana Mostrar](#window-show-state)
    -   [Ventana activa](#active-window)
    -   [Ventanas deshabilitadas](#disabled-windows)
    -   [Visibilidad de la ventana](#window-visibility)
    -   [Ventanas minimizadas, maximizadas y restauradas](#minimized-maximized-and-restored-windows)
-   [Tamaño y posición de la ventana](#window-size-and-position)
    -   [Tamaño y posición predeterminados](#default-size-and-position)
    -   [Tamaño de seguimiento](#tracking-size)
    -   [Comandos del sistema](#system-commands)
    -   [Funciones de tamaño y posición](#size-and-position-functions)
    -   [Mensajes de tamaño y posición](#size-and-position-messages)
-   [Animación de ventana](#window-animation)
-   [Diseño y creación de reflejo de ventanas](#window-layout-and-mirroring)
    -   [Cuadros de diálogo de creación de reflejo y cuadros de mensaje](#mirroring-dialog-boxes-and-message-boxes)
    -   [Contextos de dispositivo de creación de reflejo no asociados a una ventana](#mirroring-device-contexts-not-associated-with-a-window)
-   [Destrucción de ventanas](#window-destruction)

## <a name="window-types"></a>Tipos de ventana

Esta sección contiene los siguientes temas que describen los tipos de ventana.

-   [Ventanas superpuestas](#overlapped-windows)
-   [Ventanas emergentes](#pop-up-windows)
-   [Ventanas secundarias](#child-windows)
-   [Ventanas superpuestas](#layered-windows)
-   [Solo mensajes de Windows](#message-only-windows)

### <a name="overlapped-windows"></a>Ventanas superpuestas

Una *ventana superpuesta* es una ventana de nivel superior (ventana no secundaria) que tiene una barra de título, un borde y un área de cliente. está diseñado para actuar como ventana principal de una aplicación. También puede tener un menú ventana, botones minimizar y maximizar y barras de desplazamiento. Una ventana superpuesta utilizada como ventana principal incluye normalmente todos estos componentes.

Al especificar el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ OVERLAPPEDWINDOW** en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , una aplicación crea una ventana superpuesta. Si usa el estilo **WS \_ superpuesto** , la ventana tiene una barra de título y un borde. Si usa el estilo **WS \_ OVERLAPPEDWINDOW** , la ventana tiene una barra de título, un borde de tamaño, un menú ventana y botones minimizar y maximizar.

### <a name="pop-up-windows"></a>Ventanas emergentes

Una *ventana emergente* es un tipo especial de ventana superpuesta que se usa para cuadros de diálogo, cuadros de mensaje y otras ventanas temporales que aparecen fuera de la ventana principal de una aplicación. Las barras de título son opcionales para las ventanas emergentes; de lo contrario, las ventanas emergentes son las mismas que las ventanas superpuestas de [**WS \_**](window-styles.md) .

Para crear una ventana emergente, especifique el estilo de [**\_ elemento emergente WS**](window-styles.md) en [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Para incluir una barra de título, especifique el estilo de **\_ título de WS** . Use el estilo **WS \_ POPUPWINDOW** para crear una ventana emergente que tenga un borde y un menú ventana. El estilo de **\_ título de WS** se debe combinar con el estilo **WS \_ POPUPWINDOW** para que el menú ventana esté visible.

### <a name="child-windows"></a>Ventanas secundarias

Una *ventana secundaria* tiene el estilo [**WS \_ secundario**](window-styles.md) y se limita al área cliente de su ventana primaria. Normalmente, una aplicación usa ventanas secundarias para dividir el área de cliente de una ventana primaria en áreas funcionales. Puede crear una ventana secundaria especificando el estilo **\_ secundario WS** en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Una ventana secundaria debe tener una ventana primaria. La ventana primaria puede ser una ventana superpuesta, una ventana emergente o incluso otra ventana secundaria. La ventana primaria se especifica cuando se llama a [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Si especifica el estilo [**\_ secundario WS**](window-styles.md) en **CreateWindowEx** pero no especifica una ventana primaria, el sistema no crea la ventana.

Una ventana secundaria tiene un área cliente pero no tiene otras características, a menos que se soliciten explícitamente. Una aplicación puede solicitar una barra de título, un menú ventana, botones minimizar y maximizar, un borde y barras de desplazamiento para una ventana secundaria, pero una ventana secundaria no puede tener un menú. Si la aplicación especifica un identificador de menú, bien cuando registra la clase de ventana secundaria o crea la ventana secundaria, se omite el identificador de menú. Si no se especifica ningún estilo de borde, el sistema crea una ventana sin borde. Una aplicación puede usar ventanas secundarias sin borde para dividir el área de cliente de una ventana primaria mientras mantiene las divisiones invisibles para el usuario.

En esta sección se describen los siguientes aspectos de las ventanas secundarias:

-   [Posición](#positioning)
-   [Recorte](#clipping)
-   [Relación con la ventana primaria](#relationship-to-parent-window)
-   [Mensajes](#size-and-position-messages)

#### <a name="positioning"></a>Posición

El sistema siempre coloca una ventana secundaria en relación con la esquina superior izquierda del área de cliente de su ventana primaria. Ninguna parte de una ventana secundaria aparece nunca fuera de los bordes de la ventana primaria. Si una aplicación crea una ventana secundaria que es mayor que la ventana primaria o coloca una ventana secundaria para que una o todas las ventanas secundarias se expandan más allá de los bordes del elemento primario, el sistema recorta la ventana secundaria; es decir, no se muestra la parte fuera del área cliente de la ventana primaria. Las acciones que afectan a la ventana primaria también pueden afectar a la ventana secundaria, como se indica a continuación.



| Ventana primaria | Ventana secundaria                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Destruido     | Se destruye antes de que se destruya la ventana primaria.                                                                         |
| Hidden        | Oculto antes de que se oculte la ventana primaria. Una ventana secundaria solo es visible cuando la ventana primaria está visible.             |
| Puesto         | Se mueve con el área de cliente de la ventana primaria. La ventana secundaria es responsable de pintar su área cliente después del movimiento. |
| Aparece         | Se muestra después de mostrar la ventana primaria.                                                                                  |



 

#### <a name="clipping"></a>Recorte

El sistema no recorta automáticamente una ventana secundaria del área de cliente de la ventana primaria. Esto significa que la ventana primaria dibuja sobre la ventana secundaria si lleva a cabo cualquier dibujo en la misma ubicación que la ventana secundaria. Sin embargo, el sistema recorta la ventana secundaria del área de cliente de la ventana primaria si la ventana primaria tiene el estilo [**WS \_ CLIPCHILDREN**](window-styles.md) . Si la ventana secundaria está recortada, la ventana primaria no puede dibujar sobre ella.

Una ventana secundaria puede superponerse A otras ventanas secundarias en el mismo área cliente. Una ventana secundaria que comparte la misma ventana primaria que una o varias ventanas secundarias se denomina *ventana relacionada*. Las ventanas relacionadas pueden dibujarse en el área de cliente de los demás, a menos que una de las ventanas secundarias tenga el estilo [**WS \_ CLIPSIBLINGS**](window-styles.md) . Si una ventana secundaria tiene este estilo, se recorta cualquier parte de la ventana relacionada que se encuentra dentro de la ventana secundaria.

Si una ventana tiene el estilo [**WS \_ CLIPCHILDREN**](window-styles.md) o **WS \_ CLIPSIBLINGS** , se produce una ligera pérdida de rendimiento. Cada ventana ocupa recursos del sistema, por lo que una aplicación no debe utilizar indiscriminadamente ventanas secundarias. Para obtener el mejor rendimiento, una aplicación que necesita dividir lógicamente su ventana principal debería hacerlo en el procedimiento de ventana de la ventana principal, en lugar de usar ventanas secundarias.

#### <a name="relationship-to-parent-window"></a>Relación con la ventana primaria

Una aplicación puede cambiar la ventana primaria de una ventana secundaria existente llamando a la función [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent) . En este caso, el sistema quita la ventana secundaria del área cliente de la ventana primaria anterior y la mueve al área cliente de la nueva ventana primaria. Si **SetParent** especifica un identificador **nulo** , la ventana del escritorio se convierte en la nueva ventana primaria. En este caso, la ventana secundaria se dibuja en el escritorio, fuera de los bordes de cualquier otra ventana. La función [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) recupera un identificador de la ventana primaria de una ventana secundaria.

La ventana primaria deja una parte de su área de cliente en una ventana secundaria y la ventana secundaria recibe todas las entradas de esta área. La clase Window no debe ser la misma para cada una de las ventanas secundarias de la ventana primaria. Esto significa que una aplicación puede rellenar una ventana primaria con ventanas secundarias que tienen un aspecto diferente y llevan a cabo diferentes tareas. Por ejemplo, un cuadro de diálogo puede contener muchos tipos de controles, cada uno de los cuales es una ventana secundaria que acepta distintos tipos de datos del usuario.

Una ventana secundaria tiene solo una ventana primaria, pero un elemento primario puede tener cualquier número de ventanas secundarias. Cada ventana secundaria, a su vez, puede tener ventanas secundarias. En esta cadena de ventanas, cada ventana secundaria se denomina ventana descendiente de la ventana primaria original. Una aplicación utiliza la función [**ischild (**](/windows/win32/api/winuser/nf-winuser-ischild) para detectar si una ventana determinada es una ventana secundaria o una ventana descendiente de una ventana primaria determinada.

La función [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) enumera las ventanas secundarias de una ventana primaria. A continuación, **EnumChildWindows** pasa el identificador de cada ventana secundaria a una función de devolución de llamada definida por la aplicación. También se enumeran las ventanas descendientes de la ventana primaria especificada.

#### <a name="messages"></a>error de Hadoop

El sistema pasa los mensajes de entrada de una ventana secundaria directamente a la ventana secundaria; los mensajes no se pasan a través de la ventana primaria. La única excepción es que la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) haya deshabilitado la ventana secundaria. En este caso, el sistema pasa a la ventana primaria todos los mensajes de entrada que hubieran ido a la ventana secundaria. Esto permite que la ventana primaria examine los mensajes de entrada y habilite la ventana secundaria, si es necesario.

Una ventana secundaria puede tener un identificador entero único. Los identificadores de las ventanas secundarias son importantes cuando se trabaja con ventanas de control. Una aplicación dirige la actividad de un control mediante el envío de mensajes. La aplicación usa el identificador de la ventana secundaria del control para dirigir los mensajes al control. Además, un control envía mensajes de notificación a su ventana primaria. Un mensaje de notificación incluye el identificador de la ventana secundaria del control, que el elemento primario usa para identificar qué control envió el mensaje. Una aplicación especifica el identificador de la ventana secundaria para otros tipos de ventanas secundarias estableciendo el parámetro *hMenu* de la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) en un valor en lugar de un identificador de menú.

### <a name="layered-windows"></a>Ventanas superpuestas

El uso de una ventana superpuesta puede mejorar significativamente el rendimiento y los efectos visuales de una ventana que tiene una forma compleja, anima su forma o desea usar efectos de combinación alfa. El sistema crea y vuelve a dibujar automáticamente ventanas superpuestas y las ventanas de las aplicaciones subyacentes. Como resultado, las ventanas superpuestas se representan sin problemas, sin el parpadeo típico de las regiones de ventana complejas. Además, las ventanas superpuestas pueden ser parcialmente translúcidas, es decir, de mezcla alfa.

Para crear una ventana en capas, especifique el estilo de ventana extendida de **WS \_ ex con \_ capas** al llamar a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , o llame a la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para establecer WS- **ex en \_ \_ capas** después de crear la ventana. Después de la llamada a **CreateWindowEx** , la ventana superpuesta no estará visible hasta que se llame a la función [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) o [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) para esta ventana.

> [!Note]  
> A partir de Windows 8, la **\_ \_ capa de WS ex** se puede usar con ventanas secundarias y ventanas de nivel superior. Las versiones anteriores de Windows admiten **WS \_ ex en \_ capas** solo para las ventanas de nivel superior.

 

Para establecer el nivel de opacidad o la clave de color de transparencia para una ventana en capas determinada, llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Después de la llamada, el sistema puede seguir solicitando a la ventana que pinte cuando se muestra o cambia el tamaño de la ventana. Sin embargo, dado que el sistema almacena la imagen de una ventana superpuesta, el sistema no pedirá a la ventana que pinte si se revela parte de ella como resultado de los movimientos de ventana relativos en el escritorio. No es necesario que las aplicaciones heredadas reestructuren su código de dibujo si quieren agregar translucidez o efectos de transparencia para una ventana, ya que el sistema redirige el dibujo de las ventanas que llamaron a **SetLayeredWindowAttributes** a la memoria fuera de la pantalla y la recompone para lograr el efecto deseado.

Para una animación más rápida y eficaz o si se necesita alfa por píxel, llame a [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** debe usarse principalmente cuando la aplicación debe proporcionar directamente la forma y el contenido de una ventana superpuesta, sin usar el mecanismo de redirección que proporciona el sistema a través de [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Además, el uso de **UpdateLayeredWindow** usa directamente la memoria de forma más eficaz, porque el sistema no necesita la memoria adicional necesaria para almacenar la imagen de la ventana redirigida. Para obtener la máxima eficacia en la animación de ventanas, llame a **UpdateLayeredWindow** para cambiar la posición y el tamaño de una ventana superpuesta. Tenga en cuenta que, una vez que se ha llamado a **SetLayeredWindowAttributes** , se producirá un error en las llamadas posteriores a **UpdateLayeredWindow** hasta que el bit de estilo de capas se borre y se vuelva a establecer.

La prueba de posicionamiento de una ventana superpuesta se basa en la forma y la transparencia de la ventana. Esto significa que las áreas de la ventana que tienen una clave de color o cuyo valor alfa es cero permitirán que el mouse pase por los mensajes. Sin embargo, si la ventana superpuesta tiene el estilo de ventana extendida **WS \_ ex \_ transparente** , se omitirá la forma de la ventana superpuesta y los eventos del mouse se pasarán a otras ventanas debajo de la ventana superpuesta.

### <a name="message-only-windows"></a>Message-Only Windows

Una *ventana de solo mensaje* le permite enviar y recibir mensajes. No es visible, no tiene ningún orden z, no se puede enumerar y no recibe mensajes de difusión. La ventana simplemente envía los mensajes.

Para crear una ventana de solo mensaje, especifique la constante de [ \_ mensaje HWND](#message-only-windows) o un identificador para una ventana de solo mensaje existente en el parámetro *HWndParent* de la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . También puede cambiar una ventana existente a una ventana de solo mensaje especificando \_ el mensaje HWND en el parámetro *hWndNewParent* de la función [**SetParent**](/windows/win32/api/winuser/nf-winuser-setparent) .

Para buscar ventanas de solo mensaje, especifique [el \_ mensaje HWND](#message-only-windows) en el parámetro *HwndParent* de la función [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) . Además, **FindWindowEx** busca en las ventanas de solo mensajes, así como en las ventanas de nivel superior, si los parámetros *hwndParent* y *hwndChildAfter* son **null**.

## <a name="window-relationships"></a>Relaciones de ventanas

Hay muchas maneras en las que una ventana se puede relacionar con el usuario u otra ventana. Una ventana puede ser una ventana de propiedad, una ventana de primer plano o una ventana de fondo. Una ventana también tiene un orden z relativo a otras ventanas. Para obtener más información, vea los temas siguientes:

-   [Ventanas de primer y segundo plano](#foreground-and-background-windows)
-   [Ventanas de propiedad](#owned-windows)
-   [Orden Z](#z-order)

### <a name="foreground-and-background-windows"></a>Ventanas de primer y segundo plano

Cada proceso puede tener varios subprocesos de ejecución y cada subproceso puede crear ventanas. El subproceso que creó la ventana con la que el usuario está trabajando actualmente se denomina subproceso en primer plano y la ventana se denomina *ventana de primer plano*. Todos los demás subprocesos son subprocesos en segundo plano y las ventanas creadas por subprocesos en segundo plano se denominan *ventanas en segundo plano*.

Cada subproceso tiene un nivel de prioridad que determina la cantidad de tiempo de CPU que recibe el subproceso. Aunque una aplicación puede establecer el nivel de prioridad de sus subprocesos, normalmente el subproceso en primer plano tiene un nivel de prioridad ligeramente superior al de los subprocesos en segundo plano. Dado que tiene una prioridad más alta, el subproceso en primer plano recibe más tiempo de CPU que los subprocesos en segundo plano. El subproceso en primer plano tiene una prioridad base normal de 9; un subproceso en segundo plano tiene una prioridad base normal de 7.

El usuario establece la ventana de primer plano haciendo clic en una ventana o mediante la combinación de teclas ALT + TAB o ALT + ESC. Para recuperar un identificador de la ventana de primer plano, use la función [**GetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) . Para comprobar si la ventana de la aplicación es la ventana de primer plano, compare el identificador devuelto por **GetForegroundWindow** con el de la ventana de la aplicación.

Una aplicación establece la ventana de primer plano mediante la función [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) .

El sistema restringe los procesos que pueden establecer la ventana de primer plano. Un proceso solo puede establecer la ventana de primer plano si:

- Se cumplen todas las condiciones siguientes:
  - El proceso que llama a **SetForegroundWindow** pertenece a una aplicación de escritorio, no una aplicación para UWP o una aplicación de la tienda Windows diseñada para Windows 8 o 8,1.
  - El proceso en primer plano no ha deshabilitado las llamadas a **SetForegroundWindow** mediante una llamada anterior a la función [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .
  - Expiró el tiempo de espera de bloqueo en primer plano (consulte [ **SPI_GETFOREGROUNDLOCKTIMEOUT** en **SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - No hay menús activos.
- Además, al menos una de las siguientes condiciones es verdadera:
  - El proceso de llamada es el proceso en primer plano.
  - El proceso en primer plano inició el proceso de llamada.
  - Actualmente no hay ninguna ventana de primer plano y, por tanto, ningún proceso en primer plano.
  - El proceso de llamada recibió el último evento de entrada.
  - Se está depurando el proceso en primer plano o el proceso de llamada.

Es posible que se deniegue el derecho a un proceso para establecer la ventana de primer plano aunque cumpla estas condiciones.

Un proceso que puede establecer la ventana de primer plano puede permitir que otro proceso establezca la ventana de primer plano mediante una llamada a la función [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) o mediante una llamada a la función [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) con la marca **BSF \_ ALLOWSFW** . El proceso en primer plano puede deshabilitar las llamadas a [**SetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) llamando a la función [**LockSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow) .

### <a name="owned-windows"></a>Ventanas de propiedad

Una ventana superpuesta o emergente puede pertenecer a otra ventana emergente o superpuesta. Ser propiedad coloca varias restricciones en una ventana.

-   Una ventana propiedad siempre está por encima de su propietario en el orden z.
-   El sistema destruye automáticamente una ventana propiedad cuando se destruye su propietario.
-   Una ventana de propiedad se oculta cuando se minimiza su propietario.

Solo una ventana superpuesta o emergente puede ser una ventana propietaria; una ventana secundaria no puede ser una ventana propietaria. Una aplicación crea una ventana propiedad especificando el identificador de ventana del propietario como el parámetro *hwndParent* de [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) cuando crea una ventana con el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ popup** . El parámetro *hwndParent* debe identificar una ventana superpuesta o emergente. Si *hwndParent* identifica una ventana secundaria, el sistema asigna la propiedad a la ventana primaria de nivel superior de la ventana secundaria. Después de crear una ventana de propiedad, una aplicación no puede transferir la propiedad de la ventana a otra ventana.

Los cuadros de diálogo y cuadros de mensaje son ventanas de propiedad de forma predeterminada. Una aplicación especifica la ventana propietaria al llamar a una función que crea un cuadro de diálogo o un cuadro de mensaje.

Una aplicación puede usar la función [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con la marca de **\_ propietario de GW** para recuperar un identificador del propietario de una ventana.

### <a name="z-order"></a>Orden Z

El *orden z* de una ventana indica la posición de la ventana en una pila de ventanas superpuestas. Esta pila de ventana está orientada a lo largo de un eje imaginario, el eje z, que se extiende hacia afuera desde la pantalla. La ventana situada en la parte superior del orden z se superpone a todas las demás ventanas. Todas las demás ventanas superponen la ventana situada en la parte inferior del orden z.

El sistema mantiene el orden z en una sola lista. Agrega ventanas al orden z en función de si son las ventanas de nivel superior, las ventanas de nivel superior o las ventanas secundarias. Una *ventana superior* se superpone a todas las demás ventanas que no son de nivel superior, independientemente de si se trata de la ventana activa o de primer plano. Una ventana superior tiene el estilo **WS \_ ex \_ más alto** . Todas las ventanas de nivel superior aparecen en el orden z antes que las ventanas que no son de nivel superior. Una ventana secundaria se agrupa con su elemento primario en orden z.

Cuando una aplicación crea una ventana, el sistema la coloca en la parte superior del orden z para ventanas del mismo tipo. Puede usar la función [**BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) para mostrar una ventana en la parte superior del orden z para ventanas del mismo tipo. Puede reorganizar el orden z mediante las funciones [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) y [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) .

El usuario cambia el orden z activando una ventana diferente. El sistema coloca la ventana activa en la parte superior del orden z para ventanas del mismo tipo. Cuando una ventana se encuentra en la parte superior del orden z, por tanto, realice sus ventanas secundarias. Puede usar la función [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) para buscar en todas las ventanas secundarias de una ventana primaria y devolver un identificador a la ventana secundaria más alta en orden z. La función [**GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) recupera un identificador de la ventana siguiente o anterior en el orden z.

## <a name="window-show-state"></a>Estado de la ventana Mostrar

En un momento dado, una ventana puede estar activa o inactiva. oculto o visible; y minimizado, maximizado o restaurado. Estas cualidades se conocen colectivamente como el estado de la *ventana*. En los temas siguientes se describe el estado de la ventana Mostrar:

-   [Ventana activa](#active-window)
-   [Ventanas deshabilitadas](#disabled-windows)
-   [Visibilidad de la ventana](#window-visibility)
-   [Ventanas minimizadas, maximizadas y restauradas](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Ventana activa

Una *ventana activa* es la ventana de nivel superior de la aplicación con la que el usuario trabaja actualmente. Para que el usuario pueda identificar fácilmente la ventana activa, el sistema la coloca en la parte superior del orden z y cambia el color de la barra de título y el borde a los colores de la ventana activa definidos por el sistema. Solo una ventana de nivel superior puede ser una ventana activa. Cuando el usuario trabaja con una ventana secundaria, el sistema activa la ventana primaria de nivel superior asociada a la ventana secundaria.

Solo una ventana de nivel superior del sistema está activa a la vez. El usuario activa una ventana de nivel superior haciendo clic en ella (o en una de sus ventanas secundarias) o mediante la combinación de teclas ALT + ESC o ALT + TAB. Una aplicación activa una ventana de nivel superior mediante una llamada a la función [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Otras funciones pueden hacer que el sistema Active una ventana de nivel superior diferente, como [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos), [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)y [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow). Aunque una aplicación puede activar una ventana de nivel superior diferente en cualquier momento, para evitar confundir al usuario, debería hacerlo solo en respuesta a una acción del usuario. Una aplicación utiliza la función [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) para recuperar un identificador de la ventana activa.

Cuando la activación cambia de una ventana de nivel superior de una aplicación a la ventana de nivel superior de otra, el sistema envía un mensaje de [**WM \_ ACTIVATEAPP**](wm-activateapp.md) a ambas aplicaciones y le notifica el cambio. Cuando la activación cambia a una ventana de nivel superior diferente en la misma aplicación, el sistema envía un mensaje de [**\_ activación**](../inputdev/wm-activate.md) de Windows a WM.

### <a name="disabled-windows"></a>Ventanas deshabilitadas

Una ventana se puede deshabilitar. Una *ventana deshabilitada* no recibe ninguna entrada de teclado ni de mouse del usuario, pero puede recibir mensajes de otras ventanas, de otras aplicaciones y del sistema. Normalmente, una aplicación deshabilita una ventana para evitar que el usuario Use la ventana. Por ejemplo, una aplicación puede deshabilitar un botón de comando en un cuadro de diálogo para evitar que el usuario lo seleccione. Una aplicación puede habilitar una ventana deshabilitada en cualquier momento; al habilitar una ventana se restaura la entrada normal.

De forma predeterminada, una ventana se habilita cuando se crea. Sin embargo, una aplicación puede especificar el estilo de [**WS \_ deshabilitado**](window-styles.md) para deshabilitar una nueva ventana. Una aplicación habilita o deshabilita una ventana existente mediante la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) . El sistema envía un mensaje de [**\_ habilitación de WM**](wm-enable.md) a una ventana cuando su estado habilitado está a punto de cambiar. Una aplicación puede determinar si una ventana está habilitada mediante la función [**IsWindowEnabled**](/windows/win32/api/winuser/nf-winuser-iswindowenabled) .

Cuando se deshabilita una ventana secundaria, el sistema pasa los mensajes de entrada del mouse del elemento secundario a la ventana primaria. El elemento primario usa los mensajes para determinar si se debe habilitar la ventana secundaria. Para obtener más información, vea [entrada del mouse](../inputdev/mouse-input.md).

Solo una ventana a la vez puede recibir entradas del teclado; se dice que la ventana tiene el foco de teclado. Si una aplicación usa la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) para deshabilitar una ventana de foco del teclado, la ventana pierde el foco del teclado además de deshabilitarse. A continuación, **EnableWindow** establece el foco de teclado en **null**, lo que significa que no hay ninguna ventana que tenga el foco. Si una ventana secundaria, u otra ventana descendiente, tiene el foco de teclado, la ventana descendiente pierde el foco cuando la ventana primaria está deshabilitada. Para obtener más información, consulte [entrada de teclado](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Visibilidad de la ventana

Una ventana puede estar visible u oculta. El sistema muestra una *ventana visible* en la pantalla. Oculta una *ventana oculta* , no la dibuja. Si la ventana está visible, el usuario puede introducir información en la ventana y ver los resultados de la misma. Si una ventana está oculta, en realidad está deshabilitada. Una ventana oculta puede procesar mensajes del sistema o de otras ventanas, pero no puede procesar los datos de entrada del usuario ni mostrar los de salida. Una aplicación establece el estado de visibilidad de una ventana al crear la ventana. Posteriormente, la aplicación puede cambiar el estado de visibilidad.

Una ventana está visible cuando se establece el estilo [**\_ visible de WS**](window-styles.md) para la ventana. De forma predeterminada, la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una ventana oculta a menos que la aplicación especifique el estilo **\_ visible de WS** . Normalmente, una aplicación establece el **estilo \_ visible de WS** después de haber creado una ventana para mantener los detalles del proceso de creación oculto del usuario. Por ejemplo, una aplicación puede mantener oculta una ventana nueva mientras Personaliza la apariencia de la ventana. Si el estilo de **WS \_ visible** se especifica en **CreateWindowEx**, el sistema envía el mensaje de [**WM \_ SHOWWINDOW**](wm-showwindow.md) a la ventana después de crear la ventana, pero antes de mostrarla.

Una aplicación puede determinar si una ventana es visible mediante la función [**IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) . Una aplicación puede mostrar (hacer visible) u ocultar una ventana mediante las funciones [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)o [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Estas funciones muestran u ocultan una ventana al establecer o quitar el estilo [**\_ visible de WS**](window-styles.md) para la ventana. También envían el mensaje [**de \_ WM de WM**](wm-showwindow.md) a la ventana antes de mostrarla u ocultarla.

Cuando se minimiza una ventana propietaria, el sistema oculta automáticamente las ventanas de propiedad asociadas. Del mismo modo, cuando se restaura una ventana propietaria, el sistema muestra automáticamente las ventanas de propiedad asociadas. En ambos casos, el sistema envía el mensaje de [**WM \_ SHOWWINDOW**](wm-showwindow.md) a las ventanas de la propiedad antes de ocultarlas o mostrarlas. En ocasiones, es posible que una aplicación tenga que ocultar las ventanas de propiedad sin tener que minimizar u ocultar el propietario. En este caso, la aplicación usa la función [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) . Esta función establece o quita el [**estilo \_ visible de WS**](window-styles.md) para todas las ventanas que son propiedad y envía el mensaje de **WM \_ SHOWWINDOW** a las ventanas de la propiedad antes de ocultarlas o mostrarlas. Ocultar una ventana de propietario no tiene ningún efecto en el estado de visibilidad de las ventanas de propiedad.

Cuando una ventana primaria está visible, las ventanas secundarias asociadas también están visibles. Del mismo modo, cuando se oculta la ventana primaria, también se ocultan sus ventanas secundarias. Minimizar la ventana primaria no tiene ningún efecto en el estado de visibilidad de las ventanas secundarias; es decir, las ventanas secundarias se minimizan junto con el elemento primario, pero el estilo [**WS \_ visible**](window-styles.md) no cambia.

Aunque una ventana tenga el estilo [**\_ visible de WS**](window-styles.md) , es posible que el usuario no pueda ver la ventana en la pantalla; otras ventanas pueden superponerse por completo o puede que se haya colocado más allá del borde de la pantalla. Además, una ventana secundaria visible está sujeta a las reglas de recorte establecidas por su relación de elementos primarios y secundarios. Si la ventana primaria de la ventana no está visible, tampoco estará visible. Si la ventana primaria se desplaza más allá del borde de la pantalla, la ventana secundaria también se mueve porque se dibuja una ventana secundaria con respecto a la esquina superior izquierda del elemento primario. Por ejemplo, un usuario puede desplace la ventana primaria que contiene la ventana secundaria lo suficientemente lejos fuera del borde de la pantalla que es posible que el usuario no pueda ver la ventana secundaria, aunque la ventana secundaria y la ventana primaria tengan el estilo **\_ visible de WS** .

### <a name="minimized-maximized-and-restored-windows"></a>Ventanas minimizadas, maximizadas y restauradas

Una *ventana maximizada* es una ventana que tiene el estilo [**WS \_ Maximize**](window-styles.md) . De manera predeterminada, el sistema agranda una ventana maximizada para que ocupe toda la pantalla o, en el caso de las ventanas secundarias, toda el área de cliente de la ventana primaria. Aunque el tamaño de una ventana se puede establecer en el mismo tamaño de una ventana maximizada, una ventana maximizada es ligeramente diferente. El sistema mueve automáticamente la barra de título de la ventana a la parte superior de la pantalla o a la parte superior del área de cliente de la ventana primaria. Además, el sistema deshabilita el borde de ajuste de tamaño de la ventana y la funcionalidad de posición de la ventana de la barra de título (de modo que el usuario no pueda mover la ventana arrastrando la barra de título).

Una *ventana minimizada* es una ventana que tiene el estilo [**WS \_ miniMIZE**](window-styles.md) . De manera predeterminada, el sistema reduce una ventana minimizada al tamaño del botón de la barra de tareas y la mueve a la barra de tareas. Una *ventana restaurada* es una ventana que se ha devuelto a su tamaño y posición anteriores, es decir, el tamaño que tenía antes de ser minimizada o maximizada.

Si una aplicación especifica el estilo [**WS \_ Maximize**](window-styles.md) o **WS \_ miniMIZE** en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , la ventana se maximiza o minimiza inicialmente. Después de crear una ventana, una aplicación puede usar la función [**CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) para minimizar la ventana. La función [**ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) organiza los iconos en el escritorio o organiza las ventanas secundarias minimizadas de una ventana primaria en la ventana primaria. La función [**OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) restaura una ventana minimizada a su tamaño y posición anteriores.

La función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) puede minimizar, maximizar o restaurar una ventana. También puede establecer la visibilidad y los Estados de activación de la ventana. La función [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) incluye la misma funcionalidad que **ShowWindow**, pero puede invalidar las posiciones minimizadas, maximizadas y restauradas predeterminadas de la ventana.

Las funciones [**IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) y [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) determinan si una ventana determinada está maximizada o minimizada, respectivamente. La función [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) recupera las posiciones minimizada, maximizada y restaurada para la ventana, y también determina el estado de la ventana.

Cuando el sistema recibe un comando para maximizar o restaurar una ventana minimizada, envía la ventana a un mensaje de [**WM \_ QUERYOPEN**](wm-queryopen.md) . Si el procedimiento de ventana devuelve **false**, el sistema omite el comando Maximize o restore.

El sistema establece automáticamente el tamaño y la posición de una ventana maximizada en los valores predeterminados definidos por el sistema para una ventana maximizada. Para invalidar estos valores predeterminados, una aplicación puede llamar a la función [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o procesar el mensaje de [**\_ GETMINMAXINFO de WM**](wm-getminmaxinfo.md) que recibe una ventana cuando el sistema está a punto de maximizar la ventana. **WM \_ GETMINMAXINFO** incluye un puntero a una estructura [**minmaxinfo (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene valores que el sistema utiliza para establecer el tamaño y la posición maximizados. Reemplazar estos valores invalida los valores predeterminados.

## <a name="window-size-and-position"></a>Tamaño y posición de la ventana

El tamaño y la posición de una ventana se expresan como un rectángulo delimitador, dado en coordenadas relativas a la pantalla o a la ventana primaria. Las coordenadas de una ventana de nivel superior son relativas a la esquina superior izquierda de la pantalla. las coordenadas de una ventana secundaria son relativas a la esquina superior izquierda de la ventana primaria. Una aplicación especifica el tamaño inicial y la posición de una ventana cuando crea la ventana, pero puede cambiar el tamaño y la posición de la ventana en cualquier momento. Para obtener más información, vea [formas rellenas](../gdi/filled-shapes.md).

Esta sección contiene los siguientes temas:

-   [Tamaño y posición predeterminados](#default-size-and-position)
-   [Tamaño de seguimiento](#tracking-size)
-   [Comandos del sistema](#system-commands)
-   [Funciones de tamaño y posición](#size-and-position-functions)
-   [Mensajes de tamaño y posición](#size-and-position-messages)

### <a name="default-size-and-position"></a>Tamaño y posición predeterminados

Una aplicación puede permitir que el sistema calcule el tamaño o la posición inicial de una ventana de nivel superior especificando CW \_ USEDEFAULT en [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Si la aplicación establece las coordenadas de la ventana en CW \_ USEDEFAULT y no ha creado otras ventanas de nivel superior, el sistema establece la posición de la nueva ventana con respecto a la esquina superior izquierda de la pantalla; de lo contrario, establece la posición relativa a la posición de la ventana de nivel superior que creó la aplicación más recientemente. Si los parámetros de ancho y alto se establecen en CW \_ USEDEFAULT, el sistema calcula el tamaño de la nueva ventana. Si la aplicación ha creado otras ventanas de nivel superior, el sistema basa el tamaño de la nueva ventana en el tamaño de la ventana de nivel superior creada más recientemente de la aplicación. Al especificar CW \_ USEDEFAULT al crear una ventana secundaria o emergente, el sistema establece el tamaño de la ventana en el tamaño mínimo predeterminado de la ventana.

### <a name="tracking-size"></a>Tamaño de seguimiento

El sistema mantiene un tamaño de seguimiento mínimo y máximo para una ventana del estilo [**WS \_ THICKFRAME**](window-styles.md) ; una ventana con este estilo tiene un borde de ajuste de tamaño. El *tamaño mínimo de seguimiento* es el tamaño de ventana más pequeño que puede producir arrastrando el borde de tamaño de la ventana. Del mismo modo, el *tamaño máximo de seguimiento* es el tamaño de ventana más grande que se puede producir arrastrando el borde de ajuste de tamaño.

Los tamaños de seguimiento mínimo y máximo de una ventana se establecen en los valores predeterminados definidos por el sistema cuando el sistema crea la ventana. Una aplicación puede detectar los valores predeterminados e invalidarlos procesando el mensaje de [**\_ GETMINMAXINFO de WM**](wm-getminmaxinfo.md) . Para obtener más información, vea [cambiar el tamaño y la posición de los mensajes](#size-and-position-messages).

### <a name="system-commands"></a>Comandos del sistema

Una aplicación con un menú ventana puede cambiar el tamaño y la posición de la ventana mediante el envío de comandos del sistema. Los comandos del sistema se generan cuando el usuario elige comandos en el menú ventana. Una aplicación puede emular la acción del usuario mediante el envío de un mensaje de [**\_ SYSCOMMAND de WM**](../menurc/wm-syscommand.md) a la ventana. Los siguientes comandos del sistema afectan al tamaño y la posición de una ventana.



| Get-Help      | Descripción                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cierre SC    | Cierra la ventana. Este comando envía un mensaje de [**\_ cierre de WM**](wm-close.md) a la ventana. La ventana lleva a cabo los pasos necesarios para realizar la limpieza y la destrucción. |
| \_maximizar SC | Maximiza la ventana.                                                                                                                                                |
| \_minimizar SC | Minimiza la ventana.                                                                                                                                                |
| movimiento de SC \_     | Mueve la ventana.                                                                                                                                                    |
| restauración de SC \_  | Restaura una ventana minimizada o maximizada a su tamaño y posición anteriores.                                                                                          |
| \_tamaño SC     | Inicia un comando de tamaño. Para cambiar el tamaño de la ventana, use el mouse o el teclado.                                                                                  |



 

### <a name="size-and-position-functions"></a>Funciones de tamaño y posición

Después de crear una ventana, una aplicación puede establecer el tamaño o la posición de la ventana mediante una llamada a una de las distintas funciones, como [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement), [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)y [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos). **SetWindowPlacement** establece la posición minimizada de una ventana, la posición maximizada, el tamaño y la posición restaurados y el estado de presentación. Las funciones **MoveWindow** y **SetWindowPos** son similares; ambos establecen el tamaño o la posición de una sola ventana de la aplicación. La función **SetWindowPos** incluye un conjunto de marcas que afectan al estado de presentación de la ventana. **MoveWindow** no incluye estas marcas. Use las funciones [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** y [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) para establecer simultáneamente la posición de un número de ventanas, incluidos el tamaño, la posición, la posición en el orden z y el estado de presentación.

Una aplicación puede recuperar las coordenadas del rectángulo delimitador de una ventana mediante la función [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) . **GetWindowRect** rellena una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de las esquinas superior izquierda e inferior derecha de la ventana. Las coordenadas son relativas a la esquina superior izquierda de la pantalla, incluso para una ventana secundaria. La función [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) o [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) asigna las coordenadas de pantalla del rectángulo delimitador de una ventana secundaria a las coordenadas relativas al área de cliente de la ventana primaria.

La función [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) recupera las coordenadas del área de cliente de una ventana. **GetClientRect** rellena una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de las esquinas superior izquierda e inferior derecha del área cliente, pero las coordenadas son relativas al propio área cliente. Esto significa que las coordenadas de la esquina superior izquierda de un área cliente siempre son (0,0) y las coordenadas de la esquina inferior derecha son el ancho y el alto del área cliente.

La función [**CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) en cascada en el escritorio o en cascada las ventanas secundarias de la ventana primaria especificada. La función [**TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) coloca los iconos en las ventanas del escritorio o coloca en mosaico las ventanas secundarias de la ventana primaria especificada.

### <a name="size-and-position-messages"></a>Mensajes de tamaño y posición

El sistema envía el mensaje de [**\_ GETMINMAXINFO de WM**](wm-getminmaxinfo.md) a una ventana cuyo tamaño o posición está a punto de cambiar. Por ejemplo, el mensaje se envía cuando el usuario hace clic en **movimiento** o **tamaño** en el menú ventana o hace clic en el borde de ajuste de tamaño o en la barra de título. también se envía el mensaje cuando una aplicación llama a [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para moverse o cambiar el tamaño de la ventana. **WM \_ GETMINMAXINFO** incluye un puntero a una estructura [**minmaxinfo (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene el tamaño y la posición maximizados predeterminados para la ventana, así como los tamaños de seguimiento mínimo y máximo predeterminados. Una aplicación puede invalidar los valores predeterminados procesando **WM \_ GETMINMAXINFO** y estableciendo los miembros adecuados de **minmaxinfo (**. Una ventana debe tener el estilo [**WS \_ THICKFRAME**](window-styles.md) o **WS \_ Caption** para recibir **WM \_ GETMINMAXINFO**. Una ventana con el estilo **WS \_ THICKFRAME** recibe este mensaje durante el proceso de creación de ventana, así como cuando se mueve o se ajusta su tamaño.

El sistema envía el mensaje de [**WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) a una ventana cuyo tamaño, posición, posición en el orden z o mostrar estado está a punto de cambiar. Este mensaje incluye un puntero a una estructura [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) que especifica el nuevo tamaño, la posición y la posición de la ventana en el orden z, y el estado de presentación. Al establecer los miembros de **windowpos (**, una aplicación puede afectar al nuevo tamaño, posición y apariencia de la ventana.

Después de cambiar el tamaño, la posición y la posición de una ventana en el orden z o mostrar el estado, el sistema envía el mensaje de [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) a la ventana. Este mensaje incluye un puntero a [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) que informa a la ventana de su nuevo tamaño, posición, posición en el orden z y mostrar el estado. Establecer los miembros de la estructura **windowpos (** que se pasa con **WM \_ WINDOWPOSCHANGED** no tiene ningún efecto en la ventana. Una ventana que debe procesar los mensajes de [**\_ tamaño de WM**](wm-size.md) y de [**\_ movimiento de WM**](wm-move.md) debe pasar **WM \_ WINDOWPOSCHANGED** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; de lo contrario, el sistema no envía mensajes de **\_ tamaño de WM** y de **\_ movimiento de WM** a la ventana.

El sistema envía el mensaje de [**\_ NCCALCSIZE de WM**](wm-nccalcsize.md) a una ventana cuando se crea o se ajusta el tamaño de la ventana. El sistema utiliza el mensaje para calcular el tamaño del área de cliente de una ventana y la posición del área de cliente con respecto a la esquina superior izquierda de la ventana. Normalmente, una ventana pasa este mensaje al procedimiento de ventana predeterminado; sin embargo, este mensaje puede ser útil en aplicaciones que personalizan el área no cliente de una ventana o conservan partes del área cliente cuando se cambia el tamaño de la ventana. Para obtener más información, vea [pintar y dibujar](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Animación de ventana

Puede producir efectos especiales al mostrar u ocultar ventanas mediante la función [**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow) . Cuando la ventana se anima de esta manera, el sistema lo retirará, deslizará o atenuará la ventana, en función de las marcas que especifique en una llamada a **AnimateWindow**.

De forma predeterminada, el sistema utiliza la *animación Roll*. Con este efecto, la ventana parece abrirse (Mostrar la ventana) o cerrar (ocultando la ventana). Puede usar el parámetro *dwFlags* para especificar si la ventana se desplaza horizontal, vertical o diagonalmente.

Cuando se especifica la marca de **\_ diapositiva AW** , el sistema utiliza la *animación de diapositivas*. Con este efecto, la ventana aparece como deslizar en la vista (mostrando la ventana) o desplazarse fuera de la vista (ocultando la ventana). Puede usar el parámetro *dwFlags* para especificar si la ventana se desliza horizontalmente, verticalmente o diagonalmente.

Cuando se especifica la marca **AW \_ Blend** , el sistema utiliza una *atenuación alfa combinada*.

También puede usar la marca **AW del \_ Centro** para que parezca que una ventana se contrae hacia adentro o hacia afuera.

## <a name="window-layout-and-mirroring"></a>Diseño y creación de reflejo de ventanas

El diseño de ventana define cómo se colocan los objetos de texto y Windows Interfaz de dispositivo gráfico (GDI) en una ventana o un contexto de dispositivo (DC). Algunos idiomas, como inglés, francés y alemán, requieren un diseño de izquierda a derecha (LTR). Otros idiomas, como el árabe y el hebreo, requieren un diseño de derecha a izquierda (RTL). El diseño de ventana se aplica al texto, pero también afecta a los demás elementos GDI de la ventana, incluidos los mapas de bits, los iconos, la ubicación del origen, los botones, los controles de árbol en cascada y si la coordenada horizontal aumenta a medida que se desplaza a la izquierda o a la derecha. Por ejemplo, después de que una aplicación tenga establecido el diseño RTL, el origen se coloca en el borde derecho de la ventana o dispositivo y el número que representa la coordenada horizontal aumenta a medida que se mueve a la izquierda. Sin embargo, no todos los objetos se ven afectados por el diseño de una ventana. Por ejemplo, el diseño de los cuadros de diálogo, los cuadros de mensaje y los contextos de dispositivo que no están asociados a una ventana, como los DC de metarchivo y de impresora, deben administrarse por separado. Más adelante en este tema se mencionan las características específicas para estas.

Las funciones de ventana permiten especificar o cambiar el diseño de ventana en las versiones árabe y hebreo de Windows. Tenga en cuenta que el cambio a un diseño de derecha a izquierda (también conocido como creación de reflejo) no es compatible con Windows que tenga el estilo [CS \_ OWNDC](about-window-classes.md) o para un controlador de dominio con el \_ modo gráfico avanzado de GM.

De forma predeterminada, el diseño de la ventana es de izquierda a derecha (LTR). Para establecer el diseño de la ventana de derecha a izquierda, llame a [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con el estilo **WS \_ ex \_ LAYOUTRTL**. Además, de forma predeterminada, una ventana secundaria (es decir, una creada con el estilo [**WS \_ Child**](window-styles.md) y con un parámetro *hWnd* primario válido en la llamada a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o **CreateWindowEx**) tiene el mismo diseño que su elemento primario. Para deshabilitar la herencia de la creación de reflejo en todas las ventanas secundarias, especifique **WS \_ ex \_ NOINHERITLAYOUT** en la llamada a **CreateWindowEx**. Tenga en cuenta que las ventanas de propiedad no heredan la creación de reflejo (las creadas sin el estilo **\_ secundario WS** ) o las creadas con el parámetro *hWnd* primario en **CreateWindowEx** establecida en **null**. Para deshabilitar la herencia de la creación de reflejo de una ventana individual, procese el mensaje de [**WM \_ NCCREATE**](wm-nccreate.md) con [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para desactivar la marca **WS \_ ex \_ LAYOUTRTL** . Este procesamiento se suma a cualquier otro procesamiento necesario. En el fragmento de código siguiente se muestra cómo hacerlo.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Puede establecer el diseño predeterminado en RTL llamando a [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(diseño \_ RTL). Todas las ventanas creadas después de la llamada se reflejarán, pero las ventanas existentes no se verán afectadas. Para desactivar la creación de reflejo predeterminada, llame a **SetProcessDefaultLayout**(0).

Tenga en cuenta que [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) solo refleja los DC de las ventanas reflejadas. Para reflejar cualquier DC, llame a [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(HDC, diseño \_ RTL). Para obtener más información, vea la explicación sobre los contextos de dispositivo de creación de reflejo no asociados a Windows, que se incluye más adelante en este tema.

Los mapas de bits y los iconos de una ventana reflejada también se reflejan de forma predeterminada. Sin embargo, no todas estas deben reflejarse. Por ejemplo, los que tengan texto, un logotipo de empresa o un reloj analógico no deben reflejarse. Para deshabilitar la creación de reflejo de mapas de bits, llame a [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) con el bit de diseño \_ BITMAPORIENTATIONPRESERVED establecido en *dwLayout*. Para deshabilitar la creación de reflejo en un controlador de dominio, llame a **SetLayout**(HDC, 0).

Para consultar el diseño predeterminado actual, llame a [**GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout). Cuando la devolución es correcta, *pdwDefaultLayout* contiene el diseño \_ RTL o 0. Para consultar la configuración de diseño del contexto de dispositivo, llame a [**GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). Una vez que se devuelve correctamente, **GetLayout** devuelve un **valor DWORD** que indica la configuración de diseño por la configuración del diseño \_ RTL y el BITMAPORIENTATIONPRESERVED de diseño \_ bits.

Una vez creada una ventana, se cambia el diseño mediante la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . Por ejemplo, esto es necesario cuando el usuario cambia el idioma de la interfaz de usuario de una ventana existente de árabe o hebreo a alemán. Sin embargo, al cambiar el diseño de una ventana existente, debe invalidar y actualizar la ventana para asegurarse de que todo el contenido de la ventana se dibuja en el mismo diseño. El ejemplo de código siguiente es del código de ejemplo que cambia el diseño de la ventana según sea necesario:


```
// Using ANSI versions of GetWindowLong and SetWindowLong because Unicode
// is not needed for these calls

lExStyles = GetWindowLongA(hWnd, GWL_EXSTYLE);

// Check whether new layout is opposite the current layout
if (!!(pLState -> IsRTLLayout) != !!(lExStyles & WS_EX_LAYOUTRTL))
{
    // the following lines will update the window layout

    lExStyles ^= WS_EX_LAYOUTRTL;        // toggle layout
    SetWindowLongA(hWnd, GWL_EXSTYLE, lExStyles);
    InvalidateRect(hWnd, NULL, TRUE);    // to update layout in the client area
}
```



En la creación de reflejo, debe pensar en términos de "near" y "Far" en lugar de "left" y "Right". Si no lo hace, pueden producirse problemas. Una práctica de codificación común que provoca problemas en una ventana reflejada se produce al asignar entre coordenadas de pantalla y coordenadas de cliente. Por ejemplo, las aplicaciones a menudo usan código similar al siguiente para colocar un control en una ventana:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Esto provoca problemas en la creación de reflejo porque el borde izquierdo del rectángulo se convierte en el borde derecho de una ventana reflejada y viceversa. Para evitar este problema, reemplace las llamadas a [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) por una llamada a [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) como se indica a continuación:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Este código funciona porque, en las plataformas que admiten la creación de reflejo, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) se modifica para intercambiar las coordenadas de punto izquierdo y derecho cuando la ventana de cliente está reflejada. Para obtener más información, vea la sección Comentarios de **MapWindowPoints**.

Otra práctica común que puede causar problemas en ventanas reflejadas es colocar objetos en una ventana de cliente mediante desplazamientos en coordenadas de pantalla en lugar de coordenadas de cliente. Por ejemplo, el código siguiente usa la diferencia en coordenadas de pantalla como la posición x en coordenadas de cliente para colocar un control en un cuadro de diálogo.


```
// OK if LTR layout and mapping mode of client is MM_TEXT,
// but WRONG for a mirrored dialog 

RECT rdDialog;
RECT rcControl;

HWND hControl = GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hDlg, &rcDialog);             // gets rect in screen coordinates
GetWindowRect(hControl, &rcControl);
MoveWindow(hControl,
           rcControl.left - rcDialog.left,  // uses x position in client coords
           rcControl.top - rcDialog.top,
           nWidth,
           nHeight,
           FALSE);
```



Este código es correcto cuando la ventana del cuadro de diálogo tiene un diseño de izquierda a derecha (LTR) y el modo de asignación del cliente es MM \_ , porque la nueva posición x en coordenadas de cliente corresponde a la diferencia en los bordes izquierdos del control y el cuadro de diálogo en las coordenadas de la pantalla. Sin embargo, en un cuadro de diálogo reflejado, izquierda y derecha se invierten, por lo que debe usar [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) como se indica a continuación:


```
RECT rcDialog;
RECT rcControl;

HWND hControl - GetDlgItem(hDlg, IDD_CONTROL);
GetWindowRect(hControl, &rcControl);

// MapWindowPoints works correctly in both mirrored and non-mirrored windows.
MapWindowPoints(NULL, hDlg, (LPPOINT) &rcControl, 2);

// Now rcControl is in client coordinates.
MoveWindow(hControl, rcControl.left, rcControl.top, nWidth, nHeight, FALSE)
```



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Cuadros de diálogo de creación de reflejo y cuadros de mensaje

Los cuadros de diálogo y los cuadros de mensaje no heredan el diseño, por lo que debe establecer el diseño explícitamente. Para reflejar un cuadro de mensaje, llame a [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) con la opción **MB \_ RTLREADING** Para diseñar un cuadro de diálogo de derecha a izquierda, use el estilo extendido WS \_ ex \_ LAYOUTRTL en la estructura de plantilla de cuadro de diálogo [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Las hojas de propiedades son un caso especial de cuadros de diálogo. Cada pestaña se trata como un cuadro de diálogo independiente, por lo que debe incluir el \_ estilo WS ex \_ LAYOUTRTL en cada pestaña que desee reflejar.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Contextos de dispositivo de creación de reflejo no asociados a una ventana

Los controladores de usuario que no están asociados a una ventana, como los DC de metarchivo o de impresora, no heredan el diseño, por lo que debe establecer el diseño explícitamente. Para cambiar el diseño del contexto de dispositivo, utilice la función [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) .

La función [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) rara vez se usa con Windows. Normalmente, Windows solo recibe un DC asociado en el procesamiento de un mensaje de [**\_ pintura de WM**](../gdi/wm-paint.md) . En ocasiones, un programa crea un controlador de dominio para una ventana mediante una llamada a [**GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). En cualquier caso, el diseño inicial del controlador de dominio se establece mediante [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) o **GetDC** según la marca de WS ex LAYOUTRTL de la ventana \_ \_ .

Los valores devueltos por [**GetWindowOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex), [**GetWindowExtEx**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex), [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) y [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) no se ven afectados por la llamada a [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout).

Cuando el diseño es de derecha a izquierda, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) devolverá mm \_ anisotrópico en lugar de \_ texto mm. La llamada a [**SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) con \_ texto mm funcionará correctamente; solo se verá afectado el valor devuelto de **GetMapMode** . Del mismo modo, al llamar a [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(HDC, layout \_ RTL) cuando el modo de asignación es \_ texto mm, el modo de asignación indicado cambia a mm \_ anisotrópico.

## <a name="window-destruction"></a>Destrucción de ventanas

En general, una aplicación debe destruir todas las ventanas que crea. Para ello, se usa la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) . Cuando se destruye una ventana, el sistema oculta la ventana, si está visible, y, a continuación, quita los datos internos asociados a la ventana. Esto invalida el identificador de ventana, que la aplicación ya no puede usar.

Una aplicación destruye muchas de las ventanas que crea poco después de crearlas. Por ejemplo, una aplicación normalmente destruye una ventana de cuadro de diálogo en cuanto la aplicación tiene una entrada suficiente del usuario para continuar con su tarea. Finalmente, una aplicación destruye la ventana principal de la aplicación (antes de finalizar).

Antes de destruir una ventana, una aplicación debe guardar o quitar los datos asociados a la ventana y debe liberar todos los recursos del sistema asignados a la ventana. Si la aplicación no libera los recursos, el sistema liberará los recursos no liberados por la aplicación.

La destrucción de una ventana no afecta a la clase de ventana desde la que se crea la ventana. Todavía se pueden crear ventanas nuevas con esa clase y todas las ventanas existentes de esa clase seguirán funcionando. Al destruir una ventana, también se destruyen las ventanas descendientes de la ventana. La función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envía primero un mensaje de [**\_ destrucción de WM**](wm-destroy.md) a la ventana y, a continuación, a sus ventanas secundarias y descendientes. De esta manera, también se destruyen todas las ventanas descendientes de la ventana que se va a destruir.

Una ventana con un menú ventana recibe un mensaje de [**\_ cierre de WM**](wm-close.md) cuando el usuario hace clic en **cerrar**. Al procesar este mensaje, una aplicación puede solicitar confirmación al usuario antes de destruir la ventana. Si el usuario confirma que se debe destruir la ventana, la aplicación puede llamar a la función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir la ventana.

Si la ventana que se va a destruir es la ventana activa, los Estados activo y foco se transfieren a otra ventana. La ventana que se convierte en la ventana activa es la ventana siguiente, determinada por la combinación de teclas ALT + ESC. A continuación, la nueva ventana activa determina qué ventana recibe el foco de teclado.

 

 
