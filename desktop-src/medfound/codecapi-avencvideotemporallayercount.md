---
description: Establece el recuento de capas temporales de vídeo para un codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269207"
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
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

