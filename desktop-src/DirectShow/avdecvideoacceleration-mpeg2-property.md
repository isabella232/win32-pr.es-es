---
description: Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: Propiedad AVDecVideoAcceleration_MPEG2 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806589"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>AVDecVideoAcceleration \_ propiedad de MPEG2

Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo MPEG-2.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoAcceleration \_ MPEG2**

## <a name="remarks"></a>Observaciones

Si el valor es cero, el descodificador no usa DirectX video Acceleration (DXVA) para la descodificación de vídeo MPEG-2. En el caso de los filtros DirectShow, establezca esta propiedad antes de que se conecte el PIN de salida del descodificador.

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

 

 




