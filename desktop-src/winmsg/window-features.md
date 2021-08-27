---
description: Esta introducción describe las características de las ventanas, como los tipos de ventana, los estados, el tamaño y la posición.
ms.assetid: 8318c22f-85a2-490e-8233-ee1e234890d9
title: Características de las ventanas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437ab95d12ccc56cdf5e87af2127f4c34ad6def7f07f4e79246a2ad591a5ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110685"
---
# <a name="window-features"></a>Características de las ventanas

Esta introducción describe las características de las ventanas, como los tipos de ventana, los estados, el tamaño y la posición.

-   [Tipos de ventana](#window-types)
    -   [Datos superpuestos Windows](#overlapped-windows)
    -   [Ventana emergente Windows](#pop-up-windows)
    -   [Datos Windows](#child-windows)
        -   [Posicionamiento](#positioning)
        -   [Recorte](#clipping)
        -   [Relación con la ventana primaria](#relationship-to-parent-window)
        -   [Mensajes](#size-and-position-messages)
    -   [Capas Windows](#layered-windows)
    -   [Solo mensaje Windows](#message-only-windows)
-   [Relaciones de ventana](#window-relationships)
    -   [Primer plano y fondo Windows](#foreground-and-background-windows)
    -   [Propiedad Windows](#owned-windows)
    -   [Orden Z](#z-order)
-   [Estado de presentación de ventana](#window-show-state)
    -   [Ventana activa](#active-window)
    -   [Deshabilitada Windows](#disabled-windows)
    -   [Visibilidad de las ventanas](#window-visibility)
    -   [Minimizado, maximizado y restaurado Windows](#minimized-maximized-and-restored-windows)
-   [Tamaño y posición de la ventana](#window-size-and-position)
    -   [Tamaño y posición predeterminados](#default-size-and-position)
    -   [Tamaño de seguimiento](#tracking-size)
    -   [Comandos del sistema](#system-commands)
    -   [Funciones de tamaño y posición](#size-and-position-functions)
    -   [Mensajes de tamaño y posición](#size-and-position-messages)
-   [Animación de ventana](#window-animation)
-   [Diseño y creación de reflejo de ventanas](#window-layout-and-mirroring)
    -   [Cuadros de diálogo y cuadros de mensaje de creación de reflejo](#mirroring-dialog-boxes-and-message-boxes)
    -   [Creación de reflejo de contextos de dispositivo no asociados a una ventana](#mirroring-device-contexts-not-associated-with-a-window)
-   [Destrucción de ventanas](#window-destruction)

## <a name="window-types"></a>Tipos de ventana

Esta sección contiene los temas siguientes que describen los tipos de ventana.

-   [Datos superpuestos Windows](#overlapped-windows)
-   [Ventana emergente Windows](#pop-up-windows)
-   [Datos Windows](#child-windows)
-   [Capas Windows](#layered-windows)
-   [Solo mensaje Windows](#message-only-windows)

### <a name="overlapped-windows"></a>Datos superpuestos Windows

Una *ventana superpuesta* es una ventana de nivel superior (ventana no secundaria) que tiene una barra de título, un borde y un área de cliente. está diseñado para servir como ventana principal de una aplicación. También puede tener un menú de ventana, minimizar y maximizar botones y barras de desplazamiento. Una ventana superpuesta que se usa como ventana principal normalmente incluye todos estos componentes.

Al especificar el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ OVERLAPPEDWINDOW** en la [**función CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) una aplicación crea una ventana superpuesta. Si usa el estilo **\_ OVERLAPPED de WS,** la ventana tiene una barra de título y un borde. Si usa el estilo **WS \_ OVERLAPPEDWINDOW,** la ventana tiene una barra de título, un borde de tamaño, un menú de ventana y botones para minimizar y maximizar.

### <a name="pop-up-windows"></a>Ventana emergente Windows

Una *ventana emergente es un tipo* especial de ventana superpuesta que se usa para cuadros de diálogo, cuadros de mensaje y otras ventanas temporales que aparecen fuera de la ventana principal de una aplicación. Las barras de título son opcionales para las ventanas emergentes; De lo contrario, las ventanas emergentes son las mismas que las ventanas superpuestas del [**estilo \_ OVERLAPPED de WS.**](window-styles.md)

Para crear una ventana emergente, especifique el estilo POPUP de [**WS \_**](window-styles.md) [**en CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Para incluir una barra de título, especifique el **estilo WS \_ CAPTION.** Use el **estilo \_ POPUPWINDOW de WS** para crear una ventana emergente que tenga un borde y un menú de ventana. El **estilo WS \_ CAPTION** debe combinarse con el estilo **\_ POPUPWINDOW** de WS para que el menú de la ventana sea visible.

### <a name="child-windows"></a>Datos Windows

Una *ventana secundaria* tiene el estilo [**WS \_ CHILD**](window-styles.md) y se limita al área de cliente de su ventana primaria. Normalmente, una aplicación usa ventanas secundarias para dividir el área de cliente de una ventana primaria en áreas funcionales. Para crear una ventana secundaria, especifique el **estilo SECUNDARIO de WS \_** en [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

Una ventana secundaria debe tener una ventana primaria. La ventana primaria puede ser una ventana superpuesta, una ventana emergente o incluso otra ventana secundaria. La ventana primaria se especifica cuando se llama a [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Si especifica el [**estilo WS \_ CHILD**](window-styles.md) en **CreateWindowEx** pero no especifica una ventana primaria, el sistema no crea la ventana.

Una ventana secundaria tiene un área de cliente, pero no otras características, a menos que se soliciten explícitamente. Una aplicación puede solicitar una barra de título, un menú de ventana, minimizar y maximizar botones, un borde y barras de desplazamiento para una ventana secundaria, pero una ventana secundaria no puede tener un menú. Si la aplicación especifica un identificador de menú, ya sea cuando registra la clase de ventana del elemento secundario o crea la ventana secundaria, se omite el identificador de menú. Si no se especifica ningún estilo de borde, el sistema crea una ventana sin borde. Una aplicación puede usar ventanas secundarias sin borde para dividir el área de cliente de una ventana primaria y mantener las divisiones invisibles para el usuario.

En esta sección se de abordan los siguientes aspectos de las ventanas secundarias:

-   [Posicionamiento](#positioning)
-   [Recorte](#clipping)
-   [Relación con la ventana primaria](#relationship-to-parent-window)
-   [Mensajes](#size-and-position-messages)

#### <a name="positioning"></a>Posicionamiento

El sistema siempre coloca una ventana secundaria en relación con la esquina superior izquierda del área de cliente de la ventana primaria. Ninguna parte de una ventana secundaria aparece fuera de los bordes de su ventana primaria. Si una aplicación crea una ventana secundaria mayor que la ventana primaria o coloca una ventana secundaria para que parte o toda la ventana secundaria se extienda más allá de los bordes del elemento primario, el sistema recorta la ventana secundaria; Es decir, no se muestra la parte fuera del área de cliente de la ventana primaria. Las acciones que afectan a la ventana primaria también pueden afectar a la ventana secundaria, como se muestra a continuación.



| Ventana primaria | Ventana secundaria                                                                                                             |
|---------------|--------------------------------------------------------------------------------------------------------------------------|
| Destruido     | Se destruye antes de que se destruya la ventana primaria.                                                                         |
| Hidden        | Se oculta antes de que se oculta la ventana primaria. Una ventana secundaria solo es visible cuando la ventana primaria está visible.             |
| Movido         | Se ha movido con el área de cliente de la ventana primaria. La ventana secundaria es responsable de pintar su área de cliente después del traslado. |
| Mostrado         | Se muestra después de que se muestra la ventana primaria.                                                                                  |



 

#### <a name="clipping"></a>Recorte

El sistema no recorta automáticamente una ventana secundaria del área de cliente de la ventana primaria. Esto significa que la ventana primaria se dibuja sobre la ventana secundaria si lleva a cabo cualquier dibujo en la misma ubicación que la ventana secundaria. Sin embargo, el sistema recorta la ventana secundaria del área de cliente de la ventana primaria si la ventana primaria tiene el estilo [**\_ CLIPCHILDREN de WS.**](window-styles.md) Si se recorta la ventana secundaria, la ventana primaria no puede dibujar sobre ella.

Una ventana secundaria puede superponerse a otras ventanas secundarias en el mismo área de cliente. Una ventana secundaria que comparte la misma ventana primaria que una o varias ventanas secundarias se denomina ventana *del mismo nivel.* Las ventanas del mismo nivel se pueden dibujar entre sí en el área de cliente, a menos que una de las ventanas secundarias tenga el estilo [**\_ CLIPSIBLINGS de WS.**](window-styles.md) Si una ventana secundaria tiene este estilo, se recorta cualquier parte de su ventana del mismo nivel que se encuentra dentro de la ventana secundaria.

Si una ventana tiene el estilo [**WS \_ CLIPCHILDREN**](window-styles.md) o **WS \_ CLIPSIBLINGS,** se produce una ligera pérdida de rendimiento. Cada ventana ocupa recursos del sistema, por lo que una aplicación no debe usar ventanas secundarias de forma indiscriminada. Para obtener el mejor rendimiento, una aplicación que necesite dividir lógicamente su ventana principal debe hacerlo en el procedimiento de ventana de la ventana principal en lugar de mediante ventanas secundarias.

#### <a name="relationship-to-parent-window"></a>Relación con la ventana primaria

Una aplicación puede cambiar la ventana primaria de una ventana secundaria existente llamando a la [**función SetParent.**](/windows/win32/api/winuser/nf-winuser-setparent) En este caso, el sistema quita la ventana secundaria del área de cliente de la ventana primaria anterior y la mueve al área cliente de la nueva ventana primaria. Si **SetParent especifica** un identificador **NULL,** la ventana de escritorio se convierte en la nueva ventana primaria. En este caso, la ventana secundaria se dibuja en el escritorio, fuera de los bordes de cualquier otra ventana. La [**función GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) recupera un identificador en la ventana primaria de una ventana secundaria.

La ventana primaria cuelca una parte de su área de cliente en una ventana secundaria y la ventana secundaria recibe todas las entradas de esta área. La clase window no necesita ser la misma para cada una de las ventanas secundarias de la ventana primaria. Esto significa que una aplicación puede rellenar una ventana primaria con ventanas secundarias que tienen un aspecto diferente y llevar a cabo tareas diferentes. Por ejemplo, un cuadro de diálogo puede contener muchos tipos de controles, cada uno de ellos una ventana secundaria que acepta distintos tipos de datos del usuario.

Una ventana secundaria solo tiene una ventana primaria, pero un elemento primario puede tener cualquier número de ventanas secundarias. Cada ventana secundaria, a su vez, puede tener ventanas secundarias. En esta cadena de ventanas, cada ventana secundaria se denomina ventana descendiente de la ventana primaria original. Una aplicación usa la [**función IsChild**](/windows/win32/api/winuser/nf-winuser-ischild) para detectar si una ventana determinada es una ventana secundaria o una ventana descendiente de una ventana primaria determinada.

La [**función EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) enumera las ventanas secundarias de una ventana primaria. A continuación, **EnumChildWindows** pasa el identificador a cada ventana secundaria a una función de devolución de llamada definida por la aplicación. También se enumeran las ventanas descendientes de la ventana primaria dada.

#### <a name="messages"></a>error de Hadoop

El sistema pasa los mensajes de entrada de una ventana secundaria directamente a la ventana secundaria. los mensajes no se pasan a través de la ventana primaria. La única excepción es si la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) ha deshabilitado la ventana secundaria. En este caso, el sistema pasa los mensajes de entrada que hubieran ido a la ventana secundaria a la ventana primaria en su lugar. Esto permite que la ventana primaria examine los mensajes de entrada y habilite la ventana secundaria, si es necesario.

Una ventana secundaria puede tener un identificador entero único. Los identificadores de ventana secundarios son importantes al trabajar con ventanas de control. Una aplicación dirige la actividad de un control enviándole mensajes. La aplicación usa el identificador de ventana secundaria del control para dirigir los mensajes al control. Además, un control envía mensajes de notificación a su ventana primaria. Un mensaje de notificación incluye el identificador de ventana secundaria del control, que el elemento primario usa para identificar qué control envió el mensaje. Una aplicación especifica el identificador de ventana secundaria para otros tipos de ventanas secundarias estableciendo el parámetro *hMenu* de la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) en un valor en lugar de en un identificador de menú.

### <a name="layered-windows"></a>Capas Windows

El uso de una ventana en capas puede mejorar significativamente el rendimiento y los efectos visuales de una ventana que tiene una forma compleja, anima su forma o desea usar efectos de mezcla alfa. El sistema crea y vuelve a dibujar automáticamente las ventanas en capas y las ventanas de las aplicaciones subyacentes. Como resultado, las ventanas en capas se representan sin problemas, sin el parpadeo típico de las regiones de ventana complejas. Además, las ventanas en capas pueden ser parcialmente translúcidas, es decir, con mezcla alfa.

Para crear una ventana en capas, especifique el estilo de ventana extendida **WS \_ EX \_ LAYERED** al llamar a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) o llame a la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para establecer **WS \_ EX \_ LAYERED** una vez creada la ventana. Después de la llamada a **CreateWindowEx,** la ventana por capas no estará visible hasta que se haya llamado a la función [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) o [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow) para esta ventana.

> [!Note]  
> A partir Windows 8, **WS \_ EX \_ LAYERED** se puede usar con ventanas secundarias y ventanas de nivel superior. Las Windows anteriores **admiten WS \_ EX \_ LAYERED solo** para ventanas de nivel superior.

 

Para establecer el nivel de opacidad o la clave de color de transparencia para una ventana en capas determinada, llame a [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes). Después de la llamada, es posible que el sistema todavía pida a la ventana que pinte cuando se muestra o cambia el tamaño de la ventana. Sin embargo, dado que el sistema almacena la imagen de una ventana en capas, el sistema no pedirá a la ventana que pinte si se revelan partes de ella como resultado de un movimiento relativo de la ventana en el escritorio. Las aplicaciones heredadas no necesitan reestructurar su código de dibujo si quieren agregar translucency o efectos de transparencia para una ventana, ya que el sistema redirige el dibujo de ventanas que llamaron **SetLayeredWindowAttributes** a la memoria fuera de la pantalla y la vuelve a compilar para lograr el efecto deseado.

Para una animación más rápida y eficaz o si se necesita alfa por píxel, llame a [**UpdateLayeredWindow**](/windows/win32/api/winuser/nf-winuser-updatelayeredwindow). **UpdateLayeredWindow** debe usarse principalmente cuando la aplicación debe proporcionar directamente la forma y el contenido de una ventana en capas, sin usar el mecanismo de redireccionamiento que proporciona el sistema a través de [**SetLayeredWindowAttributes.**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) Además, el uso **de UpdateLayeredWindow usa** directamente la memoria de forma más eficaz, ya que el sistema no necesita la memoria adicional necesaria para almacenar la imagen de la ventana redirigida. Para obtener la máxima eficacia en la animación de ventanas, llame a **UpdateLayeredWindow** para cambiar la posición y el tamaño de una ventana en capas. Tenga en cuenta que después de llamar a **SetLayeredWindowAttributes,** se producirá un error en las llamadas **a UpdateLayeredWindow** posteriores hasta que el bit de estilo de capas se borra y se vuelve a establecer.

Las pruebas de acceso de una ventana en capas se basan en la forma y la transparencia de la ventana. Esto significa que las áreas de la ventana con clave de color o cuyo valor alfa es cero permitirán que pasen los mensajes del mouse. Sin embargo, si la ventana superada tiene el estilo de ventana extendida **WS \_ EX \_ TRANSPARENT,** la forma de la ventana superada se omitirá y los eventos del mouse se pasarán a otras ventanas debajo de la ventana superada.

### <a name="message-only-windows"></a>Message-Only Windows

Una *ventana de solo mensaje* le permite enviar y recibir mensajes. No es visible, no tiene ningún orden Z, no se puede enumerar y no recibe mensajes de difusión. La ventana simplemente envía mensajes.

Para crear una ventana de solo mensaje, especifique la constante [HWND \_ MESSAGE](#message-only-windows) o un identificador para una ventana de solo mensaje existente en el *parámetro hWndParent* de la [**función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) También puede cambiar una ventana existente a una ventana de solo mensaje especificando HWND MESSAGE en el \_ *parámetro hWndNewParent* de la [**función SetParent.**](/windows/win32/api/winuser/nf-winuser-setparent)

Para buscar ventanas de solo mensaje, especifique [HWND \_ MESSAGE](#message-only-windows) en el *parámetro hwndParent* de la [**función FindWindowEx.**](/windows/win32/api/winuser/nf-winuser-findwindowexa) Además, **FindWindowEx** busca ventanas de solo mensaje, así como ventanas de nivel superior si los parámetros *hwndParent* y *hwndChildAfter* son **NULL.**

## <a name="window-relationships"></a>Relaciones de ventana

Hay muchas maneras en que una ventana puede relacionarse con el usuario u otra ventana. Una ventana puede ser una ventana de propiedad, una ventana de primer plano o una ventana de fondo. Una ventana también tiene un orden Z con respecto a otras ventanas. Para obtener más información, vea los temas siguientes:

-   [Primer plano y fondo Windows](#foreground-and-background-windows)
-   [Propiedad Windows](#owned-windows)
-   [Orden Z](#z-order)

### <a name="foreground-and-background-windows"></a>Primer plano y fondo Windows

Cada proceso puede tener varios subprocesos de ejecución y cada subproceso puede crear ventanas. El subproceso que creó la ventana con la que el usuario está trabajando actualmente se denomina subproceso en primer plano y la ventana se denomina ventana *de primer plano.* Todos los demás subprocesos son subprocesos en segundo plano y las ventanas creadas por subprocesos en segundo plano se *denominan ventanas en segundo plano.*

Cada subproceso tiene un nivel de prioridad que determina la cantidad de tiempo de CPU que recibe el subproceso. Aunque una aplicación puede establecer el nivel de prioridad de sus subprocesos, normalmente el subproceso en primer plano tiene un nivel de prioridad ligeramente mayor que los subprocesos en segundo plano. Dado que tiene una prioridad mayor, el subproceso en primer plano recibe más tiempo de CPU que los subprocesos en segundo plano. El subproceso de primer plano tiene una prioridad base normal de 9; un subproceso en segundo plano tiene una prioridad base normal de 7.

El usuario establece la ventana en primer plano haciendo clic en una ventana o usando la combinación de teclas ALT+TAB o ALT+ESC. Para recuperar un identificador en la ventana de primer plano, use la [**función GetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-getforegroundwindow) Para comprobar si la ventana de la aplicación es la ventana de primer plano, compare el identificador devuelto por **GetForegroundWindow** con el de la ventana de la aplicación.

Una aplicación establece la ventana de primer plano mediante la [**función SetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow)

El sistema restringe qué procesos pueden establecer la ventana de primer plano. Un proceso solo puede establecer la ventana de primer plano si:

- Se cumplen todas las condiciones siguientes:
  - El proceso que llama a **SetForegroundWindow** pertenece a una aplicación de escritorio, no a una aplicación para UWP o a una aplicación de Windows Store diseñada para Windows 8 o 8.1.
  - El proceso de primer plano no ha deshabilitado las llamadas a **SetForegroundWindow** mediante una llamada anterior a la [**función LockSetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)
  - El tiempo de espera del bloqueo de primer plano ha [ **expirado (vea SPI_GETFOREGROUNDLOCKTIMEOUT** **en SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - No hay menús activos.
- Además, se cumple al menos una de las condiciones siguientes:
  - El proceso de llamada es el proceso de primer plano.
  - El proceso de llamada inició el proceso en primer plano.
  - Actualmente no hay ninguna ventana de primer plano y, por tanto, no hay ningún proceso de primer plano.
  - El proceso de llamada recibió el último evento de entrada.
  - Se está depurando el proceso de primer plano o el proceso de llamada.

Es posible que un proceso se deniegue el derecho a establecer la ventana de primer plano incluso si cumple estas condiciones.

Un proceso que puede establecer la ventana de primer plano puede permitir que otro proceso establezca la ventana de primer plano llamando a la función [**AllowSetForegroundWindow**](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow) o llamando a la función [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) con la marca **\_ BSF ALLOWSFW.** El proceso de primer plano puede deshabilitar las [**llamadas a SetForegroundWindow llamando**](/windows/win32/api/winuser/nf-winuser-setforegroundwindow) a la función [**LockSetForegroundWindow.**](/windows/win32/api/winuser/nf-winuser-locksetforegroundwindow)

### <a name="owned-windows"></a>Propiedad Windows

Una ventana superpuesta o emergente puede ser propiedad de otra ventana superpuesta o emergente. Ser propietario coloca varias restricciones en una ventana.

-   Una ventana de propiedad siempre está por encima de su propietario en el orden Z.
-   El sistema destruye automáticamente una ventana propiedad cuando se destruye su propietario.
-   Una ventana de propiedad se oculta cuando se minimiza su propietario.

Solo una ventana superpuesta o emergente puede ser una ventana de propietario; una ventana secundaria no puede ser una ventana de propietario. Una aplicación crea una ventana propiedad especificando el identificador de ventana del propietario como el parámetro *hwndParent* de [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) cuando crea una ventana con el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ POPUP.** El *parámetro hwndParent* debe identificar una ventana superpuesta o emergente. Si *hwndParent identifica* una ventana secundaria, el sistema asigna la propiedad a la ventana primaria de nivel superior de la ventana secundaria. Después de crear una ventana de propiedad, una aplicación no puede transferir la propiedad de la ventana a otra ventana.

Los cuadros de diálogo y los cuadros de mensaje son ventanas de propiedad de forma predeterminada. Una aplicación especifica la ventana de propietario al llamar a una función que crea un cuadro de diálogo o un cuadro de mensaje.

Una aplicación puede usar la [**función GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con la **marca GW \_ OWNER** para recuperar un identificador para el propietario de una ventana.

### <a name="z-order"></a>Orden Z

El *orden z de* una ventana indica la posición de la ventana en una pila de ventanas superpuestas. Esta pila de ventanas está orientada a lo largo de un eje imaginario, el eje Z, que se extiende hacia el exterior desde la pantalla. La ventana de la parte superior del orden Z se superpone a todas las demás ventanas. Todas las demás ventanas superponen la ventana de la parte inferior del orden Z.

El sistema mantiene el orden Z en una sola lista. Agrega ventanas al orden z en función de si son ventanas de nivel superior, ventanas de nivel superior o ventanas secundarias. Una *ventana de nivel superior* se superpone a todas las demás ventanas no superiores, independientemente de si es la ventana activa o en primer plano. Una ventana de nivel superior tiene el **estilo WS \_ EX \_ TOPMOST.** Todas las ventanas superiores aparecen en el orden z antes que las ventanas que no son superiores. Una ventana secundaria se agrupa con su elemento primario en orden z.

Cuando una aplicación crea una ventana, el sistema la coloca en la parte superior del orden Z para las ventanas del mismo tipo. Puede usar la [**función BringWindowToTop**](/windows/win32/api/winuser/nf-winuser-bringwindowtotop) para llevar una ventana a la parte superior del orden Z para las ventanas del mismo tipo. Puede reorganizar el orden z mediante las [**funciones SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) [**y DeferWindowPos.**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)

El usuario cambia el orden Z activando una ventana diferente. El sistema coloca la ventana activa en la parte superior del orden Z para las ventanas del mismo tipo. Cuando una ventana llega a la parte superior del orden Z, también lo hacen sus ventanas secundarias. Puede usar la función [**GetTopWindow**](/windows/win32/api/winuser/nf-winuser-gettopwindow) para buscar en todas las ventanas secundarias de una ventana primaria y devolver un identificador a la ventana secundaria que sea más alta en orden z. La [**función GetNextWindow**](/windows/win32/api/winuser/nf-winuser-getnextwindow) recupera un identificador de la ventana siguiente o anterior en orden z.

## <a name="window-show-state"></a>Mostrar estado de la ventana

En un momento dado, una ventana puede estar activa o inactiva; hidden o visible; y se minimizan, maximizan o restauran. Estas calidades se conocen colectivamente como el estado *de presentación de la ventana.* En los temas siguientes se describe el estado de presentación de la ventana:

-   [Ventana activa](#active-window)
-   [Deshabilitada Windows](#disabled-windows)
-   [Visibilidad de las ventanas](#window-visibility)
-   [Minimizado, maximizado y restaurado Windows](#minimized-maximized-and-restored-windows)

### <a name="active-window"></a>Ventana activa

Una *ventana activa* es la ventana de nivel superior de la aplicación con la que el usuario está trabajando actualmente. Para permitir que el usuario identifique fácilmente la ventana activa, el sistema la coloca en la parte superior del orden z y cambia el color de la barra de título y el borde a los colores de la ventana activa definidos por el sistema. Solo una ventana de nivel superior puede ser una ventana activa. Cuando el usuario trabaja con una ventana secundaria, el sistema activa la ventana primaria de nivel superior asociada a la ventana secundaria.

Solo una ventana de nivel superior del sistema está activa a la vez. El usuario activa una ventana de nivel superior haciendo clic en ella (o en una de sus ventanas secundarias) o mediante la combinación de teclas ALT+ESC o ALT+TAB. Una aplicación activa una ventana de nivel superior llamando a la [**función SetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-setactivewindow) Otras funciones pueden hacer que el sistema active otra ventana de nivel superior, como [**SetWindowPos,**](/windows/win32/api/winuser/nf-winuser-setwindowpos) [**DeferWindowPos,**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement)y [**DestroyWindow.**](/windows/win32/api/winuser/nf-winuser-destroywindow) Aunque una aplicación puede activar una ventana de nivel superior diferente en cualquier momento, para evitar confundir al usuario, solo debe hacerlo en respuesta a una acción del usuario. Una aplicación usa la [**función GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) para recuperar un identificador en la ventana activa.

Cuando la activación cambia de una ventana de nivel superior de una aplicación a la ventana de nivel superior de otra, el sistema envía un mensaje [**WM \_ ACTIVATEAPP**](wm-activateapp.md) a ambas aplicaciones, notificándolos del cambio. Cuando la activación cambia a otra ventana de nivel superior en la misma aplicación, el sistema envía a ambas ventanas un [**mensaje WM \_ ACTIVATE.**](../inputdev/wm-activate.md)

### <a name="disabled-windows"></a>Deshabilitada Windows

Se puede deshabilitar una ventana. Una *ventana deshabilitada* no recibe ninguna entrada de teclado o mouse del usuario, pero puede recibir mensajes de otras ventanas, de otras aplicaciones y del sistema. Normalmente, una aplicación deshabilita una ventana para impedir que el usuario use la ventana. Por ejemplo, una aplicación puede deshabilitar un botón de inserción en un cuadro de diálogo para impedir que el usuario la elija. Una aplicación puede habilitar una ventana deshabilitada en cualquier momento; al habilitar una ventana, se restaura la entrada normal.

De forma predeterminada, se habilita una ventana cuando se crea. Sin embargo, una aplicación puede especificar [**el estilo WS \_ DISABLED**](window-styles.md) para deshabilitar una nueva ventana. Una aplicación habilita o deshabilita una ventana existente mediante la [**función EnableWindow.**](/windows/win32/api/winuser/nf-winuser-enablewindow) El sistema envía un mensaje [**\_ WM ENABLE**](wm-enable.md) a una ventana cuando su estado habilitado está a punto de cambiar. Una aplicación puede determinar si una ventana está habilitada mediante la [**función IsWindowEnabled.**](/windows/win32/api/winuser/nf-winuser-iswindowenabled)

Cuando se deshabilita una ventana secundaria, el sistema pasa los mensajes de entrada del mouse del elemento secundario a la ventana primaria. El elemento primario usa los mensajes para determinar si se va a habilitar la ventana secundaria. Para obtener más información, vea [Mouse Input](../inputdev/mouse-input.md).

Solo una ventana a la vez puede recibir entradas de teclado; se dice que esa ventana tiene el foco del teclado. Si una aplicación usa la [**función EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) para deshabilitar una ventana de foco de teclado, la ventana pierde el foco del teclado además de deshabilitarse. **Después, EnableWindow** establece el foco del teclado **en NULL,** lo que significa que ninguna ventana tiene el foco. Si una ventana secundaria, u otra ventana descendiente, tiene el foco de teclado, la ventana descendiente pierde el foco cuando la ventana primaria está deshabilitada. Para obtener más información, vea [Entrada de teclado](../inputdev/keyboard-input.md).

### <a name="window-visibility"></a>Visibilidad de las ventanas

Una ventana puede estar visible u oculta. El sistema muestra una *ventana visible* en la pantalla. Oculta una ventana *oculta al* no dibujarla. Si la ventana está visible, el usuario puede introducir información en la ventana y ver los resultados de la misma. Si una ventana está oculta, en realidad está deshabilitada. Una ventana oculta puede procesar mensajes del sistema o de otras ventanas, pero no puede procesar los datos de entrada del usuario ni mostrar los de salida. Una aplicación establece el estado de visibilidad de una ventana al crear la ventana. Más adelante, la aplicación puede cambiar el estado de visibilidad.

Una ventana es visible cuando se establece el estilo visible de [**WS \_**](window-styles.md) para la ventana. De forma predeterminada, [**la función CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) crea una ventana oculta a menos que la aplicación especifique el **estilo visible de \_ WS.** Normalmente, una aplicación establece el estilo visible de **WS \_** después de crear una ventana para mantener los detalles del proceso de creación ocultos al usuario. Por ejemplo, una aplicación puede mantener oculta una nueva ventana mientras personaliza la apariencia de la ventana. Si el **estilo WS \_ VISIBLE** se especifica en **CreateWindowEx**, el sistema envía el mensaje [**WM \_ SHOWWINDOW**](wm-showwindow.md) a la ventana después de crear la ventana, pero antes de mostrarla.

Una aplicación puede determinar si una ventana está visible mediante la [**función IsWindowVisible.**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) Una aplicación puede mostrar (hacer visible) u ocultar una ventana mediante la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow), [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos), [**DeferWindowPos**](/windows/win32/api/winuser/nf-winuser-deferwindowpos)o [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) [**o SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) Estas funciones muestran u ocultan una ventana estableciendo o quitando el estilo [**visible de WS \_**](window-styles.md) para la ventana. También envían el mensaje [**\_ WM SHOWWINDOW**](wm-showwindow.md) a la ventana antes de mostrarlo u ocultarlo.

Cuando se minimiza una ventana de propietario, el sistema oculta automáticamente las ventanas de propiedad asociadas. De forma similar, cuando se restaura una ventana de propietario, el sistema muestra automáticamente las ventanas de propiedad asociadas. En ambos casos, el sistema envía el [**mensaje \_ WM SHOWWINDOW**](wm-showwindow.md) a las ventanas que poseen antes de ocultarlas o mostrarlas. En ocasiones, es posible que una aplicación tenga que ocultar las ventanas de propiedad sin tener que minimizar u ocultar el propietario. En este caso, la aplicación usa la [**función ShowOwnedPopups.**](/windows/win32/api/winuser/nf-winuser-showownedpopups) Esta función establece o quita el estilo visible de [**WS \_**](window-styles.md) para todas las ventanas de propiedad y envía el mensaje **\_ SHOWWINDOW** de WM a las ventanas que poseen antes de ocultarlas o mostrarlas. Ocultar una ventana de propietario no tiene ningún efecto en el estado de visibilidad de las ventanas de propiedad.

Cuando una ventana primaria está visible, también están visibles sus ventanas secundarias asociadas. De forma similar, cuando la ventana primaria está oculta, también se ocultan sus ventanas secundarias. Minimizar la ventana primaria no tiene ningún efecto en el estado de visibilidad de las ventanas secundarias; Es decir, las ventanas secundarias se minimizan junto con el elemento primario, pero el [**estilo WS \_ VISIBLE**](window-styles.md) no cambia.

Incluso si una ventana tiene el estilo [**WS \_ VISIBLE,**](window-styles.md) es posible que el usuario no pueda ver la ventana en la pantalla; es posible que otras ventanas se superpongan por completo o que se haya movido más allá del borde de la pantalla. Además, una ventana secundaria visible está sujeta a las reglas de recorte establecidas por su relación de elementos primarios y secundarios. Si la ventana primaria de la ventana no está visible, tampoco estará visible. Si la ventana primaria se mueve más allá del borde de la pantalla, la ventana secundaria también se mueve porque se dibuja una ventana secundaria con respecto a la esquina superior izquierda del elemento primario. Por ejemplo, un usuario puede mover la ventana primaria que contiene la ventana secundaria lo suficientemente lejos del borde de la pantalla para que el usuario no pueda ver la ventana secundaria, aunque la ventana secundaria y su ventana primaria tengan el estilo VISIBLE de **WS. \_**

### <a name="minimized-maximized-and-restored-windows"></a>Minimizado, maximizado y restaurado Windows

Una *ventana maximizada* es una ventana que tiene el [**estilo WS \_ MAXIMIZE.**](window-styles.md) De manera predeterminada, el sistema agranda una ventana maximizada para que ocupe toda la pantalla o, en el caso de las ventanas secundarias, toda el área de cliente de la ventana primaria. Aunque el tamaño de una ventana se puede establecer en el mismo tamaño de una ventana maximizada, una ventana maximizada es ligeramente diferente. El sistema mueve automáticamente la barra de título de la ventana a la parte superior de la pantalla o a la parte superior del área de cliente de la ventana primaria. Además, el sistema deshabilita el borde de tamaño de la ventana y la funcionalidad de posicionamiento de la ventana de la barra de título (para que el usuario no pueda mover la ventana arrastrando la barra de título).

Una *ventana minimizada* es una ventana que tiene el [**estilo WS \_ MINIMIZE.**](window-styles.md) De manera predeterminada, el sistema reduce una ventana minimizada al tamaño del botón de la barra de tareas y la mueve a la barra de tareas. Una *ventana restaurada* es una ventana que se ha devuelto a su tamaño y posición anteriores, es decir, el tamaño que tenía antes de que se minimizara o maximizara.

Si una aplicación especifica el estilo [**WS \_ MAXIMIZE**](window-styles.md) o **WS \_ MINIMIZE** en la [**función CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) la ventana se maximiza o minimiza inicialmente. Después de crear una ventana, una aplicación puede usar la [**función CloseWindow**](/windows/win32/api/winuser/nf-winuser-closewindow) para minimizar la ventana. La [**función ArrangeIconicWindows**](/windows/win32/api/winuser/nf-winuser-arrangeiconicwindows) organiza los iconos en el escritorio o organiza las ventanas secundarias minimizadas de una ventana primaria en la ventana primaria. La [**función OpenIcon**](/windows/win32/api/winuser/nf-winuser-openicon) restaura una ventana minimizada a su tamaño y posición anteriores.

La [**función ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) puede minimizar, maximizar o restaurar una ventana. También puede establecer los estados de visibilidad y activación de la ventana. La [**función SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) incluye la misma funcionalidad que **ShowWindow,** pero puede invalidar las posiciones predeterminadas minimizadas, maximizadas y restauradas de la ventana.

Las [**funciones IsZoomed**](/windows/win32/api/winuser/nf-winuser-iszoomed) [**e IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) determinan si una ventana determinada está maximizada o minimizada, respectivamente. La [**función GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) recupera las posiciones minimizadas, maximizadas y restauradas de la ventana, y también determina el estado de presentación de la ventana.

Cuando el sistema recibe un comando para maximizar o restaurar una ventana minimizada, envía a la ventana un [**mensaje \_ WM QUERYOPEN.**](wm-queryopen.md) Si el procedimiento de ventana devuelve **FALSE**, el sistema omite el comando maximize o restore.

El sistema establece automáticamente el tamaño y la posición de una ventana maximizada en los valores predeterminados definidos por el sistema para una ventana maximizada. Para invalidar estos valores predeterminados, una aplicación puede llamar a la función [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) o procesar el mensaje [**\_ GETMINMAXINFO**](wm-getminmaxinfo.md) de WM que recibe una ventana cuando el sistema está a punto de maximizar la ventana. **WM \_ GETMINMAXINFO incluye** un puntero a una estructura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene valores que el sistema usa para establecer el tamaño y la posición maximizados. Reemplazar estos valores invalida los valores predeterminados.

## <a name="window-size-and-position"></a>Tamaño y posición de la ventana

El tamaño y la posición de una ventana se expresan como un rectángulo delimitador, dado en coordenadas relativas a la pantalla o a la ventana primaria. Las coordenadas de una ventana de nivel superior son relativas a la esquina superior izquierda de la pantalla; las coordenadas de una ventana secundaria son relativas a la esquina superior izquierda de la ventana primaria. Una aplicación especifica el tamaño inicial y la posición de una ventana cuando crea la ventana, pero puede cambiar el tamaño y la posición de la ventana en cualquier momento. Para obtener más información, vea [Formas rellenas.](../gdi/filled-shapes.md)

Esta sección contiene los siguientes temas:

-   [Tamaño y posición predeterminados](#default-size-and-position)
-   [Tamaño de seguimiento](#tracking-size)
-   [Comandos del sistema](#system-commands)
-   [Funciones de tamaño y posición](#size-and-position-functions)
-   [Mensajes de tamaño y posición](#size-and-position-messages)

### <a name="default-size-and-position"></a>Tamaño y posición predeterminados

Una aplicación puede permitir que el sistema calcule el tamaño inicial o la posición de una ventana de nivel superior especificando CW \_ USEDEFAULT en [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa). Si la aplicación establece las coordenadas de la ventana en CW USEDEFAULT y no ha creado ninguna otra ventana de nivel superior, el sistema establece la posición de la nueva ventana con respecto a la esquina superior izquierda de la pantalla; de lo contrario, establece la posición con respecto a la posición de la ventana de nivel superior que la aplicación creó \_ más recientemente. Si los parámetros de ancho y alto se establecen en CW USEDEFAULT, el sistema \_ calcula el tamaño de la nueva ventana. Si la aplicación ha creado otras ventanas de nivel superior, el sistema basa el tamaño de la nueva ventana en el tamaño de la ventana de nivel superior creada más recientemente. La especificación de CW USEDEFAULT al crear una ventana secundaria o emergente hace que el sistema establezca el tamaño de la ventana en el tamaño mínimo predeterminado \_ de la ventana.

### <a name="tracking-size"></a>Tamaño de seguimiento

El sistema mantiene un tamaño de seguimiento mínimo y máximo para una ventana del estilo [**\_ WS THICKFRAME;**](window-styles.md) una ventana con este estilo tiene un borde de tamaño. El *tamaño mínimo de seguimiento es* el tamaño de ventana más pequeño que puede generar arrastrando el borde de tamaño de la ventana. Del mismo modo, el *tamaño máximo de seguimiento* es el mayor tamaño de ventana que puede generar arrastrando el borde de tamaño.

Los tamaños de seguimiento mínimo y máximo de una ventana se establecen en valores predeterminados definidos por el sistema cuando el sistema crea la ventana. Una aplicación puede detectar los valores predeterminados e invalidarlos procesando el [**\_ mensaje WM GETMINMAXINFO.**](wm-getminmaxinfo.md) Para obtener más información, vea [Mensajes de tamaño y posición.](#size-and-position-messages)

### <a name="system-commands"></a>Comandos del sistema

Una aplicación que tiene un menú de ventana puede cambiar el tamaño y la posición de esa ventana mediante el envío de comandos del sistema. Los comandos del sistema se generan cuando el usuario elige comandos en el menú de la ventana. Una aplicación puede emular la acción del usuario mediante el envío de un [**mensaje \_ SYSCOMMAND**](../menurc/wm-syscommand.md) de WM a la ventana. Los siguientes comandos del sistema afectan al tamaño y la posición de una ventana.



| Get-Help      | Descripción                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SC \_ CLOSE    | Cierra la ventana. Este comando envía un [**mensaje WM \_ CLOSE**](wm-close.md) a la ventana. La ventana lleva a cabo los pasos necesarios para limpiarse y destruirse. |
| SC \_ MAXIMIZE | Maximiza la ventana.                                                                                                                                                |
| SC \_ MINIMIZE | Minimiza la ventana.                                                                                                                                                |
| SC \_ MOVE     | Mueve la ventana.                                                                                                                                                    |
| RESTAURACIÓN \_ DE SC  | Restaura una ventana minimizada o maximizada a su tamaño y posición anteriores.                                                                                          |
| SC \_ SIZE     | Inicia un comando de tamaño. Para cambiar el tamaño de la ventana, use el mouse o el teclado.                                                                                  |



 

### <a name="size-and-position-functions"></a>Funciones de tamaño y posición

Después de crear una ventana, una aplicación puede establecer el tamaño o la posición de la ventana llamando a una de varias funciones diferentes, como [**SetWindowPlacement,**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) [**MoveWindow,**](/windows/win32/api/winuser/nf-winuser-movewindow) [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)y [**DeferWindowPos.**](/windows/win32/api/winuser/nf-winuser-deferwindowpos) **SetWindowPlacement establece** la posición minimizada, la posición maximizada, el tamaño y la posición restaurados y el estado de presentación de una ventana. Las **funciones MoveWindow** **y SetWindowPos** son similares; ambos establecen el tamaño o la posición de una sola ventana de aplicación. La **función SetWindowPos** incluye un conjunto de marcas que afectan al estado de presentación de la ventana; **MoveWindow** no incluye estas marcas. Use las funciones [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos), **DeferWindowPos** y [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos) para establecer simultáneamente la posición de varias ventanas, incluidos el tamaño, la posición, la posición en el orden z y el estado de presentación.

Una aplicación puede recuperar las coordenadas del rectángulo delimitador de una ventana mediante la [**función GetWindowRect.**](/windows/win32/api/winuser/nf-winuser-getwindowrect) **GetWindowRect** rellena una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de las esquinas superior izquierda e inferior derecha de la ventana. Las coordenadas son relativas a la esquina superior izquierda de la pantalla, incluso para una ventana secundaria. La [**función ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) o [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) asigna las coordenadas de pantalla del rectángulo delimitador de una ventana secundaria a las coordenadas relativas al área cliente de la ventana primaria.

La [**función GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) recupera las coordenadas del área de cliente de una ventana. **GetClientRect** rellena una estructura [**RECT**](/previous-versions//dd162897(v=vs.85)) con las coordenadas de las esquinas superior izquierda e inferior derecha del área cliente, pero las coordenadas son relativas al propio área de cliente. Esto significa que las coordenadas de la esquina superior izquierda de un área cliente siempre son (0,0) y las coordenadas de la esquina inferior derecha son el ancho y alto del área cliente.

La [**función CascadeWindows**](/windows/win32/api/winuser/nf-winuser-cascadewindows) en cascada las ventanas del escritorio o las ventanas secundarias de la ventana primaria especificada. La [**función TileWindows**](/windows/win32/api/winuser/nf-winuser-tilewindows) iconos las ventanas del escritorio o iconos de las ventanas secundarias de la ventana primaria especificada.

### <a name="size-and-position-messages"></a>Mensajes de tamaño y posición

El sistema envía el [**mensaje \_ WM GETMINMAXINFO**](wm-getminmaxinfo.md) a una ventana cuyo tamaño o posición está a punto de cambiar. Por ejemplo, el mensaje se envía  cuando  el usuario hace clic en Mover o Tamaño en el menú de la ventana o hace clic en el borde de tamaño o la barra de título; El mensaje también se envía cuando una aplicación llama a [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para mover o cambiar el tamaño de la ventana. **WM \_ GETMINMAXINFO incluye** un puntero a una estructura [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene el tamaño y la posición maximizados predeterminados para la ventana, así como los tamaños de seguimiento mínimo y máximo predeterminados. Una aplicación puede invalidar los valores predeterminados **procesando WM \_ GETMINMAXINFO** y estableciendo los miembros adecuados **de MINMAXINFO**. Una ventana debe tener el [**estilo WS \_ THICKFRAME**](window-styles.md) o **WS \_ CAPTION** para recibir **WM \_ GETMINMAXINFO**. Una ventana con el **estilo \_ WS THICKFRAME** recibe este mensaje durante el proceso de creación de la ventana, así como cuando se mueve o se dimensiona.

El sistema envía el [**mensaje WM \_ WINDOWPOSCHANGING**](wm-windowposchanging.md) a una ventana cuyo tamaño, posición, posición en el orden z o estado de presentación está a punto de cambiar. Este mensaje incluye un puntero a una estructura [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que especifica el nuevo tamaño, la posición, la posición en el orden z y el estado de presentación de la ventana. Al establecer los miembros de **WINDOWPOS,** una aplicación puede afectar al nuevo tamaño, la posición y la apariencia de la ventana.

Después de cambiar el tamaño, la posición, la posición de una ventana en el estado z o mostrar, el sistema envía el mensaje [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) a la ventana. Este mensaje incluye un puntero a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) que informa a la ventana de su nuevo tamaño, posición, posición en el orden z y estado de presentación. Establecer los miembros de la **estructura WINDOWPOS** que se pasa con **WM \_ WINDOWPOSCHANGED** no tiene ningún efecto en la ventana. Una ventana que debe procesar los mensajes [**WM \_ SIZE**](wm-size.md) y [**WM \_ MOVE**](wm-move.md) debe pasar **WM \_ WINDOWPOSCHANGED** a la función [**DefWindowProc;**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) de lo contrario, el sistema no envía mensajes **WM \_ SIZE** y **WM \_ MOVE** a la ventana.

El sistema envía el [**mensaje \_ WM NCCALCSIZE**](wm-nccalcsize.md) a una ventana cuando se crea o se dimensiona la ventana. El sistema usa el mensaje para calcular el tamaño del área de cliente de una ventana y la posición del área de cliente con respecto a la esquina superior izquierda de la ventana. Normalmente, una ventana pasa este mensaje al procedimiento de ventana predeterminado; sin embargo, este mensaje puede ser útil en aplicaciones que personalizan el área no cliente de una ventana o conservan partes del área de cliente cuando se dimensiona la ventana. Para obtener más información, vea [Pintar y dibujar](../gdi/painting-and-drawing.md).

## <a name="window-animation"></a>Animación de ventana

Puede producir efectos especiales al mostrar u ocultar ventanas mediante la [**función AnimateWindow.**](/windows/win32/api/winuser/nf-winuser-animatewindow) Cuando la ventana se anima de esta manera, el sistema deslizará, deslizará o atenuará la ventana, en función de las marcas que especifique en una llamada a **AnimateWindow**.

De forma predeterminada, el sistema usa *la animación de lanzamiento*. Con este efecto, parece que la ventana se abre (que muestra la ventana) o se enrolla cerrada (ocultando la ventana). Puede usar el parámetro *dwFlags* para especificar si la ventana se enrolla horizontal, vertical o diagonalmente.

Al especificar la marca **SLIDE de \_ AW,** el sistema usa la *animación de diapositivas*. Con este efecto, la ventana parece deslizarse hacia la vista (que muestra la ventana) o deslizarse fuera de la vista (ocultando la ventana). Puede usar el parámetro *dwFlags* para especificar si la ventana se desliza horizontal, vertical o diagonalmente.

Cuando se especifica la **marca \_ BLEND de AW,** el sistema usa una *atenuación de mezcla alfa.*

También puede usar la marca **CENTRO de AW \_** para que una ventana parezca contraerse hacia dentro o expandirse hacia fuera.

## <a name="window-layout-and-mirroring"></a>Diseño y creación de reflejo de ventanas

El diseño de la ventana define cómo se disposición el texto Windows Interfaz de dispositivo gráfico objetos (GDI) en una ventana o contexto de dispositivo (DC). Algunos idiomas, como inglés, francés y alemán, requieren un diseño de izquierda a derecha (LTR). Otros idiomas, como el árabe y el hebreo, requieren un diseño de derecha a izquierda (RTL). El diseño de la ventana se aplica al texto, pero también afecta a los demás elementos GDI de la ventana, incluidos los mapas de bits, los iconos, la ubicación del origen, los botones, los controles de árbol en cascada y si la coordenada horizontal aumenta a medida que se va hacia la izquierda o la derecha. Por ejemplo, una vez que una aplicación ha establecido el diseño RTL, el origen se coloca en el borde derecho de la ventana o el dispositivo, y el número que representa la coordenada horizontal aumenta a medida que se desplaza a la izquierda. Sin embargo, no todos los objetos se ven afectados por el diseño de una ventana. Por ejemplo, el diseño de cuadros de diálogo, cuadros de mensaje y contextos de dispositivo que no están asociados a una ventana, como metarchivo e controladores de dominio de impresora, se debe controlar por separado. Los detalles de estos se mencionan más adelante en este tema.

Las funciones de ventana permiten especificar o cambiar el diseño de la ventana en las versiones árabe y hebreo de Windows. Tenga en cuenta que el cambio a un diseño RTL (también conocido como creación de reflejo) no se admite para las ventanas que tienen el estilo [CS \_ OWNDC](about-window-classes.md) o para un controlador de dominio con el modo gráfico GM \_ ADVANCED.

De forma predeterminada, el diseño de la ventana es de izquierda a derecha (LTR). Para establecer el diseño de la ventana RTL, llame [**a CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) con el estilo **WS \_ EX \_ LAYOUTRTL**. Además, de forma predeterminada, una ventana secundaria (es decir, una creada con el estilo [**WS \_ CHILD**](window-styles.md) y con un parámetro *hWnd* primario válido en la llamada a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o **CreateWindowEx)** tiene el mismo diseño que su elemento primario. Para deshabilitar la herencia de la creación de reflejo en todas las ventanas secundarias, especifique **WS \_ EX \_ NOINHERITLAYOUT** en la llamada a **CreateWindowEx**. Tenga en cuenta que la creación de reflejo no la heredan las ventanas de propiedad (las creadas sin el estilo **WS \_ CHILD)** o las creadas con el parámetro *hWnd* primario en **CreateWindowEx** establecido en **NULL.** Para deshabilitar la herencia de la creación de reflejo para una ventana individual, procese el mensaje [**\_ WM NCCREATE**](wm-nccreate.md) con [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) para desactivar la marca **\_ \_ LAYOUTRTL de WS EX.** Este procesamiento se suma a cualquier otro procesamiento necesario. El fragmento de código siguiente muestra cómo se hace esto.


```
SetWindowLong (hWnd, 
               GWL_EXSTYLE, 
               GetWindowLong(hWnd,GWL_EXSTYLE) & ~WS_EX_LAYOUTRTL))
```



Puede establecer el diseño predeterminado en RTL llamando a [**SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout)(LAYOUT \_ RTL). Todas las ventanas creadas después de la llamada se reflejarán, pero las ventanas existentes no se verán afectadas. Para desactivar la creación de reflejo predeterminada, llame **a SetProcessDefaultLayout**(0).

Tenga en [**cuenta que SetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-setprocessdefaultlayout) solo refleja los DCs de las ventanas reflejadas. Para reflejar cualquier controlador de dominio, llame [**a SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT \_ RTL). Para obtener más información, vea la explicación sobre la creación de reflejo de contextos de dispositivo no asociados a windows, que se incluye más adelante en este tema.

Los mapas de bits y los iconos de una ventana reflejada también se reflejan de forma predeterminada. Sin embargo, no todos estos deben reflejarse. Por ejemplo, los que tienen texto, un logotipo empresarial o un reloj análogo no deben reflejarse. Para deshabilitar la creación de reflejo de los mapas de bits, llame a [**SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) con el conjunto de \_ bits LAYOUT BITMAPORIENTATIONPRESERVED en *dwLayout*. Para deshabilitar la creación de reflejo en un controlador de dominio, llame a **SetLayout**(hdc, 0).

Para consultar el diseño predeterminado actual, llame [**a GetProcessDefaultLayout**](/windows/win32/api/winuser/nf-winuser-getprocessdefaultlayout). Tras una devolución correcta, *pdwDefaultLayout contiene* LAYOUT \_ RTL o 0. Para consultar la configuración de diseño del contexto del dispositivo, llame [**a GetLayout**](/windows/win32/api/wingdi/nf-wingdi-getlayout). Tras una devolución correcta, **GetLayout** devuelve un **DWORD** que indica la configuración de diseño por la configuración de LAYOUT RTL y los \_ bits LAYOUT \_ BITMAPORIENTATIONPRESERVED.

Una vez creada una ventana, se cambia el diseño mediante la [**función SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) Por ejemplo, esto es necesario cuando el usuario cambia el idioma de la interfaz de usuario de una ventana existente de árabe o hebreo a alemán. Sin embargo, al cambiar el diseño de una ventana existente, debe invalidar y actualizar la ventana para asegurarse de que el contenido de la ventana se dibuja en el mismo diseño. El ejemplo de código siguiente es del código de ejemplo que cambia el diseño de la ventana según sea necesario:


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



En la creación de reflejo, debe pensar en términos de "cerca" y "lejos" en lugar de "izquierda" y "derecha". Si no lo hace, puede producir problemas. Una práctica de codificación común que provoca problemas en una ventana reflejada se produce al asignar entre coordenadas de pantalla y coordenadas de cliente. Por ejemplo, las aplicaciones suelen usar código similar al siguiente para colocar un control en una ventana:


```
// DO NOT USE THIS IF APPLICATION MIRRORS THE WINDOW

// get coordinates of the window in screen coordinates
GetWindowRect(hControl, (LPRECT) &rControlRect);  

// map screen coordinates to client coordinates in dialog
ScreenToClient(hDialog, (LPPOINT) &rControlRect.left); 
ScreenToClient(hDialog, (LPPOINT) &rControlRect.right);
```



Esto provoca problemas en la creación de reflejo porque el borde izquierdo del rectángulo se convierte en el borde derecho de una ventana reflejada y viceversa. Para evitar este problema, reemplace las llamadas [**ScreenToClient**](/windows/win32/api/winuser/nf-winuser-screentoclient) por una llamada a [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) como se muestra a continuación:


```
// USE THIS FOR MIRRORING

GetWindowRect(hControl, (LPRECT) &rControlRect);
MapWindowPoints(NULL, hDialog, (LPPOINT) &rControlRect, 2)
```



Este código funciona porque, en plataformas que admiten la creación de reflejo, [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) se modifica para intercambiar las coordenadas de punto izquierdo y derecho cuando se refleja la ventana del cliente. Para obtener más información, vea la sección Comentarios de **MapWindowPoints**.

Otra práctica común que puede causar problemas en las ventanas reflejadas es colocar objetos en una ventana de cliente mediante desplazamientos en coordenadas de pantalla en lugar de coordenadas de cliente. Por ejemplo, el código siguiente usa la diferencia en coordenadas de pantalla como la posición x en coordenadas de cliente para colocar un control en un cuadro de diálogo.


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



Este código es correcto cuando la ventana de diálogo tiene un diseño de izquierda a derecha (LTR) y el modo de asignación del cliente es MM TEXT, porque la nueva posición x en coordenadas de cliente corresponde a la diferencia en los bordes izquierdos del control y el diálogo en coordenadas de \_ pantalla. Sin embargo, en un cuadro de diálogo reflejado, se invierten izquierda y derecha, por lo que en su lugar debe usar [**MapWindowPoints**](/windows/win32/api/winuser/nf-winuser-mapwindowpoints) como se muestra a continuación:


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



### <a name="mirroring-dialog-boxes-and-message-boxes"></a>Cuadros de diálogo y cuadros de mensaje de creación de reflejo

Los cuadros de diálogo y los cuadros de mensaje no heredan el diseño, por lo que debe establecer el diseño explícitamente. Para reflejar un cuadro de mensaje, llame [**a MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) con la **opción MB \_ RTLREADING.** Para crear un cuadro de diálogo de derecha a izquierda, use el estilo extendido WS EX LAYOUTRTL en la estructura de plantilla de diálogo \_ \_ [**DLGTEMPLATEEX**](../dlgbox/dlgtemplateex.md). Las hojas de propiedades son un caso especial de cuadros de diálogo. Cada pestaña se trata como un cuadro de diálogo independiente, por lo que debe incluir el estilo LAYOUTRTL de WS EX en cada pestaña que \_ \_ desee reflejar.

### <a name="mirroring-device-contexts-not-associated-with-a-window"></a>Creación de reflejo de contextos de dispositivo no asociados a una ventana

Los controladores de dominio que no están asociados a una ventana, como los controladores de dominio de metarchivo o impresora, no heredan el diseño, por lo que debe establecer el diseño explícitamente. Para cambiar el diseño del contexto del dispositivo, use la [**función SetLayout.**](/windows/win32/api/wingdi/nf-wingdi-setlayout)

La [**función SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout) rara vez se usa con windows. Normalmente, las ventanas reciben un controlador de dominio asociado solo al procesar un [**mensaje \_ WM PAINT.**](../gdi/wm-paint.md) En ocasiones, un programa crea un controlador de dominio para una ventana mediante una llamada [**a GetDC**](/windows/win32/api/winuser/nf-winuser-getdc). En cualquier caso, [**beginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint) u **GetDC** establecen el diseño inicial del controlador de dominio según la marca LAYOUTRTL de WS \_ EX \_ de la ventana.

Los valores devueltos por [**GetWindowOrgEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindoworgex) [**GetWindowExtEx,**](/windows/win32/api/wingdi/nf-wingdi-getwindowextex) [**GetViewportOrgEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportorgex) y [**GetViewportExtEx**](/windows/win32/api/wingdi/nf-wingdi-getviewportextex) no se ven afectados al llamar [**a SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout).

Cuando el diseño es RTL, [**GetMapMode**](/windows/win32/api/wingdi/nf-wingdi-getmapmode) devolverá MM \_ ANISOTROPIC en lugar de MM \_ TEXT. La [**llamada a SetMapMode**](/windows/win32/api/wingdi/nf-wingdi-setmapmode) con MM TEXT funcionará correctamente; solo se verá afectado el valor devuelto de \_ **GetMapMode.** De forma similar, al llamar [**a SetLayout**](/windows/win32/api/wingdi/nf-wingdi-setlayout)(hdc, LAYOUT RTL) cuando el modo de asignación es MM TEXT, el modo de asignación notificado cambia a \_ MM \_ \_ ANISOTROPIC.

## <a name="window-destruction"></a>Destrucción de ventanas

En general, una aplicación debe destruir todas las ventanas que crea. Para ello, usa la [**función DestroyWindow.**](/windows/win32/api/winuser/nf-winuser-destroywindow) Cuando se destruye una ventana, el sistema oculta la ventana, si está visible, y, a continuación, quita los datos internos asociados a la ventana. Esto invalida el identificador de ventana, que la aplicación ya no puede usar.

Una aplicación destruye muchas de las ventanas que crea poco después de crearlas. Por ejemplo, una aplicación normalmente destruye una ventana de cuadro de diálogo en cuanto la aplicación tiene suficiente entrada del usuario para continuar con su tarea. Una aplicación finalmente destruye la ventana principal de la aplicación (antes de finalizar).

Antes de destruir una ventana, una aplicación debe guardar o quitar los datos asociados a la ventana y liberar todos los recursos del sistema asignados a la ventana. Si la aplicación no libera los recursos, el sistema liberará los recursos no liberados por la aplicación.

Destruir una ventana no afecta a la clase de ventana desde la que se crea la ventana. Todavía se pueden crear nuevas ventanas con esa clase y todas las ventanas existentes de esa clase seguirán funcionando. Al destruir una ventana también se destruyen las ventanas descendientes de la ventana. La [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envía primero un [**mensaje WM \_ DESTROY**](wm-destroy.md) a la ventana y, después, a sus ventanas secundarias y ventanas descendientes. De esta manera, también se destruyen todas las ventanas descendientes de la ventana que se va a destruir.

Una ventana con un menú de ventana recibe un [**mensaje WM \_ CLOSE**](wm-close.md) cuando el usuario hace clic en **Cerrar.** Al procesar este mensaje, una aplicación puede pedir confirmación al usuario antes de destruir la ventana. Si el usuario confirma que se debe destruir la ventana, la aplicación puede llamar a la [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) para destruir la ventana.

Si la ventana que se destruye es la ventana activa, los estados activo y de foco se transfieren a otra ventana. La ventana que se convierte en la ventana activa es la siguiente, determinada por la combinación de teclas ALT+ESC. A continuación, la nueva ventana activa determina qué ventana recibe el foco del teclado.

 

 
