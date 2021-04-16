---
description: Especifica la marca de información de producción de audio en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Propiedad AVEncDDProductionInfoExists (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686390"
---
# <a name="avencddproductioninfoexists-property"></a>Propiedad AVEncDDProductionInfoExists

Especifica la marca de información de producción de audio en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Observaciones

Si el valor es **Variant \_ true**, los valores de nivel de combinación y tipo de sala son válidos. Especifique estos valores con las propiedades [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) y [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .

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

 

 




