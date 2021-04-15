---
title: Botón (controles de Windows)
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de botón. Un botón es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babe31ec9f11ee445167e57394da0fa88fd781dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488722"
---
# <a name="button-windows-controls"></a>Botón (controles de Windows)

Esta sección contiene información sobre los elementos de programación utilizados con controles de botón. Un *botón* es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.

### <a name="overviews"></a>Temas de introducción



| Tema                                       | Contenido                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Mensajes de botón](button-messages.md)      | En este tema se describen los mensajes que se utilizan con los botones.<br/>                                               |
| [Estados del botón](button-states.md)          | En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.<br/> |
| [Tipos de botón](button-types-and-styles.md) | En este tema se describen los diferentes tipos de botones.<br/>                                                    |
| [Usar botones](using-buttons.md)          | En esta sección se explica cómo realizar ciertas tareas asociadas a los botones.<br/>                            |



 

### <a name="functions"></a>Functions



| Tema                                            | Contenido                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Cambia el estado de activación de un control de botón.<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Agrega una marca de verificación a (comprueba) un botón de radio especificado en un grupo y quita una marca de verificación de (borra) todos los demás botones de radio del grupo. <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | La función [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) determina si un control de botón está activado o si un control de botón de tres Estados está activado, desactivado o indeterminado. <br/> |



 

### <a name="macros"></a>Macros



