---
title: Barra de herramientas
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de herramientas.
ms.assetid: vs|controls|~\controls\toolbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0cadd2eb1560d3486073810e86a143b7fccca5
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795220"
---
# <a name="toolbar"></a>Barra de herramientas

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de herramientas.

### <a name="overviews"></a>Temas de introducción



| Tema                                                   | Contenido                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles de barra de herramientas](toolbar-controls-overview.md) | Una barra de herramientas es un control que contiene uno o varios botones. Cada botón, cuando un usuario hace clic en él, envía un mensaje de comando a la ventana primaria. Normalmente, los botones de una barra de herramientas corresponden a elementos del menú de la aplicación, lo que proporciona una forma adicional y más directa para que el usuario tenga acceso a los comandos de una aplicación.<br/> |
| [Usar controles Toolbar](using-toolbar-controls.md)    | Este tema contiene detalles de implementación y código de ejemplo para usar los controles de barra de herramientas en las aplicaciones.<br/>                                                                                                                                                                                                                  |



 

### <a name="functions"></a>Functions



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
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap"><strong>CreateMappedBitmap</strong></a></td>
<td>Crea un mapa de bits para usarlo en una barra de herramientas. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex"><strong>CreateToolbarEx</strong></a></td>
<td>Crea una ventana de barra de herramientas y agrega los botones especificados a la barra de herramientas.
<blockquote>
[!Note]<br />
Esta función está en desuso, ya que no admite todas las características de las barras de herramientas. En su lugar, use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> . Para obtener ejemplos, vea <a href="using-toolbar-controls.md">usar controles Toolbar</a>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>error de Hadoop



