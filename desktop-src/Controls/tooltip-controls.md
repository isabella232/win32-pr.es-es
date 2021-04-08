---
title: Acerca de los controles ToolTip
description: La información sobre herramientas aparece automáticamente o emergente cuando el usuario detiene el puntero del mouse sobre una herramienta o algún otro elemento de la interfaz de usuario.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078449"
---
# <a name="about-tooltip-controls"></a>Acerca de los controles ToolTip

La información sobre herramientas aparece automáticamente o emergente cuando el usuario detiene el puntero del mouse sobre una herramienta o algún otro elemento de la interfaz de usuario. La información sobre herramientas aparece cerca del puntero y desaparece cuando el usuario hace clic en un botón del mouse, desplaza el puntero fuera de la herramienta o simplemente espera unos segundos.

El control ToolTip de la siguiente ilustración muestra información acerca de un archivo en el escritorio de Windows. A medida que mueve el mouse sobre la ilustración, también debería ver una información sobre herramientas en directo que contiene texto descriptivo.

![captura de pantalla que muestra texto en una información sobre herramientas que aparece sobre un archivo en el escritorio](images/tt-desktop.png)

En esta sección se describe cómo funcionan los controles de información sobre herramientas y cómo se crean.

-   [Apariencia y comportamiento de la información sobre herramientas](#tooltip-behavior-and-appearance)
-   [Crear controles de información sobre herramientas](#creating-tooltip-controls)
-   [Activar controles de información sobre herramientas](#activating-tooltip-controls)
-   [Herramientas auxiliares](#supporting-tools)
-   [Mostrar texto](#displaying-text)
-   [Mensajería y notificación](#messaging-and-notification)
-   [Pruebas de posicionamiento](#hit-testing)
-   [Procesamiento de mensajes predeterminado](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Apariencia y comportamiento de la información sobre herramientas

Los controles de información sobre herramientas pueden mostrar una sola línea de texto o varias líneas. Sus esquinas se pueden redondear o cuadrado. Pueden tener o no una tallo que apunte a las herramientas como un globo de voz animado. El texto de información sobre herramientas puede ser estacionario o puede moverse con el puntero del mouse, denominado Tracking. El texto estacionario se puede mostrar junto a una herramienta o se puede mostrar en una herramienta, lo que se conoce como in situ. La información sobre herramientas estándar es estacionaria, muestra una sola línea de texto, tiene esquinas cuadradas y no tiene ningún tronco que señale a la herramienta.

La información sobre herramientas de seguimiento, que son compatibles con la [versión 4,70](common-control-versions.md) de los controles comunes, cambian la posición en la pantalla dinámicamente. Al actualizar rápidamente la posición, estos controles de información sobre herramientas parecen moverse sin problemas o "realizar un seguimiento". Resultan útiles cuando se desea que el texto de información sobre herramientas siga la posición del puntero del mouse a medida que se mueve. Para obtener más información sobre cómo realizar un seguimiento de la información sobre herramientas y un ejemplo con código que muestra cómo se crean, consulte [información sobre herramientas de seguimiento](using-tooltip-contro.md).

La información sobre herramientas de varias líneas, que también es compatible con la versión 4,70 de los controles comunes, muestra el texto en más de una línea. Son útiles para mostrar mensajes largos. Para obtener más información y un ejemplo en el que se muestra cómo crear información sobre herramientas de varias líneas, vea [información sobre herramientas multilínea](using-tooltip-contro.md).

La información sobre herramientas de globo se muestra en un cuadro con esquinas redondeadas y un tallo que apunta a la herramienta. Pueden ser de una o varias líneas. En la ilustración siguiente se muestra un globo de información sobre herramientas con el tallo y el rectángulo en sus posiciones predeterminadas. Para obtener más información acerca de la información sobre herramientas de globo y un ejemplo en el que se muestra cómo crearlos, vea [usar controles de información sobre herramientas](using-tooltip-contro.md).

![captura de pantalla que muestra una información sobre herramientas que contiene una línea de texto, colocada sobre un botón en un cuadro de diálogo](images/tt-balloon.png)

La información sobre herramientas también puede tener texto de título y un icono, tal como se muestra en la siguiente ilustración. Tenga en cuenta que la información sobre herramientas debe tener texto; Si solo tiene texto de título, la información sobre herramientas no se muestra. Además, el icono no aparece a menos que haya un título.

![captura de pantalla que muestra una información sobre herramientas con un icono, título y texto, que se encuentra debajo de un botón en un cuadro de diálogo](images/tt-titled.png)

A veces, las cadenas de texto se recortan porque son demasiado largas para mostrarse completamente en una ventana pequeña. La información sobre herramientas en contexto se usa para mostrar las cadenas de texto de los objetos que se han recortado, como el nombre de archivo en la siguiente ilustración. Para ver un ejemplo en el que se muestra cómo crear información sobre herramientas en contexto, vea [información sobre herramientas en contexto](using-tooltip-contro.md).

![captura de pantalla que muestra una información sobre herramientas que contiene un nombre de archivo situado junto a un icono de archivo en un control de árbol](images/tt-inplace.png)

El cursor debe mantener el mouse sobre una herramienta durante un período de tiempo antes de que se muestre la información sobre herramientas. La duración predeterminada de este tiempo de espera se controla mediante el tiempo de doble clic del usuario y suele ser de un segundo medio. Para especificar un valor de tiempo de espera no predeterminado, envíe el control de información sobre herramientas a un mensaje [**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md) .

## <a name="creating-tooltip-controls"></a>Crear controles de información sobre herramientas

Para crear un control de información sobre herramientas, llame a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la clase de ventana de [**\_ clase tooltips**](common-control-window-classes.md) . Esta clase se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, incluya la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) en la aplicación. Debe definir explícitamente un control ToolTip como el nivel superior. De lo contrario, podría estar incluido en la ventana primaria. En el siguiente fragmento de código se muestra cómo crear un control ToolTip.


```
HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                            WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            CW_USEDEFAULT, CW_USEDEFAULT,
                            hwndParent, NULL, hinstMyDll,
                            NULL);

SetWindowPos(hwndTip, HWND_TOPMOST,0, 0, 0, 0,
             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);
```



El procedimiento de ventana para el control ToolTip establece automáticamente el tamaño, la posición y la visibilidad del control. El alto de la ventana de información sobre herramientas se basa en el alto de la fuente seleccionada actualmente en el contexto del dispositivo para el control ToolTip. El ancho varía en función de la longitud de la cadena actualmente en la ventana de información sobre herramientas.

## <a name="activating-tooltip-controls"></a>Activar controles de información sobre herramientas

Un control ToolTip puede estar activo o inactivo. Cuando está activo, el texto de información sobre herramientas aparece cuando el puntero del mouse está sobre una herramienta. Cuando está inactivo, el texto de la información sobre herramientas no aparece, aunque el puntero esté en una herramienta. El mensaje de [**\_ activación de TTM**](ttm-activate.md) activa y desactiva un control de información sobre herramientas.

## <a name="supporting-tools"></a>Herramientas auxiliares

Un control de información sobre herramientas puede admitir cualquier número de herramientas. Para admitir una herramienta determinada, debe registrar la herramienta con el control de información sobre herramientas mediante el envío del mensaje de control [**TTM \_ ADDTOOL**](ttm-addtool.md) . El mensaje incluye la dirección de una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , que proporciona información que el control ToolTip necesita para mostrar el texto de la herramienta. La aplicación define el miembro **uID** de la estructura **TOOLINFO** . Cada vez que se agrega una herramienta, la aplicación proporciona un identificador único. El miembro **cbSize** de la estructura **TOOLINFO** es obligatorio y debe especificar el tamaño de la estructura.

Un control ToolTip admite herramientas implementadas como ventanas (como ventanas secundarias o ventanas de control) y como áreas rectangulares dentro del área de cliente de una ventana. Cuando se agrega una herramienta implementada como un área rectangular, el miembro **hWnd** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe especificar el identificador de la ventana que contiene el área y el miembro **Rect** debe especificar las coordenadas de cliente del rectángulo delimitador del área. Además, el miembro **uID** debe especificar el identificador definido por la aplicación para la herramienta.

Cuando se agrega una herramienta implementada como una ventana, el miembro **uID** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe contener el identificador de ventana de la herramienta. Además, el miembro **uFlags** debe especificar el valor de **ttf \_ IDISHWND** , que indica al control ToolTip que interprete el miembro **uID** como un identificador de ventana.

## <a name="displaying-text"></a>Mostrar texto

Cuando se agrega una herramienta a un control ToolTip, el miembro **lpszText** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe especificar la dirección de la cadena que se va a mostrar para la herramienta. Después de agregar una herramienta, puede cambiar el texto mediante el mensaje [**\_ UPDATETIPTEXT de TTM**](ttm-updatetiptext.md) .

Si la palabra de orden superior de **lpszText** es cero, la palabra de orden inferior debe ser el identificador de un recurso de cadena. Cuando el control ToolTip necesita el texto, el sistema carga el recurso de cadena especificado desde la instancia de la aplicación identificada por el miembro **HINST** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .

Si especifica el \_ valor de LPSTR TEXTCALLBACK en el miembro **lpszText** , el control ToolTip notifica a la ventana especificada en el miembro **hWnd** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)cada vez que el control ToolTip necesita mostrar texto para la herramienta. El control ToolTip envía el código de notificación [TTN \_ GETDISPINFO](ttn-getdispinfo.md) a la ventana. El mensaje incluye la dirección de una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) , que contiene el identificador de ventana, así como el identificador definido por la aplicación para la herramienta. La ventana examina la estructura para determinar la herramienta para la que se necesita texto y rellena los miembros adecuados de la estructura con la información que necesita el control ToolTip para mostrar la cadena.

> [!Note]  
> La longitud máxima del texto de información sobre herramientas estándar es de 80 caracteres. Para obtener más información, vea la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) . El texto de información sobre herramientas multilínea puede ser más largo.

 

Muchas aplicaciones crean barras de herramientas que contienen herramientas que corresponden a comandos de menú. Para estas herramientas, es conveniente que el control de información sobre herramientas muestre el mismo texto que el elemento de menú correspondiente. El sistema quita automáticamente los caracteres de aceleración de y comercial (&) de todas las cadenas que se pasan a un control de información sobre herramientas y finaliza la cadena en el primer carácter de tabulación ( \\ t), a menos que el control tenga el estilo [**TTS \_ noprefix**](tooltip-styles.md) .

Para recuperar el texto de una herramienta, use el mensaje [**TTM \_ GETTEXT**](ttm-gettext.md) .

## <a name="messaging-and-notification"></a>Mensajería y notificación

El texto de información sobre herramientas se muestra normalmente cuando el puntero del mouse se desplaza sobre un área, normalmente el rectángulo definido por una herramienta, como un control de botón. Sin embargo, Microsoft Windows solo envía mensajes relacionados con el mouse a la ventana que contiene el puntero, no al propio control de información sobre herramientas. La información relacionada con el mouse debe retransmitirse al control de información sobre herramientas para que muestre el texto de información sobre herramientas en el momento y lugar adecuados.

Puede hacer que los mensajes se retransmitan automáticamente si:

-   La herramienta es un control o se define como un rectángulo en la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la herramienta.
-   La ventana asociada a la herramienta está en el mismo subproceso que el control ToolTip.

Si se cumplen estas dos condiciones, establezca la marca de la **\_ subclase ttf** en el miembro **UFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la herramienta cuando agregue la herramienta al control ToolTip con [**TTM \_ ADDTOOL**](ttm-addtool.md). Los mensajes del mouse necesarios se retransmitirán automáticamente al control ToolTip.

La configuración de la **\_ subclase ttf** para que los mensajes del mouse retransmitidos al control sea suficiente para la mayoría de los propósitos. Sin embargo, no funcionará en casos en los que no haya ninguna conexión directa entre el control de información sobre herramientas y la ventana de la herramienta. Por ejemplo, si una herramienta se implementa como un área rectangular en una ventana definida por la aplicación, el procedimiento de ventana recibe los mensajes del mouse. Establecer **la \_ subclase ttf** es suficiente para asegurarse de que se pasan al control. Sin embargo, si una herramienta se implementa como una ventana definida por el sistema, los mensajes del mouse se envían a esa ventana y no están directamente disponibles para la aplicación. En este caso, debe subclaser la ventana o utilizar un enlace de mensaje para tener acceso a los mensajes del mouse. Después, debe retransmitir explícitamente los mensajes del mouse al control ToolTip con [**TTM \_ RELAYEVENT**](ttm-relayevent.md). Para obtener un ejemplo de cómo usar **TTM \_ RELAYEVENT**, consulte la [información sobre herramientas de seguimiento](using-tooltip-contro.md).

Cuando un control ToolTip recibe un mensaje de el [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) , determina si el puntero del mouse está en el rectángulo delimitador de una herramienta. Si es así, el control ToolTip establece un temporizador. Al final del intervalo de tiempo de espera, el control ToolTip comprueba la posición del puntero para ver si se ha cambiado. Si no es así, el control ToolTip recupera el texto de la herramienta y muestra la información sobre herramientas. El control de información sobre herramientas continúa mostrando la ventana hasta que recibe un mensaje retransmitido de botón arriba o abajo o hasta que un mensaje de Windows de **WM \_** indica que el puntero se ha colocado fuera del rectángulo delimitador de la herramienta.

En realidad, un control ToolTip tiene tres duraciones de tiempo de espera asociadas. La duración inicial es el tiempo que el puntero del mouse debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que se muestre la ventana de información sobre herramientas. La duración de la representación es la duración del retraso antes de que se muestren las siguientes ventanas de información sobre herramientas cuando el puntero se mueve de una herramienta a otra. La duración del elemento emergente es el tiempo que la ventana de información sobre herramientas permanece visible antes de ocultarse. Es decir, si el puntero permanece inmóvil dentro del rectángulo delimitador después de que se muestre la ventana de información sobre herramientas, la ventana de información sobre herramientas se oculta automáticamente al final de la duración del elemento emergente. Puede ajustar todas las duraciones de tiempo de espera mediante el mensaje [**\_ SETDELAYTIME de TTM**](ttm-setdelaytime.md) .

Si una aplicación incluye una herramienta implementada como área rectangular y el tamaño o la posición del control cambia, la aplicación puede usar el [**mensaje \_ NEWTOOLRECT de TTM**](ttm-newtoolrect.md) para notificar el cambio en el control de información sobre herramientas. Una aplicación no necesita informar de los cambios de tamaño y posición de una herramienta implementada como una ventana porque el control de información sobre herramientas usa el identificador de ventana de la herramienta para determinar si el puntero del mouse está en la herramienta, no en el rectángulo delimitador de la herramienta.

Cuando una información sobre herramientas está a punto de mostrarse, el control ToolTip envía a la ventana propietaria un código de notificación [TTN \_ ](ttn-show.md) . La ventana propietaria recibe un código de notificación de [ \_ pop TTN](ttn-pop.md) cuando una información sobre herramientas está a punto de ocultarse. Cada código de notificación se envía en el contexto de un mensaje de notificación de [**WM \_**](wm-notify.md) .

## <a name="hit-testing"></a>Pruebas de posicionamiento

El mensaje [**TTM \_ HITTEST**](ttm-hittest.md) permite recuperar información que el control ToolTip mantiene sobre la herramienta que ocupa un punto determinado. El mensaje incluye una estructura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) que contiene un identificador de ventana, las coordenadas de un punto y la dirección de una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . El control ToolTip determina si una herramienta ocupa el punto y, si lo hace, rellena **TOOLINFO** con información sobre la herramienta.

## <a name="default-message-processing"></a>Procesamiento de mensajes predeterminado

En la tabla siguiente se describen los mensajes administrados por el procedimiento de ventana para el control ToolTip.



| Message                                        | Descripción                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)             | Garantiza que el control ToolTip tenga los estilos de ventana [**\_ emergente**](/windows/desktop/winmsg/window-styles) [**WS \_ ex \_**](/windows/desktop/winmsg/window-styles) y WS. También asigna memoria e inicializa variables internas. |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera los recursos asignados para el control ToolTip.                                                                                                                                                                                                                |
| [**GETFONT de WM \_**](/windows/desktop/winmsg/wm-getfont)           | Devuelve el identificador de la fuente que el control ToolTip usará para dibujar el texto.                                                                                                                                                                                    |
| [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)     | Oculta la ventana de información sobre herramientas.                                                                                                                                                                                                                                         |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                  | Dibuja la ventana de información sobre herramientas.                                                                                                                                                                                                                                         |
| [**WM \_**](/windows/desktop/winmsg/wm-setfont)           | Establece el identificador de la fuente que el control ToolTip usará para dibujar el texto.                                                                                                                                                                                       |
| [**temporizador de WM \_**](/windows/desktop/winmsg/wm-timer)               | Oculta la ventana de información sobre herramientas si la herramienta ha cambiado de posición o si el puntero del mouse se ha colocado fuera de la herramienta. De lo contrario, muestra la ventana de información sobre herramientas.                                                                                                             |
| [**WININICHANGE de WM \_**](/windows/desktop/winmsg/wm-wininichange) | Restablece las variables internas basadas en las métricas del sistema.                                                                                                                                                                                                       |



 

 

 