| Tema                                                                         | Contenido                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Botón \_ Habilitar**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Habilita o deshabilita un botón.<br/>                                                                                                                                                                                                          |
| [**Botón \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Obtiene el estado de activación de un botón de radio o casilla. Puede usar esta macro o enviar el mensaje [**\_ GETCHECK de BM**](bm-getcheck.md) explícitamente. <br/>                                                                                       |
| [**Botón \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Obtiene el tamaño del botón que mejor se adapta al texto y la imagen, si hay una lista de imágenes. Puede usar esta macro o enviar el mensaje [**\_ GETIDEALSIZE de BCM**](bcm-getidealsize.md) explícitamente. <br/>                                      |
| [**Botón \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Obtiene la estructura del [**botón \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes que se establece para un control de botón. Puede usar esta macro o enviar el mensaje [**\_ GETIMAGELIST de BCM**](bcm-getimagelist.md) explícitamente. <br/> |
| [**Botón \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede usar esta macro o enviar el mensaje [**\_ GETNOTE de BCM**](bcm-getnote.md) explícitamente.<br/>                                                                            |
| [**Botón \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un vínculo de comando. Use esta macro o envíe el [**mensaje \_ GETNOTELENGTH de BCM**](bcm-getnotelength.md) explícitamente.<br/>                                           |
| [**Botón \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Obtiene información para un control de botón de expansión especificado. Use esta macro o envíe el [**mensaje \_ GETSPLITINFO de BCM**](bcm-getsplitinfo.md) explícitamente.<br/>                                                                                    |
| [**Botón \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Obtiene el estado de activación de un botón de radio o casilla. Puede usar esta macro o enviar el mensaje [**\_ GETSTATE de BM**](bm-getstate.md) explícitamente. <br/>                                                                                       |
| [**Botón \_ gettext**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Obtiene el texto de un botón.<br/>                                                                                                                                                                                                             |
| [**Botón \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Obtiene el número de caracteres en el texto de un botón.<br/>                                                                                                                                                                                 |
| [**Botón \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Obtiene los márgenes utilizados para dibujar texto en un control de botón. Puede usar esta macro o enviar el mensaje [**\_ GETTEXTMARGIN de BCM**](bcm-gettextmargin.md) explícitamente. <br/>                                                                        |
| [**Botón \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Establece el estado de activación de un botón o casilla de radio. Puede usar esta macro o enviar el mensaje [**\_ SETCHECK de BM**](bm-setcheck.md) explícitamente. <br/>                                                                                       |
| [**Botón \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Establece el estado desplegable de un botón especificado con el estilo [**BS \_ SPLITBUTTON**](button-styles.md). Use esta macro o envíe el [**mensaje \_ SETDROPDOWNSTATE de BCM**](bcm-setdropdownstate.md) explícitamente. <br/>           |
| [**Botón \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Use esta macro o envíe el [**mensaje \_ SETSHIELD de BCM**](bcm-setshield.md) explícitamente. <br/>                                          |
| [**Botón \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Asigna una lista de imágenes a un control de botón. Puede usar esta macro o enviar el mensaje [**\_ SETIMAGELIST de BCM**](bcm-setimagelist.md) explícitamente. <br/>                                                                                       |
| [**Botón \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Establece el texto de la nota asociada a un botón de vínculo de comando especificado. Puede usar esta macro o enviar el mensaje [**\_ SETNOTE de BCM**](bcm-setnote.md) explícitamente.<br/>                                                                  |
| [**Botón \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Establece la información de un control de botón de expansión especificado. Use esta macro o envíe el [**mensaje \_ SETSPLITINFO de BCM**](bcm-setsplitinfo.md) explícitamente.<br/>                                                                                    |
| [**Botón \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado. Puede usar esta macro o enviar el mensaje de [**BM \_ SETSTATE**](bm-setstate.md) explícitamente. <br/>        |
| [**Botón \_ setStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Establece el estilo de un botón. Puede usar esta macro o enviar el mensaje de [**BM \_ SETSTYLE**](bm-setstyle.md) explícitamente. <br/>                                                                                                                |
| [**Botón \_ setText**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Establece el texto de un botón.<br/>                                                                                                                                                                                                             |
| [**Botón \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Establece los márgenes para dibujar texto en un control de botón. Puede usar esta macro o enviar el mensaje [**\_ SETTEXTMARGIN de BCM**](bcm-settextmargin.md) explícitamente. <br/>                                                                         |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETIDEALSIZE de BCM \_**](bcm-getidealsize.md)         | Obtiene el tamaño del botón que mejor se adapta a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) .<br/>                                                                                   |
| [**GETIMAGELIST de BCM \_**](bcm-getimagelist.md)         | Obtiene la estructura del [**botón \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes asignada a un control de botón. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .<br/>                                                  |
| [**GETNOTE de BCM \_**](bcm-getnote.md)                   | Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .<br/>                                                                                                                        |
| [**GETNOTELENGTH de BCM \_**](bcm-getnotelength.md)       | Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando. Envíe este mensaje explícitamente o mediante la macro [**Button \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) .<br/>                                                                           |
| [**GETSPLITINFO de BCM \_**](bcm-getsplitinfo.md)         | Obtiene información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la macro [**Button \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) . <br/>                                                                                                                                    |
| [**GETTEXTMARGIN de BCM \_**](bcm-gettextmargin.md)       | Obtiene los márgenes utilizados para dibujar texto en un control de botón. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) .<br/>                                                                                                                     |
| [**SETDROPDOWNSTATE de BCM \_**](bcm-setdropdownstate.md) | Establece el estado desplegable de un botón con la [**\_ lista desplegable**](toolbar-control-and-button-styles.md)de estilo TBSTYLE. Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .<br/>                                        |
| [**SETIMAGELIST de BCM \_**](bcm-setimagelist.md)         | Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .<br/>                                                                                                                                    |
| [**SETNOTE de BCM \_**](bcm-setnote.md)                   | Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .<br/>                                                                                                                        |
| [**SETSHIELD de BCM \_**](bcm-setshield.md)               | Establece el estado de elevación necesario para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) .<br/>                                                  |
| [**SETSPLITINFO de BCM \_**](bcm-setsplitinfo.md)         | Establece la información de un control de botón de expansión. Envíe este mensaje explícitamente o mediante la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) .<br/>                                                                                                                                     |
| [**SETTEXTMARGIN de BCM \_**](bcm-settextmargin.md)       | El [**mensaje \_ SETTEXTMARGIN de BCM**](bcm-settextmargin.md) establece los márgenes para dibujar texto en un control de botón. <br/>                                                                                                                                                                      |
| [**\_clic en BM**](bm-click.md)                         | Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , y la ventana primaria del botón para recibir un código de notificación en el que se ha [ \_ haga clic en BN](bn-clicked.md) .<br/> |
| [**\_GETCHECK BM**](bm-getcheck.md)                   | Obtiene el estado de activación de un botón de radio o casilla. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .<br/>                                                                                                                                  |
| [**BM \_ de BM**](bm-getimage.md)                   | Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.<br/>                                                                                                                                                                                                             |
| [**\_GETSTATE BM**](bm-getstate.md)                   | Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .<br/>                                                                                                                                         |
| [**\_SETCHECK BM**](bm-setcheck.md)                   | Establece el estado de activación de un botón o casilla de radio. Puede enviar este mensaje explícitamente o mediante el [**botón \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.<br/>                                                                                                                             |
| [**\_SETDONTCLICK BM**](bm-setdontclick.md)           | Establece una marca en un botón de radio que controla la generación de mensajes [ \_ clics de BN](bn-clicked.md) cuando el botón recibe el foco.<br/>                                                                                                                                                     |
| [**BM \_ SETIMAGE**](bm-setimage.md)                   | Asocia una nueva imagen (icono o mapa de bits) al botón.<br/>                                                                                                                                                                                                                                 |
| [**BM \_ SETSTATE**](bm-setstate.md)                   | Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera insertado. Puede enviar este mensaje explícitamente o usar la macro de [**botón \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .<br/>                                                   |
| [**BM \_ SETSTYLE**](bm-setstyle.md)                   | Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar el [**botón \_ setStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>Notificaciones



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bcn-dropdown.md">BCN_DROPDOWN</a></td>
<td>Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de un mensaje de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a></td>
<td>Notifica al propietario del control de botón que el mouse está entrando o saliendo del área cliente del control de botón. El control de botón envía este código de notificación en forma de un mensaje de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-clicked.md">BN_CLICKED</a></td>
<td>Se envía cuando el usuario hace clic en un botón. <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-clicked.md">BN_CLICKED</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-dblclk.md">BN_DBLCLK</a></td>
<td>Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los botones <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>y <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Otros tipos de botón solo envían <a href="bn-dblclk.md">BN_DBLCLK</a> si tienen el estilo <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-dblclk.md">BN_DBLCLK</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-disable.md">BN_DISABLE</a></td>
<td>Se envía cuando se deshabilita un botón.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-disable.md">BN_DISABLE</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a></td>
<td>Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los botones <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>y <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Otros tipos de botón solo envían <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> si tienen el estilo <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-hilite.md">BN_HILITE</a></td>
<td>Se envía cuando el usuario selecciona un botón.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-hilite.md">BN_HILITE</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-killfocus.md">BN_KILLFOCUS</a></td>
<td>Se envía cuando un botón pierde el foco del teclado. El botón debe tener el estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificación. <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-killfocus.md">BN_KILLFOCUS</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-paint.md">BN_PAINT</a></td>
<td>Se envía cuando se debe pintar un botón.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-paint.md">BN_PAINT</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-pushed.md">BN_PUSHED</a></td>
<td>Se envía cuando el estado de inserción de un botón se establece en insertado.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-pushed.md">BN_PUSHED</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-setfocus.md">BN_SETFOCUS</a></td>
<td>Se envía cuando un botón recibe el foco de teclado. El botón debe tener el estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificación. <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-setfocus.md">BN_SETFOCUS</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-unhilite.md">BN_UNHILITE</a></td>
<td>Se envía cuando se debe quitar el resaltado de un botón.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-unhilite.md">BN_UNHILITE</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-unpushed.md">BN_UNPUSHED</a></td>
<td>Se envía cuando el estado de la extracción de un botón está establecido en no presionado.
<blockquote>
[!Note]<br />
Este código de notificación solo se proporciona por compatibilidad con versiones de Windows de 16 bits anteriores a la versión 3,0. Las aplicaciones deben usar el estilo del botón <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> y la estructura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>drawitemstruct (</strong></a> para esta tarea.
</blockquote>
<br/> <br/> La ventana primaria del botón recibe el código de notificación de <a href="bn-unpushed.md">BN_UNPUSHED</a> a través del mensaje de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="nm-customdraw-button.md">NM_CUSTOMDRAW (botón)</a></td>
<td>Notifica a la ventana primaria de un control de botón sobre las operaciones de dibujo personalizadas en el botón. <br/> El control de botón envía este código de notificación en forma de un mensaje de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a></td>
<td>El mensaje de <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y de fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Estructuras



| Tema                                         | Contenido                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BOTÓN \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Contiene información sobre una lista de imágenes que se utiliza con un control de botón.<br/>                                                                                                                                                                                                                                 |
| [**BOTÓN \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Contiene información que define un botón de expansión (los estilos de [**\_ SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON**](button-styles.md) ). Se usa con los mensajes [**\_ GETSPLITINFO**](bcm-getsplitinfo.md) y [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md) .<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Contiene información sobre una notificación de [ \_ desplegable de BCN](bcn-dropdown.md) .<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Contiene información sobre el movimiento del mouse sobre un control de botón.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Constantes



| Tema                              | Contenido                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de botón](button-styles.md) | Especifica una combinación de estilos de botón. Si crea un botón mediante la clase BUTTON con la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , puede especificar cualquiera de los estilos de botón que se enumeran a continuación.<br/> |



 

