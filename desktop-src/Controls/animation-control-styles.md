---
title: Estilos de control de animación (CommCtrl. h)
description: En esta sección se enumeran los estilos de ventana utilizados con los controles de animación.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660539"
---
# <a name="animation-control-styles"></a>Estilos de control de animación

En esta sección se enumeran los estilos de ventana utilizados con los controles de animación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Comienza a reproducir la animación en cuanto se abre el clip AVI. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centra la animación en la ventana del control de animación. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">De forma predeterminada, el control crea un subproceso para reproducir el clip AVI. Si establece esta marca, el control reproduce el clip sin crear un subproceso; internamente, el control usa un temporizador Win32 para sincronizar la reproducción. <br/> <strong>Comctl32.dll versión 6 y posteriores:</strong> Este estilo no es compatible. De forma predeterminada, el control reproduce el clip AVI sin crear un subproceso.<br/>
<blockquote>
[!Note]<br />
Comctl32.dll versión 6 no es redistribuible. Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Permite hacer coincidir el color de fondo de una animación con el de la ventana subyacente, creando un &quot; &quot; fondo transparente. El elemento primario del control Animation no debe tener el estilo WS_CLIPCHILDREN (vea <a href="/windows/desktop/winmsg/window-styles">estilos de ventana</a>). El control envía un mensaje <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> a su elemento primario. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> para establecer el color de fondo del contexto de dispositivo en un valor adecuado. El control interpreta el píxel superior izquierdo del primer fotograma como el color de fondo predeterminado de la animación. Reasignará todos los píxeles con ese color al valor proporcionado en respuesta a WM_CTLCOLORSTATIC. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



