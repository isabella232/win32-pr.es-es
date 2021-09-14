---
title: Rebar
description: Esta sección contiene información sobre los elementos de programación utilizados con controles rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef14343d33fb5ae45a2d93df74a9b915aca6d7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167178"
---
# <a name="rebar"></a>Rebar

Esta sección contiene información sobre los elementos de programación utilizados con controles rebar.

### <a name="overviews"></a>Temas de introducción



| Tema                                            | Contenido                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Controles Rebar](rebar-controls.md)             | *Los controles rebar* actúan como contenedores para las ventanas secundarias.<br/>                       |
| [Usar controles Rebar](using-rebar-controls.md) | Esta sección contiene código de ejemplo que muestra cómo implementar controles rebar.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                               | Contenido                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RB \_ BEGINDRAG**](rb-begindrag.md)               | Coloca el control rebar en modo de arrastrar y colocar. Este mensaje no hace que se envíe una notificación [ \_ BEGINDRAG de RBN.](rbn-begindrag.md) <br/>                                                 |
| [**RB \_ DELETEBAND**](rb-deleteband.md)             | Elimina una banda de un control rebar. <br/>                                                                                                                                                     |
| [**RB \_ DRAGMOVE**](rb-dragmove.md)                 | Actualiza la posición de arrastre en el control rebar después de un mensaje [**\_ BEGINDRAG de RB**](rb-begindrag.md) anterior. <br/>                                                                           |
| [**RB \_ ENDDRAG**](rb-enddrag.md)                   | Finaliza la operación de arrastrar y colocar del control rebar. Este mensaje no hace que se envíe una notificación [ \_ ENDDRAG de RBN.](rbn-enddrag.md) <br/>                                          |
| [**RB \_ GETBANDBORDERS**](rb-getbandborders.md)     | Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda. <br/>                                                                          |
| [**RB \_ GETBANDCOUNT**](rb-getbandcount.md)         | Recupera el recuento de bandas actualmente en el control rebar. <br/>                                                                                                                             |
| [**RB \_ GETBANDINFO**](rb-getbandinfo.md)           | Recupera información sobre una banda especificada en un control rebar. <br/>                                                                                                                         |
| [**RB \_ GETBANDMARGINS**](rb-getbandmargins.md)     | Recupera los márgenes de una banda.<br/>                                                                                                                                                          |
| [**RB \_ GETBARHEIGHT**](rb-getbarheight.md)         | Recupera el alto del control rebar. <br/>                                                                                                                                               |
| [**RB \_ GETBARINFO**](rb-getbarinfo.md)             | Recupera información sobre el control rebar y la lista de imágenes que usa. <br/>                                                                                                                |
| [**RB \_ GETBKCOLOR**](rb-getbkcolor.md)             | Recupera el color de fondo predeterminado de un control rebar. <br/>                                                                                                                                    |
| [**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)     | Recupera la información de combinación de colores del control rebar. <br/>                                                                                                                           |
| [**RB \_ GETDROPTARGET**](rb-getdroptarget.md)       | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control rebar. <br/>                                                                                                        |
| [**RB \_ GETEXTENDEDSTYLE**](rb-getextendedstyle.md) | Obtiene el estilo extendido. <br/>                                                                                                                                                                 |
| [**RB \_ GETPALETTE**](rb-getpalette.md)             | Recupera la paleta actual del control rebar. <br/>                                                                                                                                           |
| [**RB \_ GETRECT**](rb-getrect.md)                   | Recupera el rectángulo delimitador de una banda determinada en un control rebar. <br/>                                                                                                                    |
| [**RB \_ GETROWCOUNT**](rb-getrowcount.md)           | Recupera el número de filas de bandas de un control rebar. <br/>                                                                                                                                |
| [**RB \_ GETROWHEIGHT**](rb-getrowheight.md)         | Recupera el alto de una fila especificada en un control rebar. <br/>                                                                                                                              |
| [**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)         | Recupera el color de texto predeterminado de un control rebar. <br/>                                                                                                                                          |
| [**RB \_ GETTOOLTIPS**](rb-gettooltips.md)           | Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar. <br/>                                                                                                           |
| [**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md) | Recupera la marca de formato de caracteres Unicode para el control . <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Determina qué parte de una banda de rebar se encuentra en un punto determinado de la pantalla, si existe una banda de rebar en ese momento. <br/>                                                                        |
| [**RB \_ IDTOINDEX**](rb-idtoindex.md)               | Convierte un identificador de banda en un índice de banda en un control rebar. <br/>                                                                                                                           |
| [**RB \_ INSERTBAND**](rb-insertband.md)             | Inserta una nueva banda en un control rebar. <br/>                                                                                                                                                   |
| [**RB \_ MAXIMIZEBAND**](rb-maximizeband.md)         | Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor. <br/>                                                                                                                   |
| [**RB \_ MINIMIZEBAND**](rb-minimizeband.md)         | Cambia el tamaño de una banda de un control rebar a su tamaño más pequeño. <br/>                                                                                                                                  |
| [**RB \_ MOVEBAND**](rb-moveband.md)                 | Mueve una banda de un índice a otro. <br/>                                                                                                                                                  |
| [**RB \_ PUSHCHEVRON**](rb-pushchevron.md)           | Se envía a un control rebar para insertar mediante programación un botón de contenido adicional.<br/>                                                                                                                               |
| [**RB \_ SETBANDINFO**](rb-setbandinfo.md)           | Establece las características de una banda existente en un control rebar. <br/>                                                                                                                             |
| [**RB \_ SETBANDWIDTH**](rb-setbandwidth.md)         | Establece el ancho de una banda acoplada.<br/>                                                                                                                                                         |
| [**RB \_ SETBARINFO**](rb-setbarinfo.md)             | Establece las características de un control rebar. <br/>                                                                                                                                             |
| [**RB \_ SETBKCOLOR**](rb-setbkcolor.md)             | Establece el color de fondo predeterminado de un control rebar. <br/>                                                                                                                                         |
| [**RB \_ SETCOLORSCHEME**](rb-setcolorscheme.md)     | Establece la información de combinación de colores para el control rebar. <br/>                                                                                                                                 |
| [**RB \_ SETEXTENDEDSTYLE**](rb-setextendedstyle.md) | Establece el estilo extendido. Este mensaje no se implementa.<br/>                                                                                                                                 |
| [**RB \_ SETPALETTE**](rb-setpalette.md)             | Establece la paleta actual del control rebar. <br/>                                                                                                                                                |
| [**RB \_ SETPARENT**](rb-setparent.md)               | Establece la ventana primaria de un control rebar. <br/>                                                                                                                                                    |
| [**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)         | Establece el color de texto predeterminado de un control rebar. <br/>                                                                                                                                               |
| [**RB \_ SETTOOLTIPS**](rb-settooltips.md)           | Asocia un control de información sobre herramientas al control rebar. <br/>                                                                                                                                     |
| [**RB \_ SETUNICODEFORMAT**](rb-setunicodeformat.md) | Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. <br/> |
| [**RB \_ SETWINDOWTHEME**](rb-setwindowtheme.md)     | Establece el estilo visual de un control rebar.<br/>                                                                                                                                                 |
| [**RB \_ SHOWBAND**](rb-showband.md)                 | Muestra u oculta una banda determinada en un control rebar. <br/>                                                                                                                                          |
| [**RB \_ SIZETORECT**](rb-sizetorect.md)             | Intenta encontrar el mejor diseño de las bandas para el rectángulo especificado. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                        | Contenido                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (rebar)](nm-customdraw-rebar.md)            | Enviado por el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                               |
| [NM \_ NCHITTEST (rebar)](nm-nchittest-rebar.md)              | Enviado por un control rebar cuando el control recibe un [**mensaje \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (rebar)](nm-releasedcapture-rebar-.md) | Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ AUTOBREAK](rbn-autobreak.md)                          | Notifica al elemento [primario de una barra](rebar-controls.md) de rebar que aparecerá una interrupción en la barra. El elemento primario determina si se debe realizar la interrupción. <br/>                                                                                                                            |
| [RBN \_ AUTOSIZE](rbn-autosize.md)                            | Enviado por un control de rebar creado con el [**estilo \_ AUTOSIZE de RBS**](rebar-control-styles.md) cuando la barra se cambia automáticamente de tamaño. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Enviado por un control rebar cuando el usuario comienza a arrastrar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Enviado por un control rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Enviado por un control rebar cuando se cambia el tamaño de la ventana secundaria de una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Enviado por un control rebar después de que se haya eliminado una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |
| [ELIMINACIÓN \_ DE RBNBAND](rbn-deletingband.md)                    | Enviado por un control rebar cuando una banda está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Enviado por un control rebar cuando el usuario deja de arrastrar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Enviado por un control rebar creado con el estilo [**\_ REGISTERDROP de RBS**](rebar-control-styles.md) cuando se arrastra un objeto sobre una banda del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [CAMBIO ALTO DE RBN \_](rbn-heightchange.md)                    | Enviado por un control rebar cuando ha cambiado su alto. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                    |
| [DISEÑO DE RBN \_ MODIFICADO](rbn-layoutchanged.md)                  | Lo envía un control rebar cuando el usuario cambia el diseño de las bandas del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                        |
| [RBN \_ MINMAX](rbn-minmax.md)                                | Enviado por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Enviado por un control rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |



 

### <a name="structures"></a>Estructuras



| Tema                                        | Contenido                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contiene información que se usa para controlar los [códigos de notificación DE \_ RBN AUTOSIZE.](rbn-autosize.md) <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contiene información que se usa para controlar varios códigos de notificación de rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contiene información que se usa con la [notificación \_ AUTOBREAK de RBN.](rbn-autobreak.md)<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contiene información que se usa para controlar el [código de notificación \_ RBN CHEVRONPUSHED.](rbn-chevronpushed.md) <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contiene información que se usa para controlar el [código de notificación \_ CHILDSIZE de RBN.](rbn-childsize.md) <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contiene información que se usa para controlar un código [de notificación \_ SPLITTERDRAG de RBN.](rbn-splitterdrag.md)<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contiene información específica de una operación de prueba de acceso. Esta estructura se usa con el [**mensaje \_ RB HITTEST.**](rb-hittest.md) <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contiene información que define una banda en un control rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contiene información que describe las características del control rebar. <br/>                                                                |



 

### <a name="constants"></a>Constantes



| Tema                                            | Contenido                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Estilos de control Rebar](rebar-control-styles.md) | Los controles rebar admiten una variedad de estilos de control, además de los estilos de ventana estándar. <br/> |



 

 

