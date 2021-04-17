---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del fotograma.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690151"
---
# <a name="wmt_videoimage_transition_diagonal"></a>DIAGONAL de transición de imagen de videotransmisión WMT \_ \_ \_

La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del fotograma.

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
<td>Ancho de la sección diagonal en píxeles.</td>
</tr>
<tr class="even">
<td>Alto</td>
<td><strong>fEffectPara1</strong></td>
<td>Alto de la sección diagonal en píxeles.</td>
</tr>
<tr class="odd">
<td>Dirección</td>
<td><strong>fEffectPara2</strong></td>
<td>Determina la esquina desde la que se origina la transición. Establezca en uno de los siguientes elementos:<br/>
<ul>
<li>0: parte superior derecha</li>
<li>1: parte superior izquierda</li>
<li>2-inferior derecha</li>
<li>3-inferior izquierda</li>
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

 

 





