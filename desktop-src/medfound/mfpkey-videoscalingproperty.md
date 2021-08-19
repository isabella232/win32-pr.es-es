---
description: Especifica si el códec usará la optimización de escalado de vídeo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2dc069d70b167dd8da6cb308d70149aec1028f3aaf4e50b5c1cc8ab11104c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887664"
---
# <a name="mfpkey_videoscaling-property"></a>MFPKEY \_ VIDEOSCALING Property

Especifica si el códec usará la optimización de escalado de vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

El escalado de vídeo es un tipo de optimización perceptual que puede mejorar la calidad visual del vídeo codificado a velocidades de bits bajas. La optimización del escalado de vídeo reduce los artefactos pronunciados, pero puede sacrificar los detalles de la imagen. Esta optimización afecta al intervalo luma del vídeo codificado como se describe a continuación, pero no afecta a la resolución física del vídeo de salida.

Esta propiedad puede establecerse en uno de los valores siguientes.



| Value | Descripción                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | No se usará el escalado de vídeo.                                                                                       |
| 1     | El codificador usará la optimización del escalado de vídeo conservador. El intervalo luma se escalará de 0...255 a 26...229. |
| 2     | El codificador usará una optimización agresiva del escalado de vídeo. El intervalo luma se escalará de 0...255 a 31...224.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




