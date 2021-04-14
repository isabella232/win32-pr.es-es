---
description: Establece el número de capas temporales de vídeo para un codificador de vídeo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Propiedad CODECAPI_AVEncVideoTemporalLayerCount (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496840"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>\_Propiedad AVEncVideoTemporalLayerCount de CODECAPI

Establece el número de capas temporales de vídeo para un codificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades del codificador estático. Una vez que se han establecido, solo surtirán efecto después de llamar a un tipo de medio establecido en el PIN de salida de la cámara.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

