---
description: Especifica el método que se usará para la coincidencia de movimiento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0604acc7dc0634be296e5097c3594dc74e5ceb7bdb7563b48a164cd13b164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355735"
---
# <a name="mfpkey_motionmatchmethod-property"></a>Propiedad MFPKEY \_ MOTIONMATCHMETHOD

Especifica el método que se usará para la coincidencia de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

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
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




