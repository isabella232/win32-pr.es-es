---
title: Barra de estado
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de estado.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794769"
---
# <a name="status-bar"></a>Barra de estado

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles de barra de estado.

### <a name="overviews"></a>Temas de introducción



| Tema                          | Contenido                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de estado](status-bars.md) | Una *barra de estado* es una ventana horizontal situada en la parte inferior de una ventana primaria en la que una aplicación puede mostrar diversos tipos de información de estado.<br/> |



 

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
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></td>
<td>Crea una ventana de estado, que se utiliza normalmente para mostrar el estado de una aplicación. La ventana aparece generalmente en la parte inferior de la ventana primaria y contiene el texto especificado.
<blockquote>
[!Note]<br />
Esta función está obsoleta. Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> en su lugar.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></td>
<td>La función <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> dibuja el texto especificado en el estilo de una ventana de estado con bordes.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></td>
<td>Procesa <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> y <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensajes y muestra texto de ayuda sobre el menú actual en la ventana de estado especificada.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>error de Hadoop



| Tema                                               | Contenido                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETBORDERS**](sb-getborders.md)             | Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado. <br/>                                                                                                  |
| [**SB \_ GETICON**](sb-geticon.md)                   | Recupera el icono de un elemento en una barra de estado. <br/>                                                                                                                                           |
| [**SB \_ GETPARTS**](sb-getparts.md)                 | Recupera un recuento de los elementos de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número especificado de partes. <br/>                                         |
| [**SB \_ GETRECT**](sb-getrect.md)                   | Recupera el rectángulo delimitador de un elemento de una ventana de estado. <br/>                                                                                                                           |
| [**GETTEXT de SB \_**](sb-gettext.md)                   | El [**mensaje \_ GETTEXT de SB**](sb-gettext.md) recupera el texto de la parte especificada de una ventana de estado. <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | El [**mensaje \_ GETTEXTLENGTH de SB**](sb-gettextlength.md) recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado. <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado se debe crear con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas. <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | Recupera la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                             |
| [**SB \_ ISSIMPLE**](sb-issimple.md)                 | Comprueba un control de barra de estado para determinar si está en modo simple. <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | Establece el color de fondo de una barra de estado. <br/>                                                                                                                                               |
| [**SB \_ SETICON**](sb-seticon.md)                   | Establece el icono de un elemento en una barra de estado. <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | Establece el alto mínimo del área de dibujo de una ventana de estado. <br/>                                                                                                                               |
| [**SB \_ SETPARTS**](sb-setparts.md)                 | Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte. <br/>                                                                                           |
| [**SETTEXT de SB \_**](sb-settext.md)                   | El \_ mensaje SETTEXT de SB establece el texto de la parte especificada de una ventana de estado.<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | Establece el texto de información sobre herramientas para un elemento de una barra de estado. La barra de estado se debe haber creado con el estilo de [**\_ información sobre herramientas de SBT**](status-bar-styles.md) para habilitar la información sobre herramientas.<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/> |
| [**SB \_ simple**](sb-simple.md)                     | Especifica si una ventana de estado muestra texto simple o muestra todos los elementos de ventana establecidos por un mensaje [**\_ SETPARTS de SB**](sb-setparts.md) anterior. <br/>                                       |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                 | Contenido                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ haga clic (barra de estado)](nm-click-status-bar.md)     | Notifica a la ventana primaria de un control de barra de estado que el usuario ha pulsado el botón primario del mouse en el control. [Nm \_ Haga clic en (barra de estado)](nm-click-status-bar.md) se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .<br/>              |
| [NM \_ DBLCLK (barra de estado)](nm-dblclk-status-bar.md)   | Notifica a la ventana primaria de un control de barra de estado que el usuario ha haga doble clic en el botón primario del mouse dentro del control. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .<br/>                                       |
| [NM \_ RCLICK (barra de estado)](nm-rclick-status-bar.md)   | Notifica a la ventana primaria de un control de barra de estado que el usuario ha hace clic con el botón secundario del mouse en el control. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .<br/>                                             |
| [NM \_ RDBLCLK (barra de estado)](nm-rdblclk-status-bar.md) | Notifica a las ventanas principales de un control de barra de estado que el usuario hizo doble clic con el botón secundario del mouse en el control. [Nm \_ RDBLCLK (barra de estado)](nm-rdblclk-status-bar.md) se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Lo envía un control de barra de estado cuando cambia el modo simple debido a un mensaje [**\_ simple de SB**](sb-simple.md) . Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/>                                                        |



 

### <a name="constants"></a>Constantes



| Tema                                      | Contenido                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Estilos de barra de estado](status-bar-styles.md) | En esta sección se enumeran los estilos, además de los estilos de ventana estándar, que admiten los controles de *barra de estado* . <br/> |



 

 

