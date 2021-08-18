---
title: 'Funciones de entrada del mouse '
description: 'Funciones de entrada del mouse '
ms.assetid: a666b25b-a75c-4500-8077-fabe07589a1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9b6abb4283ce4101b2e22c36653500db8109a0b8efbc01f9f3affe20c367a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717385"
---
# <a name="mouse-input-functions"></a>Funciones de entrada del mouse 


## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a><br/></td>
<td>Envía mensajes cuando el puntero del mouse sale de una ventana o mantiene el puntero sobre una ventana durante un período de tiempo especificado. Esta función llama <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>a TrackMouseEvent</strong></a> si existe; de lo contrario, lo emula.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-dragdetect"><strong>DragDetect</strong></a><br/></td>
<td>Captura el mouse y realiza un seguimiento de su movimiento hasta que el usuario suelta el botón primario, presiona la tecla ESC o mueve el mouse fuera del rectángulo de arrastre alrededor del punto especificado. El ancho y alto del rectángulo de <strong></strong> arrastre se especifican mediante los valores SM_CXDRAG y <strong>SM_CYDRAG</strong> devueltos por la <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics"><strong>función GetSystemMetrics.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getcapture"><strong>GetCapture</strong></a><br/></td>
<td>Recupera un identificador de la ventana (si hay alguno) que ha capturado el mouse. Solo una ventana a la vez puede capturar el mouse; esta ventana recibe la entrada del mouse tanto si el cursor está dentro de sus bordes como si no. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime"><strong>GetDoubleClickTime</strong></a><br/></td>
<td>Recupera la hora actual del doble clic del mouse. Un doble clic es una serie de dos clics del botón del mouse, el segundo se produce dentro de un tiempo especificado después del primero. El tiempo de doble clic es el número máximo de milisegundos que puede producirse entre el primer y el segundo clic de un doble clic. El tiempo máximo de doble clic es de 5000 milisegundos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getmousemovepointsex"><strong>GetMouseMovePointsEx</strong></a><br/></td>
<td>Recupera un historial de hasta 64 coordenadas anteriores del mouse o el lápiz.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a><br/></td>
<td>La <a href="/windows/desktop/api/winuser/nf-winuser-mouse_event"><strong>mouse_event</strong></a> sintetiza el movimiento del mouse y los clics de botón.<br/>
<blockquote>
[!Note]<br />
Esta función se ha reemplazado. Use <a href="/windows/desktop/api/winuser/nf-winuser-sendinput"><strong>SendInput en</strong></a> su lugar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-releasecapture"><strong>ReleaseCapture</strong></a><br/></td>
<td>Libera la captura del mouse desde una ventana del subproceso actual y restaura el procesamiento normal de entrada del mouse. Una ventana que ha capturado el mouse recibe todas las entradas del mouse, independientemente de la posición del cursor, excepto cuando se hace clic en un botón del mouse mientras la zona activa del cursor está en la ventana de otro subproceso. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setcapture"><strong>SetCapture</strong></a><br/></td>
<td>Establece la captura del mouse en la ventana especificada que pertenece al subproceso actual.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setdoubleclicktime"><strong>SetDoubleClickTime</strong></a><br/></td>
<td>Establece el tiempo de doble clic del mouse. Un doble clic es una serie de dos clics de un botón del mouse, el segundo se produce dentro de un tiempo especificado después del primero. El tiempo de doble clic es el número máximo de milisegundos que pueden producirse entre el primer y el segundo clic de un doble clic. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-swapmousebutton"><strong>SwapMouseButton</strong></a><br/></td>
<td>Invierte o restaura el significado de los botones del mouse izquierdo y derecho. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a><br/></td>
<td>Envía mensajes cuando el puntero del mouse sale de una ventana o mantiene el puntero sobre una ventana durante un período de tiempo especificado.<br/>
<blockquote>
[!Note]<br />
La <a href="/windows/win32/api/commctrl/nf-commctrl-_trackmouseevent"><strong>_TrackMouseEvent</strong></a> llama a <a href="/windows/desktop/api/winuser/nf-winuser-trackmouseevent"><strong>TrackMouseEvent</strong></a> si existe; de lo <strong>contrario, _TrackMouseEvent</strong> emula <strong>TrackMouseEvent</strong>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

