---
description: Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo se recorta.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propiedad AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152238"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Propiedad AVEncVideoEncodeOffsetOrigin

Especifica las esquinas izquierda y superior del rectángulo de recorte, si el vídeo se recorta.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits superiores del valor contienen el desplazamiento desde el borde izquierdo del fotograma de entrada, en píxeles. Los 16 bits inferiores contienen el desplazamiento desde el borde superior del fotograma de entrada, en píxeles.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada. Use la propiedad [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) para especificar el ancho y el alto del rectángulo de recorte.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




