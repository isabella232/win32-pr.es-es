---
description: Establece el recuento de capas temporales de vídeo para un codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743882"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>Propiedad CODECAPI \_ AVEncVideoVideoLayerCount

Establece el recuento de capas temporales de vídeo para un codificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoVideoLayerCount**

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

CODECAPI \_ AVEncVideoVideoLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades de codificador estático. Una vez establecido, solo tendrán efecto después de llamar a un tipo de medio establecido en el pin de salida de la cámara.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