| Tema                                                         | Contenido                                                                                                                                                                                                |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TB \_ ADDBITMAP**](tb-addbitmap.md)                         | Agrega una o más imágenes a la lista de imágenes de botón disponibles para una barra de herramientas. <br/>                                                                                                               |
| [**TB \_ ADDBUTTONS**](tb-addbuttons.md)                       | Agrega uno o más botones a una barra de herramientas.<br/>                                                                                                                                                       |
| [**TB \_ ADDSTRING**](tb-addstring.md)                         | Agrega una nueva cadena al grupo de cadenas de la barra de herramientas.<br/>                                                                                                                                              |
| [**\_tamaño automático de TB**](tb-autosize.md)                           | Hace que se cambie el tamaño de una barra de herramientas. <br/>                                                                                                                                                             |
| [**TB \_ BUTTONCOUNT**](tb-buttoncount.md)                     | Recupera un recuento de los botones que se encuentran actualmente en la barra de herramientas. <br/>                                                                                                                                  |
| [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md)           | Especifica el tamaño de la estructura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) . <br/>                                                                                                                           |
| [**TB \_ CHANGEBITMAP**](tb-changebitmap.md)                   | Cambia el mapa de bits de un botón de una barra de herramientas.<br/>                                                                                                                                                |
| [**TB \_ CHECKBUTTON**](tb-checkbutton.md)                     | Comprueba o desactiva un botón determinado en una barra de herramientas.<br/>                                                                                                                                              |
| [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md)               | Recupera el índice de base cero para el botón asociado al identificador de comando especificado. <br/>                                                                                             |
| [**\_Personalización de TB**](tb-customize.md)                         | Muestra el cuadro de diálogo **personalizar barra de herramientas** .<br/>                                                                                                                                               |
| [**TB \_ DELETEBUTTON**](tb-deletebutton.md)                   | Elimina un botón de la barra de herramientas. <br/>                                                                                                                                                          |
| [**TB \_ ENABLEBUTTON**](tb-enablebutton.md)                   | Habilita o deshabilita el botón especificado en una barra de herramientas.<br/>                                                                                                                                       |
| [**TB \_ GETANCHORHIGHLIGHT**](tb-getanchorhighlight.md)       | Recupera el valor de resaltado de delimitador de una barra de herramientas. <br/>                                                                                                                                       |
| [**TB \_ GETBITMAP**](tb-getbitmap.md)                         | Recupera el índice del mapa de bits asociado a un botón en una barra de herramientas. <br/>                                                                                                                    |
| [**TB \_ GETBITMAPFLAGS**](tb-getbitmapflags.md)               | Recupera las marcas que describen el tipo de mapa de bits que se va a utilizar.<br/>                                                                                                                             |
| [**TB \_ GETBUTTON**](tb-getbutton.md)                         | Recupera información sobre el botón especificado en una barra de herramientas.<br/>                                                                                                                               |
| [**TB \_ GETBUTTONINFO**](tb-getbuttoninfo.md)                 | Recupera información extendida para un botón de una barra de herramientas. <br/>                                                                                                                                   |
| [**TB \_ GETBUTTONSIZE**](tb-getbuttonsize.md)                 | Recupera el ancho y el alto actuales de los botones de la barra de herramientas, en píxeles. <br/>                                                                                                                       |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)                 | Recupera el texto para mostrar de un botón de una barra de herramientas.<br/>                                                                                                                                         |
| [**TB \_ GETCOLORSCHEME**](tb-getcolorscheme.md)               | Recupera la información de la combinación de colores del control de barra de herramientas. <br/>                                                                                                                            |
| [**TB \_ GETDISABLEDIMAGELIST**](tb-getdisabledimagelist.md)   | Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar botones inactivos. <br/>                                                                                                           |
| [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)           | Recupera los estilos extendidos para un control de barra de herramientas. <br/>                                                                                                                                        |
| [**TB \_ GETHOTIMAGELIST**](tb-gethotimagelist.md)             | Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones de acceso rápido.<br/>                                                                                                                 |
| [**TB \_ GETHOTITEM**](tb-gethotitem.md)                       | Recupera el índice del elemento activo en una barra de herramientas. <br/>                                                                                                                                           |
| [**TB \_ GETIDEALSIZE**](tb-getidealsize.md)                   | Obtiene el tamaño ideal de la barra de herramientas.<br/>                                                                                                                                                          |
| [**TB \_ GETIMAGELIST**](tb-getimagelist.md)                   | Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en su estado predeterminado. Un control de barra de herramientas usa esta lista de imágenes para mostrar botones cuando no están activos o deshabilitados.<br/> |
| [**TB \_ GETIMAGELISTCOUNT**](tb-getimagelistcount.md)         | Obtiene el número de listas de imágenes asociadas a la barra de herramientas.<br/>                                                                                                                                  |
| [**TB \_ GETINSERTMARK**](tb-getinsertmark.md)                 | Recupera la marca de inserción actual de la barra de herramientas. <br/>                                                                                                                                       |
| [**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)       | Recupera el color usado para dibujar la marca de inserción de la barra de herramientas. <br/>                                                                                                                        |
| [**TB \_ GETITEMDROPDOWNRECT**](tb-getitemdropdownrect.md)     | Obtiene el rectángulo delimitador de la ventana desplegable para un elemento de barra de herramientas con la [**\_ lista desplegable**](toolbar-control-and-button-styles.md)de estilo BTNS.<br/>                                  |
| [**TB \_ GETITEMRECT**](tb-getitemrect.md)                     | Recupera el rectángulo delimitador de un botón de una barra de herramientas. <br/>                                                                                                                                  |
| [**TB \_ GETMAXSIZE**](tb-getmaxsize.md)                       | Recupera el tamaño total de todos los botones y separadores visibles en la barra de herramientas. <br/>                                                                                                       |
| [**TB \_ GETMETRICS**](tb-getmetrics.md)                       | Recupera las métricas de un control de barra de herramientas.<br/>                                                                                                                                                  |
| [**TB \_ GETOBJECT**](tb-getobject.md)                         | Recupera [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control de barra de herramientas. <br/>                                                                                                                     |
| [**TB \_ GETPADDING**](tb-getpadding.md)                       | Recupera el relleno de un control de barra de herramientas. <br/>                                                                                                                                                |
| [**TB \_ GETPRESSEDIMAGELIST**](tb-getpressedimagelist.md)     | Obtiene la lista de imágenes que usa un control de barra de herramientas para mostrar los botones en estado presionado.<br/>                                                                                                       |
| [**TB \_ GETRECT**](tb-getrect.md)                             | Recupera el rectángulo delimitador para un botón de la barra de herramientas especificado. <br/>                                                                                                                            |
| [**GB \_ GETROWS**](tb-getrows.md)                             | Recupera el número de filas de los botones de una barra de herramientas con el estilo de [**\_ ajuste TBSTYLE**](toolbar-control-and-button-styles.md) . <br/>                                        |
| [**TB \_ GETSTATE**](tb-getstate.md)                           | Recupera información sobre el estado del botón especificado en una barra de herramientas, como, por ejemplo, si está habilitado, presionado o activado. <br/>                                                             |
| [**GETSTRING de TB \_**](tb-getstring.md)                         | Recupera una cadena del grupo de cadenas de una barra de herramientas.<br/>                                                                                                                                             |
| [**. \_ GETSTYLE de TB**](tb-getstyle.md)                           | Recupera los estilos actualmente en uso para un control de barra de herramientas. <br/>                                                                                                                                |
| [**TB \_ GETTEXTROWS**](tb-gettextrows.md)                     | Recupera el número máximo de filas de texto que se pueden mostrar en un botón de la barra de herramientas. <br/>                                                                                                        |
| [**TB \_ GETTOOLTIPS**](tb-gettooltips.md)                     | Recupera el identificador del control de información sobre herramientas, si existe, asociado a la barra de herramientas. <br/>                                                                                                           |
| [**TB \_ GETUNICODEFORMAT**](tb-getunicodeformat.md)           | Recupera la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                                |
| [**TB \_ HASACCELERATOR**](tb-hasaccelerator.md)               | **Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.**<br/> Recupera un recuento de botones de la barra de herramientas que tienen el carácter de aceleración especificado. <br/>                      |
| [**TB \_ HIDEBUTTON**](tb-hidebutton.md)                       | Oculta o muestra el botón especificado en una barra de herramientas.<br/>                                                                                                                                            |
| [**TB \_ HITTEST**](tb-hittest.md)                             | Determina dónde se encuentra un punto en un control de barra de herramientas. <br/>                                                                                                                                         |
| [**TB \_ indeterminados**](tb-indeterminate.md)                 | Establece o borra el estado indeterminado del botón especificado en una barra de herramientas.<br/>                                                                                                                 |
| [**TB \_ INSERTBUTTON**](tb-insertbutton.md)                   | Inserta un botón en una barra de herramientas.<br/>                                                                                                                                                               |
| [**TB \_ INSERTMARKHITTEST**](tb-insertmarkhittest.md)         | Recupera la información de la marca de inserción para un punto de una barra de herramientas. <br/>                                                                                                                          |
| [**TB \_ ISBUTTONCHECKED**](tb-isbuttonchecked.md)             | Determina si el botón especificado de una barra de herramientas está activado. <br/>                                                                                                                            |
| [**TB \_ ISBUTTONENABLED**](tb-isbuttonenabled.md)             | Determina si el botón especificado de una barra de herramientas está habilitado. <br/>                                                                                                                            |
| [**TB \_ ISBUTTONHIDDEN**](tb-isbuttonhidden.md)               | Determina si el botón especificado de una barra de herramientas está oculto. <br/>                                                                                                                             |
| [**TB \_ ISBUTTONHIGHLIGHTED**](tb-isbuttonhighlighted.md)     | Comprueba el estado de resaltado de un botón de la barra de herramientas. <br/>                                                                                                                                             |
| [**TB \_ ISBUTTONINDETERMINATE**](tb-isbuttonindeterminate.md) | Determina si el botón especificado de una barra de herramientas es indeterminado. <br/>                                                                                                                      |
| [**TB \_ ISBUTTONPRESSED**](tb-isbuttonpressed.md)             | Determina si se presiona el botón especificado en una barra de herramientas. <br/>                                                                                                                            |
| [**TB \_ LOADIMAGES**](tb-loadimages.md)                       | Carga las imágenes de botón definidas por el sistema en la lista de imágenes de un control de barra de herramientas.<br/>                                                                                                                      |
| [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md)               | Determina el identificador del botón que corresponde al carácter de acelerador especificado.<br/>                                                                                                     |
| [**TB \_ MARKBUTTON**](tb-markbutton.md)                       | Establece el estado de resaltado de un botón determinado en un control de barra de herramientas.<br/>                                                                                                                             |
| [**TB \_ MOVEBUTTON**](tb-movebutton.md)                       | Mueve un botón de un índice a otro. <br/>                                                                                                                                                   |
| [**TB \_ PRESSBUTTON**](tb-pressbutton.md)                     | Presiona o suelta el botón especificado en una barra de herramientas.<br/>                                                                                                                                       |
| [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md)                 | Reemplaza un mapa de bits existente por un nuevo mapa de bits.<br/>                                                                                                                                               |
| [**TB \_ SAVERESTORE**](tb-saverestore.md)                     | Envíe este mensaje para iniciar el guardado o la restauración de un estado de la barra de herramientas.<br/>                                                                                                                           |
| [**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)       | Establece la configuración de resaltado de delimitador de una barra de herramientas. <br/>                                                                                                                                            |
| [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md)                 | Establece el tamaño de las imágenes de mapa de imágenes que se van a agregar a una barra de herramientas. <br/>                                                                                                                             |
| [**TB \_ SETBOUNDINGSIZE**](tb-setboundingsize.md)             | **Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.**<br/> Establece el tamaño de límite de un control de barra de herramientas de varias columnas. <br/>                                               |
| [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)                 | Establece la información de un botón existente en una barra de herramientas.<br/>                                                                                                                                    |
| [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md)                 | Establece el tamaño de los botones de una barra de herramientas.<br/>                                                                                                                                                       |
| [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md)               | Establece los anchos de botón mínimo y máximo en el control de barra de herramientas.<br/>                                                                                                                           |
| [**TB \_ SETCMDID**](tb-setcmdid.md)                           | Establece el identificador de comando de un botón de la barra de herramientas. <br/>                                                                                                                                            |
| [**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)               | Establece la información de la combinación de colores para el control de barra de herramientas. <br/>                                                                                                                                  |
| [**TB \_ SETDISABLEDIMAGELIST**](tb-setdisabledimagelist.md)   | Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar botones deshabilitados. <br/>                                                                                                          |
| [**TB \_ SETDRAWTEXTFLAGS**](tb-setdrawtextflags.md)           | Establece las marcas de dibujo de texto de la barra de herramientas. <br/>                                                                                                                                                |
| [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)           | Establece los estilos extendidos para un control de barra de herramientas. <br/>                                                                                                                                             |
| [**TB \_ SETHOTIMAGELIST**](tb-sethotimagelist.md)             | Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar los botones de acceso rápido.<br/>                                                                                                                |
| [**TB \_ SETHOTITEM**](tb-sethotitem.md)                       | Establece el elemento activo en una barra de herramientas.<br/>                                                                                                                                                              |
| [**TB \_ SETHOTITEM2**](tb-sethotitem2.md)                     | Establece el elemento activo en una barra de herramientas.<br/>                                                                                                                                                              |
| [**TB \_ SETIMAGELIST**](tb-setimagelist.md)                   | Establece la lista de imágenes que utiliza la barra de herramientas para mostrar los botones que se encuentran en su estado predeterminado.<br/>                                                                                                |
| [**TB \_ SETINDENT**](tb-setindent.md)                         | Establece la sangría del primer botón en un control de barra de herramientas. <br/>                                                                                                                             |
| [**TB \_ SETINSERTMARK**](tb-setinsertmark.md)                 | Establece la marca de inserción actual de la barra de herramientas. <br/>                                                                                                                                            |
| [**TB \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)       | Establece el color utilizado para dibujar la marca de inserción de la barra de herramientas. <br/>                                                                                                                             |
| [**TB \_ SETLISTGAP**](tb-setlistgap.md)                       | Establece la distancia entre los botones de la barra de herramientas en una barra de herramientas concreta.<br/>                                                                                                                         |
| [**TB \_ SETMAXTEXTROWS**](tb-setmaxtextrows.md)               | Establece el número máximo de filas de texto que se muestran en un botón de la barra de herramientas. <br/>                                                                                                                         |
| [**TB \_ SETMETRICS**](tb-setmetrics.md)                       | Establece las métricas de un control de barra de herramientas.<br/>                                                                                                                                                       |
| [**TB \_ SETPADDING**](tb-setpadding.md)                       | Establece el relleno de un control de barra de herramientas.<br/>                                                                                                                                                      |
| [**TB \_ SETPARENT**](tb-setparent.md)                         | Establece la ventana a la que el control de barra de herramientas envía códigos de notificación. <br/>                                                                                                                      |
| [**TB \_ SETPRESSEDIMAGELIST**](tb-setpressedimagelist.md)     | Establece la lista de imágenes que utiliza la barra de herramientas para mostrar los botones que se encuentran en estado presionado.<br/>                                                                                                    |
| [**TB \_ SETROWS**](tb-setrows.md)                             | Establece el número de filas de los botones de una barra de herramientas.<br/>                                                                                                                                             |
| [**TB \_ SETSTATE**](tb-setstate.md)                           | Establece el estado del botón especificado en una barra de herramientas.<br/>                                                                                                                                        |
| [**TB \_ SETSTYLE**](tb-setstyle.md)                           | Establece el estilo de un control de barra de herramientas. <br/>                                                                                                                                                       |
| [**TB \_ SETTOOLTIPS**](tb-settooltips.md)                     | Asocia un control ToolTip a una barra de herramientas. <br/>                                                                                                                                                |
| [**TB \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)           | Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/>    |
| [**TB \_ SETWINDOWTHEME**](tb-setwindowtheme.md)               | Establece el estilo visual de un control de barra de herramientas.<br/>                                                                                                                                                  |
| [**TB \_ TRANSLATEACCELERATOR**](tb-translateaccelerator.md)   | Pasa un mensaje de teclado a la barra de herramientas.<br/>                                                                                                                                                    |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                            | Contenido                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ Char (barra de herramientas)](nm-char-toolbar.md)                        | Enviado por la barra de herramientas cuando recibe un mensaje de tipo [**WM \_ Char**](/windows/desktop/inputdev/wm-char) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                       |
| [NM \_ clic (barra de herramientas)](nm-click-toolbar.md)                      | Se envía por un control de barra de herramientas cuando el usuario hace clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                     |
| [NM \_ CUSTOMDRAW (barra de herramientas)](nm-customdraw-toolbar.md)            | Enviado por la barra de herramientas para notificar a su ventana primaria sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                              |
| [NM \_ DBLCLK (barra de herramientas)](nm-dblclk-toolbar.md)                    | Notifica a la ventana primaria de un control de barra de herramientas que el usuario ha hace doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                             |
| [NM \_ KEYDOWN (barra de herramientas)](nm-keydown-toolbar.md)                  | Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                 |
| [NM \_ LDOWN](nm-ldown-toolbar.md)                                | Notifica a la ventana primaria de una barra de herramientas que se ha presionado el botón primario del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                        |
| [NM \_ RCLICK (barra de herramientas)](nm-rclick-toolbar.md)                    | Se envía por un control de barra de herramientas cuando el usuario hace clic en la barra de herramientas con el botón secundario del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                |
| [NM \_ RDBLCLK (barra de herramientas)](nm-rdblclk-toolbar.md)                  | Notifica a la ventana primaria de un control que el usuario ha doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                         |
| [NM \_ RELEASEDCAPTURE (barra de herramientas)](nm-releasedcapture-toolbar-.md) | Notifica a la ventana primaria de un control de la barra de herramientas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                               |
| [NM \_ TOOLTIPSCREATED (barra de herramientas)](nm-tooltipscreated-toolbar-.md) | Notifica a la ventana primaria de una barra de herramientas que la barra de herramientas ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                    |
| [TBN \_ BEGINADJUST](tbn-beginadjust.md)                          | Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a personalizar una barra de herramientas. Este código de mensaje se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ BEGINDRAG](tbn-begindrag.md)                              | Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                            |
| [TBN \_ CUSTHELP](tbn-custhelp.md)                                | Notifica a la ventana primaria de una barra de herramientas que el usuario ha elegido el botón ayuda en el cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                       |
| [TBN \_ DELETINGBUTTON](tbn-deletingbutton.md)                    | Se envía por un control de barra de herramientas cuando un botón está a punto de eliminarse. <br/>                                                                                                                                                                                                                                                |
| [TBN \_ DRAGOUT](tbn-dragout.md)                                  | Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                     |
| [TBN \_ DRAGOVER](tbn-dragover.md)                                | Determina si se debe enviar un mensaje [**TB \_ MARKBUTTON**](tb-markbutton.md) para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                           |
| [\_lista desplegable TBN](tbn-dropdown.md)                                | Se envía por un control de barra de herramientas cuando el usuario hace clic en un botón desplegable. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                     |
| [TBN \_ DUPACCELERATOR](tbn-dupaccelerator.md)                    | Determina si se puede usar una tecla de aceleración en dos o más barras de herramientas activas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                      |
| [TBN \_ ENDADJUST](tbn-endadjust.md)                              | Notifica a la ventana primaria de una barra de herramientas que el usuario ha detenido la personalización de una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                   |
| [TBN \_ ENDDRAG](tbn-enddrag.md)                                  | Notifica a la ventana primaria de la barra de herramientas que el usuario ha dejado de arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                        |
| [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md)                      | Recupera información de personalización de la barra de herramientas y notifica a la ventana primaria de la barra de herramientas los cambios realizados en la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ GETDISPINFO](tbn-getdispinfo.md)                          | Recupera información de presentación de un elemento de la barra de herramientas. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                                                           |
| [TBN \_ GETINFOTIP](tbn-getinfotip.md)                            | Recupera información de recuadro informativo para un elemento de la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                                                      |
| [TBN \_ GETOBJECT](tbn-getobject.md)                              | Se envía mediante un control de barra de herramientas que usa el estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar un objeto de destino de colocación cuando el puntero pasa sobre uno de sus botones. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/> |
| [TBN \_ HOTITEMCHANGE](tbn-hotitemchange.md)                      | Se envía por un control de barra de herramientas cuando cambia el elemento activo (resaltado). Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                    |
| [TBN \_ INITCUSTOMIZE](tbn-initcustomize.md)                      | Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                                       |
| [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md)                    | Solicita el índice del botón en la barra de herramientas correspondiente al carácter acelerador especificado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                  |
| [TBN \_ QUERYDELETE](tbn-querydelete.md)                          | Notifica a la ventana primaria de la barra de herramientas si se puede eliminar un botón de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                        |
| [TBN \_ QUERYINSERT](tbn-queryinsert.md)                          | Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario está personalizando una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                     |
| [restablecimiento de TBN \_](tbn-reset.md)                                      | Notifica a la ventana primaria de la barra de herramientas que el usuario ha restablecido el contenido del cuadro de diálogo Personalizar barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                          |
| [restauración de TBN \_](tbn-restore.md)                                  | Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                 |
| [TBN \_ Guardar](tbn-save.md)                                        | Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de guardarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                    |
| [TBN \_ TOOLBARCHANGE](tbn-toolbarchange.md)                      | Notifica a la ventana primaria de la barra de herramientas que el usuario ha personalizado una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                          |
| [TBN \_ WRAPACCELERATOR](tbn-wrapaccelerator.md)                  | Solicita el índice del botón en una o más barras de herramientas correspondientes al carácter de aceleración especificado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                         |
| [TBN \_ WRAPHOTITEM](tbn-wraphotitem.md)                          | Notifica a una aplicación con dos o más barras de herramientas que el elemento activo va a cambiar. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                                                                                                                                |



 

