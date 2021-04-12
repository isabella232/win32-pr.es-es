---
title: error de Hadoop
description: En los temas de esta sección se proporcionan las especificaciones de referencia para mensajes y notificaciones de entrada de puntero específicos.
ms.assetid: 65F4DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3e143990c65daad306ef6f743d25ef4e0cca8001
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420695"
---
# <a name="messages"></a>error de Hadoop

En los temas de esta sección se proporcionan las especificaciones de referencia para [mensajes y notificaciones de entrada de puntero](messages-and-notifications-portal.md)específicos.

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
<td>[<strong>DM_POINTERHITTEST</strong>] (dm-pointerhittest.md)<br/></td>
<td>Se envía a una ventana, cuando la entrada de puntero se detecta por primera vez, con el fin de determinar el destino de entrada más probable para la [manipulación directa](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal). <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERDOWN</strong>] (wm-ncpointerdown.md)<br/></td>
<td>Se envía cuando un puntero hace contacto sobre el área no cliente de una ventana. El mensaje se dirige a la ventana sobre la que el puntero establece contacto. El puntero se captura implícitamente en la ventana para que la ventana siga recibiendo entradas para el puntero hasta que interrumpa el contacto. <br/> Si una ventana ha capturado este puntero, este mensaje no se publica. En su lugar, se expone [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) en la ventana que ha capturado este puntero. <br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_NCPOINTERUP</strong>] (wm-ncpointerup.md)<br/></td>
<td>Se envía cuando un puntero que hizo contacto sobre el área no cliente de una ventana interrumpe el contacto. El mensaje se dirige a la ventana sobre la que el puntero hace contacto y el puntero es, en ese punto, capturado implícitamente en la ventana para que la ventana siga recibiendo entradas para el puntero hasta que interrumpa el contacto, incluida la notificación [<strong>WM_NCPOINTERUP</strong>] (WM-ncpointerup.MD). <br/> Si una ventana ha capturado este puntero, este mensaje no se publica. En su lugar, se expone [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) en la ventana que ha capturado este puntero. <br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_NCPOINTERUPDATE</strong>] (wm-ncpointerupdate.md)<br/></td>
<td>Se publica para proporcionar una actualización en un puntero que se puso en contacto sobre el área no cliente de una ventana o cuando un contacto que mantiene el mouse sin capturar se mueve sobre el área no cliente de una ventana. Mientras se mantiene el puntero, el mensaje se dirige a la ventana en la que se encuentra el puntero. Mientras el puntero se encuentra en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero se pone en contacto y la ventana continúa recibiendo entradas para el puntero hasta que interrumpe el contacto. <br/> Si una ventana ha capturado este puntero, este mensaje no se publica. En su lugar, se expone [<strong>WM_POINTERUPDATE</strong>] (WM-pointerupdate.MD) en la ventana que ha capturado este puntero.<br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_PARENTNOTIFY</strong>] (wm-parentnotify.md)<br/></td>
<td>Se envía a una ventana cuando se produce una acción significativa en una ventana descendiente. Este mensaje se ha ampliado para incluir el evento [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD). Cuando se crea la ventana secundaria, el sistema envía [<strong>WM_PARENTNOTIFY</strong>] (/Previous-Versions/Windows/Desktop/inputmsg/WM-parentnotify) justo antes de la función [<strong>CreateWindow</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowa) o [<strong>CreateWindowEx</strong>] (/Windows/Win32/API/winuser/NF-winuser-createwindowexa) que crea la ventana que devuelve. Cuando se destruye la ventana secundaria, el sistema envía el mensaje antes de que se produzca cualquier procesamiento para destruir la ventana.<br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERACTIVATE</strong>] (wm-pointeractivate.md)<br/></td>
<td>Se envía a una ventana inactiva cuando un puntero primario genera un [<strong>WM_POINTERDOWN</strong>] (WM-pointerdown.MD) en la ventana. Siempre que el mensaje permanezca no controlado, recorre la cadena de la ventana primaria hasta que llega a la ventana de nivel superior. Las aplicaciones pueden responder a este mensaje para especificar si desean que se activen.<br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERCAPTURECHANGED</strong>] (wm-pointercapturechanged.md)<br/></td>
<td>Se envía a una ventana que está perdiendo la captura de un puntero de entrada.<br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICECHANGE</strong>] (wm-pointerdevicechange.md)<br/></td>
<td>Se envía a una ventana cuando se produce un cambio en la configuración de un monitor que tiene un digitalizador adjunto. Este mensaje contiene información sobre el escalado del modo de presentación. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDEVICEINRANGE</strong>] (wm-pointerdeviceinrange.md)<br/></td>
<td>Se envía a una ventana cuando se detecta un dispositivo de puntero dentro del intervalo de un digitalizador de entrada. Este mensaje contiene información relacionada con el dispositivo y su proximidad. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERDEVICEOUTOFRANGE</strong>] (wm-pointerdeviceoutofrange.md)<br/></td>
<td>Se envía a una ventana cuando un dispositivo de puntero ha devuelto el intervalo de un digitalizador de entrada. Este mensaje contiene información relacionada con el dispositivo y su proximidad. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERDOWN</strong>] (wm-pointerdown.md)<br/></td>
<td>Se envía cuando un puntero hace contacto sobre el área de cliente de una ventana. Este mensaje de entrada se dirige a la ventana en la que el puntero hace contacto y el puntero se captura implícitamente en la ventana para que la ventana siga recibiendo entradas para el puntero hasta que se interrumpa el contacto. <br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERENTER</strong>] (wm-pointerenter.md)<br/></td>
<td>Se envía a una ventana cuando un nuevo puntero entra en el intervalo de detección sobre la ventana (se mantiene el mouse) o cuando un puntero existente se mueve dentro de los límites de la ventana. <br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERLEAVE</strong>] (wm-pointerleave.md)<br/></td>
<td>Se envía a una ventana cuando un puntero deja el intervalo de detección sobre la ventana (se mantiene el mouse) o cuando un puntero se mueve fuera de los límites de la ventana. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDAWAY</strong>] (wm-pointerroutedaway.md)<br/></td>
<td>Se produce en el proceso que recibe la entrada cuando la entrada del puntero se enruta a otro proceso.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERROUTEDRELEASED</strong>] (wm-pointerroutedreleased.md)<br/></td>
<td>Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de [<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) y no de controlar actualmente la entrada de puntero) se asocian a un identificador de puntero específico, cuando se recibe un mensaje [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) en el proceso actual. <br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERROUTEDTO</strong>] (wm-pointerroutedto.md)<br/></td>
<td>Se envía cuando la entrada de puntero continua, para un identificador de puntero existente, realiza la transición de un proceso a otro en el contenido configurado para el encadenamiento entre procesos ([<strong>AddContentWithCrossProcessChaining</strong>] (/Windows/Win32/API/directmanipulation/NF-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERUP</strong>] (wm-pointerup.md)<br/></td>
<td>Se envía cuando un puntero que hizo contacto sobre el área de cliente de una ventana interrumpe el contacto. Este mensaje de entrada se dirige a la ventana sobre la que el puntero hace contacto y el puntero es, en ese punto, capturado implícitamente en la ventana para que la ventana siga recibiendo mensajes de entrada, incluida la notificación [<strong>WM_POINTERUP</strong>] (WM-pointerup.MD) para el puntero hasta que interrumpa el contacto. <br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)). <br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERUPDATE</strong>] (wm-pointerupdate.md)<br/></td>
<td>Se publica para proporcionar una actualización en un puntero que se puso en contacto con el área de cliente de una ventana o en un puntero no capturado al mantener el mouse sobre el área cliente de una ventana. Mientras se mantiene el puntero, el mensaje se dirige a la ventana en la que se encuentra el puntero. Mientras el puntero se encuentra en contacto con la superficie, el puntero se captura implícitamente en la ventana en la que el puntero se pone en contacto y la ventana continúa recibiendo entradas para el puntero hasta que interrumpe el contacto. <br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_POINTERWHEEL</strong>] (wm-pointerwheel.md)<br/></td>
<td>Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento. <br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>[<strong>WM_POINTERHWHEEL</strong>] (wm-pointerhwheel.md)<br/></td>
<td>Se envía a la ventana con el foco de teclado en primer plano cuando se gira una rueda de desplazamiento horizontal. <br/> Una ventana recibe este mensaje a través de su función [<strong>WindowProc</strong>] (/Previous-Versions/Windows/Desktop/Legacy/ms633573 (v = vs. 85)).<br/>
<blockquote>
[!Important]<br />
Las aplicaciones de escritorio deben tener en cuenta los ppp. Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>[<strong>WM_TOUCHHITTESTING</strong>] (wm-touchhittesting.md)<br/></td>
<td>Se envía a una ventana en un toque hacia abajo para determinar el destino táctil más probable. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de mensajes de entrada de puntero](wmpointer-reference.md)
</dt> </dl>

 

