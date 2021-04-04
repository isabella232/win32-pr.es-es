---
title: Scroll Bar
description: Esta sección contiene información sobre los elementos de programación utilizados con barras de desplazamiento.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cf549a37fd5d4a271f6e12642a9bfd45b65d79
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794104"
---
# <a name="scroll-bar"></a>Scroll Bar

Esta sección contiene información sobre los elementos de programación utilizados con barras de desplazamiento. Una ventana puede mostrar un objeto de datos, como un documento o un mapa de bits, que es mayor que el área cliente de la ventana. Cuando se proporciona con una *barra de desplazamiento*, el usuario puede desplazarse por un objeto de datos en el área cliente para mostrar las partes del objeto que se extienden más allá de los bordes de la ventana.

### <a name="overviews"></a>Temas de introducción



| Tema                                      | Contenido                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de las barras de desplazamiento](about-scroll-bars.md) | Una barra de desplazamiento consta de un eje sombreado con un botón de flecha en cada extremo y un *cuadro de desplazamiento* (a veces denominado control de posición) entre los botones de flecha.<br/>                                                                                                                                                                     |
| [Usar barras de desplazamiento](using-scroll-bars.md) | Al crear una ventana superpuesta, emergente o secundaria, puede Agregar barras de desplazamiento estándar mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)o ambos estilos.<br/> |



 

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
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> habilita o deshabilita una o ambas flechas de la barra de desplazamiento. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a> recupera información sobre la barra de desplazamiento especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> recupera los parámetros de una barra de desplazamiento, incluidas las posiciones de desplazamiento mínima y máxima, el tamaño de página y la posición del cuadro de desplazamiento (Thumb).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> recupera la posición actual del cuadro de desplazamiento (Thumb) en la barra de desplazamiento especificada. La posición actual es un valor relativo que depende del intervalo de desplazamiento actual. Por ejemplo, si el intervalo de desplazamiento es de 0 a 100 y el cuadro de desplazamiento está en el centro de la barra, la posición actual es 50.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> se proporciona para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> recupera las posiciones mínima y máxima del cuadro de desplazamiento (Thumb) actual para la barra de desplazamiento especificada.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> solo se proporciona por compatibilidad. Las nuevas aplicaciones deben usar la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a> desplaza un rectángulo de bits horizontal y verticalmente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> desplaza el contenido del área de cliente de la ventana especificada.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> se proporciona para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar la función <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> desplaza el contenido del área de cliente de la ventana especificada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> establece los parámetros de una barra de desplazamiento, incluidas las posiciones de desplazamiento mínima y máxima, el tamaño de página y la posición del cuadro de desplazamiento (Thumb). La función también vuelve a dibujar la barra de desplazamiento, si se solicita.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> establece la posición del cuadro de desplazamiento (Thumb) en la barra de desplazamiento especificada y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> se proporciona para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> establece las posiciones mínima y máxima del cuadro de desplazamiento para la barra de desplazamiento especificada.
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> se proporciona para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>La función <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> muestra u oculta la barra de desplazamiento especificada. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_flechas de habilitación de SBM \_**](sbm-enable-arrows.md)      | Una aplicación envía el mensaje de [**\_ \_ flechas habilitar SBM**](sbm-enable-arrows.md) para habilitar o deshabilitar una o ambas flechas de un control de barra de desplazamiento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SBM \_ GETPOS**](sbm-getpos.md)                     | El mensaje [**SBM \_ GETPOS**](sbm-getpos.md) se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento. La posición actual es un valor relativo que depende del intervalo de desplazamiento actual. Por ejemplo, si el intervalo de desplazamiento es de 0 a 100 y el cuadro de desplazamiento está en el centro de la barra, la posición actual es 50. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollPos** funcione correctamente.<br/> |
| [**SBM \_ GETRANGE**](sbm-getrange.md)                 | El mensaje [**SBM \_ GETRANGE**](sbm-getrange.md) se envía para recuperar los valores de posición mínimo y máximo del control de barra de desplazamiento. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollRange** funcione correctamente.<br/>                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLBARINFO**](sbm-getscrollbarinfo.md) | Lo envía una aplicación para recuperar información sobre la barra de desplazamiento especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)       | El mensaje [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md) se envía para recuperar los parámetros de una barra de desplazamiento. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **GetScrollInfo** funcione correctamente.<br/>                                                                                                                                                                                                                                           |
| [**SBM \_ SETPOS**](sbm-setpos.md)                     | El mensaje [**SBM \_ SETPOS**](sbm-setpos.md) se envía para establecer la posición del cuadro de desplazamiento (Thumb) y, si se solicita, vuelve a dibujar la barra de desplazamiento para reflejar la nueva posición del cuadro de desplazamiento. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollPos** funcione correctamente.<br/>                                                                                                                                                                  |
| [**SBM \_ SetRange**](sbm-setrange.md)                 | El mensaje [**SBM \_ SetRange**](sbm-setrange.md) se envía para establecer los valores de posición mínimo y máximo del control de barra de desplazamiento. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollRange** funcione correctamente.<br/>                                                                                                                                                                                                                   |
| [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)     | Una aplicación envía el mensaje [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md) a un control de barra de desplazamiento para establecer los valores de posición mínimo y máximo y para volver a dibujar el control.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)       | El mensaje [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md) se envía para establecer los parámetros de una barra de desplazamiento. <br/> Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollInfo** funcione correctamente.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CTLCOLORSCROLLBAR de WM \_**](wm-ctlcolorscrollbar.md) | El mensaje de [**\_ CTLCOLORSCROLLBAR de WM**](wm-ctlcolorscrollbar.md) se envía a la ventana primaria de un control de barra de desplazamiento cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de presentación para establecer el color de fondo del control de barra de desplazamiento. <br/> Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**HSCROLL de WM \_**](wm-hscroll.md)                     | El mensaje de [**\_ HSCROLL de WM**](wm-hscroll.md) se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento horizontal estándar de la ventana. Este mensaje también se envía al propietario de un control de barra de desplazamiento horizontal cuando se produce un evento de desplazamiento en el control. <br/> Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                        |
| [**VSCROLL de WM \_**](wm-vscroll.md)                     | El mensaje de [**\_ VSCROLL de WM**](wm-vscroll.md) se envía a una ventana cuando se produce un evento de desplazamiento en la barra de desplazamiento vertical estándar de la ventana. Este mensaje también se envía al propietario de un control de barra de desplazamiento vertical cuando se produce un evento de desplazamiento en el control. <br/> Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                            |



 

### <a name="structures"></a>Estructuras



| Tema                                  | Contenido                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | La estructura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) contiene información de la barra de desplazamiento.<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | La estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) contiene los parámetros de la barra de desplazamiento que va a establecer la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) (o el mensaje [**SBM \_ SetScrollInfo**](sbm-setscrollinfo.md) ) o que se puede recuperar mediante la función [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) (o el mensaje [**SBM \_ GetScrollInfo**](sbm-getscrollinfo.md) ). <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                                      | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de control de barra de desplazamiento](scroll-bar-control-styles.md) | Para crear un control de barra de desplazamiento mediante la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique la clase ScrollBar, las constantes de estilo de ventana apropiadas y una combinación de los siguientes estilos de control de barra de desplazamiento. Algunos de los estilos crean un control de barra de desplazamiento que usa un ancho o un alto predeterminados. Sin embargo, siempre debe especificar las coordenadas x e y y las demás dimensiones de la barra de desplazamiento cuando llame a **CreateWindow** o a **CreateWindowEx**. <br/> |



 

 

