---
title: Botón (controles de Windows)
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de botón. Un botón es un control en el que el usuario puede hacer clic para proporcionar datos de entrada a una aplicación.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50b9bf5875bc063d8b74626c528d5ec057492c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471301"
---
# <a name="button-windows-controls"></a>Botón (controles de Windows)

Esta sección contiene información sobre los elementos de programación utilizados con controles de botón. Un *botón* es un control en el que el usuario puede hacer clic para proporcionar datos de entrada a una aplicación.

### <a name="overviews"></a>Temas de introducción



| Tema                                       | Contenido                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Mensajes de botón](button-messages.md)      | En este tema se deba a los mensajes que se usan con botones.<br/>                                               |
| [Estados de los botones](button-states.md)          | En esta sección se describe cómo la selección de un botón cambia su estado y cómo debe responder la aplicación.<br/> |
| [Tipos de botón](button-types-and-styles.md) | En este tema se de abordan los distintos tipos de botones.<br/>                                                    |
| [Usar botones](using-buttons.md)          | En esta sección se explica cómo realizar ciertas tareas asociadas a los botones.<br/>                            |



 

### <a name="functions"></a>Functions



| Tema                                            | Contenido                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Cambia el estado de comprobación de un control de botón.<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Agrega una marca de verificación a (comprueba) un botón de radio especificado en un grupo y quita una marca de verificación de (borra) todos los demás botones de radio del grupo. <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | La [**función IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) determina si un control de botón está activado o si un control de botón de tres estados está activado, desactivado o indeterminado. <br/> |



 

### <a name="macros"></a>Macros



