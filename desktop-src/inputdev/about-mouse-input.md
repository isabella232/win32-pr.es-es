---
title: Acerca de la entrada del mouse
description: En este tema se describe la entrada del mouse.
ms.assetid: 1f945a31-76d5-4e23-a55a-769ca114dbe9
keywords:
- entrada del usuario, entrada del mouse
- capturar datos proporcionados por el usuario, entrada del mouse
- entrada del mouse
- cursor del mouse
- cursores, entrada del mouse
- captura del mouse
- Bloqueo de clic del mouse
- XBUTTONs
- configuración del mouse
- mensajes del mouse
- Mensaje WM_NCHITTEST
- Característica de accesibilidad de desaparecer del mouse
- Característica de accesibilidad de mouse Sónar
- rueda del mouse
- Mensaje WM_MOUSEWHEEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2294027cb4ca2c97371a7a06c90a7e46188e3b7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791386"
---
# <a name="about-mouse-input"></a>Acerca de la entrada del mouse

El mouse es un dispositivo de entrada de usuario importante, pero opcional, para las aplicaciones. Una aplicación bien escrita debe incluir una interfaz del mouse, pero no debe depender únicamente del mouse para la adquisición de datos proporcionados por el usuario. La aplicación debe proporcionar también compatibilidad completa con el teclado.

Una aplicación recibe la entrada del mouse en forma de mensajes que se envían o se publican en sus ventanas.

En esta sección se describen los temas siguientes:

