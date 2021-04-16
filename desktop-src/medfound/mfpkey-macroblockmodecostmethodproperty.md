---
description: Especifica el método de costo que usa el códec para determinar qué modo de adaptativo macrobloque debe usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Propiedad MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696940"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>\_Propiedad MACROBLOCKMODECOSTMETHOD de MFPKEY

Especifica el método de costo que usa el códec para determinar qué modo de adaptativo macrobloque debe usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad se puede establecer en uno de los valores siguientes.



| Value | Método usado                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadamard. Esta opción configura el códec para usar solo la distorsión al calcular el costo.             |
| 1     | Costo de RD. Esta opción configura el códec para que tenga en cuenta la tasa y la distorsión al calcular el costo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




