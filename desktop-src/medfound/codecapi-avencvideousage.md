---
description: Establece el uso de vídeo para un codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6d3ee174fbc22ca7b1ab4e309d87112463740a075b497cc35033f8c96bbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777715"
---
# <a name="codecapi_avencvideousage-property"></a>Propiedad CODECAPI \_ AVEncVideoUsage

Establece el uso de vídeo para un codificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Comentarios

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5.](camera-encoder-h264-uvc-1-5.md)

[CODECAPI \_ AVEncVideo PseudoLayerCount,](codecapi-avencvideotemporallayercount.md)CODECAPI \_ AVEncVideoUsage y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades de codificador estático. Una vez establecidos, solo tendrán efecto después de llamar a un tipo de medio establecido en el pin de salida de la cámara.

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

 

