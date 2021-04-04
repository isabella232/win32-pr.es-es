---
description: Especifica si el códec usará la optimización del escalado de vídeo.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Propiedad MFPKEY_VIDEOSCALING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908657"
---
# <a name="mfpkey_videoscaling-property"></a>MFPKEY \_ propiedad de VIDEOescalación

Especifica si el códec usará la optimización del escalado de vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

El escalado de vídeo es un tipo de optimización perceptual que puede mejorar la calidad visual del vídeo codificado a velocidades de bits bajas. La optimización del escalado de vídeo reduce los artefactos pronunciados, pero puede sacrificar los detalles de la imagen. Esta optimización afecta al intervalo de luminancia del vídeo codificado como se describe a continuación, pero no afecta a la resolución física del vídeo de salida.

Esta propiedad se puede establecer en uno de los valores siguientes.



| Value | Descripción                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | No se usará el escalado de vídeo.                                                                                       |
| 1     | El codificador usará la optimización del escalado de vídeo conservador. El intervalo de luminancia se escalará desde 0... 255 hasta 26... 229. |
| 2     | El codificador usará una optimización de escalado de vídeo agresiva. El intervalo de luminancia se escalará de 0... 255 a 31... 224.   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




