---
description: Especifica el ancho y alto del vídeo codificado, si el vídeo se recorta.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propiedad AVEncVideoEncodeDimension (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159324"
---
# <a name="avencvideoencodedimension-property"></a>AvEncVideoEncodeDimension, propiedad

Especifica el ancho y alto del vídeo codificado, si el vídeo se recorta.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits superiores del valor contienen el ancho en píxeles y los 16 bits inferiores contienen el alto en píxeles.

## <a name="remarks"></a>Comentarios

Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada. El tamaño especificado debe ser menor que el tamaño de los fotogramas de vídeo de entrada. Use la [**propiedad AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) para especificar las esquinas izquierda y superior del rectángulo de recorte.

Los codificadores pueden devolver esta propiedad como una funcionalidad.

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

En el caso de los codificadores de cámara UVC 1.5, no se admite [AVEncVideoEncodeOffsetOrigin.](avencvideoencodeoffsetorigin-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

