---
description: Especifica el ancho y el alto del vídeo codificado, si se recorta el vídeo.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propiedad AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666099"
---
# <a name="avencvideoencodedimension-property"></a>Propiedad AVEncVideoEncodeDimension

Especifica el ancho y el alto del vídeo codificado, si se recorta el vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valor de propiedad

Los 16 bits superiores del valor contienen el ancho en píxeles y los 16 bits inferiores contienen el alto en píxeles.

## <a name="remarks"></a>Observaciones

Las aplicaciones pueden establecer esta propiedad para recortar el vídeo de entrada. El tamaño especificado debe ser menor que el tamaño de los fotogramas de vídeo de entrada. Use la propiedad [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) para especificar las esquinas izquierda y superior del rectángulo de recorte.

Los codificadores pueden devolver esta propiedad como una capacidad.

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

En el caso de los codificadores de cámara UVC 1,5, no se admite [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) .

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

 