### <a name="structures"></a>Estructuras



| Tema                                      | Contenido                                                                                                                                                                                                                                                                |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COLORMAP**](/windows/desktop/api/Commctrl/ns-commctrl-colormap)               | Contiene información usada por la función [**CreateMappedBitmap**](/windows/desktop/api/Commctrl/nf-commctrl-createmappedbitmap) para asignar los colores del mapa de bits. <br/>                                                                                                                                 |
| [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)   | Contiene información específica de un código de notificación de [nm \_ CUSTOMDRAW](nm-customdraw-toolbar.md) enviado por un control de barra de herramientas. <br/>                                                                                                                                |
| [**NMTBDISPINFO**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbdispinfoa)       | Contiene y recibe información de presentación para un elemento de la barra de herramientas. Esta estructura se usa con el código de notificación [ \_ GETDISPINFO de TBN](tbn-getdispinfo.md) . <br/>                                                                                                    |
| [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)   | Contiene y recibe información de recuadro informativo para un elemento de la barra de herramientas. Esta estructura se usa con el código de notificación [ \_ GETINFOTIP de TBN](tbn-getdispinfo.md) . <br/>                                                                                                     |
| [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem)         | Contiene información que se usa con el código de notificación [ \_ HOTITEMCHANGE de TBN](tbn-hotitemchange.md) . <br/>                                                                                                                                                           |
| [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)         | Permite a las aplicaciones extraer la información que se colocó en [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave) cuando se guardó el estado de la barra de herramientas. Esta estructura se pasa a las aplicaciones cuando reciben un código de notificación de [ \_ restauración de TBN](tbn-restore.md) .<br/>             |
| [**NMTBSAVE**](/windows/win32/api/commctrl/ns-commctrl-nmtbsave)               | Esta estructura se pasa a las aplicaciones cuando reciben un código de notificación de [ \_ guardar de TBN](tbn-save.md) . Contiene información sobre el botón que se está guardando actualmente. Las aplicaciones pueden modificar los valores de los miembros para guardar información adicional. <br/> |
| [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)             | Contiene información que se usa para procesar los códigos de notificación de la barra de herramientas. Esta estructura reemplaza a la estructura **TBNOTIFY** . <br/>                                                                                                                                      |
| [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap)         | Agrega un mapa de bits que contiene imágenes de botón a una barra de herramientas.<br/>                                                                                                                                                                                                      |
| [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton)               | Contiene información sobre un botón de una barra de herramientas.<br/>                                                                                                                                                                                                            |
| [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa)       | Contiene o recibe información de un botón específico en una barra de herramientas.<br/>                                                                                                                                                                                         |
| [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)       | Contiene información sobre la marca de inserción en un control de barra de herramientas. <br/>                                                                                                                                                                                            |
| [**TBMETRICS**](/windows/desktop/api/Commctrl/ns-commctrl-tbmetrics)             | Define las métricas de una barra de herramientas que se usan para reducir o expandir los elementos de la barra de herramientas.<br/>                                                                                                                                                                            |
| [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) | Se usa con el mensaje [**TB \_ REPLACEBITMAP**](tb-replacebitmap.md) para reemplazar un mapa de bits de la barra de herramientas por otro.<br/>                                                                                                                                              |
| [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa)       | Especifica la ubicación en el registro donde el mensaje [**TB \_ SAVERESTORE**](tb-saverestore.md) almacena y recupera información sobre el estado de una barra de herramientas. <br/>                                                                                           |



 

