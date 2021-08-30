---
description: Especifica el tipo de sala para una secuencia de audio de Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propiedad AVEncDProductionRoomType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e740138f90d06da8934fdfe1dc8f4d4f3e1afd37537c6c91e1e5bd774847eb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103415"
---
# <a name="avencddproductionroomtype-property"></a>Propiedad AVEncDProductionRoomType

Especifica el tipo de sala para una secuencia de audio de Dolby Digital. Esta propiedad se aplica a los codificadores de audio Dolby Digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVEncDProductionRoomType.**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype)

## <a name="remarks"></a>Comentarios

*El tipo de* habitación hace referencia al tamaño de la sala utilizada durante la producción. Si establece esta propiedad, establezca la propiedad [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **TRUE.**

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

 

