---
title: Acerca de la entrada del mouse
description: En este tema se describe la entrada del mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- entrada del usuario, entrada del mouse
- capturar la entrada del usuario, la entrada del mouse
- entrada del mouse
- cursor del mouse
- cursores, entrada del mouse
- captura del mouse
- Mouse ClickLock
- XBUTTONs
- configuración del mouse
- mensajes del mouse
- WM_NCHITTEST mensaje
- Característica de accesibilidad Desvanección del mouse
- Característica de accesibilidad de Sonar de mouse
- rueda del mouse
- WM_MOUSEWHEEL mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c4978babd6322102908699dbf88b68e2d3b92f57fa9bfa79b9b8c3eae88931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105794"
---
# <a name="about-mouse-input"></a>Acerca de la entrada del mouse

El mouse es un dispositivo de entrada de usuario importante, pero opcional, para las aplicaciones. Una aplicación bien escrita debe incluir una interfaz de mouse, pero no debe depender únicamente del mouse para adquirir la entrada del usuario. La aplicación también debe proporcionar compatibilidad completa con el teclado.

Una aplicación recibe la entrada del mouse en forma de mensajes que se envían o publican en sus ventanas.

En esta sección se describen los temas siguientes:

-   [Mouse Cursor](#mouse-cursor)
-   [Captura del mouse](#mouse-capture)
-   [Mouse ClickLock](#mouse-clicklock)
-   [Configuración del mouse](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Mensajes del mouse](#mouse-messages)
    -   [Mensajes del mouse del área de cliente](#client-area-mouse-messages)
    -   [Mensajes del mouse de área no cliente](#nonclient-area-mouse-messages)
    -   [El mensaje \_ WM NCHITTEST](/windows)
-   [Mouse Sonar](#mouse-sonar)
-   [Mouse Desvaneciendo](#mouse-vanish)
-   [Rueda del mouse](#the-mouse-wheel)
-   [Activación de ventana](#window-activation)

## <a name="mouse-cursor"></a>Mouse Cursor

Cuando el usuario mueve el mouse, el sistema mueve un mapa de bits en la pantalla denominado *cursor del mouse*. El cursor del mouse contiene un punto de un solo píxel denominado zona *activa,* un punto que el sistema realiza un seguimiento y reconoce como la posición del cursor. Cuando se produce un evento del mouse, la ventana que contiene la zona activa normalmente recibe el mensaje del mouse resultante del evento. La ventana no necesita estar activa o tener el foco del teclado para recibir un mensaje del mouse.

El sistema mantiene una variable que controla la velocidad del mouse, es decir, la distancia que el cursor mueve cuando el usuario mueve el mouse. Puede usar la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la **marca SPI \_ GETMOUSE** o **SPI \_ SETMOUSE** para recuperar o establecer la velocidad del mouse. Para obtener más información sobre los cursores del mouse, vea [Cursores](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Captura del mouse

Normalmente, el sistema envía un mensaje del mouse a la ventana que contiene la zona activa del cursor cuando se produce un evento del mouse. Una aplicación puede cambiar este comportamiento mediante la función [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) para enrutar los mensajes del mouse a una ventana específica. La ventana recibe todos los mensajes del mouse hasta que la aplicación llama a la función [**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) o especifica otra ventana de captura, o hasta que el usuario hace clic en una ventana creada por otro subproceso.

Cuando cambia la captura del mouse, el sistema envía un mensaje [**\_ WM CAPTURECHANGED**](wm-capturechanged.md) a la ventana que pierde la captura del mouse. El *parámetro lParam* del mensaje especifica un identificador para la ventana que obtiene la captura del mouse.

Solo la ventana de primer plano puede capturar la entrada del mouse. Cuando una ventana en segundo plano intenta capturar la entrada del mouse, recibe mensajes solo para los eventos del mouse que se producen cuando la zona activa del cursor está dentro de la parte visible de la ventana.

Capturar la entrada del mouse es útil si una ventana debe recibir todas las entradas del mouse, incluso cuando el cursor se mueve fuera de la ventana. Por ejemplo, una aplicación normalmente realiza un seguimiento de la posición del cursor después de un evento de botón del mouse hacia abajo, siguiendo el cursor hasta que se produce un evento de botón del mouse hacia arriba. Si una aplicación no ha capturado la entrada del mouse y el usuario suelta el botón del mouse fuera de la ventana, la ventana no recibe el mensaje de botón hacia arriba.

Un subproceso puede usar la [**función GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) para determinar si una de sus ventanas ha capturado el mouse. Si una de las ventanas del subproceso ha capturado el mouse, **GetCapture** recupera un identificador en la ventana.

## <a name="mouse-clicklock"></a>Mouse ClickLock

La característica de accesibilidad Mouse ClickLock permite que un usuario bloquee el botón primario del mouse después de un solo clic. En una aplicación, el botón sigue estando presionado. Para desbloquear el botón, una aplicación puede enviar cualquier mensaje del mouse o el usuario puede hacer clic en cualquier botón del mouse. Esta característica permite a un usuario realizar combinaciones complejas de mouse más sencillamente. Por ejemplo, aquellos con ciertas limitaciones físicas pueden resaltar texto, arrastrar objetos o abrir menús más fácilmente. Para obtener más información, vea las marcas siguientes y los comentarios en [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **SPI \_ GETMOUSECLICKLOCK**
-   **SPI \_ SETMOUSECLICKLOCK**
-   **SPI \_ GETMOUSECLICKLOCKTIME**
-   **SPI \_ SETMOUSECLICKLOCKTIME**

## <a name="mouse-configuration"></a>Configuración del mouse

Aunque el mouse es un dispositivo de entrada importante para las aplicaciones, no todos los usuarios tienen necesariamente un mouse. Una aplicación puede determinar si el sistema incluye un mouse pasando el valor **DE SM \_ MOUSEPRESENT** a la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)

Windows admite un mouse con hasta tres botones. En un mouse de tres botones, los botones se designan como botones izquierdo, central y derecho. Los mensajes y las constantes con nombre relacionadas con los botones del mouse usan las letras L, M y R para identificar los botones. El botón de un solo botón se considera el botón izquierdo. Aunque Windows un mouse con varios botones, la mayoría de las aplicaciones usan el botón izquierdo principalmente y los demás mínimamente, si es que lo tienen.

Las aplicaciones también pueden admitir una rueda del mouse. La rueda del mouse se puede presionar o girar. Cuando se presiona la rueda del mouse, actúa como el botón central (tercer) y envía mensajes de botón central normales a la aplicación. Cuando se gira, se envía un mensaje de rueda a la aplicación. Para obtener más información, vea [la sección Rueda del](#the-mouse-wheel) mouse.

Las aplicaciones pueden admitir botones de comandos de aplicación. Estos botones, denominados botones X, están diseñados para permitir un acceso más sencillo a un explorador de Internet, correo electrónico y servicios multimedia. Cuando se presiona un botón X, se envía un [**mensaje \_ DE WM APPCOMMAND**](wm-appcommand.md) a la aplicación. Para obtener más información, vea la descripción en el **mensaje \_ WM APPCOMMAND.**

Una aplicación puede determinar el número de botones del mouse pasando el valor **\_ CMOUSEBUTTONS** de SM a la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Para configurar el mouse para un usuario de la izquierda, la aplicación puede usar la función [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) para invertir el significado de los botones del mouse izquierdo y derecho. Pasar el **\_ valor SETMOUSEBUTTONSWAP** de SPI a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) es otra manera de invertir el significado de los botones. Sin embargo, tenga en cuenta que el mouse es un recurso compartido, por lo que invertir el significado de los botones afecta a todas las aplicaciones.

## <a name="xbuttons"></a>XBUTTONs

Windows admite un mouse con cinco botones. Además de los botones izquierdo, central y derecho, hay XBUTTON1 y XBUTTON2, que proporcionan navegación hacia atrás y hacia delante cuando se usa el explorador.

El administrador de ventanas admite XBUTTON1 y XBUTTON2 a través de los mensajes **WM \_ XBUTTON \* *_ y _* WM \_ NCXBUTTON \* *_. El HIWORD de _* WPARAM en** estos mensajes contiene una marca que indica qué botón X se presionó. Dado que estos mensajes del mouse también caben entre las constantes **WM \_ MOUSEFIRST** y **WM \_ MOUSELAST,** una aplicación puede filtrar todos los mensajes del mouse con [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) [**o PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

Los siguientes admiten XBUTTON1 y XBUTTON2:

-   [**WM \_ APPCOMMAND**](wm-appcommand.md)
-   [**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
-   [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
-   [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
-   [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md)
-   [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
-   [**WM \_ XBUTTONUP**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Las siguientes API se modificaron para admitir estos botones:

-   [**evento \_ mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

Es poco probable que una ventana secundaria de una aplicación de componentes pueda implementar directamente comandos para XBUTTON1 y XBUTTON2. Por [**lo tanto, DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un [**mensaje DE WM \_ APPCOMMAND**](wm-appcommand.md) a una ventana cuando se hace clic en un botón X. **DefWindowProc también** envía el mensaje **\_ APPCOMMAND de WM** a su ventana primaria. Esto es similar a la forma en que se invocan los menús contextuales con un clic con el botón derecho:**DefWindowProc** envía un mensaje [**\_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) de WM al menú y también lo envía a su elemento primario. Además, si **DefWindowProc** recibe un mensaje **DE WM \_ APPCOMMAND** para una ventana de nivel superior, llama a un enlace de shell con código \_ APPCOMMAND de HSHELL.

Hay compatibilidad con los teclados que tienen teclas adicionales para las funciones del explorador, las funciones multimedia, el inicio de aplicaciones y la administración de energía. Para obtener más información, vea [Teclas de teclado para examinar y otras funciones](about-keyboard-input.md).

## <a name="mouse-messages"></a>Mensajes del mouse

El mouse genera un evento de entrada cuando el usuario mueve el mouse o presiona o suelta un botón del mouse. El sistema convierte los eventos de entrada del mouse en mensajes y los envía a la cola de mensajes del subproceso adecuado. Cuando los mensajes del mouse se publican más rápido de lo que un subproceso puede procesarlos, el sistema descarta todos los mensajes del mouse, menos el más reciente.

Una ventana recibe un mensaje del mouse cuando se produce un evento del mouse mientras el cursor está dentro de los bordes de la ventana o cuando la ventana ha capturado el mouse. Los mensajes del mouse se dividen en dos grupos: mensajes de área de cliente y mensajes de área no cliente. Normalmente, una aplicación procesa los mensajes del área de cliente y omite los mensajes de área no cliente.

En esta sección se describen los temas siguientes:

-   [Mensajes del mouse del área de cliente](#client-area-mouse-messages)
-   [Mensajes del mouse de área no cliente](#nonclient-area-mouse-messages)
-   [El mensaje \_ WM NCHITTEST](/windows)

### <a name="client-area-mouse-messages"></a>Mensajes del mouse del área de cliente

Una ventana recibe un mensaje de mouse del área de cliente cuando se produce un evento del mouse dentro del área de cliente de la ventana. El sistema envía el [**mensaje \_ WM MOUSEMOVE**](wm-mousemove.md) a la ventana cuando el usuario mueve el cursor dentro del área de cliente. Publica uno de los mensajes siguientes cuando el usuario presiona o suelta un botón del mouse mientras el cursor está dentro del área de cliente.



| Mensaje                                       | Significado                                     |
|-----------------------------------------------|---------------------------------------------|
| [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md) | Se hizo doble clic en el botón izquierdo del mouse.   |
| [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)     | Se presionó el botón primario del mouse.          |
| [**WM \_ LBUTTONUP**](wm-lbuttonup.md)         | Se ha liberado el botón izquierdo del mouse.         |
| [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md) | Se hizo doble clic en el botón central del mouse. |
| [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md)     | Se presionó el botón central del mouse.        |
| [**WM \_ MBUTTONUP**](wm-mbuttonup.md)         | Se ha liberado el botón central del mouse.       |
| [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) | Se ha hecho doble clic con el botón derecho del mouse.  |
| [**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)     | Se presionó el botón secundario del mouse.         |
| [**WM \_ RBUTTONUP**](wm-rbuttonup.md)         | Se ha liberado el botón derecho del mouse.        |
| [**WM \_ XBUTTONDBLCLK**](wm-xbuttondblclk.md) | Se hizo doble clic en un botón X del mouse.       |
| [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)     | Se presionó un botón X del mouse.              |
| [**WM \_ XBUTTONUP**](wm-xbuttonup.md)         | Se ha liberado un botón X del mouse.             |



 

Además, una aplicación puede llamar a [**la función TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que el sistema envíe otros dos mensajes. Envía el mensaje [**WM \_ MOUSEHOVER**](wm-mousehover.md) cuando el cursor mantiene el puntero sobre el área de cliente durante un período de tiempo determinado. Envía el mensaje [**WM \_ MOUSELEAVE**](wm-mouseleave.md) cuando el cursor sale del área de cliente.

### <a name="message-parameters"></a>Parámetros de mensaje

El *parámetro lParam* de un mensaje del mouse del área de cliente indica la posición de la zona de acceso directo del cursor. La palabra de orden bajo indica la coordenada x de la zona de acceso caliente y la palabra de orden superior indica la coordenada Y. Las coordenadas se especifican en coordenadas de cliente. En el sistema de coordenadas de cliente, todos los puntos de la pantalla se especifican en relación con las coordenadas (0,0) de la esquina superior izquierda del área de cliente.

El *parámetro wParam* contiene marcas que indican el estado de los demás botones del mouse y las teclas CTRL y MAYÚS en el momento del evento del mouse. Puede comprobar estas marcas cuando el procesamiento de mensajes del mouse dependa del estado de otro botón del mouse o de la tecla CTRL o MAYÚS. El *parámetro wParam* puede ser una combinación de los valores siguientes.



| Valor            | Descripción                      |
|------------------|----------------------------------|
| **MK \_ CONTROL**  | La tecla CTRL está presionada.            |
| **MK \_ LBUTTON**  | El botón izquierdo del mouse está apagado.   |
| **MK \_ MBUTTON**  | El botón central del mouse está apagado. |
| **MK \_ RBUTTON**  | El botón derecho del mouse está apagado.  |
| **MK \_ SHIFT**    | La tecla MAYÚS está abajo.           |
| **MK \_ XBUTTON1** | El primer botón X está apagado.      |
| **MK \_ XBUTTON2** | El segundo botón X está apagado.     |



 

### <a name="double-click-messages"></a>Double-Click mensajes

El sistema genera un mensaje de doble clic cuando el usuario hace clic dos veces en un botón del mouse en sucesión rápida. Cuando el usuario hace clic en un botón, el sistema establece un rectángulo centrado alrededor de la zona de acceso directo del cursor. También marca la hora a la que se produjo el clic. Cuando el usuario hace clic en el mismo botón una segunda vez, el sistema determina si la zona activa sigue dentro del rectángulo y calcula el tiempo transcurrido desde el primer clic. Si la zona activa sigue dentro del rectángulo y el tiempo transcurrido no supera el valor de tiempo de espera del doble clic, el sistema genera un mensaje de doble clic.

Una aplicación puede obtener y establecer valores de tiempo de espera de doble clic mediante las funciones [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) y [**SetDoubleClickTime,**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) respectivamente. Como alternativa, la aplicación puede establecer el valor de doble clic y tiempo de espera mediante la marca **\_ SPI SETDOUBLECLICKTIME** con la función [**SystemParametersInfo.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) También puede establecer el tamaño del rectángulo que el sistema usa para detectar los doble clics pasando las marcas **SPI \_ SETDOUBLECLPARAMETERIDTH** y **SPI \_ SETDOUBLECLKHEIGHT** a **SystemParametersInfo**. Sin embargo, tenga en cuenta que establecer el valor de doble clic y tiempo de espera y el rectángulo afecta a todas las aplicaciones.

De forma predeterminada, una ventana definida por la aplicación no recibe mensajes de doble clic. Debido a la sobrecarga del sistema implicada en la generación de mensajes de doble clic, estos mensajes solo se generan para las ventanas que pertenecen a clases que tienen el estilo de clase **\_ DBLCLKS de CS.** La aplicación debe establecer este estilo al registrar la clase de ventana. Para obtener más información, vea [Clases de ventana](/windows/desktop/winmsg/window-classes).

Un mensaje de doble clic siempre es el tercer mensaje de una serie de cuatro mensajes. Los dos primeros mensajes son los mensajes de botón hacia abajo y de botón hacia arriba generados por el primer clic. El segundo clic genera el mensaje de doble clic seguido de otro mensaje de botón arriba. Por ejemplo, al hacer doble clic en el botón izquierdo del mouse se genera la siguiente secuencia de mensajes:

1.  [**WM \_ LBUTTONDOWN**](wm-lbuttondown.md)
2.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)
3.  [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
4.  [**WM \_ LBUTTONUP**](wm-lbuttonup.md)

Dado que una ventana siempre recibe un mensaje de botón abajo antes de recibir un mensaje de doble clic, una aplicación suele usar un mensaje de doble clic para extender una tarea que inició durante un mensaje de botón. Por ejemplo, cuando el usuario hace clic en un color en la paleta de colores de Microsoft Paint, Paint muestra el color seleccionado junto a la paleta. Cuando el usuario hace doble clic en un color, Paint muestra el color y abre el **cuadro de diálogo** Editar colores.

### <a name="nonclient-area-mouse-messages"></a>Mensajes del mouse del área no cliente

Una ventana recibe un mensaje de mouse de área no cliente cuando se produce un evento de mouse en cualquier parte de una ventana, excepto en el área de cliente. El área no cliente de una ventana consta de su borde, barra de menús, barra de título, barra de desplazamiento, menú de ventana, botón minimizar y botón maximizar.

El sistema genera mensajes de área no cliente principalmente para su propio uso. Por ejemplo, el sistema usa mensajes de área no cliente para cambiar el cursor a una flecha de dos puntas cuando la zona activa del cursor se mueve al borde de una ventana. Una ventana debe pasar mensajes del mouse de área no cliente a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para aprovechar las ventajas de la interfaz del mouse integrada.

Hay un mensaje de mouse de área no cliente correspondiente para cada mensaje del mouse del área de cliente. Los nombres de estos mensajes son similares, salvo que las constantes con nombre para los mensajes de área no cliente incluyen las letras NC. Por ejemplo, mover el cursor en el área no cliente genera un mensaje [**\_ WM NCMOUSEMOVE**](wm-ncmousemove.md) y presionar el botón izquierdo del mouse mientras el cursor está en el área no cliente genera un mensaje [**WM \_ NCLBUTTONDOWN.**](wm-nclbuttondown.md)

El *parámetro lParam* de un mensaje de mouse de área no cliente es una estructura que contiene las coordenadas x e y de la zona de acceso directo del cursor. A diferencia de las coordenadas de los mensajes del mouse del área de cliente, las coordenadas se especifican en coordenadas de pantalla en lugar de coordenadas de cliente. En el sistema de coordenadas de pantalla, todos los puntos de la pantalla son relativos a las coordenadas (0,0) de la esquina superior izquierda de la pantalla.

El *parámetro wParam* contiene un valor de prueba de posición, un valor que indica dónde se produjo el evento del mouse en el área no cliente. En la sección siguiente se explica el propósito de los valores de prueba de éxito.

### <a name="the-wm_nchittest-message"></a>El mensaje \_ WM NCHITTEST

Cada vez que se produce un evento de mouse, el sistema envía un mensaje [**\_ WM NCHITTEST**](wm-nchittest.md) a la ventana que contiene la zona activa del cursor o a la ventana que ha capturado el mouse. El sistema usa este mensaje para determinar si se va a enviar un mensaje de mouse de área cliente o no cliente. Una aplicación que debe recibir mensajes de movimiento del mouse y de botón del mouse debe pasar el mensaje **\_ WM NCHITTEST** a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

El *parámetro lParam* del mensaje [**WM \_ NCHITTEST**](wm-nchittest.md) contiene las coordenadas de pantalla de la zona de acceso directo del cursor. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina las coordenadas y devuelve un valor de prueba de acceso que indica la ubicación de la zona activa. El valor de la prueba de impacto puede ser uno de los siguientes valores.



| Valor             | Ubicación de la zona de acceso                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | En el borde de una ventana que no tiene un borde de tamaño.                                                                                                                                       |
| **HTBOTTOM**      | En el borde horizontal inferior de una ventana.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | En la esquina inferior izquierda de un borde de ventana.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | En la esquina inferior derecha de un borde de ventana.                                                                                                                                                       |
| **HOTELAPTION**     | En una barra de título.                                                                                                                                                                                     |
| **HTCLIENT**      | En un área de cliente.                                                                                                                                                                                   |
| **HTCLOSE**       | En un **botón** Cerrar.                                                                                                                                                                              |
| **HTERROR**       | En el fondo de la pantalla o en una línea divisora entre ventanas (igual que HTNOWHERE, salvo que la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un pitido del sistema para indicar un error). |
| **HTGROWBOX**     | En un cuadro de tamaño (igual que **HTSIZE).**                                                                                                                                                                 |
| **HTHELP**        | En un **botón Ayuda.**                                                                                                                                                                               |
| **HTHSCROLL**     | En una barra de desplazamiento horizontal.                                                                                                                                                                         |
| **HTLEFT**        | En el borde izquierdo de una ventana.                                                                                                                                                                     |
| **HTMENU**        | En un menú.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | En un **botón Maximizar.**                                                                                                                                                                           |
| **HTMINBUTTON**   | En un **botón Minimizar.**                                                                                                                                                                           |
| **HTNOWHERE**     | En el fondo de la pantalla o en una línea divisora entre ventanas.                                                                                                                                     |
| **HTREDUCE**      | En un **botón Minimizar.**                                                                                                                                                                           |
| **HTRIGHT**       | En el borde derecho de una ventana.                                                                                                                                                                    |
| **HTSIZE**        | En un cuadro de tamaño (igual que **HTGROWBOX).**                                                                                                                                                              |
| **HTSYSMENU**     | En un **menú** Sistema o en un **botón** Cerrar de una ventana secundaria.                                                                                                                                    |
| **HTTOP**         | En el borde horizontal superior de una ventana.                                                                                                                                                         |
| **HTTOPLEFT**     | En la esquina superior izquierda de un borde de ventana.                                                                                                                                                        |
| **HTTOPRIGHT**    | En la esquina superior derecha de un borde de ventana.                                                                                                                                                       |
| **HTTRANSPARENT** | En una ventana cubierta actualmente por otra ventana del mismo subproceso.                                                                                                                                 |
| **HTVSCROLL**     | En la barra de desplazamiento vertical.                                                                                                                                                                         |
| **HTZOOM**        | En un **botón Maximizar.**                                                                                                                                                                           |



 

Si el cursor está en el área de cliente de una ventana, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve el valor de la prueba de acceso **HTCLIENT** al procedimiento de ventana. Cuando el procedimiento de ventana devuelve este código al sistema, el sistema convierte las coordenadas de pantalla de la zona activa del cursor en coordenadas de cliente y, a continuación, envía el mensaje de mouse del área de cliente correspondiente.

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve uno de los otros valores de prueba de acceso cuando la zona activa del cursor está en el área no cliente de una ventana. Cuando el procedimiento de ventana devuelve uno de estos valores de prueba de impacto, el sistema envía un mensaje de mouse de área no cliente, colocando el valor de la prueba de posición en el parámetro *wParam* del mensaje y las coordenadas del cursor en el *parámetro lParam.*

## <a name="mouse-sonar"></a>Mouse Sonar

La característica de accesibilidad Sonar del mouse muestra brevemente varios círculos concéntarios alrededor del puntero cuando el usuario presiona y suelta la tecla CTRL. Esta característica ayuda a un usuario a localizar el puntero del mouse en una pantalla desordenada o con la resolución establecida en alta, en un monitor de baja calidad o para usuarios con discapacidades visuales. Para obtener más información, vea las marcas siguientes [**en SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSESONAR**

**SPI \_ SETMOUSESONAR**

## <a name="mouse-vanish"></a>Mouse Desvaneciendo

La característica de accesibilidad Desvaneciendo del mouse oculta el puntero cuando el usuario escribe. El puntero del mouse vuelve a aparecer cuando el usuario mueve el mouse. Esta característica evita que el puntero obscure el texto que se escribe, por ejemplo, en un correo electrónico u otro documento. Para obtener más información, vea las marcas siguientes [**en SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**SPI \_ GETMOUSEVANISH**

**SPI \_ SETMOUSEVANISH**

## <a name="the-mouse-wheel"></a>Rueda del mouse

La rueda del mouse combina las características de una rueda y un botón del mouse. La rueda tiene notches discretos y espaciados uniformemente. Al girar la rueda, se envía un mensaje de rueda a la aplicación a medida que se encuentra cada marca. El botón de rueda también puede funcionar como un botón Windows botón central (tercer). Al presionar y soltar la rueda del mouse se envían mensajes [**\_ estándar MBUTTONUP**](wm-mbuttonup.md) [**y WM \_ MBUTTONDOWN.**](wm-mbuttondown.md) Al hacer doble clic en el tercer botón, se envía el [**mensaje \_ estándar WM MBUTTONDBLCLK.**](wm-mbuttondblclk.md)

La rueda del mouse se admite a través del [**mensaje \_ WM MOUSEWHEEL.**](wm-mousewheel.md)

Al girar el mouse, se envía el [**mensaje \_ WM MOUSEWHEEL**](wm-mousewheel.md) a la ventana de enfoque. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga el mensaje al elemento primario de la ventana. No debe haber ningún reenvío interno del mensaje, ya que **DefWindowProc** lo propaga por la cadena primaria hasta que se encuentra una ventana que lo procesa.

### <a name="determining-the-number-of-scroll-lines"></a>Determinar el número de líneas de desplazamiento

Las aplicaciones deben usar [**la función SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para recuperar el número de líneas que se desplaza un documento para cada operación de desplazamiento (notch de rueda). Para recuperar el número de líneas, una aplicación realiza la siguiente llamada:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



La variable "pulScrollLines" apunta a un valor entero sin signo que recibe el número sugerido de líneas para desplazarse cuando se gira la rueda del mouse sin teclas modificadoras:

-   Si este número es 0, no debe producirse ningún desplazamiento.
-   Si este número es **WHEEL \_ PAGESCROLL,** se debe interpretar una rueda como hacer clic una vez en las regiones de página hacia abajo o hacia arriba de la barra de desplazamiento.
-   Si el número de líneas que se va a desplazar es mayor que el número de líneas que se pueden ver, la operación de desplazamiento también debe interpretarse como una operación de página hacia abajo o hacia arriba.

El valor predeterminado para el número de líneas de desplazamiento será 3. Si un usuario cambia el número de líneas de desplazamiento, mediante la hoja Propiedades del mouse de Panel de control, el sistema operativo difunde un mensaje [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) a todas las ventanas de nivel superior con **SPI \_ SETWHEELSCROLLLINES especificado.** Cuando una aplicación recibe el **mensaje \_ WM SETTINGCHANGE,** puede obtener el nuevo número de líneas de desplazamiento llamando a:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Controles que se desplazan

En la tabla siguiente se enumeran los controles con funcionalidad de desplazamiento (incluidas las líneas de desplazamiento establecidas por el usuario). 

| Control                 | Desplazamiento                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Editar control            | Vertical y horizontal.                                                                                                                                                |
| Control Cuadro de lista        | Vertical y horizontal.                                                                                                                                                |
| Cuadro combinado               | Cuando no se deja, cada desplazamiento recupera el elemento siguiente o anterior. Cuando se deja fuera, cada desplazamiento reenvía el mensaje al cuadro de lista, que se desplaza en consecuencia. |
| CMD (línea de comandos)      | Vertical.                                                                                                                                                               |
| Vista de árbol               | Vertical y horizontal.                                                                                                                                                |
| Vista de lista               | Vertical y horizontal.                                                                                                                                                |
| Desplazamientos hacia arriba y hacia abajo         | Un elemento a la vez.                                                                                                                                                     |
| Desplazamientos de la barra de seguimiento        | Un elemento a la vez.                                                                                                                                                     |
| Edición enriquecte de Microsoft 1.0 | Vertical. Tenga en cuenta que Exchange cliente tiene sus propias versiones de la vista de lista y los controles de vista de árbol que no tienen compatibilidad con rueda.                                        |
| Edición enriquecte de Microsoft 2.0 | Vertical.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Detección de un mouse con una rueda

Para determinar si un mouse con una rueda está conectado, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ MOUSEWHEELPRESENT**. Un valor devuelto **de TRUE** indica que el mouse está conectado.

El ejemplo siguiente es del procedimiento de ventana para un control de edición multilínea:


```
BOOL ScrollLines(
     PWNDDATA pwndData,   //scrolls the window indicated
     int cLinesToScroll); //number of times

short gcWheelDelta; //wheel delta from roll
PWNDDATA pWndData; //pointer to structure containing info about the window
UINT gucWheelScrollLines=0;//number of lines to scroll on a wheel rotation

gucWheelScrollLines = SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 
                             0, 
                             pulScrollLines, 
                             0);

case WM_MOUSEWHEEL:
    /*
     * Do not handle zoom and datazoom.
     */
    if (wParam & (MK_SHIFT | MK_CONTROL)) {
        goto PassToDefaultWindowProc;
    }

    gcWheelDelta -= (short) HIWORD(wParam);
    if (abs(gcWheelDelta) >= WHEEL_DELTA && gucWheelScrollLines > 0) 
    {
        int cLineScroll;

        /*
         * Limit a roll of one (1) WHEEL_DELTA to
         * scroll one (1) page.
         */
        cLineScroll = (int) min(
                (UINT) pWndData->ichLinesOnScreen - 1,
                gucWheelScrollLines);

        if (cLineScroll == 0) {
            cLineScroll++;
        }

        cLineScroll *= (gcWheelDelta / WHEEL_DELTA);
        assert(cLineScroll != 0);

        gcWheelDelta = gcWheelDelta % WHEEL_DELTA;
        return ScrollLines(pWndData, cLineScroll);
    }

    break;
```



## <a name="window-activation"></a>Activación de ventanas

Cuando el usuario hace clic en una ventana de nivel superior inactiva o en la ventana secundaria de una ventana de nivel superior inactiva, el sistema envía el mensaje [**\_ WM MOUSEACTIVATE**](wm-mouseactivate.md) (entre otros) al nivel superior o a la ventana secundaria. El sistema envía este mensaje después de publicar el [**mensaje \_ WM NCHITTEST**](wm-nchittest.md) en la ventana, pero antes de publicar el mensaje de botón. Cuando **WM \_ MOUSEACTIVATE** se pasa a la función [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el sistema activa la ventana de nivel superior y, a continuación, envía el mensaje de botón hacia abajo a la ventana de nivel superior o secundario.

Al procesar [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), una ventana puede controlar si la ventana de nivel superior se convierte en la ventana activa como resultado de un clic del mouse y si la ventana en la que se hizo clic recibe el mensaje de botón abajo posterior. Para ello, devuelve uno de los siguientes valores después de procesar **WM \_ MOUSEACTIVATE**.



| Valor                    | Significado                                                              |
|--------------------------|----------------------------------------------------------------------|
| **MA \_ ACTIVATE**         | Activa la ventana y no descarta el mensaje del mouse.         |
| **MA \_ NOACTIVATE**       | No activa la ventana y no descarta el mensaje del mouse. |
| **MA \_ ACTIVATEANDEAT**   | Activa la ventana y descarta el mensaje del mouse.                 |
| **MA \_ NOACTIVATEANDEAT** | No activa la ventana, pero descarta el mensaje del mouse.         |

## <a name="see-also"></a>Consulte también

[Aprovechar las ventajas del High-Definition del mouse](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)