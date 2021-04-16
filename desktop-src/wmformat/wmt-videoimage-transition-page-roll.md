---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transición de avance de página transforma la imagen anterior con un efecto de volteo de página, que revela la nueva imagen debajo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649575"
---
# <a name="wmt_videoimage_transition_page_roll"></a>\_rollo de página de transición de VIDEOIMAGE WMT \_ \_ \_

La transición de avance de página transforma la imagen anterior con un efecto de volteo de página, que revela la nueva imagen debajo.

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
<td>Radio</td>
<td><strong>fEffectPara0</strong></td>
<td>Radio del efecto de relanzamiento de página.</td>
</tr>
<tr class="even">
<td>Distancia</td>
<td><strong>fEffectPara1</strong></td>
<td>Cantidad de la nueva imagen revelada por el efecto de relanzamiento de página, en píxeles.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><strong>fEffectPara2</strong></td>
<td>Esquina o lado del fotograma del vídeo desde el que se origina el lanzamiento de la página. Establezca en uno de los valores siguientes:<br/>
<ul>
<li>0: lado izquierdo</li>
<li>1-lado derecho</li>
<li>2-inferior</li>
<li>3-superior</li>
<li>4: esquina inferior izquierda</li>
<li>5: esquina inferior derecha</li>
<li>6: esquina superior izquierda</li>
<li>7: esquina superior derecha</li>
</ul></td>
</tr>
<tr class="even">
<td>Composición</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





