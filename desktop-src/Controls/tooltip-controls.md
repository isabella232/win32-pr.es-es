---
title: Acerca de los controles de información sobre herramientas
description: La información sobre herramientas aparece automáticamente o aparece cuando el usuario pausa el puntero del mouse sobre una herramienta o algún otro elemento de la interfaz de usuario.
ms.assetid: 1020cec7-57b4-4463-9419-f80fd14fa12c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9c1042523c86e794865da5d38fb023ee37d60b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166005"
---
# <a name="about-tooltip-controls"></a>Acerca de los controles de información sobre herramientas

La información sobre herramientas aparece automáticamente o aparece cuando el usuario pausa el puntero del mouse sobre una herramienta o algún otro elemento de la interfaz de usuario. La información sobre herramientas aparece cerca del puntero y desaparece cuando el usuario hace clic en un botón del mouse, mueve el puntero fuera de la herramienta o simplemente espera unos segundos.

El control de información sobre herramientas de la ilustración siguiente muestra información sobre un archivo en Windows escritorio. Al mover el mouse sobre la ilustración, también debería ver una información sobre herramientas en directo que contiene texto descriptivo.

![captura de pantalla que muestra texto en una información sobre herramientas que aparece sobre un archivo en el escritorio](images/tt-desktop.png)

En esta sección se describe cómo funcionan los controles de información sobre herramientas y cómo se crean.

