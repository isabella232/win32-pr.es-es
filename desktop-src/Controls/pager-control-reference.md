---
title: Buscapersonas
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de paginación.
ms.assetid: vs|controls|~\controls\pager\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df98100ed649e4237c51bfcabf41420c49d004
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167810"
---
# <a name="pager"></a>Buscapersonas

Esta sección contiene información sobre los elementos de programación utilizados con controles de paginación.

### <a name="overviews"></a>Temas de introducción



| Tema                                | Contenido                                                                                                                                         |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de paginación](pager-controls.md) | Un *control de paginación* es un contenedor de ventanas que se usa con una ventana que no tiene suficiente área de visualización para mostrar todo su contenido.<br/> |



 

### <a name="macros"></a>Macros



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pager \_ ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)     | Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando el reenvío del mouse está habilitado, el control de paginación reenvía mensajes [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana independiente. Puede usar esta macro o enviar el mensaje [**\_ FORWARDMOUSE de PGM**](pgm-forwardmouse.md) explícitamente. <br/>                                                                                                                     |
| [**Pager \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)         | Recupera el color de fondo actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETBKCOLOR de PGM**](pgm-getbkcolor.md) explícitamente. <br/>                                                                                                                                                                                                                                                                 |
| [**Pager \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder)           | Recupera el tamaño del borde actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETBORDER de PGM**](pgm-getborder.md) explícitamente. <br/>                                                                                                                                                                                                                                                                        |
| [**Pager \_ GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize)   | Recupera el tamaño del botón actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETBUTTONSIZE de PGM**](pgm-getbuttonsize.md) explícitamente. <br/>                                                                                                                                                                                                                                                                |
| [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) | Recupera el estado del botón especificado en un control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETBUTTONSTATE de PGM**](pgm-getbuttonstate.md) explícitamente. <br/>                                                                                                                                                                                                                                                       |
| [**Pager \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)   | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETDROPTARGET de PGM**](pgm-getdroptarget.md) explícitamente. <br/>                                                                                                                                                                                                                                       |
| [**Pager \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos)                 | Recupera la posición de desplazamiento actual del control de paginación. Puede usar esta macro o enviar el mensaje [**\_ GETPOS de PGM**](pgm-getpos.md) explícitamente. <br/>                                                                                                                                                                                                                                                                           |
| [**Pager \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize)         | Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. El uso de esta macro dará lugar a que se envíe una notificación [ \_ CALCSIZE de PGN.](pgn-calcsize.md) Puede usar esta macro o enviar el mensaje [**\_ RECALCSIZE**](pgm-recalcsize.md) de PGM explícitamente. <br/>                                                                                                                                                        |
| [**Pager \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)         | Establece el color de fondo actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ SETBKCOLOR de PGM**](pgm-setbkcolor.md) explícitamente. <br/>                                                                                                                                                                                                                                                                      |
| [**Pager \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder)           | Establece el tamaño del borde actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ SETBORDER de PGM**](pgm-setborder.md) explícitamente. <br/>                                                                                                                                                                                                                                                                             |
| [**Pager \_ SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)   | Establece el tamaño del botón actual para el control de paginación. Puede usar esta macro o enviar el mensaje [**\_ SETBUTTONSIZE**](pgm-setbuttonsize.md) de PGM explícitamente. <br/>                                                                                                                                                                                                                                                                     |
| [**Pager \_ SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild)             | Establece la ventana independiente para el control de paginación. Esta macro no cambiará el elemento primario de la ventana independiente; solo asigna un identificador de ventana al control de paginación para el desplazamiento. En la mayoría de los casos, la ventana independiente será una ventana secundaria. Si este es el caso, la ventana independiente debe ser un elemento secundario del control de paginación. Puede usar esta macro o enviar el mensaje [**\_ SETCHILD de PGM**](pgm-setchild.md) explícitamente. <br/> |
| [**Pager \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos)                 | Establece la posición de desplazamiento del control de paginación. Puede usar esta macro o enviar el mensaje [**\_ SETPOS de PGM**](pgm-setpos.md) explícitamente. <br/>                                                                                                                                                                                                                                                                                       |
| [**Pager \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)   | **Destinado a uso interno; no se recomienda para su uso en aplicaciones.**<br/> Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede usar esta macro o enviar el mensaje [**\_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) de PGM explícitamente. <br/>                                                                                                  |



 

### <a name="messages"></a>error de Hadoop



