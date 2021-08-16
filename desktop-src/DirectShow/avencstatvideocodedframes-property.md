---
description: Devuelve el número de fotogramas de vídeo codificados.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propiedad AVEncStatVideoCodedFrames (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f8858aba7a36d79096eccad40990e1859d4073695aaf80910587bac4005d6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119342574"
---
# <a name="avencstatvideocodedframes-property"></a>Propiedad AVEncStatVideoCodedFrames

Devuelve el número de fotogramas de vídeo codificados.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncStatVideoCodedFrames**

## <a name="remarks"></a>Comentarios

Esta propiedad está disponible una vez completada la codificación.

El valor de esta propiedad es igual a la propiedad [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) menos el número de fotogramas descartados. El codificador podría quitar fotogramas para permanecer dentro de las restricciones de velocidad de bits especificadas. También podría quitar fotogramas al final de la secuencia (vea [**la propiedad AVEncCommonStreamEndHandling).**](avenccommonstreamendhandling-property.md)

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

 

 