| Tema                                                                         | Contenido                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Botón \_ Habilitar**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Habilita o deshabilita un botón.<br/>                                                                                                                                                                                                          |
| [**Button \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Obtiene el estado de comprobación de un botón de radio o una casilla. Puede usar esta macro o enviar el mensaje [**\_ GETCHECK de BM**](bm-getcheck.md) explícitamente. <br/>                                                                                       |
| [**Botón \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Obtiene el tamaño del botón que mejor se adapta al texto y la imagen, si hay una lista de imágenes. Puede usar esta macro o enviar el mensaje [**\_ GETIDEALSIZE**](bcm-getidealsize.md) de BCM explícitamente. <br/>                                      |
| [**Button \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Obtiene la [**estructura \_ BUTTON IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes que se establece para un control de botón. Puede usar esta macro o enviar el mensaje [**\_ GETIMAGELIST**](bcm-getimagelist.md) de BCM explícitamente. <br/> |
| [**Button \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede usar esta macro o enviar el mensaje [**\_ GETNOTE de BCM**](bcm-getnote.md) explícitamente.<br/>                                                                            |
| [**Button \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un vínculo de comando. Use esta macro o envíe el [**mensaje \_ GETNOTELENGTH**](bcm-getnotelength.md) de BCM explícitamente.<br/>                                           |
| [**Botón \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Obtiene información para un control de botón de división especificado. Use esta macro o envíe el [**mensaje \_ GETSPLITINFO**](bcm-getsplitinfo.md) de BCM explícitamente.<br/>                                                                                    |
| [**Button \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Obtiene el estado de comprobación de un botón de radio o una casilla. Puede usar esta macro o enviar el [**mensaje \_ GETSTATE de BM**](bm-getstate.md) explícitamente. <br/>                                                                                       |
| [**Button \_ GetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Obtiene el texto de un botón.<br/>                                                                                                                                                                                                             |
| [**Button \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Obtiene el número de caracteres del texto de un botón.<br/>                                                                                                                                                                                 |
| [**Button \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Obtiene los márgenes utilizados para dibujar texto en un control de botón. Puede usar esta macro o enviar el mensaje [**\_ GETTEXTMARGIN**](bcm-gettextmargin.md) de BCM explícitamente. <br/>                                                                        |
| [**Button \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Establece el estado de comprobación de un botón de radio o una casilla. Puede usar esta macro o enviar el [**mensaje \_ BM SETCHECK**](bm-setcheck.md) explícitamente. <br/>                                                                                       |
| [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Establece el estado de lista desplegable de un botón especificado con el estilo [**de BS \_ SPLITBUTTON**](button-styles.md). Use esta macro o envíe el [**mensaje \_ SETDROPDOWNSTATE**](bcm-setdropdownstate.md) de BCM explícitamente. <br/>           |
| [**Button \_ SetEintegraationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Establece el estado requerido de elevación para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Use esta macro o envíe el [**mensaje \_ SETSHIELD**](bcm-setshield.md) de BCM explícitamente. <br/>                                          |
| [**Button \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Asigna una lista de imágenes a un control de botón. Puede usar esta macro o enviar el mensaje [**\_ SETIMAGELIST**](bcm-setimagelist.md) de BCM explícitamente. <br/>                                                                                       |
| [**Button \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Establece el texto de la nota asociada a un botón de vínculo de comando especificado. Puede usar esta macro o enviar el mensaje [**\_ SETNOTE de BCM**](bcm-setnote.md) explícitamente.<br/>                                                                  |
| [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Establece la información de un control de botón de división especificado. Use esta macro o envíe el [**mensaje \_ SETSPLITINFO**](bcm-setsplitinfo.md) de BCM explícitamente.<br/>                                                                                    |
| [**Button \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera presionado. Puede usar esta macro o enviar el [**mensaje BM \_ SETSTATE**](bm-setstate.md) explícitamente. <br/>        |
| [**Button \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Establece el estilo de un botón. Puede usar esta macro o enviar el mensaje [**BM \_ SETSTYLE**](bm-setstyle.md) explícitamente. <br/>                                                                                                                |
| [**Button \_ SetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Establece el texto de un botón.<br/>                                                                                                                                                                                                             |
| [**Button \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Establece los márgenes para dibujar texto en un control de botón. Puede usar esta macro o enviar el mensaje [**\_ SETTEXTMARGIN**](bcm-settextmargin.md) de BCM explícitamente. <br/>                                                                         |



 

### <a name="messages"></a>Mensajes



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BCM \_ GETIDEALSIZE**](bcm-getidealsize.md)         | Obtiene el tamaño del botón que mejor se adapte a su texto e imagen, si hay una lista de imágenes. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)<br/>                                                                                   |
| [**BCM \_ GETIMAGELIST**](bcm-getimagelist.md)         | Obtiene la [**estructura BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes asignada a un control de botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)<br/>                                                  |
| [**BCM \_ GETNOTE**](bcm-getnote.md)                   | Obtiene el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)<br/>                                                                                                                        |
| [**BCM \_ GETNOTELENGTH**](bcm-getnotelength.md)       | Obtiene la longitud del texto de la nota que se puede mostrar en la descripción de un botón de vínculo de comando. Envíe este mensaje explícitamente o mediante la macro [**\_ Button GetNoteLength.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)<br/>                                                                           |
| [**BCM \_ GETSPLITINFO**](bcm-getsplitinfo.md)         | Obtiene información para un control de botón de división. Envíe este mensaje explícitamente o mediante la macro [**\_ Button GetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) <br/>                                                                                                                                    |
| [**BCM \_ GETTEXTMARGIN**](bcm-gettextmargin.md)       | Obtiene los márgenes utilizados para dibujar texto en un control de botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetTextMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)<br/>                                                                                                                     |
| [**BCM \_ SETDROPDOWNSTATE**](bcm-setdropdownstate.md) | Establece el estado desplegable de un botón con el estilo [**TBSTYLE \_ DROPDOWN**](toolbar-control-and-button-styles.md). Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetDropDownState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)<br/>                                        |
| [**BCM \_ SETIMAGELIST**](bcm-setimagelist.md)         | Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)<br/>                                                                                                                                    |
| [**BCM \_ SETNOTE**](bcm-setnote.md)                   | Establece el texto de la nota asociada a un botón de vínculo de comando. Puede enviar este mensaje explícitamente o usar la macro [**Button \_ SetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)<br/>                                                                                                                        |
| [**BCM \_ SETSHIELD**](bcm-setshield.md)               | Establece el estado requerido de elevación para que un botón o vínculo de comando especificado muestre un icono con privilegios elevados. Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetEintegraationRequiredState.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate)<br/>                                                  |
| [**BCM \_ SETSPLITINFO**](bcm-setsplitinfo.md)         | Establece la información de un control de botón de división. Envíe este mensaje explícitamente o mediante la macro [**\_ Button SetSplitInfo.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)<br/>                                                                                                                                     |
| [**BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md)       | El [**mensaje \_ SETTEXTMARGIN**](bcm-settextmargin.md) de BCM establece los márgenes para dibujar texto en un control de botón. <br/>                                                                                                                                                                      |
| [**BM \_ CLICK**](bm-click.md)                         | Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y [**WM \_ LBUTTONUP,**](/windows/desktop/inputdev/wm-lbuttonup) y la ventana primaria del botón reciba un código de notificación [ \_ CLICKED de BN.](bn-clicked.md)<br/> |
| [**BM \_ GETCHECK**](bm-getcheck.md)                   | Obtiene el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)<br/>                                                                                                                                  |
| [**BM \_ GETIMAGE**](bm-getimage.md)                   | Recupera un identificador de la imagen (icono o mapa de bits) asociado al botón.<br/>                                                                                                                                                                                                             |
| [**BM \_ GETSTATE**](bm-getstate.md)                   | Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)<br/>                                                                                                                                         |
| [**BM \_ SETCHECK**](bm-setcheck.md)                   | Establece el estado de comprobación de un botón de radio o una casilla. Puede enviar este mensaje explícitamente o mediante la macro [**Button \_ SetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)<br/>                                                                                                                             |
| [**BM \_ SETDONTCLICK**](bm-setdontclick.md)           | Establece una marca en un botón de radio que controla la generación de mensajes [ \_ CLICKED](bn-clicked.md) de BN cuando el botón recibe el foco.<br/>                                                                                                                                                     |
| [**BM \_ SETIMAGE**](bm-setimage.md)                   | Asocia una nueva imagen (icono o mapa de bits) al botón.<br/>                                                                                                                                                                                                                                 |
| [**BM \_ SETSTATE**](bm-setstate.md)                   | Establece el estado de resaltado de un botón. El estado de resaltado indica si el botón está resaltado como si el usuario lo hubiera presionado. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button SetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)<br/>                                                   |
| [**BM \_ SETSTYLE**](bm-setstyle.md)                   | Establece el estilo de un botón. Puede enviar este mensaje explícitamente o usar la macro [**Button \_ SetStyle.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>Notificaciones




| Tema | Contenido | 
|-------|----------|
| <a href="bcn-dropdown.md">BCN_DROPDOWN</a> | Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> mensaje.<br /> | 
| <a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a> | Notifica al propietario del control de botón que el mouse entra o sale del área de cliente del control de botón. El control de botón envía este código de notificación en forma de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> mensaje.<br /> | 
| <a href="bn-clicked.md">BN_CLICKED</a> | Se envía cuando el usuario hace clic en un botón. <br /> La ventana primaria del botón recibe el <a href="bn-clicked.md">BN_CLICKED</a> de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje. <br /> | 
| <a href="bn-dblclk.md">BN_DBLCLK</a> | Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a> <a href="button-styles.md"><strong>y</strong></a> BS_OWNERDRAW botones. Otros tipos de botón <a href="bn-dblclk.md">BN_DBLCLK</a> solo si tienen el <a href="button-styles.md"><strong>estilo BS_NOTIFY</strong></a> usuario.<br /> La ventana primaria del botón recibe <a href="bn-dblclk.md">el</a> BN_DBLCLK de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje. <br /> | 
| <a href="bn-disable.md">BN_DISABLE</a> | Se envía cuando se deshabilita un botón.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe el <a href="bn-disable.md">BN_DISABLE</a> de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> | Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a> <a href="button-styles.md"><strong>y</strong></a> BS_OWNERDRAW botones. Otros tipos de botón <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> solo si tienen el <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> de botón.<br /> La ventana primaria del botón recibe el <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje. <br /> | 
| <a href="bn-hilite.md">BN_HILITE</a> | Se envía cuando el usuario selecciona un botón.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe <a href="bn-hilite.md">el</a> BN_HILITE de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="bn-killfocus.md">BN_KILLFOCUS</a> | Se envía cuando un botón pierde el foco del teclado. El botón debe tener el <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificación. <br /> La ventana primaria del botón recibe <a href="bn-killfocus.md">el</a> BN_KILLFOCUS de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje. <br /> | 
| <a href="bn-paint.md">BN_PAINT</a> | Se envía cuando se debe pintar un botón.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe el <a href="bn-paint.md">BN_PAINT</a> de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje. <br /> | 
| <a href="bn-pushed.md">BN_PUSHED</a> | Se envía cuando el estado de inserción de un botón se establece en pushed.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe el <a href="bn-pushed.md">BN_PUSHED</a> de notificación a través <a href="/windows/desktop/menurc/wm-command"><strong>del WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="bn-setfocus.md">BN_SETFOCUS</a> | Se envía cuando un botón recibe el foco del teclado. El botón debe tener el <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificación. <br /> La ventana primaria del botón recibe <a href="bn-setfocus.md">el</a> BN_SETFOCUS de notificación a través del <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="bn-unhilite.md">BN_UNHILITE</a> | Se envía cuando se debe quitar el resaltado de un botón.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows versiones anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe <a href="bn-unhilite.md">el</a> BN_UNHILITE de notificación a través del <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="bn-unpushed.md">BN_UNPUSHED</a> | Se envía cuando el estado de inserción de un botón se establece en sin enviar.<blockquote>[!Note]<br />Este código de notificación solo se proporciona por compatibilidad con versiones de 16 bits de Windows versiones anteriores a la versión 3.0. Las aplicaciones deben usar <a href="button-styles.md"><strong>el BS_OWNERDRAW</strong></a> de botón y la <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>estructura DRAWITEMSTRUCT</strong></a> para esta tarea.</blockquote><br /><br /> La ventana primaria del botón recibe <a href="bn-unpushed.md">el</a> BN_UNPUSHED de notificación a través del <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensaje.<br /> | 
| <a href="nm-customdraw-button.md">NM_CUSTOMDRAW (botón)</a> | Notifica a la ventana primaria un control de botón sobre las operaciones de dibujo personalizadas en el botón. <br /> El control de botón envía este código de notificación en forma de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> mensaje.<br /> | 
| <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> | El <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> se envía a la ventana primaria de un botón antes de dibujar el botón. La ventana primaria puede cambiar los colores de texto y fondo del botón. Sin embargo, solo los botones dibujados por el propietario responden a la ventana primaria que procesa este mensaje. <br /> | 




 

### <a name="structures"></a>Estructuras



| Tema                                         | Contenido                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Contiene información sobre una lista de imágenes que se usa con un control de botón.<br/>                                                                                                                                                                                                                                 |
| [**BUTTON \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Contiene información que define un botón de división [**(estilos \_ BS SPLITBUTTON**](button-styles.md) y [**BS \_ DEFSPLITBUTTON).**](button-styles.md) Se usa con [**los mensajes \_ BCM GETSPLITINFO**](bcm-getsplitinfo.md) y [**BCM \_ SETSPLITINFO.**](bcm-setsplitinfo.md)<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Contiene información sobre una [notificación DE LISTA DESPLEGABLE \_ de BCN.](bcn-dropdown.md)<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Contiene información sobre el movimiento del mouse sobre un control de botón.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Constantes



| Tema                              | Contenido                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de botón](button-styles.md) | Especifica una combinación de estilos de botón. Si crea un botón mediante la clase BUTTON con la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) puede especificar cualquiera de los estilos de botón que se enumeran a continuación.<br/> |



 

