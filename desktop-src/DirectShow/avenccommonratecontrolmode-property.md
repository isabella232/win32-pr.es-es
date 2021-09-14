---
description: Especifica el modo de control de velocidad.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propiedad AVEncCommonRateControlMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161985"
---
# <a name="avenccommonratecontrolmode-property"></a>Propiedad AVEncCommonRateControlMode

Especifica el modo de control de velocidad.

Las aplicaciones pueden establecer esta propiedad para especificar el modo de control de velocidad. Los codificadores también pueden devolver esta propiedad como una funcionalidad.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVEncCommonRateControlMode.**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)

## <a name="remarks"></a>Observaciones

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[CODECAPI \_ AVEncVideo EncoderLayerCount,](/windows/desktop/medfound/codecapi-avencvideotemporallayercount) [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)y CODECAPI \_ AVEncCommonRateControlMode son propiedades de codificador estático. Una vez establecidos, solo se harán efectivos después de llamar a un tipo de medio establecido en el pin de salida de la cámara.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

