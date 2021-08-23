---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl.h)
description: La transición de volteo gira la imagen antigua en un eje Y a través del centro del marco. La nueva imagen se muestra como la parte posterior de la imagen anterior.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a194067fd8a5bb34569723245b68996163d0cd9a2eef332e6f42fceb8187eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590655"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FLIP

La transición de volteo gira la imagen antigua en un eje Y a través del centro del marco. La nueva imagen se muestra como la parte posterior de la imagen anterior.

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
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ángulo</td>
<td><strong>fEffectPara0</strong></td>
<td>Ángulo de rotación, de 0,0 a 180,0 grados.</td>
</tr>
<tr class="even">
<td>Composición</td>
<td><strong>fEffectPara1</strong></td>
<td>Establezca en uno de los siguientes valores:
<ul>
<li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li>
<li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Puede visualizar el efecto de esta transición como si ambas imágenes fueran fotografías físicas pegadas de vuelta a atrás. La transición tiene el mismo efecto que mantener dos fotografías de este tipo en el centro del borde inferior y girarlas 180 grados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