| Tema                                              | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PGM \_ FORWARDMOUSE**](pgm-forwardmouse.md)      | Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando el reenvío del mouse está habilitado, el control de paginación reenvía mensajes [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana independiente. Puede enviar este mensaje explícitamente o usar la macro [**\_ ForwardMouse de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) <br/>                                                                                                                       |
| [**PGM \_ GETBKCOLOR**](pgm-getbkcolor.md)          | Recupera el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetBkColor de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) <br/>                                                                                                                                                                                                                                                                   |
| [**PGM \_ GETBORDER**](pgm-getborder.md)            | Recupera el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ Pager GetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) <br/>                                                                                                                                                                                                                                                                          |
| [**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)    | Recupera el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) <br/>                                                                                                                                                                                                                                                                  |
| [**PGM \_ GETBUTTONSTATE**](pgm-getbuttonstate.md)  | Recupera el estado del botón especificado en un control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetButtonState.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) <br/>                                                                                                                                                                                                                                                         |
| [**PGM \_ GETDROPTARGET**](pgm-getdroptarget.md)    | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetDropTarget de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) <br/>                                                                                                                                                                                                                                         |
| [**GETPOS \_ de PGM**](pgm-getpos.md)                  | Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ GetPos.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) <br/>                                                                                                                                                                                                                                                                             |
| [**PGM \_ RECALCSIZE**](pgm-recalcsize.md)          | Fuerza al control de paginación a volver a calcular el tamaño de la ventana independiente. Al enviar este mensaje, se enviará una [notificación \_ PGN CALCSIZE.](pgn-calcsize.md) Puede enviar este mensaje explícitamente o usar la macro [**\_ Pager RecalcSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) <br/>                                                                                                                                                      |
| [**PGM \_ SETBKCOLOR**](pgm-setbkcolor.md)          | Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetBkColor de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) <br/>                                                                                                                                                                                                                                                                        |
| [**PGM \_ SETBORDER**](pgm-setborder.md)            | Establece el tamaño del borde actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetBorder.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) <br/>                                                                                                                                                                                                                                                                               |
| [**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)    | Establece el tamaño del botón actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetButtonSize de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) <br/>                                                                                                                                                                                                                                                                       |
| [**PGM \_ SETCHILD**](pgm-setchild.md)              | Establece la ventana independiente para el control de paginación. Este mensaje no cambiará el elemento primario de la ventana independiente; solo asigna un identificador de ventana al control de paginación para desplazarse. En la mayoría de los casos, la ventana independiente será una ventana secundaria. Si este es el caso, la ventana independiente debe ser un elemento secundario del control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetChild.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) <br/> |
| [**PGM \_ SETPOS**](pgm-setpos.md)                  | Establece la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**Pager \_ SetPos.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) <br/>                                                                                                                                                                                                                                                                                 |
| [**PGM \_ SETSETSCROLLINFO**](pgm-setscrollinfo.md) | **Diseñado para uso interno; no se recomienda para su uso en aplicaciones.**<br/> Establece los parámetros de desplazamiento del control de paginación, incluido el valor de tiempo de espera, las líneas por tiempo de espera y los píxeles por línea. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetScrollInfo de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) <br/>                                                                                                  |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                        | Contenido                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (paginador)](nm-releasedcapture-pager-.md) | Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse. NM \_ RELEASEDCAPTURE se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                |
| [PGN \_ CALCSIZE](pgn-calcsize.md)                            | Notificación enviada por un control de paginación para obtener las dimensiones desplazables de la ventana independiente. El control de paginación usa estas dimensiones para determinar el tamaño desplazable de la ventana independiente. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [PGN \_ HOTITEMCHANGE](pgn-hotitemchange.md)                  | Enviado por un control de paginación cuando cambia el elemento de acceso (resaltado). <br/>                                                                                                                                                                                                                               |
| [DESPLAZAMIENTO \_ DE PGN](pgn-scroll.md)                                | Notificación enviada por un control de paginación antes de que se desplace la ventana independiente. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                         |



 

### <a name="structures"></a>Estructuras



| Tema                                | Contenido                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) | Contiene y recibe información que el control de paginación usa para calcular el área desplazable de la ventana independiente. Se usa con la [notificación \_ PGN CALCSIZE.](pgn-calcsize.md) <br/> |
| [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem)   | Contiene información utilizada con la [notificación \_ HOTITEMCHANGE de PGN.](pgn-hotitemchange.md) <br/>                                                                                                |
| [**NMPGSCROLL**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgscroll)     | Contiene y recibe información que el control de paginación usa al desplazarse por la ventana independiente. Se usa con la notificación [PGN \_ SCROLL.](pgn-scroll.md) <br/>                          |



 

### <a name="constants"></a>Constantes



| Tema                                            | Contenido                                                                            |
|--------------------------------------------------|-------------------------------------------------------------------------------------|
| [Estilos de control de paginación](pager-control-styles.md) | En esta sección se enumeran los estilos de ventana utilizados al crear controles de paginación. <br/> |



 

 

