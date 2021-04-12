---
description: Especifica el tipo de habitación de una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Propiedad AVEncDDProductionRoomType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152562"
---
# <a name="avencddproductionroomtype-property"></a>Propiedad AVEncDDProductionRoomType

Especifica el tipo de habitación de una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionRoomType**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .

## <a name="remarks"></a>Observaciones

*Tipo de sala* hace referencia al tamaño de la habitación utilizada durante la producción. Si establece esta propiedad, establezca la propiedad [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) en **true**.

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

 

