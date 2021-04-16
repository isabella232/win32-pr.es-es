---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transición dividida revela la nueva imagen dividiendo la imagen anterior. La división aparece a lo largo de una línea recta horizontal o vertical que comienza dentro del marco.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649790"
---
# <a name="wmt_videoimage_transition_split"></a>División de transición de imagen de videotransmisión WMT \_ \_ \_

La transición dividida revela la nueva imagen dividiendo la imagen anterior. La división aparece a lo largo de una línea recta horizontal o vertical que comienza dentro del marco.

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
<td>Centrar X</td>
<td><strong>fEffectPara0</strong></td>
<td>Coordenada X, relativa al fotograma de vídeo, de la línea de origen de la división.</td>
</tr>
<tr class="even">
<td>Centrar Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada y, en relación con el fotograma de vídeo, de la línea de origen de la división.</td>
</tr>
<tr class="odd">
<td>Distancia</td>
<td><strong>fEffectPara2</strong></td>
<td>Ancho de la división en píxeles.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><strong>fEffectPara3</strong></td>
<td>Orientación de la división. Establezca en uno de los valores siguientes:<br/>
<ul>
<li>0: se divide a lo largo de una línea horizontal.</li>
<li>1: divide a lo largo de una línea vertical.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composición</td>
<td><strong>fEffectPara4</strong></td>
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

 

 





