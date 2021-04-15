---
title: Rebar
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles rebar.
ms.assetid: vs|controls|~\controls\rebar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef14343d33fb5ae45a2d93df74a9b915aca6d7b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488390"
---
# <a name="rebar"></a>Rebar

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles rebar.

### <a name="overviews"></a>Temas de introducción



| Tema                                            | Contenido                                                                               |
|--------------------------------------------------|----------------------------------------------------------------------------------------|
| [Rebar (controles)](rebar-controls.md)             | *Los controles rebar* actúan como contenedores para las ventanas secundarias.<br/>                       |
| [Usar controles rebar](using-rebar-controls.md) | Esta sección contiene código de ejemplo que muestra cómo implementar los controles rebar.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                               | Contenido                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BEGINDRAG RB**](rb-begindrag.md)               | Coloca el control rebar en el modo de arrastrar y colocar. Este mensaje no hace que se envíe una notificación de [ \_ BEGINDRAG de RBN](rbn-begindrag.md) . <br/>                                                 |
| [**\_DELETEBAND RB**](rb-deleteband.md)             | Elimina una banda de un control rebar. <br/>                                                                                                                                                     |
| [**\_DRAGMOVE RB**](rb-dragmove.md)                 | Actualiza la posición de arrastre en el control rebar después de un mensaje [**RB \_ BEGINDRAG**](rb-begindrag.md) anterior. <br/>                                                                           |
| [**\_ENDDRAG RB**](rb-enddrag.md)                   | Finaliza la operación de arrastrar y colocar del control rebar. Este mensaje no hace que se envíe una notificación de [ \_ ENDDRAG de RBN](rbn-enddrag.md) . <br/>                                          |
| [**\_GETBANDBORDERS RB**](rb-getbandborders.md)     | Recupera los bordes de una banda. El resultado de este mensaje se puede usar para calcular el área utilizable en una banda. <br/>                                                                          |
| [**\_GETBANDCOUNT RB**](rb-getbandcount.md)         | Recupera el recuento de bandas actualmente en el control rebar. <br/>                                                                                                                             |
| [**\_GETBANDINFO RB**](rb-getbandinfo.md)           | Recupera información sobre una banda especificada en un control rebar. <br/>                                                                                                                         |
| [**\_GETBANDMARGINS RB**](rb-getbandmargins.md)     | Recupera los márgenes de una banda.<br/>                                                                                                                                                          |
| [**\_GETBARHEIGHT RB**](rb-getbarheight.md)         | Recupera el alto del control rebar. <br/>                                                                                                                                               |
| [**\_GETBARINFO RB**](rb-getbarinfo.md)             | Recupera información sobre el control rebar y la lista de imágenes que utiliza. <br/>                                                                                                                |
| [**\_GETBKCOLOR RB**](rb-getbkcolor.md)             | Recupera el color de fondo predeterminado de un control rebar. <br/>                                                                                                                                    |
| [**\_GETCOLORSCHEME RB**](rb-getcolorscheme.md)     | Recupera la información de la combinación de colores del control rebar. <br/>                                                                                                                           |
| [**\_GETDROPTARGET RB**](rb-getdroptarget.md)       | Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del control rebar. <br/>                                                                                                        |
| [**\_GETEXTENDEDSTYLE RB**](rb-getextendedstyle.md) | Obtiene el estilo extendido. <br/>                                                                                                                                                                 |
| [**\_GETPALETTE RB**](rb-getpalette.md)             | Recupera la paleta actual del control rebar. <br/>                                                                                                                                           |
| [**\_GETRECT RB**](rb-getrect.md)                   | Recupera el rectángulo delimitador de una banda determinada en un control rebar. <br/>                                                                                                                    |
| [**GETROWCOUNT de RB \_**](rb-getrowcount.md)           | Recupera el número de filas de bandas en un control rebar. <br/>                                                                                                                                |
| [**\_GETROWHEIGHT RB**](rb-getrowheight.md)         | Recupera el alto de una fila especificada en un control rebar. <br/>                                                                                                                              |
| [**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)         | Recupera el color de texto predeterminado del control rebar. <br/>                                                                                                                                          |
| [**\_GETTOOLTIPS RB**](rb-gettooltips.md)           | Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar. <br/>                                                                                                           |
| [**\_GETUNICODEFORMAT RB**](rb-getunicodeformat.md) | Recupera la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                             |
| [**RB \_ HITTEST**](rb-hittest.md)                   | Determina qué parte de una banda rebar se encuentra en un punto determinado de la pantalla, si existe una banda rebar en ese punto. <br/>                                                                        |
| [**\_IDTOINDEX RB**](rb-idtoindex.md)               | Convierte un identificador de banda en un índice de banda en un control rebar. <br/>                                                                                                                           |
| [**\_INSERTBAND RB**](rb-insertband.md)             | Inserta una nueva banda en un control rebar. <br/>                                                                                                                                                   |
| [**\_MAXIMIZEBAND RB**](rb-maximizeband.md)         | Cambia el tamaño de una banda de un control rebar a su tamaño ideal o mayor. <br/>                                                                                                                   |
| [**\_MINIMIZEBAND RB**](rb-minimizeband.md)         | Cambia el tamaño de una banda de un control rebar a su tamaño más pequeño. <br/>                                                                                                                                  |
| [**\_MOVEBAND RB**](rb-moveband.md)                 | Mueve una banda de un índice a otro. <br/>                                                                                                                                                  |
| [**\_PUSHCHEVRON RB**](rb-pushchevron.md)           | Se envía a un control rebar para presionar mediante programación un botón de contenido adicional.<br/>                                                                                                                               |
| [**\_SETBANDINFO RB**](rb-setbandinfo.md)           | Establece las características de una banda existente en un control rebar. <br/>                                                                                                                             |
| [**\_SETBANDWIDTH RB**](rb-setbandwidth.md)         | Establece el ancho de una banda acoplada.<br/>                                                                                                                                                         |
| [**\_SETBARINFO RB**](rb-setbarinfo.md)             | Establece las características de un control rebar. <br/>                                                                                                                                             |
| [**\_SETBKCOLOR RB**](rb-setbkcolor.md)             | Establece el color de fondo predeterminado del control rebar. <br/>                                                                                                                                         |
| [**\_SETCOLORSCHEME RB**](rb-setcolorscheme.md)     | Establece la información de la combinación de colores para el control rebar. <br/>                                                                                                                                 |
| [**\_SETEXTENDEDSTYLE RB**](rb-setextendedstyle.md) | Establece el estilo extendido. Este mensaje no está implementado.<br/>                                                                                                                                 |
| [**\_SETPALETTE RB**](rb-setpalette.md)             | Establece la paleta actual del control rebar. <br/>                                                                                                                                                |
| [**un \_ SETPARENT de RB**](rb-setparent.md)               | Establece la ventana primaria de un control rebar. <br/>                                                                                                                                                    |
| [**\_SETTEXTCOLOR RB**](rb-settextcolor.md)         | Establece el color de texto predeterminado del control rebar. <br/>                                                                                                                                               |
| [**\_SETTOOLTIPS RB**](rb-settooltips.md)           | Asocia un control ToolTip con el control rebar. <br/>                                                                                                                                     |
| [**\_SETUNICODEFORMAT RB**](rb-setunicodeformat.md) | Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/> |
| [**\_SETWINDOWTHEME RB**](rb-setwindowtheme.md)     | Establece el estilo visual de un control rebar.<br/>                                                                                                                                                 |
| [**\_SHOWBAND RB**](rb-showband.md)                 | Muestra u oculta una banda determinada en un control rebar. <br/>                                                                                                                                          |
| [**\_SIZETORECT RB**](rb-sizetorect.md)             | Intenta encontrar el mejor diseño de las bandas del rectángulo especificado. <br/>                                                                                                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                        | Contenido                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (rebar)](nm-customdraw-rebar.md)            | Lo envía el control rebar para notificar a su ventana primaria sobre las operaciones de dibujo. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .<br/>                                                                                               |
| [NM \_ NCHITTEST (rebar)](nm-nchittest-rebar.md)              | Lo envía un control Rebar cuando el control recibe un mensaje de [**\_ NCHITTEST de WM**](/windows/desktop/inputdev/wm-nchittest) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                 |
| [NM \_ RELEASEDCAPTURE (rebar)](nm-releasedcapture-rebar-.md) | Notifica a la ventana primaria de un control rebar que el control está liberando la captura del mouse. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/>                                                                                        |
| [autobreak RBN \_](rbn-autobreak.md)                          | Notifica al elemento primario [de un rebar](rebar-controls.md) que aparecerá un salto en la barra. El elemento primario determina si se va a crear la interrupción. <br/>                                                                                                                            |
| [AutoSize de RBN \_](rbn-autosize.md)                            | Enviado por un control rebar creado con el estilo de [**\_ tamaño**](rebar-control-styles.md) automático de RBS cuando el rebar cambia automáticamente de tamaño. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                  |
| [RBN \_ BEGINDRAG](rbn-begindrag.md)                          | Lo envía un control Rebar cuando el usuario comienza a arrastrar una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                           |
| [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)                  | Se envía por un control Rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                        |
| [RBN \_ CHILDSIZE](rbn-childsize.md)                          | Se envía por un control Rebar cuando se cambia el tamaño de la ventana secundaria de una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                          |
| [RBN \_ DELETEDBAND](rbn-deletedband.md)                      | Lo envía un control rebar después de que se haya eliminado una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                  |
| [RBN \_ DELETINGBAND](rbn-deletingband.md)                    | Se envía por un control Rebar cuando una banda está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                             |
| [RBN \_ ENDDRAG](rbn-enddrag.md)                              | Lo envía un control Rebar cuando el usuario deja de arrastrar una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                            |
| [RBN \_ GETOBJECT](rbn-getobject.md)                          | Enviado por un control rebar creado con el [**estilo \_ REGISTERDROP de RBS**](rebar-control-styles.md) cuando se arrastra un objeto sobre una banda en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |
| [RBN \_ HEIGHTCHANGE](rbn-heightchange.md)                    | Se envía por un control Rebar cuando su alto ha cambiado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                    |
| [RBN \_ LAYOUTCHANGED](rbn-layoutchanged.md)                  | Lo envía un control Rebar cuando el usuario cambia el diseño de las bandas del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                        |
| [RBN \_ MinMax](rbn-minmax.md)                                | Se envía por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                       |
| [RBN \_ SPLITTERDRAG](rbn-splitterdrag.md)                    | Se envía por un control Rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                 |



 

