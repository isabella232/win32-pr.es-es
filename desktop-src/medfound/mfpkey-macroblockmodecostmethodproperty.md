---
description: Especifica el método de costo utilizado por el códec para determinar qué modo de macrobloqueo se va a usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268980"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>Propiedad MFPKEY \_ MACROBLOCKMODECOSTMETHOD

Especifica el método de costo utilizado por el códec para determinar qué modo de macrobloqueo se va a usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad puede establecerse en uno de los valores siguientes.



| Value | Método usado                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadamard. Esta opción configura el códec para usar solo distorsión al calcular el costo.             |
| 1     | Costo de Escritorio remoto. Esta opción configura el códec para tener en cuenta la velocidad y la distorsión al calcular el costo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




