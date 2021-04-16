---
title: Buscapersonas
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de paginación.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df98100ed649e4237c51bfcabf41420c49d004
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656427"
---
# <a name="pager"></a>Buscapersonas

Esta sección contiene información sobre los elementos de programación utilizados con controles de paginación.

### <a name="overviews"></a>Temas de introducción



| Tema                                | Contenido                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de paginación](pager-controls.md) | Un *control de paginación* es un contenedor de ventana que se usa con una ventana que no tiene suficiente área de visualización para mostrar todo su contenido.<br/> |



 

### <a name="macros"></a>Macros



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Buscapersonas \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando está habilitado el reenvío del mouse, el control de paginación reenvía los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana contenida. Puede usar esta macro o enviar el mensaje [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md) explícitamente. <br/>                                                                                                                     |
| [**Buscapersonas \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Recupera el color de fondo actual del control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md) explícitamente. <br/>                                                                                                                                                                                                                                                                 |
| [**Buscapersonas \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Recupera el tamaño actual del borde para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETBORDER**](pgm-getborder.md) explícitamente. <br/>                                                                                                                                                                                                                                                                        |
| [**Buscapersonas \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Recupera el tamaño actual del botón para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md) explícitamente. <br/>                                                                                                                                                                                                                                                                |
| [**Buscapersonas \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Recupera el estado del botón especificado en un control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md) explícitamente. <br/>                                                                                                                                                                                                                                                       |
| [**Buscapersonas \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md) explícitamente. <br/>                                                                                                                                                                                                                                       |
| [**Buscapersonas \_ getPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Recupera la posición de desplazamiento actual del control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ GETPOS**](pgm-getpos.md) explícitamente. <br/>                                                                                                                                                                                                                                                                           |
| [**Buscapersonas \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Obliga al control de paginación a recalcular el tamaño de la ventana contenida. El uso de esta macro hará que se envíe una notificación [ \_ CALCSIZE de PGN](pgn-calcsize.md) . Puede usar esta macro o enviar el mensaje [**PGM \_ RECALCSIZE**](pgm-recalcsize.md) explícitamente. <br/>                                                                                                                                                        |
| [**Buscapersonas \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Establece el color de fondo actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md) explícitamente. <br/>                                                                                                                                                                                                                                                                      |
| [**Buscapersonas \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Establece el tamaño actual del borde para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ SETBORDER**](pgm-setborder.md) explícitamente. <br/>                                                                                                                                                                                                                                                                             |
| [**Buscapersonas \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Establece el tamaño del botón actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md) explícitamente. <br/>                                                                                                                                                                                                                                                                     |
| [**Buscapersonas \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Establece la ventana contenida para el control de paginación. Esta macro no cambiará el elemento primario de la ventana contenida; solo asigna un identificador de ventana al control de paginación para el desplazamiento. En la mayoría de los casos, la ventana contenida será una ventana secundaria. En este caso, la ventana contenida debe ser un elemento secundario del control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ SETCHILD**](pgm-setchild.md) explícitamente. <br/> |
| [**Buscapersonas \_ setPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Establece la posición de desplazamiento para el control de paginación. Puede usar esta macro o enviar el mensaje [**PGM \_ SETPOS**](pgm-setpos.md) explícitamente. <br/>                                                                                                                                                                                                                                                                                       |
| [**Buscapersonas \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.**<br/> Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede usar esta macro o enviar el mensaje [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) explícitamente. <br/>                                                                                                  |



 

### <a name="messages"></a>error de Hadoop



| Tema                                              | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FORWARDMOUSE PGM**](pgm-forwardmouse.md)      | Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando está habilitado el reenvío del mouse, el control de paginación reenvía los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana contenida. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ ForwardMouse de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) . <br/>                                                                                                                       |
| [**\_GETBKCOLOR PGM**](pgm-getbkcolor.md)          | Recupera el color de fondo actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetBkColor de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) . <br/>                                                                                                                                                                                                                                                                   |
| [**\_GETBORDER PGM**](pgm-getborder.md)            | Recupera el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetBorder de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) . <br/>                                                                                                                                                                                                                                                                          |
| [**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)    | Recupera el tamaño actual del botón para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) . <br/>                                                                                                                                                                                                                                                                  |
| [**\_GETBUTTONSTATE PGM**](pgm-getbuttonstate.md)  | Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetButtonState de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) . <br/>                                                                                                                                                                                                                                                         |
| [**\_GETDROPTARGET PGM**](pgm-getdroptarget.md)    | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetDropTarget de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) . <br/>                                                                                                                                                                                                                                         |
| [**\_GETPOS PGM**](pgm-getpos.md)                  | Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ getPos de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) . <br/>                                                                                                                                                                                                                                                                             |
| [**\_RECALCSIZE PGM**](pgm-recalcsize.md)          | Obliga al control de paginación a recalcular el tamaño de la ventana contenida. Al enviar este mensaje, se enviará una notificación de [ \_ CALCSIZE de PGN](pgn-calcsize.md) . Puede enviar este mensaje explícitamente o utilizar la macro [**\_ RecalcSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) . <br/>                                                                                                                                                      |
| [**\_SETBKCOLOR PGM**](pgm-setbkcolor.md)          | Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBkColor de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) . <br/>                                                                                                                                                                                                                                                                        |
| [**\_SETBORDER PGM**](pgm-setborder.md)            | Establece el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBorder de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) . <br/>                                                                                                                                                                                                                                                                               |
| [**\_SETBUTTONSIZE PGM**](pgm-setbuttonsize.md)    | Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetButtonSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) . <br/>                                                                                                                                                                                                                                                                       |
| [**\_SETCHILD PGM**](pgm-setchild.md)              | Establece la ventana contenida para el control de paginación. Este mensaje no cambiará el elemento primario de la ventana contenida; solo asigna un identificador de ventana al control de paginación para el desplazamiento. En la mayoría de los casos, la ventana contenida será una ventana secundaria. En este caso, la ventana contenida debe ser un elemento secundario del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetChild de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) . <br/> |
| [**\_SETPOS PGM**](pgm-setpos.md)                  | Establece la posición de desplazamiento actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ setPos de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) . <br/>                                                                                                                                                                                                                                                                                 |
| [**\_SETSETSCROLLINFO PGM**](pgm-setscrollinfo.md) | **Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.**<br/> Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollInfo de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) . <br/>                                                                                                  |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                        | Contenido                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (buscapersonas)](nm-releasedcapture-pager-.md) | Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse. NM \_ RELEASEDCAPTURE se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Notificación enviada por un control de paginación para obtener las dimensiones desplazables de la ventana contenida. El control de paginación utiliza estas dimensiones para determinar el tamaño desplazable de la ventana contenida. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Enviado por un control de paginación cuando cambia el elemento activo (resaltado). <br/>                                                                                                                                                                                                                               |
| [\_desplazar PGN](pgn-scroll.md)                                | Notificación enviada por un control de paginación antes de que se desplace la ventana contenida. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                         |



 

### <a name="structures"></a>Estructuras



| Tema                                | Contenido                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contiene y recibe información que el control de paginación utiliza para calcular el área desplazable de la ventana contenida. Se usa con la notificación [ \_ CALCSIZE de PGN](pgn-calcsize.md) . <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contiene información que se usa con la notificación [ \_ HOTITEMCHANGE de PGN](pgn-hotitemchange.md) . <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contiene y recibe información que el control de paginación utiliza al desplazarse por la ventana contenida. Se usa con la notificación [de \_ desplazamiento PGN](pgn-scroll.md) . <br/>                          |



 

### <a name="constants"></a>Constantes



| Tema                                            | Contenido                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de control de buscapersonas](pager-control-styles.md) | En esta sección se enumeran los estilos de ventana que se usan al crear controles de buscapersonas. <br/> |



 

 

