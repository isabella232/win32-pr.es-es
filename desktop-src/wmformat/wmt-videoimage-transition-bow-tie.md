---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transición de lazo revela la nueva imagen en un conjunto de triángulos en lados opuestos del marco.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678953"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>\_ \_ vinculación de lazo de transición de imagen WMT \_ \_

La transición de lazo revela la nueva imagen en un conjunto de triángulos en lados opuestos del marco.

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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ancho</td>
<td><strong>fEffectPara0</strong></td>
<td>Ancho de cada lado triangular del empate.</td>
</tr>
<tr class="even">
<td>Alto</td>
<td><strong>fEffectPara1</strong></td>
<td>Alto de cada lado triangular del empate.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><strong>fEffectPara2</strong></td>
<td>Establezca en uno de los valores siguientes:
<ul>
<li>0: especifica el efecto de empate horizontal, en el que los triángulos entran en los lados derecho e izquierdo del marco.</li>
<li>1: especifica el efecto de empate vertical, en el que los triángulos entran en la parte superior e inferior del marco.</li>
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

 

 





