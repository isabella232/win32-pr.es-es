---
description: Especifica la marca de información de producción de audio en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propiedad AVEncDDProductionInfoExists (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161909"
---
# <a name="avencddproductioninfoexists-property"></a>Propiedad AVEncDDProductionInfoExists

Especifica la marca de información de producción de audio en una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Observaciones

Si el valor es **VARIANT \_ TRUE,** la configuración del nivel de combinación y el tipo de habitación son válidas. Especifique esta configuración con las [**propiedades AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) y [**AVEncDDProductionMixLevel.**](avencddproductionmixlevel-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




