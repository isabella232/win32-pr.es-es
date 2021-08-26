---
description: Especifica la marca de información de producción de audio en una secuencia de audio de Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propiedad AVEncDProductionInfoExists (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d0341cf97b4641dc2ece7e93408e527458235620b32b7e25abe583a67c2ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103475"
---
# <a name="avencddproductioninfoexists-property"></a>Propiedad AVEncDProductionInfoExists

Especifica la marca de información de producción de audio en una secuencia de audio de Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Comentarios

Si el valor es **VARIANT \_ TRUE,** la configuración del nivel de mezcla y el tipo de habitación son válidas. Especifique esta configuración con las [**propiedades AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) [**y AVEncDDProductionMixLevel.**](avencddproductionmixlevel-property.md)

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

 

 




