---
description: Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467214"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>Propiedad CODECAPI \_ AVEncVideoEncodeQP

Especifica el parámetro de cuantificación (QP) para la codificación de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valor de propiedad

Conjunto de cuatro campos de 16 bits que se usan para especificar los QP de fotograma en codificación de QP fija.

Los campos son:

-   Bits 0-15: QP predeterminado
-   Bits 16-31: QP usado para fotogramas I
-   Bits 32-47: QP usado para fotogramas P
-   Bits 48-63: QP usado para fotogramas B

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

Para garantizar un uso coherente en distintos codificadores, debe suponer que los codificadores solo verán el QP predeterminado y pueden omitir los valores de QP para imágenes de E/S/B.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

