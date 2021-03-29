---
description: Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: Propiedad AVDecVideoAcceleration_H264 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906798"
---
# <a name="avdecvideoacceleration_h264-property"></a>\_Propiedad H264 de AVDecVideoAcceleration

Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo H. 264.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>Observaciones

Si el valor es cero, el descodificador no usa DirectX video Acceleration (DXVA) para la descodificación de vídeo H. 264. En el caso de los filtros DirectShow, establezca esta propiedad antes de que se conecte el PIN de salida del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




