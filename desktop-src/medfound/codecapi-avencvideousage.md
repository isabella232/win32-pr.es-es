---
description: Establece el uso de vídeo para un codificador de vídeo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Propiedad CODECAPI_AVEncVideoUsage (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652353"
---
# <a name="codecapi_avencvideousage-property"></a>\_Propiedad AVEncVideoUsage de CODECAPI

Establece el uso de vídeo para un codificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage y [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) son propiedades del codificador estático. Una vez que se han establecido, solo surtirán efecto después de llamar a un tipo de medio establecido en el PIN de salida de la cámara.

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

 

