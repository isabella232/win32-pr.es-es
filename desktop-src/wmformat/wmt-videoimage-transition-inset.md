---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl.h)
description: La transición de conjunto revela la nueva imagen en un rectángulo que se origina en una esquina del marco.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f815e0bb1fc7e8e1cba277f68b7950af2b20395092b69b2c07ebb7ac51367da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843794"
---
# <a name="wmt_videoimage_transition_inset"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET

La transición de conjunto revela la nueva imagen en un rectángulo que se origina en una esquina del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros usados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.



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
<td>Ancho del conjunto en píxeles.</td>
</tr>
<tr class="even">
<td>Alto</td>
<td><strong>fEffectPara1</strong></td>
<td>Alto del conjunto en píxeles.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><strong>fEffectPara2</strong></td>
<td>Esquina desde la que se origina el conjunto. Establezca en uno de los siguientes valores:<br/>
<ul>
<li>0- Inferior izquierda</li>
<li>1 - Inferior derecha</li>
<li>2 - Parte superior izquierda</li>
<li>3 - Esquina superior derecha</li>
</ul></td>
</tr>
<tr class="even">
<td>Composición</td>
<td><strong>fEffectPara3</strong></td>
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





