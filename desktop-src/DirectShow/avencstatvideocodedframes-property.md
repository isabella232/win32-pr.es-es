---
description: Devuelve el número de fotogramas de vídeo que se han codificado.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propiedad AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152431"
---
# <a name="avencstatvideocodedframes-property"></a>Propiedad AVEncStatVideoCodedFrames

Devuelve el número de fotogramas de vídeo que se han codificado.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible una vez completada la codificación.

El valor de esta propiedad es igual a la propiedad [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) menos el número de fotogramas quitados. El codificador podría quitar fotogramas para permanecer dentro de las restricciones de velocidad de bits especificadas. También podría quitar fotogramas al final de la secuencia (vea la propiedad [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).

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

 

 




