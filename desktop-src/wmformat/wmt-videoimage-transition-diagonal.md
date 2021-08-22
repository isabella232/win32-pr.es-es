---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del marco.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL windows Media Format
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
ms.openlocfilehash: 6b1a356d7325dd01de2ad055750a062d5591fd4aa983fdb21e39e9543a3d26e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658135"
---
# <a name="wmt_videoimage_transition_diagonal"></a>DIAGONAL DE TRANSICIÓN \_ DE WMT VIDEOIMAGE \_ \_

La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del marco.

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
<td>Determina la esquina desde la que se origina la transición. Establezca en uno de los siguientes valores:<br/>
<ul>
<li>0: esquina superior derecha</li>
<li>1 - Parte superior izquierda</li>
<li>2 - Inferior derecha</li>
<li>3 - Inferior izquierda</li>
</ul></td>
</tr>
<tr class="even">
<td>Composición</td>
<td><strong>fEffectPara3</strong></td>
<td>Establezca en uno de los siguientes valores:
<ul>
<li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li>
<li>1 : especifica la composición invertida, en la que la imagen actual es la imagen de fondo y la imagen anterior es el primer plano.</li>
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

 

 





