---
description: Habilita o deshabilita la aceleración de hardware para lacodización de vídeo H.264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264 propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663969"
---
# <a name="avdecvideoacceleration_h264-property"></a>Propiedad AVDecVideoAcceleration \_ H264

Habilita o deshabilita la aceleración de hardware para lacodización de vídeo H.264.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>Observaciones

Si el valor es cero, el descodificador no usa la aceleración de vídeo de DirectX (DXVA) para la descodificación de vídeo H.264. Para DirectShow filtros, establezca esta propiedad antes de que se conecte el pin de salida del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




