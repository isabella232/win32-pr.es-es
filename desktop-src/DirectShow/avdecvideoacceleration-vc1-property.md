---
description: Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo VC-1.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: Propiedad AVDecVideoAcceleration_VC1 (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659289"
---
# <a name="avdecvideoacceleration_vc1-property"></a>\_Propiedad VC1 de AVDecVideoAcceleration

Habilita o deshabilita la aceleración de hardware para la descodificación de vídeo VC-1.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Observaciones

Si el valor es cero, el descodificador no usa DirectX video Acceleration (DXVA) para la descodificación de vídeo VC-1. En el caso de los filtros DirectShow, establezca esta propiedad antes de que se conecte el PIN de salida del descodificador.

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

 

 




