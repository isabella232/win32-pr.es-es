---
title: 'Mensajes de botón '
description: Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136310a3718f17900f604287bf78186f7c927259
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625721"
---
# <a name="button-messages"></a>Mensajes de botón 

Un botón puede enviar mensajes a su ventana primaria y una ventana primaria puede enviar mensajes a un botón.

En esta sección se tratan los temas siguientes.

-   [Envío de mensajes a botones](#sending-messages-to-buttons)
-   [Controlar mensajes desde un botón](#handling-messages-from-a-button)
-   [Mensajes de notificación de botones](#notification-messages-from-buttons)
-   [Mensajes de color de botón](#button-color-messages)
-   [Procesamiento de mensajes predeterminado de botón](#button-default-message-processing)
-   [Temas relacionados](#related-topics)

## <a name="sending-messages-to-buttons"></a>Envío de mensajes a botones

Una ventana primaria puede enviar mensajes a un botón en una ventana superpuesta o secundaria mediante la función [**SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o bien puede enviar mensajes a un botón de un cuadro de diálogo mediante las funciones [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton,**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

Una aplicación puede usar el mensaje [**\_ BM GETCHECK**](bm-getcheck.md) para recuperar el estado de comprobación de una casilla o un botón de radio. Una aplicación también puede usar el mensaje [**\_ GETSTATE**](bm-getstate.md) de BM para recuperar los estados actuales del botón (el estado de comprobación, el estado de inserción y el estado de foco). Para obtener información sobre un estado específico, use una máscara de bits en el valor de estado devuelto.

El [**mensaje \_ BM SETCHECK**](bm-setcheck.md) establece el estado de comprobación de una casilla o un botón de radio; el mensaje devuelve cero. El [**mensaje \_ BM SETSTATE**](bm-setstate.md) establece el estado de inserción de un botón; este mensaje también devuelve cero. El [**mensaje \_ BM SETSTYLE**](bm-setstyle.md) cambia el estilo de un botón. Está diseñado para cambiar los estilos de botón dentro de un tipo (por ejemplo, cambiar una casilla a una casilla automática). No está diseñado para cambiar entre tipos (por ejemplo, cambiar una casilla a un botón de radio). Una aplicación no debe cambiar un botón de un tipo a otro.

Un botón del estilo [**BS \_ BITMAP o**](button-styles.md) [**BS \_ ICON**](button-styles.md) muestra un mapa de bits o un icono en lugar de texto. El [**mensaje \_ BM SETIMAGE**](bm-setimage.md) asocia un identificador a un mapa de bits o un icono con un botón. El [**mensaje \_ BM GETIMAGE**](bm-getimage.md) recupera un identificador para el mapa de bits o el icono asociado a un botón.

Una aplicación también puede usar el mensaje [**\_ DM GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) para recuperar el identificador del control de botón de inserción predeterminado en un cuadro de diálogo. Una aplicación puede usar el mensaje [**\_ DM SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) para establecer el botón de inserción predeterminado para un cuadro de diálogo.

Llamar a [**la función CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) [**o CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) equivale a enviar un [**mensaje DE BM \_ SETCHECK.**](bm-setcheck.md) Llamar a [**la función IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) equivale a enviar un [**mensaje \_ GETCHECK de BM.**](bm-getcheck.md)

## <a name="handling-messages-from-a-button"></a>Controlar mensajes desde un botón

Las notificaciones de un botón se envían como mensajes [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) o [**WM \_ NOTIFY.**](wm-notify.md) Puede encontrar información sobre qué mensaje se usa en la página de referencia de cada notificación.

Para obtener más información sobre cómo controlar los mensajes, vea [Controlar mensajes](control-messages.md). Consulte también Mensajes de botón.

## <a name="notification-messages-from-buttons"></a>Mensajes de notificación de botones

Cuando el usuario hace clic en un botón, su estado cambia y el botón envía códigos de notificación, en forma de mensajes [**WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) a su ventana primaria. Por ejemplo, un control de botón de inserción envía el código [de notificación \_ CLICKED](bn-clicked.md) de BN cada vez que el usuario elige el botón. En todos los casos (excepto [para BCN \_ HOTITEMCHANGE),](bcn-hotitemchange.md)la palabra de orden bajo del parámetro *wParam* contiene el identificador de control, la palabra de orden superior *de wParam* contiene el código de notificación y el parámetro *lParam* contiene el identificador de la ventana de control.

Tanto el mensaje como la respuesta de la ventana primaria dependen del tipo, el estilo y el estado actual del botón. A continuación se muestra el botón de códigos de notificación que una aplicación debe supervisar y procesar.



| Código de notificación                                                        | Descripción                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | El mouse entró o salió del área de cliente de un botón. |
| [BN \_ CLICKED](bn-clicked.md)                                            | El usuario hizo clic en un botón.                             |
| [BN \_ DBLCLK](bn-dblclk.md) o [BN \_ DOUBLECLICKED](bn-doubleclicked.md) | El usuario hizo doble clic en un botón.                      |
| [BN \_ DISABLE](bn-disable.md)                                            | Un botón está deshabilitado.                                  |
| [BN \_ PUSHED](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)               | El usuario ha presionado un botón.                              |
| [KILLFOCUS de BN \_](bn-killfocus.md)                                        | El botón perdió el foco del teclado.                    |
| [BN \_ PAINT](bn-paint.md)                                                | El botón debe pintarse.                          |
| [BN \_ SETFOCUS](bn-setfocus.md)                                          | El botón obtuvo el foco del teclado.                  |
| [BN \_ UNPUSHED](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)       | El botón ya no se inserta.                        |



 

Un botón envía los códigos de [notificación BN \_ DISABLE](bn-disable.md), [BN \_ PUSHED,](bn-pushed.md) [BN \_ KILLFOCUS,](bn-killfocus.md) [BN \_ PAINT,](bn-paint.md) [BN \_ SETFOCUS](bn-setfocus.md)y [BN \_ UNPUSHED](bn-unpushed.md) solo si tiene el estilo NOTIFY de [**BS. \_**](button-styles.md) [BN \_ Los códigos de notificación DBLCLK](bn-dblclk.md) se envían automáticamente para los [**botones \_ BS USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)y [**BS \_ OWNERDRAW.**](button-styles.md) Otros tipos de botón envían \_ DBLCLK de BN solo si tienen el **estilo \_ BS NOTIFY.** Todos los botones envían el [código de notificación \_ CLICKED](bn-clicked.md) de BN independientemente de sus estilos de botón.

En el caso de los botones automáticos, el sistema cambia el estado de inserción y pinta el botón. En este caso, la aplicación normalmente procesa solo los códigos de notificación [ \_ BN CLICKED](bn-clicked.md) y [ \_ BN DBLCLK.](bn-dblclk.md) Para los botones que no son automáticos, la aplicación normalmente responde al código de notificación enviando un mensaje para cambiar el estado del botón. Para obtener información sobre el envío de mensajes a botones, vea [Enviar mensajes a botones.](#sending-messages-to-buttons)

Cuando el usuario selecciona un botón dibujado por el propietario, el botón envía a su ventana primaria un mensaje [**\_ DRAWITEM de WM**](wm-drawitem.md) que contiene el identificador del control que se va a dibujar e información sobre sus dimensiones y estado.

## <a name="button-color-messages"></a>Mensajes de color de botón

El sistema proporciona valores de color predeterminados para los botones. Una aplicación puede recuperar los valores predeterminados de estos colores mediante una llamada a la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o establecer los valores mediante una llamada a la función [**SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) En la tabla siguiente se muestran los valores predeterminados de color de botón.



| Value               | Elemento coloreado                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| COLOR \_ BTNFACE      | Caras de botón.                                                                                                              |
| COLOR \_ BTIGHIGHLIGHT | Área de resaltado (los bordes superior e izquierdo) de un botón.                                                                       |
| COLOR \_ BTNSHADOW    | Área de sombra (los bordes inferior y derecho) de un botón.                                                                      |
| COLOR \_ BTNTEXT      | Texto normal (no ingrata) en los botones.                                                                                       |
| COLOR \_ GRAYTEXT     | Texto deshabilitado (gris) en los botones. Este color se establece en 0 si el controlador de pantalla actual no admite un color gris sólido. |
| VENTANA \_ DE COLOR       | Fondos de ventana.                                                                                                        |
| MARCO \_ DE VENTANA DE COLOR  | Marcos de ventana.                                                                                                             |
| COLOR \_ WINDOWTEXT   | Texto en ventanas.                                                                                                           |



 

Sin embargo, llamar [**a SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) afecta a todas las aplicaciones, por lo que no debe llamar a esta función para personalizar los botones de la aplicación.

El sistema envía un [**mensaje \_ WM CTLCOLORBTN**](wm-ctlcolorbtn.md) a la ventana primaria de un botón antes de dibujar un botón. Este mensaje contiene un identificador para el contexto del dispositivo del botón y un identificador para la ventana secundaria. La ventana primaria puede usar estos identificadores para cambiar el texto y los colores de fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa el mensaje.

## <a name="button-default-message-processing"></a>Procesamiento de mensajes predeterminado de botón

El procedimiento de ventana de la clase de ventana de control de botón predefinida lleva a cabo el procesamiento predeterminado para todos los mensajes que el procedimiento de control de botón no procesa. Cuando el procedimiento de control de botón devuelve **FALSE** para cualquier mensaje, el procedimiento de ventana predefinido comprueba los mensajes y realiza las acciones predeterminadas enumeradas en la tabla siguiente.



<table>
<colgroup>
<col  />
<col  />
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
<td>Envía al botón un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> y <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>un WM_LBUTTONUP</strong></a> y envía <a href="bn-clicked.md">a</a> la ventana primaria un BN_CLICKED de notificación.</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Devuelve el estado de comprobación del botón.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Devuelve un identificador al mapa de bits o icono asociado al botón o <strong>NULL</strong> si el botón no tiene mapa de bits ni icono.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Devuelve el estado de comprobación actual, el estado de inserción y el estado de enfoque del botón.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Establece el estado de comprobación de todos los estilos de botones de radio y casillas. Si el <em>parámetro wParam</em> es mayor que cero para los botones de radio, el botón tiene el <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> estilo.</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Asocia el mapa de bits o el identificador de icono especificados con el botón y devuelve un identificador al icono o mapa de bits anterior.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Establece el estado de inserción del botón. En el caso de los botones dibujados por el propietario, WM_DRAWITEM mensaje se envía <a href="wm-drawitem.md"><strong>a</strong></a> la ventana primaria si el estado del botón ha cambiado.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Establece el estilo de botón. Si la palabra de orden bajo del <em>parámetro lParam</em> es <strong>TRUE,</strong>se vuelve a dibujar el botón.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Comprueba una casilla o una casilla automática cuando el usuario presiona las teclas más (+) o igual (=). Borra una casilla o una casilla automática cuando el usuario presiona la tecla menos (–).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Pinta el botón.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Borra el fondo de los botones dibujados por el propietario. Los fondos de otros botones se borran como parte del WM_PAINT <a href="/windows/desktop/gdi/wm-paint"><strong>y</strong></a> <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> procesamiento.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Devuelve valores que indican el tipo de entrada procesada por el procedimiento de botón predeterminado, como se muestra en la tabla siguiente. 
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

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Devuelve un identificador a la fuente actual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Presiona el botón si el usuario presiona la BARRA ESPACIADORA.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Libera la captura del mouse para todos los casos excepto la tecla TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Quita el rectángulo de foco de un botón. En el caso de los botones de inserción y los botones de inserción predeterminados, se invalida el rectángulo de foco. Si el botón tiene la captura del mouse, se libera la captura, no se hace clic en el botón y se quita cualquier estado de inserción.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Envía <a href="bn-dblclk.md">un</a> BN_DBLCLK de notificación a la ventana primaria para botones de radio y botones dibujados por el propietario. Para otros botones, se procesa un doble clic como <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> mensaje.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Resalta el botón si la posición del cursor del mouse está dentro del rectángulo de cliente del botón.</td>
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
<td>Convierte cualquier <a href="button-styles.md"><strong>botón BS_OWNERDRAW</strong></a> en un <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> de trabajo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Devuelve HTTRANSPARENT, si el control de botón es un cuadro de grupo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Dibuja el botón según su estilo y estado actual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Dibuja un rectángulo de foco en el botón para obtener el foco. En el caso de los botones de radio y los botones de radio automáticos, la ventana primaria se envía <a href="bn-clicked.md">BN_CLICKED</a> código de notificación.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Establece una nueva fuente y, opcionalmente, actualiza la ventana.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Establece el texto del botón. En el caso de un cuadro de grupo, el mensaje pinta sobre el texto existente antes de volver a dibujar el cuadro de grupo con el nuevo texto.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Libera la captura del mouse para todos los casos excepto la tecla TAB.</td>
</tr>
</tbody>
</table>



 

El procedimiento de ventana predefinido pasa todos los demás mensajes a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mensajes de control](control-messages.md)
</dt> </dl>

 

 