### <a name="structures"></a>Estructuras



| Tema                                        | Contenido                                                                                                                                      |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)         | Contiene información que se usa para controlar los códigos de notificación de [ \_ tamaño automático de RBN](rbn-autosize.md) . <br/>                                   |
| [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar)                   | Contiene información que se usa para controlar varios códigos de notificación rebar. <br/>                                                           |
| [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) | Contiene información que se usa con la notificación de [RBN \_ autobreak](rbn-autobreak.md) .<br/>                                               |
| [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)     | Contiene información que se usa para controlar el código de notificación [ \_ CHEVRONPUSHED de RBN](rbn-chevronpushed.md) . <br/>                          |
| [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) | Contiene información que se usa para controlar el código de notificación [ \_ CHILDSIZE de RBN](rbn-childsize.md) . <br/>                                  |
| [**NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter)   | Contiene información que se usa para controlar un código de notificación [ \_ SPLITTERDRAG de RBN](rbn-splitterdrag.md) .<br/>                                |
| [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo)       | Contiene información específica de una operación de prueba de posicionamiento. Esta estructura se usa con el mensaje de [**RB \_ HITTEST**](rb-hittest.md) . <br/> |
| [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)       | Contiene información que define una banda en un control rebar. <br/>                                                                      |
| [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)               | Contiene información que describe las características del control rebar. <br/>                                                                |



 

### <a name="constants"></a>Constantes



| Tema                                            | Contenido                                                                                              |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Estilos de control rebar](rebar-control-styles.md) | Los controles rebar admiten una variedad de estilos de control además de los estilos de ventana estándar. <br/> |



 

 

