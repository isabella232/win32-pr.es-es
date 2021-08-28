---
description: Especifica el modo de control de velocidad.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propiedad AVEncCommonRateControlMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa914f445fcbc535ec423b41306938890d64b747258cb0159add5e4fd43c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794675"
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

## <a name="remarks"></a>Comentarios

Esta propiedad también se usa con codificadores de cámara [H.264 UVC 1.5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[CODECAPI \_ AVEncVideo EncoderLayerCount,](/windows/desktop/medfound/codecapi-avencvideotemporallayercount) [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)y CODECAPI \_ AVEncCommonRateControlMode son propiedades de codificador estático. Una vez establecidos, solo se harán efectivos después de llamar a un tipo de medio establecido en el pin de salida de la cámara.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

