---
description: Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ed7ba8e3cf522c1e3cfa07d22cf5e37639717c230ca571ffd89d9e1d513a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974894"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>Propiedad CODECAPI \_ AVEncVideoEncodeQP

Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valor de propiedad

Conjunto de cuatro campos de 16 bits que se usan para especificar los QP de marco en la codificación fixed-QP.

Los campos son:

-   Bits 0-15: QP predeterminado
-   Bits 16-31: QP usado para fotogramas I
-   Bits 32-47: QP usado para fotogramas P
-   Bits 48-63: QP usado para fotogramas B

## <a name="remarks"></a>Comentarios

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5](camera-encoder-h264-uvc-1-5.md).

Para garantizar un uso coherente en distintos codificadores, debe suponer que los codificadores solo verán el QP predeterminado y pueden omitir los valores de QP para imágenes de E/S/B.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

