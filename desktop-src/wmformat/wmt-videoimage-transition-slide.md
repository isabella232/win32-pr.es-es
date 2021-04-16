---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: La transición de diapositivas revela la nueva imagen deslizando la imagen antigua fuera del marco.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649791"
---
# <a name="wmt_videoimage_transition_slide"></a>diapositiva de transición de \_ imagen WMT \_ \_

La transición de diapositivas revela la nueva imagen deslizando la imagen antigua fuera del marco.

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
<td>Distancia, en píxeles, que la imagen antigua desliza fuera del marco.</td>
</tr>
<tr class="even">
<td>Dirección</td>
<td><strong>fEffectPara1</strong></td>
<td>Dirección en la que se desplaza la imagen anterior. Establezca en uno de los valores siguientes:<br/>
<ul>
<li>0: diapositiva a la derecha.</li>
<li>1: Deslice hacia la izquierda.</li>
<li>2-deslizar hacia arriba.</li>
<li>3-deslizar hacia abajo.</li>
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

 

 





