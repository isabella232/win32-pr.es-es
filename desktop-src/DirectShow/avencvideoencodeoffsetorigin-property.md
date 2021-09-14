---
description: Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo está recortado.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propiedad AVEncVideoEncodeOffsetOrigin (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161789"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Propiedad AVEncVideoEncodeOffsetOrigin

Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo está recortado.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits superiores del valor contienen el desplazamiento del borde izquierdo del marco de entrada, en píxeles. Los 16 bits inferiores contienen el desplazamiento del borde superior del marco de entrada, en píxeles.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada. Use la [**propiedad AVEncVideoEncodeDimension para**](avencvideoencodedimension-property.md) especificar el ancho y el alto del rectángulo de recorte.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio aplicaciones para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