### <a name="constants"></a>Constantes



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
<td><a href="toolbar-button-states.md">Estados del botón de la barra de herramientas</a></td>
<td>En esta sección se enumeran los Estados que puede tener un botón de la barra de herramientas. <br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-control-and-button-styles.md">Controles de barra de herramientas y estilos de botón</a></td>
<td>Los siguientes estilos de ventana son específicos de las barras de herramientas. Se combinan con otros estilos de ventana cuando se crea la barra de herramientas.<br/> <strong>Nota:</strong> En el caso de los controles comunes <a href="common-control-versions.md">versión 6,00</a>, si se usa un <a href="themes-overview.md">estilo visual</a> con la barra de herramientas, los botones siempre son transparentes independientemente de la configuración de estilo. De lo contrario, el comportamiento de transparencia es normal como se indica mediante el uso de la <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_FLAT</strong></a> o el estilo de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_TRANSPARENT</strong></a> .
<blockquote>
[!Note]<br />
Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior. Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="toolbar-extended-styles.md">Estilos extendidos de barra de herramientas</a></td>
<td>En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.<br/></td>
</tr>
<tr class="even">
<td><a href="toolbar-standard-button-image-index-values.md">Valores de índice de imagen de botón estándar de la barra de herramientas</a></td>
<td>En esta sección se especifican valores de índice de imágenes dentro de mapas de bits estándar.<br/></td>
</tr>
</tbody>
</table>



 

