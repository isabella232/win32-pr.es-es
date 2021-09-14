---
title: Acerca de los controles trackbar
description: Una barra de seguimiento es una ventana que contiene un control deslizante (a veces denominado control de posición) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o las teclas de dirección, la barra de seguimiento envía mensajes de notificación para indicar el cambio.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165978"
---
# <a name="about-trackbar-controls"></a>Acerca de los controles trackbar

Una barra de seguimiento es una ventana que contiene un control deslizante (a veces denominado control de posición) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o las teclas de dirección, la barra de seguimiento envía mensajes de notificación para indicar el cambio.

-   [Intervalo de selección](#selection-range)
-   [Mensajes de la barra de seguimiento](#trackbar-messages)
-   [Mensajes de notificación de la barra de seguimiento](#trackbar-notification-messages)
-   [Procesamiento de mensajes de la barra de seguimiento predeterminada](#default-trackbar-message-processing)
-   [Información sobre herramientas de la barra de seguimiento](#trackbar-tooltips)

Las barras de seguimiento son útiles cuando se desea que el usuario seleccione un valor entero discreto sin signo o un conjunto de valores enteros consecutivos sin signo en un intervalo. Por ejemplo, puede usar una barra de seguimiento para permitir al usuario establecer la velocidad de repetición del teclado moviendo el control deslizante a una marca de graduación determinada. En la ilustración siguiente se muestra una barra de seguimiento típica.

![captura de pantalla de una barra de seguimiento con etiquetas en los extremos para lento y rápido](images/tkb-simple.png)

El control deslizante de una barra de seguimiento se mueve en incrementos que se especifican al crearlo. Los valores de este intervalo se conocen como unidades lógicas. Por ejemplo, si especifica que la barra de seguimiento debe tener unidades lógicas que van de 0 a 5, el control deslizante solo puede ocupar seis posiciones: una posición en el lado izquierdo de la barra de seguimiento y una posición para cada incremento del intervalo. Normalmente, cada una de estas posiciones se identifica mediante una marca de graduación. sin embargo, el número de marcas de graduación es arbitrario y puede ser menor que el número de posiciones lógicas.

Para crear una barra de seguimiento, use [**la función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique la [**clase de ventana TRACKBAR \_ CLASS.**](common-control-window-classes.md) Después de crear una barra de seguimiento, puede usar los mensajes de la barra de seguimiento para establecer y recuperar muchas de sus propiedades. Los cambios que puede realizar incluyen establecer las posiciones mínima y máxima del control deslizante, dibujar marcas de graduación, establecer un intervalo de selección y cambiar la posición del control deslizante.

## <a name="selection-range"></a>Intervalo de selección

Si crea una barra de seguimiento con el [**estilo TBS \_ ENABLESELRANGE,**](trackbar-control-styles.md) puede especificar un intervalo de selección. La barra de seguimiento resalta el intervalo de selección y muestra marcas de graduación triangulares al principio y al final, como se muestra en la ilustración siguiente.

![captura de pantalla de una barra de seguimiento con un intervalo resaltado](images/tkb-selrange.png)

El intervalo de selección de la barra de seguimiento no afecta a su funcionalidad de ninguna manera. Es la aplicación la que debe implementar el intervalo. Puede hacerlo de una de las maneras siguientes:

-   Use un intervalo de selección para permitir que el usuario establezca los valores máximo y mínimo para algún parámetro. Por ejemplo, el usuario podría mover el control deslizante a una posición y, a continuación, hacer clic en un botón con la etiqueta "Max". A continuación, la aplicación establece el intervalo de selección para mostrar los valores elegidos por el usuario.
-   Limite el movimiento del control deslizante a un subrango predeterminado dentro del control, controlando la notificación [**\_ WM HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) y dis permitiendo cualquier movimiento fuera del intervalo de selección. Puede hacerlo, por ejemplo, si el intervalo de valores disponibles para el usuario puede cambiar debido a otras opciones que ha tomado el usuario o según los recursos disponibles.

## <a name="trackbar-messages"></a>Mensajes de la barra de seguimiento

Las unidades lógicas de una barra de seguimiento son el conjunto de valores contiguos que la barra de seguimiento puede representar. Normalmente se definen especificando el intervalo de valores posibles con un mensaje [**\_ TBM SETRANGE**](tbm-setrange.md) en cuanto se crea la barra de seguimiento. Las aplicaciones pueden modificar dinámicamente el intervalo mediante **TBM \_ SETRANGE,** [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)o [**TBM \_ SETRANGEMIN.**](tbm-setrangemin.md)

Para recuperar la posición del control deslizante (es decir, el valor elegido por el usuario), use el [**mensaje \_ GETPOS de TBM.**](tbm-getpos.md) Para establecer la posición del control deslizante, use el [**mensaje \_ TBM SETPOS.**](tbm-setpos.md)

Una barra de seguimiento muestra automáticamente las marcas de graduación al principio y al final, a menos que especifique [**el estilo \_ NOTICKS de TBS.**](trackbar-control-styles.md) (En el editor Microsoft Visual Studio recursos, esto significa establecer la propiedad Marcas de graduación en False). Puede usar el estilo [**\_ TBS AUTOTICKS**](trackbar-control-styles.md) para mostrar automáticamente marcas de graduación adicionales a intervalos regulares a lo largo de la barra de seguimiento. De forma predeterminada, una barra de **seguimiento \_ DE TBS AUTOTICKS** muestra una marca de paso en cada incremento del intervalo de la barra de seguimiento. Para especificar un intervalo diferente para las marcas de graduación automáticas, envíe el [**mensaje \_ TBM SETTICFREQ**](tbm-setticfreq.md) a la barra de seguimiento. Por ejemplo, podría usar este mensaje para mostrar solo 10 marcas de graduación en un intervalo de 1 a 100.

Para establecer la posición de una sola marca de graduación, envíe el [**mensaje TBM \_ SETTIC.**](tbm-settic.md) Una barra de seguimiento mantiene una matriz de valores DWORD que almacena la posición de cada marca de graduación. La matriz no incluye las marcas de graduación primera y última, que la barra de seguimiento crea automáticamente. Puede especificar un índice en esta matriz al enviar el mensaje [**\_ GETTIC**](tbm-gettic.md) de TBM para recuperar la posición de la marca de graduación correspondiente. Como alternativa, puede enviar el mensaje [**\_ GETPTICS**](tbm-getptics.md) de TBM para recuperar un puntero a la matriz. El número de elementos de la matriz es igual a dos menos que el número de tics devuelto por el [**mensaje \_ GETNUMTICS de TBM.**](tbm-getnumtics.md) Esto se debe a que el recuento devuelto por **TBM \_ GETNUMTICS** incluye las marcas de graduación primera y última, que no se incluyen en la matriz. Para recuperar la posición física de una marca de graduación, en coordenadas de cliente de la ventana de la barra de seguimiento, envíe el [**mensaje \_ GETTICPOS de TBM.**](tbm-getticpos.md) El [**mensaje \_ CLEARTICS de TBM**](tbm-cleartics.md) quita todas las marcas de graduación de una barra de seguimiento, menos la primera y la última.

El tamaño de línea de una barra de seguimiento determina hasta qué punto se mueve el control deslizante en respuesta a la entrada del teclado desde las teclas de dirección, como la tecla FLECHA DERECHA o FLECHA ABAJO. Para recuperar o establecer el tamaño de línea, envíe los [**mensajes \_ TBM GETLINESIZE**](tbm-getlinesize.md) y [**TBM \_ SETLINESIZE.**](tbm-setlinesize.md) La barra de seguimiento también envía los códigos de notificación LINEUP y TB LINEDOWN a su ventana primaria cuando el usuario \_ presiona las teclas de \_ dirección.

El tamaño de página de una barra de seguimiento determina hasta qué punto se mueve el control deslizante en respuesta a la entrada del teclado, como la tecla PAGE UP o PAGE DOWN, o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Para recuperar o establecer el tamaño de página, envíe los [**mensajes \_ TBM GETPAGESIZE**](tbm-getpagesize.md) y [**TBM \_ SETPAGESIZE.**](tbm-setpagesize.md) La barra de seguimiento también envía los códigos de notificación PAGEUP y TB PAGEDOWN a su ventana primaria cuando recibe la entrada del teclado o del mouse que \_ se desplaza por la \_ página. Para obtener más información, vea [Trackbar Notification Messages](#trackbar-notification-messages).

Una aplicación puede enviar mensajes para recuperar las dimensiones de una barra de seguimiento. El [**mensaje \_ GETTHUMBRECT de TBM**](tbm-getthumbrect.md) recupera el rectángulo delimitador del control deslizante. El [**mensaje \_ GETTHUMBLENGTH de TBM**](tbm-getthumblength.md) recupera la longitud del control deslizante. El [**mensaje \_ GETCHANNELRECT**](tbm-getchannelrect.md) de TBM recupera el rectángulo delimitador del canal de la barra de seguimiento, que es el área sobre la que se mueve el control deslizante. Contiene el resaltado cuando se selecciona un intervalo. Si una barra de seguimiento tiene el estilo [**\_ FIXEDLENGTH de TBS,**](trackbar-control-styles.md) puede enviar el mensaje [**\_ TBM SETTHUMBLENGTH**](tbm-setthumblength.md) para cambiar la longitud del control deslizante.

Para recuperar o establecer el intervalo de selección, envíe mensajes a la barra de seguimiento. Use el [**mensaje TBM \_ SETSEL**](tbm-setsel.md) para establecer las posiciones inicial y final de una selección. Para establecer solo la posición inicial o simplemente la posición final de una selección, envíe un mensaje [**TBM \_ SETSELSTART**](tbm-setselstart.md) o [**TBM \_ SETSELEND.**](tbm-setselend.md) Para recuperar las posiciones inicial o final de un intervalo de selección, envíe un [**mensaje TBM \_ GETSELSTART**](tbm-getselstart.md) o [**TBM \_ GETSELEND.**](tbm-getselend.md) Para borrar un intervalo de selección y restaurar la barra de seguimiento a su intervalo original, envíe el [**mensaje \_ CLEARSEL de TBM.**](tbm-clearsel.md)

> [!Note]  
> Es responsabilidad de la aplicación asegurarse de que el usuario no puede seleccionar valores fuera del intervalo de selección. El propio control no impide que el usuario mueva el control deslizante fuera del intervalo.

 

## <a name="trackbar-notification-messages"></a>Mensajes de notificación de la barra de seguimiento

Una barra de seguimiento notifica a su ventana primaria las acciones del usuario enviando al elemento primario un mensaje [**\_ VSCROLL**](wm-vscroll.md) de [**WM O \_ HSCROLL**](wm-hscroll.md) o WM. Una barra de seguimiento con el [**estilo \_ TBS HORZ**](trackbar-control-styles.md) envía **mensajes WM \_ HSCROLL.** Una barra de seguimiento con el [**estilo \_ VERT de TBS**](trackbar-control-styles.md) envía **mensajes \_ VSCROLL de WM.** La palabra de orden bajo del *parámetro wParam* de **WM \_ HSCROLL** o **WM \_ VSCROLL** contiene el código de notificación. Para los códigos de notificación TB THUMBPOSITION y TB THUMBTRACK, la palabra de orden superior del parámetro \_ \_ *wParam* especifica la posición del control deslizante. Para todos los demás códigos de notificación, la palabra de orden superior es cero; envíe el [**mensaje \_ GETPOS de TBM**](tbm-getpos.md) para determinar la posición del control deslizante. El *parámetro lParam* es el identificador de la barra de seguimiento.

El sistema envía los códigos de notificación \_ TB BOTTOM, TB LINEDOWN, TB LINEUP y TB TOP solo cuando el usuario interactúa con una barra de seguimiento \_ \_ mediante el \_ teclado. Los códigos de notificación TB THUMBPOSITION y TB THUMBTRACK solo se envían \_ cuando el usuario usa el \_ mouse. Los códigos de \_ notificación TB ENDTRACK, TB PAGEDOWN y \_ \_ TB PAGEUP se envían en ambos casos. En la tabla siguiente se enumeran los códigos de notificación de la [](/windows/desktop/inputdev/virtual-key-codes)barra de seguimiento y los eventos (códigos de clave virtual o eventos del mouse) que hacen que se envíen las notificaciones de códigos de clave virtual.



| Código de notificación | Motivo enviado                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB \_ INFERIOR        | [**VK \_ END**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (el usuario publicó una clave que envió un código de clave virtual pertinente)                              |
| LÍNEA \_ DE TB      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ DOWN**](/windows/desktop/inputdev/virtual-key-codes)     |
| ALINEACIÓN \_ DE TB        | [**VK \_ LEFT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ UP**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ PAGEDOWN      | [**VK \_ NEXT**](/windows/desktop/inputdev/virtual-key-codes) (el usuario hizo clic en el canal siguiente o a la derecha del control deslizante)   |
| PAGEUP \_ de TB        | [**VK \_ PRIOR**](/windows/desktop/inputdev/virtual-key-codes) (el usuario hizo clic en el canal anterior o a la izquierda del control deslizante) |
| TB \_ THUMBPOSITION | [**WM \_ LBUTTONUP después de**](/windows/desktop/inputdev/wm-lbuttonup) un código de notificación \_ THUMBTRACK de TB                                         |
| TB \_ THUMBTRACK    | Movimiento del control deslizante (el usuario arrastró el control deslizante)                                                                                   |
| TB \_ TOP           | [**VK \_ HOME**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Procesamiento de mensajes de la barra de seguimiento predeterminada

En esta sección se describe el procesamiento de mensajes de ventana realizado por una barra de seguimiento.



| Message                                              | Procesamiento realizado                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAPTURECHANGED**](/windows/desktop/inputdev/wm-capturechanged) | Elimina el temporizador si se estableció uno durante el procesamiento [**de WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y envía el código de notificación THUMBPOSITION de \_ TB, si es necesario. Siempre envía el código de notificación \_ ENDTRACK de TB.                                     |
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)                   | Realiza una inicialización adicional, como establecer el tamaño de línea, el tamaño de página y la frecuencia de marca de graduación en los valores predeterminados.                                                                                                                                 |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)                 | Libera recursos.                                                                                                                                                                                                                                         |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)                   | Vuelve a dibujar la ventana de la barra de seguimiento.                                                                                                                                                                                                                            |
| [**WM \_ ERASEBNDAND**](/windows/desktop/winmsg/wm-erasebkgnd)           | Borra el fondo de la ventana con el color de fondo actual de la barra de seguimiento.                                                                                                                                                                       |
| [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode)           | Devuelve el valor \_ WANTARROWS de DLGC.                                                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)               | Procesa las claves de dirección y envía los códigos de notificación \_ TB TOP, TB \_ BOTTOM, TB \_ PAGEUP, TB \_ PAGEDOWN, TB LINEUP y \_ TB \_ LINEDOWN, según corresponda.                                                                                               |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)                   | Envía el código de notificación ENDTRACK de TB \_ si la clave era una de las claves de dirección.                                                                                                                                                                       |
| [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus)           | Vuelve a dibujar la ventana de la barra de seguimiento.                                                                                                                                                                                                                            |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)       | Establece el foco y la captura del mouse en la barra de seguimiento. Cuando sea necesario, establece un temporizador que determina la rapidez con la que el control deslizante se mueve hacia el cursor del mouse cuando el usuario mantiene presionado el botón del mouse en la ventana.                                      |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera la captura del mouse y finaliza el temporizador si se estableció uno durante el [**procesamiento \_ de WM LBUTTONDOWN.**](/windows/desktop/inputdev/wm-lbuttondown) Envía el código de notificación \_ THUMBPOSITION de TB, si es necesario. Siempre envía el código de notificación \_ ENDTRACK de TB. |
| [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove)           | Mueve el control deslizante y envía el código de notificación THUMBTRACK de TB \_ al realizar el seguimiento del mouse (vea WM [**\_ TIMER**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                        | Pinta la barra de seguimiento. Si el parámetro wParam no es NULL, el control asume que el valor es un HDC y pinta con ese contexto de dispositivo.                                                                                                             |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)             | Vuelve a dibujar la ventana de la barra de seguimiento.                                                                                                                                                                                                                            |
| [**TAMAÑO \_ WM**](/windows/desktop/winmsg/wm-size)                       | Establece las dimensiones de la barra de seguimiento, quitando el control deslizante si no hay espacio suficiente para mostrarlo.                                                                                                                                                      |
| [**TEMPORIZADOR \_ WM**](/windows/desktop/winmsg/wm-timer)                     | Recupera la posición del mouse y actualiza la posición del control deslizante. (Solo se recibe cuando el usuario arrastra el control deslizante).                                                                                                                         |
| [**WM \_ WININICHANGE**](/windows/desktop/winmsg/wm-wininichange)       | Inicializa las dimensiones del control deslizante.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Información sobre herramientas de la barra de seguimiento

Una barra de seguimiento que se crea con el estilo [**TBS \_ TOOLTIPS**](trackbar-control-styles.md) tiene un control de información sobre herramientas predeterminado. La información sobre herramientas permanece visible y muestra el valor actual a medida que el usuario arrastra el control deslizante con el mouse.

Puede asignar un nuevo control de información sobre herramientas a una barra de seguimiento mediante el envío del [**mensaje \_ SETTOOLTIPS de TBM.**](tbm-settooltips.md) Para recuperar el identificador de un control de información sobre herramientas asignado, use el [**mensaje \_ GETTOOLTIPS de TBM.**](tbm-gettooltips.md)

 

 