---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transición Mostrar revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL formato de Windows Media
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
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650065"
---
# <a name="wmt_videoimage_transition_reveal"></a>transición de imagen de transmisión de \_ imágenes WMT \_ \_

La transición Mostrar revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.



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
<td>Dirección de la revelación. Establezca en uno de los valores siguientes:<br/>
<ul>
<li>0: mostrar a la derecha; se origina desde el lado izquierdo del marco.</li>
<li>1: mostrar a la izquierda; se origina desde el lado derecho del marco.</li>
<li>2-revelar hacia arriba; se origina desde la parte inferior del marco.</li>
<li>3-revelar hacia abajo; se origina desde la parte superior del marco.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composición</td>
<td><strong>fEffectPara2</strong></td>
<td>Establezca en uno de los valores siguientes:
<ul>
<li>0: especifica una composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li>
<li>1: especifica una composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Transiciones de imagen de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





