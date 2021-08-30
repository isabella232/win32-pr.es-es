---
title: Barra de estado
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de barra de estado.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8e1b4119754d524bccfbe4153e12783d9bd38d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467092"
---
# <a name="status-bar"></a>Barra de estado

Esta sección contiene información sobre los elementos de programación utilizados con controles de barra de estado.

### <a name="overviews"></a>Temas de introducción



| Tema                          | Contenido                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de estado](status-bars.md) | Una *barra de estado* es una ventana horizontal en la parte inferior de una ventana primaria en la que una aplicación puede mostrar varios tipos de información de estado.<br/> |



 

### <a name="functions"></a>Functions




| Tema | Contenido | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a> | Crea una ventana de estado, que normalmente se usa para mostrar el estado de una aplicación. Por lo general, la ventana aparece en la parte inferior de la ventana primaria y contiene el texto especificado.<blockquote>[!Note]<br />Esta función está obsoleta. Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow en</strong></a> su lugar.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> | La <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>función DrawStatusText</strong></a> dibuja el texto especificado en el estilo de una ventana de estado con bordes.<br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a> | Procesa <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> y <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> y muestra el texto de ayuda sobre el menú actual en la ventana de estado especificada.<br /> | 




 

### <a name="messages"></a>Mensajes



| Tema                                               | Contenido                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SB \_ GETBORDERS**](sb-getborders.md)             | Recupera los anchos actuales de los bordes horizontal y vertical de una ventana de estado. <br/>                                                                                                  |
| [**SB \_ GETICON**](sb-geticon.md)                   | Recupera el icono de un elemento de una barra de estado. <br/>                                                                                                                                           |
| [**SB \_ GETPARTS**](sb-getparts.md)                 | Recupera un recuento de las partes de una ventana de estado. El mensaje también recupera la coordenada del borde derecho del número especificado de partes. <br/>                                         |
| [**SB \_ GETRECT**](sb-getrect.md)                   | Recupera el rectángulo delimitador de un elemento en una ventana de estado. <br/>                                                                                                                           |
| [**SB \_ GETTEXT**](sb-gettext.md)                   | El [**mensaje \_ SB GETTEXT**](sb-gettext.md) recupera el texto de la parte especificada de una ventana de estado. <br/>                                                                             |
| [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md)       | El [**mensaje SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera la longitud, en caracteres, del texto de la parte especificada de una ventana de estado. <br/>                                   |
| [**SB \_ GETTIPTEXT**](sb-gettiptext.md)             | Recupera el texto de información sobre herramientas de un elemento de una barra de estado. La barra de estado debe crearse con el estilo [**SBT \_ TOOLTIPS**](status-bar-styles.md) para habilitar la información sobre herramientas. <br/>         |
| [**SB \_ GETUNICODEFORMAT**](sb-getunicodeformat.md) | Recupera la marca de formato de caracteres Unicode para el control . <br/>                                                                                                                             |
| [**SB \_ ISSIMPLE**](sb-issimple.md)                 | Comprueba un control de barra de estado para determinar si está en modo simple. <br/>                                                                                                                        |
| [**SB \_ SETBKCOLOR**](sb-setbkcolor.md)             | Establece el color de fondo en una barra de estado. <br/>                                                                                                                                               |
| [**SB \_ SETICON**](sb-seticon.md)                   | Establece el icono de un elemento en una barra de estado. <br/>                                                                                                                                                |
| [**SB \_ SETMINHEIGHT**](sb-setminheight.md)         | Establece el alto mínimo del área de dibujo de una ventana de estado. <br/>                                                                                                                               |
| [**SB \_ SETPARTS**](sb-setparts.md)                 | Establece el número de partes de una ventana de estado y la coordenada del borde derecho de cada parte. <br/>                                                                                           |
| [**SB \_ SETTEXT**](sb-settext.md)                   | El mensaje \_ SB SETTEXT establece el texto en la parte especificada de una ventana de estado.<br/>                                                                                                           |
| [**SB \_ SETTIPTEXT**](sb-settiptext.md)             | Establece el texto de información sobre herramientas de un elemento en una barra de estado. La barra de estado debe haber sido creada con el estilo [**SBT \_ TOOLTIPS**](status-bar-styles.md) para habilitar la información sobre herramientas.<br/>        |
| [**SB \_ SETUNICODEFORMAT**](sb-setunicodeformat.md) | Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. <br/> |
| [**SB \_ SIMPLE**](sb-simple.md)                     | Especifica si una ventana de estado muestra texto simple o muestra todas las partes de la ventana establecidas por un mensaje [**SB \_ SETPARTS**](sb-setparts.md) anterior. <br/>                                       |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                 | Contenido                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CLICK (barra de estado)](nm-click-status-bar.md)     | Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho clic en el botón izquierdo del mouse dentro del control. [NM \_ CLICK (barra de estado)](nm-click-status-bar.md) se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>              |
| [NM \_ DBLCLK (barra de estado)](nm-dblclk-status-bar.md)   | Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho doble clic en el botón izquierdo del mouse dentro del control. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                       |
| [NM \_ RCLICK (barra de estado)](nm-rclick-status-bar.md)   | Notifica a la ventana primaria de un control de barra de estado que el usuario ha hecho clic en el botón derecho del mouse dentro del control. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                                             |
| [NM \_ RDBLCLK (barra de estado)](nm-rdblclk-status-bar.md) | Notifica a las ventanas primarias de un control de barra de estado que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. [NM \_ RDBLCLK (barra de estado)](nm-rdblclk-status-bar.md) se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/> |
| [SBN \_ SIMPLEMODECHANGE](sbn-simplemodechange.md)     | Enviado por un control de barra de estado cuando cambia el modo simple debido a un [**mensaje SB \_ SIMPLE.**](sb-simple.md) Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                        |



 

### <a name="constants"></a>Constantes



| Tema                                      | Contenido                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Estilos de barra de estado](status-bar-styles.md) | En esta sección se enumeran los estilos, además de los estilos de ventana estándar, admitidos por los *controles de barra de* estado. <br/> |



 

 