-   [Comportamiento y apariencia de la información sobre herramientas](#tooltip-behavior-and-appearance)
-   [Crear controles de información sobre herramientas](#creating-tooltip-controls)
-   [Activación de controles de información sobre herramientas](#activating-tooltip-controls)
-   [Herramientas de soporte técnico](#supporting-tools)
-   [Mostrar texto](#displaying-text)
-   [Mensajería y notificación](#messaging-and-notification)
-   [Pruebas de posicionamiento](#hit-testing)
-   [Procesamiento de mensajes predeterminado](#default-message-processing)

## <a name="tooltip-behavior-and-appearance"></a>Comportamiento y apariencia de la información sobre herramientas

Los controles de información sobre herramientas pueden mostrar una sola línea de texto o varias líneas. Sus esquinas se pueden redondear o cuadrado. Es posible que tengan o no un lemat que señala a las herramientas como un globo de voz de animación. El texto de la información sobre herramientas puede ser stationary o puede moverse con el puntero del mouse, denominado seguimiento. El texto estacionado se puede mostrar adyacente a una herramienta o se puede mostrar sobre una herramienta, lo que se conoce como en su lugar. La información sobre herramientas estándar es inaplicada, muestra una sola línea de texto, tiene esquinas cuadradas y no tiene ninguna lematización que apunte a la herramienta.

La información sobre herramientas de seguimiento, que es compatible con la [versión 4.70](common-control-versions.md) de los controles comunes, cambia la posición en la pantalla dinámicamente. Al actualizar rápidamente la posición, estos controles de información sobre herramientas parecen moverse sin problemas o "realizar un seguimiento". Son útiles cuando se desea que el texto de la información sobre herramientas siga la posición del puntero del mouse mientras se mueve. Para obtener más información sobre la información sobre herramientas de seguimiento y un ejemplo con código que muestra cómo crearlas, vea [Información sobre herramientas de seguimiento.](using-tooltip-contro.md)

La información sobre herramientas multilínea, que también es compatible con la versión 4.70 de los controles comunes, muestra texto en más de una línea. Son útiles para mostrar mensajes largos. Para obtener más información y un ejemplo en el que se muestra cómo crear información sobre herramientas multilínea, vea Información sobre [herramientas multilínea.](using-tooltip-contro.md)

La información sobre herramientas del globo se muestra en un cuadro con esquinas redondeadas y una lemat que apunta a la herramienta. Pueden ser de una sola línea o de varias líneas. En la ilustración siguiente se muestra información sobre herramientas de un globo con la lemat y el rectángulo en sus posiciones predeterminadas. Para obtener más información sobre la información sobre herramientas de globos y un ejemplo que muestra cómo crearlas, vea [Usar controles de información sobre herramientas](using-tooltip-contro.md).

![captura de pantalla que muestra una información sobre herramientas que contiene una línea de texto, situado encima de un botón en un cuadro de diálogo](images/tt-balloon.png)

Una información sobre herramientas también puede tener texto de título y un icono, como se muestra en la ilustración siguiente. Tenga en cuenta que la información sobre herramientas debe tener texto; si solo tiene texto de título, la información sobre herramientas no se muestra. Además, el icono no aparece a menos que haya un título.

![captura de pantalla que muestra información sobre herramientas con un icono, título y texto, situado debajo de un botón en un cuadro de diálogo](images/tt-titled.png)

A veces, las cadenas de texto se recortan porque son demasiado largas para mostrarse completamente en una ventana pequeña. La información sobre herramientas local se usa para mostrar cadenas de texto para los objetos que se han recortado, como el nombre de archivo en la ilustración siguiente. Para obtener un ejemplo en el que se muestra cómo crear información sobre herramientas local, vea Información sobre [herramientas local.](using-tooltip-contro.md)

![captura de pantalla que muestra una información sobre herramientas que contiene un nombre de archivo situado junto a un icono de archivo en un control de árbol](images/tt-inplace.png)

El cursor debe mantener el puntero sobre una herramienta durante un período de tiempo antes de que se muestre la información sobre herramientas. La duración predeterminada de este tiempo de espera se controla mediante el tiempo de doble clic del usuario y suele ser de aproximadamente medio segundo. Para especificar un valor de tiempo de espera no predeterminado, envíe al control de información sobre herramientas un [**mensaje \_ SETDELAYTIME de TTM.**](ttm-setdelaytime.md)

## <a name="creating-tooltip-controls"></a>Crear controles de información sobre herramientas

Para crear un control de información sobre herramientas, llame [**a CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la [**clase de ventana TOOLTIPS \_ CLASS.**](common-control-window-classes.md) Esta clase se registra cuando se carga el archivo DLL de control común. Para asegurarse de que se carga este archivo DLL, incluya la [**función InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) en la aplicación. Debe definir explícitamente un control de información sobre herramientas como superior. De lo contrario, podría estar cubierto por la ventana primaria. El fragmento de código siguiente muestra cómo crear un control de información sobre herramientas.


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



El procedimiento de ventana para el control de información sobre herramientas establece automáticamente el tamaño, la posición y la visibilidad del control. El alto de la ventana de información sobre herramientas se basa en el alto de la fuente seleccionada actualmente en el contexto del dispositivo para el control de información sobre herramientas. El ancho varía en función de la longitud de la cadena actualmente en la ventana de información sobre herramientas.

## <a name="activating-tooltip-controls"></a>Activación de controles de información sobre herramientas

Un control de información sobre herramientas puede estar activo o inactivo. Cuando está activo, el texto de la información sobre herramientas aparece cuando el puntero del mouse está en una herramienta. Cuando está inactivo, el texto de la información sobre herramientas no aparece, incluso si el puntero está en una herramienta. El [**mensaje ACTIVATE \_ de TTM**](ttm-activate.md) activa y desactiva un control de información sobre herramientas.

## <a name="supporting-tools"></a>Herramientas de soporte técnico

Un control de información sobre herramientas puede admitir cualquier número de herramientas. Para admitir una herramienta determinada, debe registrar la herramienta con el control de información sobre herramientas mediante el envío del control [**al mensaje \_ ADDTOOL de TTM.**](ttm-addtool.md) El mensaje incluye la dirección de una [**estructura TOOLINFO,**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que proporciona información que el control de información sobre herramientas necesita para mostrar texto para la herramienta. La aplicación define el miembro **uID** de **la estructura TOOLINFO.** Cada vez que agrega una herramienta, la aplicación proporciona un identificador único. El **miembro cbSize** de la **estructura TOOLINFO** es obligatorio y debe especificar el tamaño de la estructura.

Un control de información sobre herramientas admite herramientas implementadas como ventanas (como ventanas secundarias o ventanas de control) y como áreas rectangulares dentro del área cliente de una ventana. Al agregar una herramienta implementada como un área rectangular, el **miembro hwnd** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe especificar el identificador de la ventana que contiene el área y el miembro **rect** debe especificar las coordenadas de cliente del rectángulo delimitador del área. Además, el **miembro uID** debe especificar el identificador definido por la aplicación para la herramienta.

Al agregar una herramienta implementada como una ventana, el **miembro uID** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe contener el identificador de ventana para la herramienta. Además, el **miembro uFlags** debe especificar el valor **\_ IDISHWND de TTF,** que indica al control de información sobre herramientas que interprete el miembro **uID** como un identificador de ventana.

## <a name="displaying-text"></a>Mostrar texto

Al agregar una herramienta a un control de información sobre herramientas, el miembro **lpszText** de la [**estructura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) debe especificar la dirección de la cadena que se va a mostrar para la herramienta. Después de agregar una herramienta, puede cambiar el texto mediante el mensaje [**\_ UPDATETIPTEXT de TTM.**](ttm-updatetiptext.md)

Si la palabra de orden alto **de lpszText** es cero, la palabra de orden bajo debe ser el identificador de un recurso de cadena. Cuando el control de información sobre herramientas necesita el texto, el sistema carga el recurso de cadena especificado desde la instancia de aplicación identificada por el **miembro más importante** de la estructura [**TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)

Si especifica el valor LPSTR TEXTCALLBACK en el miembro \_ **lpszText,** el control de información sobre herramientas notifica a la ventana especificada en el **miembro hwnd** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)cada vez que el control de información sobre herramientas necesite mostrar texto para la herramienta. El control de información sobre herramientas envía [el código de notificación \_ GETDISPINFO de TTN](ttn-getdispinfo.md) a la ventana. El mensaje incluye la dirección de una estructura [**NMTTDISPINFO,**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que contiene el identificador de ventana, así como el identificador definido por la aplicación para la herramienta. La ventana examina la estructura para determinar la herramienta para la que se necesita texto y rellena los miembros de estructura adecuados con la información que necesita el control de información sobre herramientas para mostrar la cadena.

> [!Note]  
> La longitud máxima del texto de información sobre herramientas estándar es de 80 caracteres. Para obtener más información, vea la [**estructura NMTTDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) El texto de la información sobre herramientas multilínea puede ser más largo.

 

Muchas aplicaciones crean barras de herramientas que contienen herramientas que corresponden a comandos de menú. Para estas herramientas, es conveniente que el control de información sobre herramientas muestre el mismo texto que el elemento de menú correspondiente. El sistema quita automáticamente los caracteres de acelerador de y comercial (&) de todas las cadenas que se pasan a un control de información sobre herramientas y finaliza la cadena en el primer carácter de tabulación ( t), a menos que el control tenga el estilo \\ [**\_ TTS NOPREFIX.**](tooltip-styles.md)

Para recuperar el texto de una herramienta, use el [**mensaje \_ GETTEXT de TTM.**](ttm-gettext.md)

## <a name="messaging-and-notification"></a>Mensajería y notificación

Normalmente, el texto de la información sobre herramientas se muestra cuando el puntero del mouse se desplaza sobre un área, normalmente el rectángulo definido por una herramienta como un control de botón. Sin embargo, Microsoft Windows solo envía mensajes relacionados con el mouse a la ventana que contiene el puntero, no al propio control de información sobre herramientas. La información relacionada con el mouse se debe retransmitir al control de información sobre herramientas para que muestre el texto de la información sobre herramientas en el momento y lugar adecuados.

Puede hacer que los mensajes se retransmiten automáticamente si:

-   La herramienta es un control o se define como un rectángulo en la estructura [**TOOLINFO de la**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) herramienta.
-   La ventana asociada a la herramienta está en el mismo subproceso que el control de información sobre herramientas.

Si se cumplen estas dos condiciones, establezca la marca **\_ TTF SUBCLASS** en el miembro **uFlags** de la estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) de la herramienta al agregar la herramienta al control de información sobre herramientas con [**\_ ADDTOOL de TTM.**](ttm-addtool.md) Los mensajes necesarios del mouse se retransmitirán automáticamente al control de información sobre herramientas.

Establecer **TTF \_ SUBCLASS para** que los mensajes del mouse se retransmiten al control es suficiente para la mayoría de los propósitos. Sin embargo, no funcionará en casos en los que no haya ninguna conexión directa entre el control de información sobre herramientas y la ventana de la herramienta. Por ejemplo, si una herramienta se implementa como un área rectangular en una ventana definida por la aplicación, el procedimiento de ventana recibe los mensajes del mouse. El **establecimiento de \_ TTF SUBCLASS** es suficiente para asegurarse de que se pasan al control. Sin embargo, si una herramienta se implementa como una ventana definida por el sistema, los mensajes del mouse se envían a esa ventana y no están disponibles directamente para la aplicación. En este caso, debe crear una subclase de la ventana o usar un enlace de mensaje para acceder a los mensajes del mouse. A continuación, debe retransmitir explícitamente los mensajes del mouse al control de información sobre herramientas [**con EL EVENTO DE \_ RETRANSMISIÓN DE TTM.**](ttm-relayevent.md) Para obtener un ejemplo de cómo usar **EL \_ EVENTO DE RETRANSMISIÓN DE TTM**, vea Seguimiento de información sobre [herramientas.](using-tooltip-contro.md)

Cuando un control de información sobre herramientas recibe un mensaje [**\_ WM MOUSEMOVE,**](/windows/desktop/inputdev/wm-mousemove) determina si el puntero del mouse está en el rectángulo delimitador de una herramienta. Si es así, el control de información sobre herramientas establece un temporizador. Al final del intervalo de tiempo de espera, el control de información sobre herramientas comprueba la posición del puntero para ver si se ha movido. Si no lo ha hecho, el control de información sobre herramientas recupera el texto de la herramienta y muestra la información sobre herramientas. El control de información sobre herramientas sigue mostrándose la ventana hasta que recibe un mensaje retransmitido con los botones arriba o abajo, o hasta que un mensaje **\_ WM MOUSEMOVE** indica que el puntero se ha movido fuera del rectángulo delimitador de la herramienta.

En realidad, un control de información sobre herramientas tiene tres duraciones de tiempo de espera asociadas. La duración inicial es el tiempo que el puntero del mouse debe permanecer estacionado dentro del rectángulo delimitador de una herramienta antes de que se muestre la ventana de información sobre herramientas. La duración de volver a mostrar es la longitud del retraso antes de que se muestren las ventanas de información sobre herramientas posteriores cuando el puntero se mueve de una herramienta a otra. La duración de la ventana emergente es el tiempo que la ventana de información sobre herramientas permanece mostrada antes de que se oculta. Es decir, si el puntero permanece estacionado dentro del rectángulo delimitador después de mostrar la ventana de información sobre herramientas, la ventana de información sobre herramientas se oculta automáticamente al final de la duración del elemento emergente. Puede ajustar todas las duraciones de tiempo de espera mediante el mensaje [**\_ SETDELAYTIME de TTM.**](ttm-setdelaytime.md)

Si una aplicación incluye una herramienta implementada como un área rectangular y cambia el tamaño o la posición del control, la aplicación puede usar el mensaje [**TTM \_ NEWTOOLRECT**](ttm-newtoolrect.md) para notificar el cambio al control de información sobre herramientas. Una aplicación no necesita notificar los cambios de tamaño y posición de una herramienta implementada como una ventana porque el control de información sobre herramientas usa el identificador de ventana de la herramienta para determinar si el puntero del mouse está en la herramienta, no el rectángulo delimitador de la herramienta.

Cuando una información sobre herramientas está a punto de mostrarse, el control de información sobre herramientas envía a la ventana de propietario un [código de notificación \_ TTN SHOW.](ttn-show.md) La ventana de propietario recibe un [código de notificación \_ POP de TTN](ttn-pop.md) cuando una información sobre herramientas está a punto de ocultarse. Cada código de notificación se envía en el contexto de un [**mensaje \_ WM NOTIFY.**](wm-notify.md)

## <a name="hit-testing"></a>Pruebas de posicionamiento

El [**mensaje \_ HITTEST**](ttm-hittest.md) de TTM permite recuperar información que un control de información sobre herramientas mantiene sobre la herramienta que ocupa un punto determinado. El mensaje incluye una [**estructura TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) que contiene un identificador de ventana, las coordenadas de un punto y la dirección de una [**estructura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) El control de información sobre herramientas determina si una herramienta ocupa el punto y, si lo hace, rellena **TOOLINFO** con información sobre la herramienta.

## <a name="default-message-processing"></a>Procesamiento de mensajes predeterminado

En la tabla siguiente se describen los mensajes controlados por el procedimiento de ventana para el control de información sobre herramientas.



| Message                                        | Descripción                                                                                                                                                                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Garantiza que el control de información sobre herramientas tiene los [**estilos de ventana EMERGENTE WS EX \_ \_ TOOLWINDOW**](/windows/desktop/winmsg/window-styles) y [**WS. \_**](/windows/desktop/winmsg/window-styles) También asigna memoria e inicializa variables internas. |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)           | Libera los recursos asignados para el control de información sobre herramientas.                                                                                                                                                                                                                |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)           | Devuelve el identificador de la fuente que usará el control de información sobre herramientas para dibujar texto.                                                                                                                                                                                    |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)     | Oculta la ventana de información sobre herramientas.                                                                                                                                                                                                                                         |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Dibuja la ventana de información sobre herramientas.                                                                                                                                                                                                                                         |
| [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)           | Establece el identificador de la fuente que usará el control de información sobre herramientas para dibujar texto.                                                                                                                                                                                       |
| [**TEMPORIZADOR \_ DE WM**](/windows/desktop/winmsg/wm-timer)               | Oculta la ventana de información sobre herramientas si la herramienta ha cambiado de posición o si el puntero del mouse se ha movido fuera de la herramienta. De lo contrario, se muestra la ventana de información sobre herramientas.                                                                                                             |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange) | Restablece las variables internas basadas en métricas del sistema.                                                                                                                                                                                                       |



 

 

 