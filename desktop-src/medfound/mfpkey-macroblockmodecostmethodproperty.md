---
description: Especifica el método de costo utilizado por el códec para determinar qué modo de macrobloqueo se va a usar.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: MFPKEY_MACROBLOCKMODECOSTMETHOD propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe61be79b07a09d1f55c09b1970c4becbf7aca9818c525420712952bac40db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873289"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>Propiedad MACROBLOCKMODECOSTMETHOD de MFPKEY \_

Especifica el método de costo utilizado por el códec para determinar qué modo de macrobloqueo se va a usar.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Esta propiedad puede establecerse en uno de los valores siguientes.



| Valor | Método usado                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | SAD/Hadamard. Esta opción configura el códec para usar solo distorsión al calcular el costo.             |
| 1     | Costo de Escritorio remoto. Esta opción configura el códec para tener en cuenta tanto la velocidad como la distorsión al calcular el costo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




