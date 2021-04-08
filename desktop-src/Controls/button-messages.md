---
title: 'Mensajes de botón '
description: Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103796683"
---
# <a name="button-messages"></a>Mensajes de botón 

Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.

Los temas siguientes se describen en esta sección.

-   [Envío de mensajes a botones](#sending-messages-to-buttons)
-   [Control de mensajes desde un botón](#handling-messages-from-a-button)
-   [Mensajes de notificación de los botones](#notification-messages-from-buttons)
-   [Mensajes de color de botón](#button-color-messages)
-   [Procesamiento de mensajes predeterminado del botón](#button-default-message-processing)
-   [Temas relacionados](#related-topics)

## <a name="sending-messages-to-buttons"></a>Envío de mensajes a botones

Una ventana primaria puede enviar mensajes a un botón de una ventana superpuesta o secundaria mediante la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , o bien puede enviar mensajes a un botón de un cuadro de diálogo mediante las funciones [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)y [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

Una aplicación puede usar el [**mensaje \_ GETCHECK de BM**](bm-getcheck.md) para recuperar el estado de activación de una casilla o un botón de radio. Una aplicación también puede usar el [**mensaje \_ GETSTATE de BM**](bm-getstate.md) para recuperar los Estados actuales del botón (el estado de activación, el estado de inserción y el estado de foco). Para obtener información acerca de un estado específico, use una máscara de máscara en el valor de estado devuelto.

El mensaje [**BM \_ SETCHECK**](bm-setcheck.md) establece el estado de activación de una casilla o un botón de opción; el mensaje devuelve cero. El mensaje de [**BM \_ SETSTATE**](bm-setstate.md) establece el estado de la extracción de un botón; este mensaje también devuelve cero. El [**mensaje \_ SETSTYLE de BM**](bm-setstyle.md) cambia el estilo de un botón. Está diseñado para cambiar los estilos de botón dentro de un tipo (por ejemplo, si se cambia una casilla a una casilla automática). No está diseñado para cambiar entre tipos (por ejemplo, al cambiar una casilla a un botón de radio). Una aplicación no debe cambiar un botón de un tipo a otro.

Un botón del estilo de [**\_ icono**](button-styles.md) de [**mapa de \_ bits BS**](button-styles.md) o BS muestra un mapa de bits o un icono en lugar de texto. El mensaje de el [**\_ SETIMAGE de BM**](bm-setimage.md) asocia un identificador a un mapa de bits o un icono con un botón. El [**mensaje \_ BM de BM**](bm-getimage.md) recupera un identificador para el mapa de bits o el icono asociado a un botón.

Una aplicación también puede usar el mensaje [**DM _ \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) para recuperar el identificador del control de botón de opción predeterminado en un cuadro de diálogo. Una aplicación puede usar el mensaje [**DM _ \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) para establecer el botón de opción predeterminado para un cuadro de diálogo.

Llamar a la función [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) o [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) es equivalente a enviar un mensaje de [**\_ SETCHECK de BM**](bm-setcheck.md) . Llamar a la función [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) es equivalente a enviar un mensaje de [**BM \_ GETCHECK**](bm-getcheck.md) .

## <a name="handling-messages-from-a-button"></a>Control de mensajes desde un botón

Las notificaciones de un botón se envían como [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) o como mensajes de [**\_ notificación de WM**](wm-notify.md) . Puede encontrar información sobre qué mensaje se usa en la página de referencia de cada notificación.

Para obtener más información sobre cómo controlar los mensajes, vea [control de mensajes](control-messages.md). Vea también mensajes de botón.

## <a name="notification-messages-from-buttons"></a>Mensajes de notificación de los botones

Cuando el usuario hace clic en un botón, su estado cambia y el botón envía códigos de notificación, en forma de mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) , a su ventana primaria. Por ejemplo, un control de botón de opción envía el código de notificación en el que se [ \_ hace clic en el BN](bn-clicked.md) cada vez que el usuario elige el botón. En todos los casos (excepto [para BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), la palabra de orden inferior del parámetro *wParam* contiene el identificador de control, la palabra de orden superior de *wParam* contiene el código de notificación y el parámetro *lParam* contiene el identificador de la ventana de control.

Tanto el mensaje como la respuesta de la ventana primaria dependen del tipo, el estilo y el estado actual del botón. A continuación se muestran los códigos de notificación de botón que una aplicación debe supervisar y procesar.



| Código de notificación                                                        | Descripción                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | El mouse entró o quedó en el área cliente de un botón. |
| [BN \_ clic](bn-clicked.md)                                            | El usuario hizo clic en un botón.                             |
| [BN \_ DBLCLK](bn-dblclk.md) o [BN \_ ](bn-doubleclicked.md) | El usuario hizo doble clic en un botón.                      |
| [Deshabilitación de BN \_](bn-disable.md)                                            | Un botón está deshabilitado.                                  |
| [BN \_ Push](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)               | El usuario insertó un botón.                              |
| [BN \_ KILLFOCUS](bn-killfocus.md)                                        | El botón perdió el foco de teclado.                    |
| [BN \_ Paint](bn-paint.md)                                                | Se debe pintar el botón.                          |
| [BN ( \_ SETFOCUS)](bn-setfocus.md)                                          | El botón obtuvo el foco de teclado.                  |
| [BN \_ Uninserted](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)       | El botón ya no se inserta.                        |



 

Un botón envía los códigos de notificación [BN \_ Disable](bn-disable.md), [BN \_ Push](bn-pushed.md), [BN \_ KILLFOCUS](bn-killfocus.md), [BN \_ Paint](bn-paint.md), [BN \_ SETFOCUS](bn-setfocus.md)y [BN \_ unpushd](bn-unpushed.md) solo si tiene el estilo [**BS \_ Notify**](button-styles.md) . [BN \_](bn-dblclk.md) Los códigos de notificación de DBLCLK se envían de forma automática para los botones [**BS \_ USERBUTTON**](button-styles.md) [**, \_ y**](button-styles.md) [**BS \_ OWNERDRAW**](button-styles.md) . Otros tipos de botón envían BN \_ DBLCLK solo si tienen el estilo de **\_ notificación de BS** . Todos los botones envían el código de notificación en el que se [ \_ hace clic](bn-clicked.md) con el BN, independientemente de sus estilos de botón.

En el caso de los botones automáticos, el sistema cambia el estado de la extracción y pinta el botón. En este caso, la aplicación normalmente solo procesa los códigos de notificación [BN \_ clic](bn-clicked.md) y [BN \_ DBLCLK](bn-dblclk.md) . En el caso de los botones que no son automáticos, la aplicación normalmente responde al código de notificación mediante el envío de un mensaje para cambiar el estado del botón. Para obtener información sobre el envío de mensajes a botones, consulte [envío de mensajes a botones](#sending-messages-to-buttons).

Cuando el usuario selecciona un botón dibujado por el propietario, el botón envía a su ventana primaria un mensaje de [**WM \_ DRAWITEM**](wm-drawitem.md) que contiene el identificador del control que se va a dibujar e información sobre sus dimensiones y estado.

## <a name="button-color-messages"></a>Mensajes de color de botón

El sistema proporciona los valores de color predeterminados para los botones. Una aplicación puede recuperar los valores predeterminados de estos colores mediante una llamada a la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o establecer los valores mediante una llamada a la función [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) . En la tabla siguiente se muestran los valores predeterminados de color de botón.



| Value               | Elemento coloreado                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| COLOR \_ BTNFACE      | Caras del botón.                                                                                                              |
| COLOR \_ BTNHIGHLIGHT | Área de resaltado (los bordes superior e izquierdo) de un botón.                                                                       |
| COLOR \_ BTNSHADOW    | Área de sombra (bordes inferior y derecho) de un botón.                                                                      |
| COLOR \_ BTNTEXT      | Texto normal (no gris) en botones.                                                                                       |
| COLOR \_ GRAYTEXT     | Texto deshabilitado (gris) en botones. Este color se establece en 0 si el controlador de pantalla actual no admite un color gris sólido. |
| ventana de COLOR \_       | Fondo de las ventanas.                                                                                                        |
| COLOR \_ WINDOWFRAME  | Marcos de ventana.                                                                                                             |
| COLOR \_ WINDOWTEXT   | Texto en Windows.                                                                                                           |



 

Sin embargo, la llamada a [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) afecta a todas las aplicaciones, por lo que no debe llamar a esta función para personalizar los botones de la aplicación.

El sistema envía un mensaje de [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) a la ventana primaria de un botón antes de dibujar un botón. Este mensaje contiene un identificador para el contexto de dispositivo del botón y un identificador de la ventana secundaria. La ventana primaria puede usar estos manipuladores para cambiar el texto del botón y los colores de fondo. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa el mensaje.

## <a name="button-default-message-processing"></a>Procesamiento de mensajes predeterminado del botón

El procedimiento de ventana de la clase de ventana de control de botón predefinido lleva a cabo el procesamiento predeterminado para todos los mensajes que no procesa el procedimiento de control de botón. Cuando el procedimiento de control de botón devuelve **false** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y realiza las acciones predeterminadas que se muestran en la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Message</th>
<th>Acción predeterminada</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Envía el botón un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> y un mensaje de <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> y envía a la ventana primaria un código de notificación de <a href="bn-clicked.md">BN_CLICKED</a> .</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Devuelve el estado de activación del botón.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Devuelve un identificador para el mapa de bits o el icono asociado al botón o <strong>null</strong> si el botón no tiene ningún mapa de bits o icono.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Devuelve el estado de activación actual, el estado de inserción y el estado de foco del botón.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Establece el estado de activación para todos los estilos de botones de radio y casillas. Si el parámetro <em>wParam</em> es mayor que cero para los botones de radio, al botón se le asigna el estilo <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Asocia el identificador de mapa de bits o icono especificado con el botón y devuelve un identificador al mapa de bits o icono anterior.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Establece el estado de la inserciones del botón. En el caso de los botones dibujados por el propietario, se envía un mensaje <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> a la ventana primaria si ha cambiado el estado del botón.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Establece el estilo del botón. Si la palabra de orden inferior del parámetro <em>lParam</em> es <strong>true</strong>, el botón vuelve a dibujarse.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Activa una casilla o una casilla automática cuando el usuario presiona las teclas más (+) o igual (=). Desactiva una casilla de verificación o automática cuando el usuario presiona la tecla menos (–).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Pinta el botón.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Borra el fondo de los botones dibujados por el propietario. Los fondos de otros botones se borran como parte de la <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> y <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> el procesamiento.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Devuelve valores que indican el tipo de entrada que procesa el procedimiento de botón predeterminado, tal como se muestra en la tabla siguiente. 
<table>
<thead>
<tr class="header">
<th>Estilo de botón</th>
<th>Devoluciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Devuelve un identificador de la fuente actual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Empuja el botón si el usuario presiona la barra ESPACIAdora.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Libera la captura del mouse para todos los casos excepto la tecla TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Quita el rectángulo de foco de un botón. En el caso de los botones de opción y los botones de preinstalación predeterminados, se invalida el rectángulo de foco. Si el botón tiene la captura del mouse, se libera la captura, no se hace clic en el botón y se quita cualquier estado de la extracción.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Envía un código de notificación de <a href="bn-dblclk.md">BN_DBLCLK</a> a la ventana primaria de los botones de radio y los botones dibujados por el propietario. Para otros botones, un doble clic se procesa como un mensaje de <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Resalta el botón si la posición del cursor del mouse está dentro del rectángulo cliente del botón.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Libera la captura del mouse si el botón tenía la captura del mouse.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Realiza la misma acción que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, si el botón tiene la captura del mouse. De lo contrario, no se realiza ninguna acción.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Convierte cualquier botón de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> en un botón de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Devuelve HTTRANSPARENT si el control de botón es un cuadro de grupo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Dibuja el botón según su estilo y su estado actual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Dibuja un rectángulo de foco en el botón que obtiene el foco. En los botones de radio y los botones de radio automáticos, se envía una <a href="bn-clicked.md">BN_CLICKED</a> código de notificación a la ventana primaria.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Establece una nueva fuente y, opcionalmente, actualiza la ventana.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Establece el texto del botón. En el caso de un cuadro de grupo, el mensaje pinta sobre el texto preexistente antes de volver a pintar el cuadro de grupo con el nuevo texto.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Libera la captura del mouse para todos los casos excepto la tecla TAB.</td>
</tr>
</tbody>
</table>



 

El procedimiento de ventana predefinido pasa todos los demás mensajes a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de control](control-messages.md)
</dt> </dl>

 

 