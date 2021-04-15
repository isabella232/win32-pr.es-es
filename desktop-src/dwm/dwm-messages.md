---
title: Mensajes DWM
description: Esta sección contiene información sobre los mensajes de Administrador de ventanas de escritorio (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Administrador de ventanas de escritorio (DWM), referencia
- DWM (Administrador de ventanas de escritorio), referencia
- Administrador de ventanas de escritorio (DWM), mensajes
- DWM (Administrador de ventanas de escritorio), mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105714323"
---
# <a name="dwm-messages"></a>Mensajes DWM

Esta sección contiene información sobre los mensajes de Administrador de ventanas de escritorio (DWM).

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
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Informa a todas las ventanas de nivel superior que la composición DWM se ha habilitado o deshabilitado. <br/>
<blockquote>
[!Note]<br />
A partir de Windows 8, la composición DWM siempre está habilitada, por lo que este mensaje no se envía independientemente de los cambios en el modo de vídeo.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Se envía cuando cambia la Directiva de representación del área que no es de cliente.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Indica a una ventana que proporcione un mapa de bits estático para usarlo como <em>vista previa dinámica</em> (también conocida como <em>vista previa de PEEK</em>) de esa ventana.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Indica a una ventana que proporcione un mapa de bits estático para usarlo como representación en miniatura de la ventana.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Se envía cuando una ventana compuesta de DWM está maximizada.<br/></td>
</tr>
</tbody>
</table>



 

 

 





