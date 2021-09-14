---
description: Especifica el método que se usará para la coincidencia de movimiento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268903"
---
# <a name="mfpkey_motionmatchmethod-property"></a>Propiedad MFPKEY \_ MOTIONMATCHMETHOD

Especifica el método que se usará para la coincidencia de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad puede establecerse en uno de los valores siguientes.



| Value | Método usado                       |
|-------|-----------------------------------|
| 0     | suma de diferencias absolutas (SAD) |
| 1     | Hadamard                          |
| -1    | Macroblock-adaptive.              |



 

La suma de las diferencias absolutas (SAD) es un método más rápido pero menos preciso que la transformación de Hadamard. La transformación de Hadamard es más precisa, pero requiere muchos cálculos. El modo de macrobloqueo adaptable proporciona un riesgo razonable entre los dos métodos al elegir dinámicamente entre las dos transformaciones, seleccionando la transformación de Hadamard solo cuando sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




