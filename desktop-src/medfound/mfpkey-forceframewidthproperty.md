---
description: Especifica un ancho de fotograma intermedio para el vídeo codificado.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468637"
---
# <a name="mfpkey_forceframewidth-property"></a>Propiedad \_ FORCEFRAMEWIDTH de MFPKEY

Especifica un ancho de fotograma intermedio para el vídeo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede establecer este valor y la propiedad [ \_ FORCEFRAMEHEIGHT de MFPKEY](mfpkey-forceframeheightproperty.md) para forzar al codificador a codificar la secuencia de vídeo con un tamaño de fotograma menor que los tamaños de fotograma de entrada o salida. Cuando se descodifica, se cambia el tamaño del vídeo a su resolución de entrada original.

Las dimensiones de marco válidas en cualquiera de los ejes son de 2 a 8192 píxeles. Las dimensiones de marco deben ser divisibles por 2.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




