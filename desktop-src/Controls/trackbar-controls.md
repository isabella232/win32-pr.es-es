---
title: Acerca de los controles TrackBar
description: Una barra de desplazamiento es una ventana que contiene un control deslizante (a veces denominado control de posición) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o con las teclas de dirección, la barra de desplazamiento envía mensajes de notificación para indicar el cambio.
ms.assetid: 9fc7bef8-da1d-493b-9a9a-3770873713f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e364f57a094ed5a29369a00a112150d0282f24
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794019"
---
# <a name="about-trackbar-controls"></a>Acerca de los controles TrackBar

Una barra de desplazamiento es una ventana que contiene un control deslizante (a veces denominado control de posición) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o con las teclas de dirección, la barra de desplazamiento envía mensajes de notificación para indicar el cambio.

-   [Intervalo de selección](#selection-range)
-   [Mensajes de TrackBar](#trackbar-messages)
-   [Mensajes de notificación de TrackBar](#trackbar-notification-messages)
-   [Procesamiento de mensajes predeterminados de TrackBar](#default-trackbar-message-processing)
-   [Información sobre herramientas de TrackBar](#trackbar-tooltips)

Trackbars son útiles cuando se desea que el usuario seleccione un valor entero sin signo discreto o un conjunto de valores enteros consecutivos sin signo en un intervalo. Por ejemplo, puede usar una barra de desplazamiento para permitir al usuario establecer la frecuencia de repetición del teclado moviendo el control deslizante a una marca de graduación determinada. En la ilustración siguiente se muestra un ejemplo de TrackBar típico.

![captura de pantalla de una barra de desplazamiento con etiquetas en los extremos para una velocidad lenta y rápida](images/tkb-simple.png)

El control deslizante de una barra de desplazamiento se mueve en incrementos que se especifican cuando se crea. Los valores de este intervalo se conocen como unidades lógicas. Por ejemplo, si especifica que la barra de desplazamiento debe tener unidades lógicas que van de 0 a 5, el control deslizante puede ocupar solo seis posiciones: una posición en el lado izquierdo de la barra de desplazamiento y una posición para cada incremento del intervalo. Normalmente, cada una de estas posiciones se identifica mediante una marca de graduación; sin embargo, el número de marcas de graduación es arbitrario y puede ser menor que el número de posiciones lógicas.

Puede crear una barra de nivel mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana [**\_ clase TrackBar**](common-control-window-classes.md) . Después de crear una barra de propiedades, puede usar los mensajes de TrackBar para establecer y recuperar muchas de sus propiedades. Entre los cambios que puede realizar se incluyen establecer las posiciones mínima y máxima para el control deslizante, dibujar marcas de graduación, establecer un intervalo de selección y cambiar la posición del control deslizante.

## <a name="selection-range"></a>Intervalo de selección

Si crea un TrackBar con el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) , puede especificar un intervalo de selección. En la barra de inicio se resalta el intervalo de selección y se muestran las marcas de graduación triangular al principio y al final, tal como se muestra en la siguiente ilustración.

![captura de pantalla de una barra de presentación con un intervalo resaltado](images/tkb-selrange.png)

El intervalo de selección de la barra de presentación no afecta a su funcionalidad de ningún modo. Depende de la aplicación implementar el intervalo. Puede hacerlo de una de las siguientes maneras:

-   Use un intervalo de selección para permitir que el usuario establezca los valores máximo y mínimo de algún parámetro. Por ejemplo, el usuario puede mover el control deslizante a una posición y, a continuación, hacer clic en un botón con la etiqueta "Max". A continuación, la aplicación establece el intervalo de selección para mostrar los valores elegidos por el usuario.
-   Limite el movimiento del control deslizante a un subintervalo predeterminado dentro del control; para ello, controle la notificación de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) y no permita ningún movimiento fuera del intervalo de selección. Podría hacer esto, por ejemplo, si el intervalo de valores disponibles para el usuario puede cambiar debido a otras opciones realizadas por el usuario o de acuerdo con los recursos disponibles.

## <a name="trackbar-messages"></a>Mensajes de TrackBar

Las unidades lógicas de una barra de superpuestos son el conjunto de valores contiguos que puede representar el TrackBar. Normalmente se definen especificando el intervalo de valores posibles con un mensaje [**TBM \_ SetRange**](tbm-setrange.md) en cuanto se crea la barra de estado. Las aplicaciones pueden modificar dinámicamente el intervalo mediante **TBM \_ SetRange**, [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)o [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md).

Para recuperar la posición del control deslizante (es decir, el valor elegido por el usuario), use el mensaje [**\_ GETPOS de TBM**](tbm-getpos.md) . Para establecer la posición del control deslizante, use el mensaje [**TBM \_ SETPOS**](tbm-setpos.md) .

La barra de aumento muestra automáticamente las marcas de graduación al principio y al final, a menos que especifique el estilo [**TBS \_ noticks**](trackbar-control-styles.md) . (En el editor de recursos de Microsoft Visual Studio, esto significa establecer la propiedad marcas de graduación en false). Puede usar el estilo de marcas de graduación de [**TBS \_**](trackbar-control-styles.md) para mostrar automáticamente las marcas de graduación adicionales a intervalos regulares a lo largo de la barra de aumento. De forma predeterminada, una barra de aumento automático de TBS muestra una marca de graduación en cada incremento del intervalo de la barra de aumento. **\_** Para especificar un intervalo diferente para las marcas de graduación automáticas, envíe el mensaje [**TBM \_ SETTICFREQ**](tbm-setticfreq.md) a la barra de mensajes. Por ejemplo, podría usar este mensaje para mostrar solo 10 marcas de graduación en un intervalo de 1 a 100.

Para establecer la posición de una sola marca de graduación, envíe el mensaje [**\_ SETTIC de TBM**](tbm-settic.md) . Una barra de aumento mantiene una matriz de valores DWORD que almacena la posición de cada marca de graduación. La matriz no incluye la primera y la última marca de graduación, que la barra de aumento crea automáticamente. Puede especificar un índice en esta matriz cuando envíe el mensaje [**TBM \_ GETTIC**](tbm-gettic.md) para recuperar la posición de la marca de graduación correspondiente. Como alternativa, puede enviar el mensaje [**TBM \_ GETPTICS**](tbm-getptics.md) para recuperar un puntero a la matriz. El número de elementos de la matriz es igual a dos menos que el número de pasos devuelto por el mensaje [**\_ GETNUMTICS de TBM**](tbm-getnumtics.md) . Esto se debe a que el recuento devuelto por **TBM \_ GETNUMTICS** incluye la primera y la última marca de graduación, que no están incluidas en la matriz. Para recuperar la posición física de una marca de graduación, en coordenadas de cliente de la ventana de la barra de aumento, envíe el mensaje [**\_ GETTICPOS de TBM**](tbm-getticpos.md) . El [**mensaje \_ CLEARTICS de TBM**](tbm-cleartics.md) quita todas las marcas de graduación de la barra de paso, excepto la primera y la última.

El tamaño de línea de una barra de desplazamiento determina hasta qué punto se mueve el control deslizante en respuesta a la entrada del teclado desde las teclas de dirección, como la flecha derecha o la tecla flecha abajo. Para recuperar o establecer el tamaño de línea, envíe los mensajes [**TBM \_ GETLINESIZE**](tbm-getlinesize.md) y [**TBM \_ SETLINESIZE**](tbm-setlinesize.md) . La barra de control también envía los códigos de notificación de la \_ línea TB y TB \_ LINEDOWN a su ventana primaria cuando el usuario presiona las teclas de dirección.

El tamaño de página de una barra de seguimiento determina hasta qué punto se mueve el control deslizante en respuesta a la entrada del teclado, como la tecla RE PÁG o Av Pág, o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Para recuperar o establecer el tamaño de página, envíe los mensajes [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md) y [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md) . La barra de desplazamiento también envía los \_ códigos de notificación TB RePág y TB \_ Av Pág a su ventana primaria cuando recibe la entrada del teclado o del mouse que se desplaza por la página. Para obtener más información, vea [los mensajes de notificación de TrackBar](#trackbar-notification-messages).

Una aplicación puede enviar mensajes para recuperar las dimensiones de una barra de información. El [**mensaje \_ GETTHUMBRECT de TBM**](tbm-getthumbrect.md) recupera el rectángulo delimitador del control deslizante. El [**mensaje \_ GETTHUMBLENGTH de TBM**](tbm-getthumblength.md) recupera la longitud del control deslizante. El [**mensaje \_ GETCHANNELRECT de TBM**](tbm-getchannelrect.md) recupera el rectángulo delimitador del canal de la barra de desplazamiento, que es el área sobre la que se mueve el control deslizante. Contiene el resaltado cuando se selecciona un intervalo. Si una barra de desplazamiento tiene el estilo [**\_ FIXEDLENGTH de TBS**](trackbar-control-styles.md) , puede enviar el mensaje [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md) para cambiar la longitud del control deslizante.

Puede recuperar o establecer el intervalo de selección mediante el envío de mensajes a la barra de superpuesto. Use el [**mensaje \_ SETSEL de TBM**](tbm-setsel.md) para establecer las posiciones inicial y final de una selección. Para establecer solo la posición inicial o simplemente la posición final de una selección, envíe un mensaje [**TBM \_ SETSELSTART**](tbm-setselstart.md) o [**TBM \_ SETSELEND**](tbm-setselend.md) . Para recuperar las posiciones inicial o final de un intervalo de selección, envíe un mensaje [**TBM \_ GETSELSTART**](tbm-getselstart.md) o [**TBM \_ GETSELEND**](tbm-getselend.md) . Para borrar un intervalo de selección y restaurar el TrackBar a su intervalo original, envíe el mensaje [**\_ CLEARSEL de TBM**](tbm-clearsel.md) .

> [!Note]  
> Es responsabilidad de la aplicación asegurarse de que el usuario no puede seleccionar valores fuera del intervalo de selección. El propio control no impide que el usuario mueva el control deslizante fuera del intervalo.

 

## <a name="trackbar-notification-messages"></a>Mensajes de notificación de TrackBar

Una barra de control notifica a su ventana primaria de acciones de usuario mediante el envío de un mensaje de [**WM \_ HSCROLL**](wm-hscroll.md) o de [**\_ VSCROLL**](wm-vscroll.md) de WM. Un TrackBar con el [**estilo \_ horizontal de TBS**](trackbar-control-styles.md) envía mensajes de **WM \_ HSCROLL** . Un TrackBar con el estilo [**TBS \_ Vert**](trackbar-control-styles.md) envía mensajes de **WM \_ VSCROLL** . La palabra de orden inferior del parámetro *wParam* de **WM \_ HSCROLL** o **WM \_ VSCROLL** contiene el código de notificación. En el caso de los códigos de notificación de TB \_ THUMBPOSITION y TB \_ THUMBTRACK, la palabra de orden superior del parámetro *wParam* especifica la posición del control deslizante. En el resto de códigos de notificación, la palabra de orden superior es cero; Envíe el [**mensaje \_ GETPOS de TBM**](tbm-getpos.md) para determinar la posición del control deslizante. El parámetro *lParam* es el identificador de la barra de control.

El sistema envía los códigos de notificación de la \_ parte inferior, TB \_ LINEDOWN, TB \_ y TB de la parte superior de TB \_ solo cuando el usuario interactúa con una barra de inicio mediante el uso del teclado. Los códigos de notificación de TB \_ THUMBPOSITION y TB \_ THUMBTRACK solo se envían cuando el usuario usa el mouse. Los \_ códigos de notificación TB ENDTRACK, TB \_ Av Pág y TB \_ se envían en ambos casos. En la tabla siguiente se enumeran los códigos de notificación de TrackBar y los eventos (códigos de tecla virtual o eventos de mouse) que hacen que se envíen las notificaciones de [**clave virtual**](/windows/desktop/inputdev/virtual-key-codes).



| Código de notificación | Motivo enviado                                                                                                                     |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| TB en la \_ parte inferior        | [**final de VK \_**](/windows/desktop/inputdev/virtual-key-codes)                                                                         |
| TB \_ ENDTRACK      | [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) (el usuario liberó una clave que envió un código de tecla virtual relevante)                              |
| TB \_ LINEDOWN      | [**VK \_ RIGHT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ Down**](/windows/desktop/inputdev/virtual-key-codes)     |
| gama de TB \_        | [**VK \_ LEFT**](/windows/desktop/inputdev/virtual-key-codes) o [ **VK \_ up**](/windows/desktop/inputdev/virtual-key-codes)              |
| TB \_ Av Pág      | [**VK \_ SIGUIENTE**](/windows/desktop/inputdev/virtual-key-codes) (el usuario hizo clic en el canal siguiente o a la derecha del control deslizante)   |
| TB \_ RePág        | [**VK \_ ANTES**](/windows/desktop/inputdev/virtual-key-codes) (el usuario hizo clic en el canal por encima o a la izquierda del control deslizante) |
| TB \_ THUMBPOSITION | [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) siguiente código de \_ notificación de TB THUMBTRACK                                         |
| TB \_ THUMBTRACK    | Movimiento del control deslizante (el usuario arrastró el control deslizante)                                                                                   |
| TB en la \_ parte superior           | [**\_Página principal de VK**](/windows/desktop/inputdev/virtual-key-codes)                                                                      |



 

## <a name="default-trackbar-message-processing"></a>Procesamiento de mensajes predeterminados de TrackBar

En esta sección se describe el procesamiento de mensajes de ventana realizado por un TrackBar.



| Message                                              | Procesamiento realizado                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAPTURECHANGED de WM \_**](/windows/desktop/inputdev/wm-capturechanged) | Elimina el temporizador si se estableció uno durante el procesamiento de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) y envía el código de notificación de TB \_ THUMBPOSITION, si es necesario. Siempre envía el código de \_ notificación de TB ENDTRACK.                                     |
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)                   | Realiza la inicialización adicional, como establecer el tamaño de la línea, el tamaño de la página y la frecuencia de la marca de graduación en los valores predeterminados.                                                                                                                                 |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)                 | Libera recursos.                                                                                                                                                                                                                                         |
| [**\_habilitación de WM**](/windows/desktop/winmsg/wm-enable)                   | Vuelve a dibujar la ventana de TrackBar.                                                                                                                                                                                                                            |
| [**ERASEBKGND de WM \_**](/windows/desktop/winmsg/wm-erasebkgnd)           | Borra el fondo de la ventana, utilizando el color de fondo actual de la barra de información.                                                                                                                                                                       |
| [**GETDLGCODE de WM \_**](/windows/desktop/dlgbox/wm-getdlgcode)           | Devuelve el valor de WANTARROWS de DLGC \_ .                                                                                                                                                                                                                      |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)               | Procesa las teclas de dirección y envía los \_ códigos de notificación TB superior, TB \_ inferior, TB \_ RePág, TB \_ AvPág, TB \_ y TB \_ LINEDOWN, según corresponda.                                                                                               |
| [**KEYUP de WM \_**](/windows/desktop/inputdev/wm-keyup)                   | Envía el \_ código de notificación TB ENDTRACK si la clave era una de las claves de dirección.                                                                                                                                                                       |
| [**KILLFOCUS de WM \_**](/windows/desktop/inputdev/wm-killfocus)           | Vuelve a dibujar la ventana de TrackBar.                                                                                                                                                                                                                            |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown)       | Establece el foco y la captura del mouse en el TrackBar. Cuando es necesario, establece un temporizador que determina la rapidez con la que se mueve el control deslizante hacia el cursor del mouse cuando el usuario mantiene presionado el botón del mouse en la ventana.                                      |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)           | Libera la captura del mouse y finaliza el temporizador si se estableció una durante el procesamiento de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) . Envía el código de \_ notificación TB THUMBPOSITION, si es necesario. Siempre envía el código de \_ notificación de TB ENDTRACK. |
| [**MOUSEMOVE de WM \_**](/windows/desktop/inputdev/wm-mousemove)           | Mueve el control deslizante y envía el código de notificación de TB \_ THUMBTRACK al hacer un seguimiento del mouse (vea [**\_ temporizador de WM**](/windows/desktop/winmsg/wm-timer)).                                                                                                                          |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                        | Pinta el TrackBar. Si el parámetro wParam no es NULL, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.                                                                                                             |
| [**SETFOCUS de WM \_**](/windows/desktop/inputdev/wm-setfocus)             | Vuelve a dibujar la ventana de TrackBar.                                                                                                                                                                                                                            |
| [**tamaño de WM \_**](/windows/desktop/winmsg/wm-size)                       | Establece las dimensiones de la barra de desplazamiento, quitando el control deslizante si no hay espacio suficiente para mostrarlo.                                                                                                                                                      |
| [**temporizador de WM \_**](/windows/desktop/winmsg/wm-timer)                     | Recupera la posición del mouse y actualiza la posición del control deslizante. (Solo se recibe cuando el usuario está arrastrando el control deslizante).                                                                                                                         |
| [**WININICHANGE de WM \_**](/windows/desktop/winmsg/wm-wininichange)       | Inicializa las dimensiones del control deslizante.                                                                                                                                                                                                                           |



 

## <a name="trackbar-tooltips"></a>Información sobre herramientas de TrackBar

Una barra de control que se crea con el estilo de [**\_ información sobre herramientas de TBS**](trackbar-control-styles.md) tiene un control ToolTip predeterminado. La información sobre herramientas permanece visible y muestra el valor actual cuando el usuario arrastra el control deslizante con el mouse.

Puede asignar un nuevo control ToolTip a una barra de herramientas mediante el envío del mensaje [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md) . Para recuperar el identificador de un control de información sobre herramientas asignado, use el mensaje [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md) .

 

 