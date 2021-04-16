---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: La transición de la rueda revela la nueva imagen al girar cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650207"
---
# <a name="wmt_videoimage_transition_wheel"></a>\_rueda de transición de VIDEOIMAGE WMT \_ \_

La transición de la rueda revela la nueva imagen al girar cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.

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
<td>Coordenada X, relativa al fotograma de vídeo, del centro del efecto de la rueda.</td>
</tr>
<tr class="even">
<td>Centrar Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada y, en relación con el fotograma de vídeo, del centro del efecto de la rueda.</td>
</tr>
<tr class="odd">
<td>Ángulo</td>
<td><strong>fEffectPara2</strong></td>
<td>Ángulo de giro, en grados, de los radios del efecto de la rueda. Un valor de 0,0 indica la imagen antigua sin que se revele ninguna de las imágenes nuevas. Un valor de 90,0 indica que la nueva imagen se ha revelado por completo. El movimiento de 0,0 a 90,0 aparece como rotación en el sentido de las agujas del reloj de los radios.<br/></td>
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

 

 





