---
description: Especifica el tipo de sala para una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propiedad AVEncDDProductionRoomType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161905"
---
# <a name="avencddproductionroomtype-property"></a>Propiedad AVEncDDProductionRoomType

Especifica el tipo de sala para una secuencia de audio Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVEncDDProductionRoomType.**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)

## <a name="remarks"></a>Observaciones

*El tipo de* sala hace referencia al tamaño de la sala utilizada durante la producción. Si establece esta propiedad, establezca la [**propiedad AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **TRUE.**

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

 

