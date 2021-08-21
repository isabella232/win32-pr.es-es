---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl.h)
description: La transición reveal revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916a5142f09628852a016754f9fb3ad691882731466d802b8367e03837b9699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083739"
---
# <a name="wmt_videoimage_transition_reveal"></a>VÍDEO DE \_ WMTIMAGE \_ TRANSITION \_ REVEAL

La transición reveal revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parámetro</th>
<th>Miembro de estructura</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Distancia</td>
<td><strong>fEffectPara0</strong></td>
<td>Cantidad de la nueva imagen revelada, en píxeles. Este valor es relativo al lado de origen del marco.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><strong>fEffectPara1</strong></td>
<td>Dirección de la revelación. Establezca en uno de los siguientes valores:<br/>
<ul>
<li>0- Mostrar a la derecha; se origina en el lado izquierdo del marco.</li>
<li>1 - Mostrar a la izquierda; se origina en el lado derecho del marco.</li>
<li>2 - Mostrar hacia arriba; se origina en la parte inferior del marco.</li>
<li>3 - Mostrar hacia abajo; se originan en la parte superior del marco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composición</td>
<td><strong>fEffectPara2</strong></td>
<td>Establezca en uno de los siguientes valores:
<ul>
<li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li>
<li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





