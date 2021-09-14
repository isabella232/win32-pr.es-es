---
description: Especifica un alto de fotograma intermedio para el vídeo codificado.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257535"
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
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




