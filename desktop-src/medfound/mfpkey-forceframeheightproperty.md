---
description: Especifica un alto de fotograma intermedio para el vídeo codificado.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e3d423fe96173829b31a889764d5423db88b5c882d853b3e0f770d17dd4691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463455"
---
# <a name="mfpkey_forceframeheight-property"></a>Propiedad FORCEFRAMEHEIGHT de MFPKEY \_

Especifica un alto de fotograma intermedio para el vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede establecer este valor y la propiedad [ \_ FORCEFRAMEWIDTH de MFPKEY](mfpkey-forceframewidthproperty.md) para forzar al codificador a codificar la secuencia de vídeo con un tamaño de fotograma menor que los tamaños de fotograma de entrada o salida. Cuando se descodifica, se cambia el tamaño del vídeo a su resolución de entrada original.

Las dimensiones de marco válidas en cualquiera de los ejes son de 2 a 8192 píxeles. Las dimensiones de marco deben ser divisibles entre 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




