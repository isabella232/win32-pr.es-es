---
title: Estilos de control de barra de progreso (CommCtrl. h)
description: Los controles de barra de progreso admiten los siguientes estilos de control
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660559"
---
# <a name="progress-bar-control-styles"></a>Estilos de control de barra de progreso

Los controles de [barra de progreso](progress-bar-control.md) admiten los siguientes estilos de control:



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
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6,0</a> o posterior. El indicador de progreso no aumenta de tamaño, sino que se mueve repetidamente a lo largo de la longitud de la barra, lo que indica una actividad sin especificar la proporción del progreso que se ha completado. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior. Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 4,70</a> o posterior. La barra de progreso muestra el estado del progreso en una barra de desplazamiento suave en lugar de en la barra segmentada predeterminada. <br/>
<blockquote>
[!Note]<br />
Este estilo solo se admite en el tema clásico de Windows. Todos los demás temas invalidan este estilo.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6,0</a> o posterior y <strong>Windows Vista.</strong> Determina el comportamiento de animación que la barra de progreso debe utilizar al retroceder (de un valor superior a un valor inferior). Si se establece, se &quot; &quot; producirá una transición suave; de lo contrario, el control &quot; saltará &quot; al valor inferior.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 4,70</a> o posterior. La barra de progreso muestra el estado de progreso verticalmente, de abajo a arriba.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Puede establecer estilos de barra de progreso, de la misma manera que otros controles comunes, con [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