-   [Cursor del mouse](#mouse-cursor)
-   [Captura del mouse](#mouse-capture)
-   [Bloqueo de clic del mouse](#mouse-clicklock)
-   [Configuración del mouse](#mouse-configuration)
-   [XBUTTONs](#xbuttons)
-   [Mensajes del mouse](#mouse-messages)
    -   [Mensajes del mouse del área cliente](#client-area-mouse-messages)
    -   [Mensajes de mouse de área no cliente](#nonclient-area-mouse-messages)
    -   [El mensaje de NCHITTEST de WM \_](/windows)
-   [Mouse Sónar](#mouse-sonar)
-   [Desaparecedo del mouse](#mouse-vanish)
-   [La rueda del mouse](#the-mouse-wheel)
-   [Activación de ventanas](#window-activation)

## <a name="mouse-cursor"></a>Cursor del mouse

Cuando el usuario mueve el mouse, el sistema mueve un mapa de bits en la pantalla denominado *cursor del mouse*. El cursor del mouse contiene un punto de un solo píxel denominado *zona activa*, un punto en el que el sistema realiza un seguimiento y lo reconoce como la posición del cursor. Cuando se produce un evento del mouse, la ventana que contiene la zona activa suele recibir el mensaje del mouse resultante del evento. La ventana no debe estar activa o tener el foco de teclado para recibir un mensaje del mouse.

El sistema mantiene una variable que controla la velocidad del mouse, es decir, la distancia que el cursor se mueve cuando el usuario mueve el mouse. Puede usar la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con la marca **SPI \_ GETMOUSE** o **SPI \_ SETMOUSE** para recuperar o establecer la velocidad del mouse. Para obtener más información sobre los cursores del mouse, vea [cursores](/windows/desktop/menurc/cursors).

## <a name="mouse-capture"></a>Captura del mouse

Normalmente, el sistema envía un mensaje del mouse a la ventana que contiene la zona activa del cursor cuando se produce un evento del mouse. Una aplicación puede cambiar este comportamiento mediante la función [**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture) para enrutar los mensajes del mouse a una ventana específica. La ventana recibe todos los mensajes del mouse hasta que la aplicación llama a la función [**releaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture) o especifica otra ventana de captura, o hasta que el usuario hace clic en una ventana creada por otro subproceso.

Cuando la captura del mouse cambia, el sistema envía un mensaje de [**WM \_ CAPTURECHANGED**](wm-capturechanged.md) a la ventana que está perdiendo la captura del mouse. El parámetro *lParam* del mensaje especifica un identificador para la ventana que obtiene la captura del mouse.

Solo la ventana de primer plano puede capturar la entrada del mouse. Cuando una ventana en segundo plano intenta capturar la entrada del mouse, solo recibe mensajes de los eventos del mouse que se producen cuando la zona activa del cursor está dentro de la parte visible de la ventana.

La captura de la entrada del mouse resulta útil si una ventana debe recibir toda la entrada del mouse, incluso cuando el cursor se mueva fuera de la ventana. Por ejemplo, una aplicación normalmente realiza un seguimiento de la posición del cursor después de un evento de presionar el botón del mouse, siguiendo el cursor hasta que se produce un evento de presionar el botón del mouse. Si una aplicación no ha capturado la entrada del mouse y el usuario suelta el botón del mouse fuera de la ventana, la ventana no recibirá el mensaje de botón.

Un subproceso puede usar la función [**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture) para determinar si una de sus ventanas ha capturado el mouse. Si una de las ventanas del subproceso ha capturado el mouse, **GetCapture** recupera un identificador de la ventana.

## <a name="mouse-clicklock"></a>Bloqueo de clic del mouse

La característica de accesibilidad de bloqueo del mouse permite a un usuario bloquear el botón primario del mouse después de un solo clic. En una aplicación, el botón todavía parece estar presionado. Para desbloquear el botón, una aplicación puede enviar cualquier mensaje del mouse o el usuario puede hacer clic en cualquier botón del mouse. Esta característica permite a un usuario realizar combinaciones complejas de mouse con más facilidad. Por ejemplo, aquellos con ciertas limitaciones físicas pueden resaltar texto, arrastrar objetos o abrir menús más fácilmente. Para obtener más información, vea las marcas siguientes y los comentarios en [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

-   **\_GETMOUSECLICKLOCK SPI**
-   **\_SETMOUSECLICKLOCK SPI**
-   **\_GETMOUSECLICKLOCKTIME SPI**
-   **\_SETMOUSECLICKLOCKTIME SPI**

## <a name="mouse-configuration"></a>Configuración del mouse

Aunque el mouse es un dispositivo de entrada importante para las aplicaciones, no todos los usuarios tienen necesariamente un mouse. Una aplicación puede determinar si el sistema incluye un mouse pasando el valor **SM \_ MOUSEPRESENT** a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) .

Windows admite un mouse que tenga hasta tres botones. En un mouse de tres botones, los botones se designan como los botones izquierdo, central y derecho. Los mensajes y las constantes con nombre relacionadas con los botones del mouse usan las letras L, M y R para identificar los botones. El botón de un mouse de un solo botón se considera el botón primario. Aunque Windows admite un mouse con varios botones, la mayoría de las aplicaciones usan el botón primario principalmente y los demás como mínimo, si es que lo están.

Las aplicaciones también pueden admitir una rueda del mouse. La rueda del mouse se puede presionar o girar. Cuando se presiona la rueda del mouse, actúa como el botón central (tercer) y envía los mensajes normales del botón central a la aplicación. Cuando se gira, se envía un mensaje de rueda a la aplicación. Para obtener más información, vea [la sección rueda del mouse](#the-mouse-wheel) .

Las aplicaciones pueden admitir botones de comando de aplicación. Estos botones, denominados botones X, están diseñados para permitir un acceso más sencillo a un explorador de Internet, correo electrónico y Media Services. Cuando se presiona un botón X, se envía un mensaje de [**\_ APPCOMMAND de WM**](wm-appcommand.md) a la aplicación. Para obtener más información, vea la descripción del mensaje de **\_ APPCOMMAND de WM** .

Una aplicación puede determinar el número de botones del mouse pasando el valor **SM \_ CMOUSEBUTTONS** a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Para configurar el mouse para un usuario de la mano izquierda, la aplicación puede usar la función [**SwapMouseButton**](/windows/win32/api/winuser/nf-winuser-swapmousebutton) para invertir el significado de los botones primario y secundario del mouse. Pasar el valor **SPI \_ SETMOUSEBUTTONSWAP** a la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) es otra manera de invertir el significado de los botones. Sin embargo, tenga en cuenta que el mouse es un recurso compartido, por lo que invertir el significado de los botones afecta a todas las aplicaciones.

## <a name="xbuttons"></a>XBUTTONs

Windows admite un mouse con cinco botones. Además de los botones izquierdo, central y derecho, hay XBUTTON1 y XBUTTON2, que proporcionan navegación hacia atrás y hacia delante cuando se usa el explorador.

El administrador de ventanas admite XBUTTON1 y XBUTTON2 a través de los mensajes de **WM \_ botón xbutton \*** y **WM \_ NCXBUTTON \*** . El HIWORD del **wParam** en estos mensajes contiene una marca que indica qué botón X se presionó. Dado que estos mensajes de mouse también se ajustan entre las constantes **WM \_ MOUSEFIRST** y **WM \_ MOUSELAST**, una aplicación puede filtrar todos los mensajes del mouse con [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

La siguiente compatibilidad con XBUTTON1 y XBUTTON2:

-   [**APPCOMMAND de WM \_**](wm-appcommand.md)
-   [**NCXBUTTONDBLCLK de WM \_**](wm-ncxbuttondblclk.md)
-   [**NCXBUTTONDOWN de WM \_**](wm-ncxbuttondown.md)
-   [**NCXBUTTONUP de WM \_**](wm-ncxbuttonup.md)
-   [**XBUTTONDBLCLK de WM \_**](wm-xbuttondblclk.md)
-   [**XBUTTONDOWN de WM \_**](wm-xbuttondown.md)
-   [**XBUTTONUP de WM \_**](wm-xbuttonup.md)
-   [**MOUSEHOOKSTRUCTEX**](/windows/win32/api/winuser/ns-winuser-mousehookstructex)

Las siguientes API se han modificado para admitir estos botones:

-   [**evento del mouse \_**](/windows/win32/api/winuser/nf-winuser-mouse_event)
-   [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))
-   [**MSLLHOOKSTRUCT**](/windows/win32/api/winuser/ns-winuser-msllhookstruct)
-   [**MOUSEINPUT**](/windows/win32/api/winuser/ns-winuser-mouseinput)
-   [**PARENTNOTIFY de WM \_**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)

No es probable que una ventana secundaria en una aplicación de componentes pueda implementar directamente comandos para XBUTTON1 y XBUTTON2. Por lo tanto, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje de [**WM \_ APPCOMMAND**](wm-appcommand.md) a una ventana cuando se hace clic en un botón X. **DefWindowProc** también envía el mensaje de **WM \_ APPCOMMAND** a su ventana primaria. Esto es similar a la manera en que se invocan los menús contextuales con un clic con el botón derecho:**DefWindowProc** envía un mensaje de control de texto de [**WM \_**](/windows/desktop/menurc/wm-contextmenu) al menú y también lo envía a su elemento primario. Además, si **DefWindowProc** recibe un mensaje de **\_ APPCOMMAND de WM** para una ventana de nivel superior, llama a un enlace de Shell con el código HSHELL \_ APPCOMMAND.

Hay compatibilidad con los teclados que tienen claves adicionales para las funciones del explorador, las funciones multimedia, el inicio de aplicaciones y la administración de energía. Para obtener más información, consulte [teclas del teclado para la exploración y otras funciones](about-keyboard-input.md).

## <a name="mouse-messages"></a>Mensajes del mouse

El mouse genera un evento de entrada cuando el usuario mueve el mouse, o presiona o suelta un botón del mouse. El sistema convierte los eventos de entrada del mouse en mensajes y los envía a la cola de mensajes del subproceso correspondiente. Cuando los mensajes del mouse se envían más rápido que un subproceso puede procesarlos, el sistema descarta todo menos el último mensaje del mouse.

Una ventana recibe un mensaje del mouse cuando se produce un evento del mouse mientras el cursor se encuentra dentro de los bordes de la ventana, o cuando la ventana ha capturado el mouse. Los mensajes del mouse se dividen en dos grupos: mensajes de área de cliente y mensajes de área no cliente. Normalmente, una aplicación procesa los mensajes de área de cliente y omite los mensajes de área no cliente.

En esta sección se describen los temas siguientes:

-   [Mensajes del mouse del área cliente](#client-area-mouse-messages)
-   [Mensajes de mouse de área no cliente](#nonclient-area-mouse-messages)
-   [El mensaje de NCHITTEST de WM \_](/windows)

### <a name="client-area-mouse-messages"></a>Mensajes del mouse del área cliente

Una ventana recibe un mensaje del mouse del área de cliente cuando se produce un evento del mouse en el área cliente de la ventana. El sistema envía el mensaje del [**\_ MOUSEMOVE de WM**](wm-mousemove.md) a la ventana cuando el usuario mueve el cursor dentro del área cliente. Envía uno de los mensajes siguientes cuando el usuario presiona o suelta un botón del mouse mientras el cursor se encuentra dentro del área cliente.



| Mensaje                                       | Significado                                     |
|-----------------------------------------------|---------------------------------------------|
| [**LBUTTONDBLCLK de WM \_**](wm-lbuttondblclk.md) | Se hizo doble clic en el botón primario del mouse.   |
| [**LBUTTONDOWN de WM \_**](wm-lbuttondown.md)     | Se presionó el botón primario del mouse.          |
| [**LBUTTONUP de WM \_**](wm-lbuttonup.md)         | Se liberó el botón primario del mouse.         |
| [**MBUTTONDBLCLK de WM \_**](wm-mbuttondblclk.md) | Se hizo doble clic en el botón central del mouse. |
| [**MBUTTONDOWN de WM \_**](wm-mbuttondown.md)     | Se presionó el botón central del mouse.        |
| [**MBUTTONUP de WM \_**](wm-mbuttonup.md)         | Se liberó el botón central del mouse.       |
| [**RBUTTONDBLCLK de WM \_**](wm-rbuttondblclk.md) | Se hizo doble clic con el botón secundario del mouse.  |
| [**RBUTTONDOWN de WM \_**](wm-rbuttondown.md)     | Se presionó el botón secundario del mouse.         |
| [**RBUTTONUP de WM \_**](wm-rbuttonup.md)         | Se liberó el botón secundario del mouse.        |
| [**XBUTTONDBLCLK de WM \_**](wm-xbuttondblclk.md) | Se hizo doble clic en un botón X del mouse.       |
| [**XBUTTONDOWN de WM \_**](wm-xbuttondown.md)     | Se presionó un botón X del mouse.              |
| [**XBUTTONUP de WM \_**](wm-xbuttonup.md)         | Se liberó un botón X del mouse.             |



 

Además, una aplicación puede llamar a la función [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) para que el sistema envíe otros dos mensajes. Envía el mensaje [**de \_ MOUSEHOVER de WM**](wm-mousehover.md) cuando el cursor se mantiene sobre el área de cliente durante un período de tiempo determinado. Envía el mensaje de [**WM \_ MOUSELEAVE**](wm-mouseleave.md) cuando el cursor sale del área cliente.

### <a name="message-parameters"></a>Parámetros de mensaje

El parámetro *lParam* de un mensaje del mouse del área de cliente indica la posición de la zona activa del cursor. La palabra de orden inferior indica la coordenada x de la zona activa y la palabra de orden superior indica la coordenada y. Las coordenadas se especifican en coordenadas de cliente. En el sistema de coordenadas de cliente, todos los puntos de la pantalla se especifican en relación con las coordenadas (0,0) de la esquina superior izquierda del área cliente.

El parámetro *wParam* contiene marcas que indican el estado de los demás botones del mouse y las teclas Ctrl y Mayús en el momento del evento del mouse. Puede buscar estas marcas cuando el procesamiento de mensajes de mouse depende del estado de otro botón del mouse o de la tecla CTRL o Mayús. El parámetro *wParam* puede ser una combinación de los valores siguientes.



| Value            | Descripción                      |
|------------------|----------------------------------|
| **MK ( \_ control)**  | La tecla CTRL está presionada.            |
| **MK \_ LBUTTON**  | El botón primario del mouse está inactivo.   |
| **MK \_ MBUTTON**  | El botón central del mouse está presionado. |
| **MK \_ RBUTTON**  | El botón secundario del mouse está inactivo.  |
| **\_MAYÚS MK**    | La tecla Mayús está presionada.           |
| **MK \_ XBUTTON1** | El primer botón X está inactivo.      |
| **MK \_ XBUTTON2** | El segundo botón X está inactivo.     |



 

### <a name="double-click-messages"></a>Mensajes de Double-Click

El sistema genera un mensaje de doble clic cuando el usuario hace clic dos veces en el botón del mouse en una sucesión rápida. Cuando el usuario hace clic en un botón, el sistema establece un rectángulo centrado alrededor de la zona activa del cursor. También marca la hora a la que se hizo clic. Cuando el usuario hace clic en el mismo botón una segunda vez, el sistema determina si la zona activa permanece dentro del rectángulo y calcula el tiempo transcurrido desde el primer clic. Si la zona activa todavía está dentro del rectángulo y el tiempo transcurrido no supera el valor de tiempo de espera de doble clic, el sistema genera un mensaje de doble clic.

Una aplicación puede obtener y establecer valores de tiempo de espera de doble clic mediante las funciones [**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime) y [**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime) , respectivamente. Como alternativa, la aplicación puede establecer el valor de tiempo de espera de doble clic mediante la marca **SPI \_ SETDOUBLECLICKTIME** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) . También puede establecer el tamaño del rectángulo que el sistema utiliza para detectar los doble clics pasando las marcas **SPI \_ SETDOUBLECLKWIDTH** y **SPI \_ SETDOUBLECLKHEIGHT** a **SystemParametersInfo**. Sin embargo, tenga en cuenta que establecer el valor de tiempo de espera y el rectángulo de doble clic afecta a todas las aplicaciones.

De forma predeterminada, una ventana definida por la aplicación no recibe mensajes de doble clic. Debido a la sobrecarga del sistema implicada en la generación de mensajes de doble clic, estos mensajes solo se generan para las ventanas que pertenecen a clases que tienen el estilo de clase **CS \_ DBLCLKS** . La aplicación debe establecer este estilo al registrar la clase de ventana. Para obtener más información, vea [clases de ventana](/windows/desktop/winmsg/window-classes).

Un mensaje de doble clic siempre es el tercer mensaje en una serie de cuatro mensajes. Los dos primeros mensajes son los mensajes de botón y de botón arriba generados por el primer clic. El segundo clic genera el mensaje de doble clic seguido de otro mensaje de botón. Por ejemplo, al hacer doble clic en el botón primario del mouse se genera la siguiente secuencia de mensajes:

1.  [**LBUTTONDOWN de WM \_**](wm-lbuttondown.md)
2.  [**LBUTTONUP de WM \_**](wm-lbuttonup.md)
3.  [**LBUTTONDBLCLK de WM \_**](wm-lbuttondblclk.md)
4.  [**LBUTTONUP de WM \_**](wm-lbuttonup.md)

Dado que una ventana siempre recibe un mensaje de botón abajo antes de recibir un mensaje de doble clic, una aplicación normalmente usa un mensaje de doble clic para extender una tarea que comenzó durante un mensaje de botón presionado. Por ejemplo, cuando el usuario hace clic en un color de la paleta de colores de Microsoft Paint, Paint muestra el color seleccionado junto a la paleta. Cuando el usuario hace doble clic en un color, Paint muestra el color y abre el cuadro de diálogo **Editar colores** .

### <a name="nonclient-area-mouse-messages"></a>Mensajes de mouse de área no cliente

Una ventana recibe un mensaje de mouse de área no cliente cuando se produce un evento del mouse en cualquier parte de una ventana excepto en el área cliente. El área no cliente de una ventana está formada por el borde, la barra de menús, la barra de título, la barra de desplazamiento, el menú ventana, el botón minimizar y el botón maximizar.

El sistema genera mensajes de área no cliente principalmente para su propio uso. Por ejemplo, el sistema utiliza mensajes de área no cliente para cambiar el cursor a una flecha de dos puntas cuando la zona activa del cursor se mueve al borde de una ventana. Una ventana debe pasar mensajes de mouse de área no cliente a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para aprovechar las ventajas de la interfaz de mouse integrada.

Hay un mensaje de mouse de área no cliente correspondiente para cada mensaje de mouse de área de cliente. Los nombres de estos mensajes son similares, salvo que las constantes con nombre para los mensajes de área no cliente incluyen las letras NC. Por ejemplo, al mover el cursor en el área no cliente, se genera un mensaje de [**WM \_ NCMOUSEMOVE**](wm-ncmousemove.md) y al presionar el botón primario del mouse mientras el cursor se encuentra en el área no cliente, se genera un mensaje de [**\_ NCLBUTTONDOWN de WM**](wm-nclbuttondown.md) .

El parámetro *lParam* de un mensaje de mouse de área no cliente es una estructura que contiene las coordenadas x e y de la zona activa del cursor. A diferencia de las coordenadas de los mensajes de mouse del área de cliente, las coordenadas se especifican en coordenadas de pantalla en lugar de en coordenadas de cliente. En el sistema de coordenadas de la pantalla, todos los puntos de la pantalla son relativos a las coordenadas (0,0) de la esquina superior izquierda de la pantalla.

El parámetro *wParam* contiene un valor de la prueba de posicionamiento, un valor que indica dónde se produjo el evento del mouse en el área no cliente. En la siguiente sección se explica el propósito de los valores de las pruebas de posicionamiento.

### <a name="the-wm_nchittest-message"></a>El mensaje de NCHITTEST de WM \_

Siempre que se produce un evento del mouse, el sistema envía un mensaje de [**WM \_ NCHITTEST**](wm-nchittest.md) a la ventana que contiene la zona activa del cursor o a la ventana que ha capturado el mouse. El sistema utiliza este mensaje para determinar si se va a enviar un área de cliente o un mensaje de mouse de área no cliente. Una aplicación que debe recibir los mensajes de botón del mouse y de movimiento del mouse debe pasar el mensaje de **\_ NCHITTEST de WM** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

El parámetro *lParam* del mensaje [**de \_ NCHITTEST de WM**](wm-nchittest.md) contiene las coordenadas de pantalla de la zona activa del cursor. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina las coordenadas y devuelve un valor de la prueba de posicionamiento que indica la ubicación de la zona activa. El valor de la prueba de posicionamiento puede ser uno de los valores siguientes.



| Value             | Ubicación de la zona activa                                                                                                                                                                                |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HTBORDER**      | En el borde de una ventana que no tiene un borde de ajuste de tamaño.                                                                                                                                       |
| **HTBOTTOM**      | En el borde inferior horizontal de una ventana.                                                                                                                                                         |
| **HTBOTTOMLEFT**  | En la esquina inferior izquierda de un borde de ventana.                                                                                                                                                        |
| **HTBOTTOMRIGHT** | En la esquina inferior derecha de un borde de ventana.                                                                                                                                                       |
| **HTCAPTION**     | En una barra de título.                                                                                                                                                                                     |
| **HTCLIENT**      | En un área cliente.                                                                                                                                                                                   |
| **HTCLOSE**       | En un botón **cerrar** .                                                                                                                                                                              |
| **HTERROR**       | En el fondo de la pantalla o en una línea divisoria entre ventanas (igual que HTNOWHERE, con la excepción de que la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un bip del sistema para indicar un error). |
| **HTGROWBOX**     | En un cuadro de tamaño (igual que **HTSIZE**).                                                                                                                                                                 |
| **HTHELP**        | En un botón **ayuda** .                                                                                                                                                                               |
| **HTHSCROLL**     | En una barra de desplazamiento horizontal.                                                                                                                                                                         |
| **HTLEFT**        | En el borde izquierdo de una ventana.                                                                                                                                                                     |
| **HTMENU**        | En un menú.                                                                                                                                                                                          |
| **HTMAXBUTTON**   | En un botón **maximizar** .                                                                                                                                                                           |
| **HTMINBUTTON**   | En un botón **minimizar** .                                                                                                                                                                           |
| **HTNOWHERE**     | En el fondo de la pantalla o en una línea divisoria entre ventanas.                                                                                                                                     |
| **HTREDUCE**      | En un botón **minimizar** .                                                                                                                                                                           |
| **HTRIGHT**       | En el borde derecho de una ventana.                                                                                                                                                                    |
| **HTSIZE**        | En un cuadro de tamaño (igual que **HTGROWBOX**).                                                                                                                                                              |
| **HTSYSMENU**     | En un menú **del sistema** o en un botón **cerrar** de una ventana secundaria.                                                                                                                                    |
| **HTTOP**         | En el borde superior horizontal de una ventana.                                                                                                                                                         |
| **HTTOPLEFT**     | En la esquina superior izquierda de un borde de ventana.                                                                                                                                                        |
| **HTTOPRIGHT**    | En la esquina superior derecha de un borde de ventana.                                                                                                                                                       |
| **HTTRANSPARENT** | En una ventana actualmente incluida en otra ventana del mismo subproceso.                                                                                                                                 |
| **HTVSCROLL**     | En la barra de desplazamiento vertical.                                                                                                                                                                         |
| **HTZOOM**        | En un botón **maximizar** .                                                                                                                                                                           |



 

Si el cursor está en el área de cliente de una ventana, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve el valor de la prueba de posicionamiento de **HTCLIENT** al procedimiento de ventana. Cuando el procedimiento de ventana devuelve este código al sistema, el sistema convierte las coordenadas de pantalla de la zona activa del cursor en coordenadas de cliente y, a continuación, envía el mensaje de mouse del área de cliente correspondiente.

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve uno de los otros valores de prueba de posicionamiento cuando la zona activa del cursor está en el área no cliente de una ventana. Cuando el procedimiento de ventana devuelve uno de estos valores de prueba de posicionamiento, el sistema envía un mensaje de mouse de área no cliente, y coloca el valor de la prueba de posicionamiento en el parámetro *wParam* del mensaje y las coordenadas del cursor en el parámetro *lParam* .

## <a name="mouse-sonar"></a>Mouse Sónar

La característica de accesibilidad Sónar del mouse muestra brevemente varios círculos concéntricos alrededor del puntero cuando el usuario presiona y suelta la tecla CTRL. Esta característica ayuda a los usuarios a encontrar el puntero del mouse sobre una pantalla que está desordenada o con una resolución establecida en alta, en un monitor de mala calidad o para usuarios con deficiencias visuales. Para obtener más información, vea las marcas siguientes en [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**\_GETMOUSESONAR SPI**

**\_SETMOUSESONAR SPI**

## <a name="mouse-vanish"></a>Desaparecedo del mouse

La característica de accesibilidad de desaparecer del mouse oculta el puntero cuando el usuario está escribiendo. El puntero del mouse vuelve a aparecer cuando el usuario mueve el mouse. Esta característica evita que el puntero oculte el texto que se va a escribir, por ejemplo, en un mensaje de correo electrónico o en otro documento. Para obtener más información, vea las marcas siguientes en [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa):

**\_GETMOUSEVANISH SPI**

**\_SETMOUSEVANISH SPI**

## <a name="the-mouse-wheel"></a>La rueda del mouse

La rueda del mouse combina las características de una rueda y un botón del mouse. La rueda tiene muescas discretas de espaciado uniforme. Al girar la rueda, se envía un mensaje de rueda a la aplicación cuando se encuentra cada muesca. El botón de rueda también puede funcionar como un botón central de Windows (tercer) normal. Al presionar y soltar la rueda del mouse se envían mensajes estándar de [**WM \_ MBUTTONUP**](wm-mbuttonup.md) y [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md) . Al hacer doble clic en el tercer botón, se envía el mensaje [**\_ MBUTTONDBLCLK de WM**](wm-mbuttondblclk.md) estándar.

La rueda del mouse se admite a través del mensaje de [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) .

Al girar el mouse, se envía el mensaje de [**WM \_ MOUSEWHEEL**](wm-mousewheel.md) a la ventana de enfoque. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga el mensaje al elemento primario de la ventana. No debe haber un reenvío interno del mensaje, ya que **DefWindowProc** lo propaga hacia arriba en la cadena primaria hasta que se encuentre una ventana que lo procese.

### <a name="determining-the-number-of-scroll-lines"></a>Determinar el número de líneas de desplazamiento

Las aplicaciones deben usar la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para recuperar el número de líneas que se desplaza un documento para cada operación de desplazamiento (muesca de rueda). Para recuperar el número de líneas, una aplicación realiza la siguiente llamada:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



La variable "pulScrollLines" apunta a un valor entero sin signo que recibe el número sugerido de líneas que se va a desplazar cuando la rueda del mouse se gira sin teclas modificadoras:

-   Si este número es 0, no se debe desplazar.
-   Si este número es la **rueda \_ PAGESCROLL**, un rollo de rueda debe interpretarse como hacer clic una vez en las regiones Av Pág o re pág de la barra de desplazamiento.
-   Si el número de líneas que se va a desplazar es mayor que el número de líneas visibles, la operación de desplazamiento también debe interpretarse como una operación Av Pág o re pág.

El valor predeterminado para el número de líneas de desplazamiento será 3. Si un usuario cambia el número de líneas de desplazamiento, mediante la hoja de propiedades del mouse en el panel de control, el sistema operativo difunde un mensaje de [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) en todas las ventanas de nivel superior con **SPI \_ SETWHEELSCROLLLINES** especificado. Cuando una aplicación recibe el mensaje de **\_ SETTINGCHANGE de WM** , puede obtener el nuevo número de líneas de desplazamiento mediante una llamada a:


```
SystemParametersInfo(SPI_GETWHEELSCROLLLINES, 0, pulScrollLines, 0)
```



### <a name="controls-that-scroll"></a>Controles que se desplazan

En la tabla siguiente se enumeran los controles con funcionalidad de desplazamiento (incluidas las líneas de desplazamiento establecidas por el usuario). 

| Control                 | Desplazamiento                                                                                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Control de edición            | Vertical y horizontal.                                                                                                                                                |
| Control de cuadro de lista        | Vertical y horizontal.                                                                                                                                                |
| Cuadro combinado               | Cuando no se quita, cada desplazamiento recupera el elemento siguiente o anterior. Cuando se quita, cada desplazamiento reenvía el mensaje al cuadro de lista, que se desplaza en consecuencia. |
| CMD (línea de comandos)      | Vertical.                                                                                                                                                               |
| Vista de árbol               | Vertical y horizontal.                                                                                                                                                |
| Vista de lista               | Vertical y horizontal.                                                                                                                                                |
| Desplazamientos arriba/abajo         | Un elemento cada vez.                                                                                                                                                     |
| Barra de desplazamiento        | Un elemento cada vez.                                                                                                                                                     |
| Microsoft Rich Edit 1,0 | Vertical. Tenga en cuenta que el cliente de Exchange tiene sus propias versiones de los controles de vista de lista y vista de árbol que no admiten la rueda.                                        |
| Microsoft Rich Edit 2,0 | Vertical.                                                                                                                                                               |



 

### <a name="detecting-a-mouse-with-a-wheel"></a>Detección de un mouse con una rueda

Para determinar si un mouse con una rueda está conectado, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ MOUSEWHEELPRESENT**. Un valor devuelto de **true** indica que el mouse está conectado.

El ejemplo siguiente es del procedimiento de ventana de un control de edición de varias líneas:


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

Cuando el usuario hace clic en una ventana de nivel superior inactiva o en la ventana secundaria de una ventana de nivel superior inactiva, el sistema envía el mensaje de [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md) (entre otros) a la ventana secundaria o de nivel superior. El sistema envía este mensaje después de publicar el mensaje de [**\_ NCHITTEST de WM**](wm-nchittest.md) en la ventana, pero antes de publicar el mensaje de botón. Cuando se pasa **WM \_ MOUSEACTIVATE** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , el sistema activa la ventana de nivel superior y, a continuación, envía el mensaje de botón a la ventana secundaria o de nivel superior.

Al procesar [**WM \_ MOUSEACTIVATE**](wm-mouseactivate.md), una ventana puede controlar si la ventana de nivel superior se convierte en la ventana activa como resultado de un clic del mouse, y si la ventana en la que se hizo clic recibe el mensaje de botón posterior. Para ello, devuelve uno de los siguientes valores después de procesar **WM \_ MOUSEACTIVATE**.



| Value                    | Significado                                                              |
|--------------------------|----------------------------------------------------------------------|
| **\_Activar MA**         | Activa la ventana y no descarta el mensaje del mouse.         |
| **MA \_ NOactivate**       | No activa la ventana y no descarta el mensaje del mouse. |
| **\_ACTIVATEANDEAT MA**   | Activa la ventana y descarta el mensaje del mouse.                 |
| **\_NOACTIVATEANDEAT MA** | No activa la ventana, pero descarta el mensaje del mouse.         |

## <a name="see-also"></a>Vea también

[Sacar partido de High-Definition movimiento del mouse](../dxtecharts/taking-advantage-of-high-dpi-mouse-movement.md)