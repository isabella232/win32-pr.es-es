---
description: Especifica el método que se va a utilizar para la coincidencia de movimiento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Propiedad MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001630"
---
# <a name="mfpkey_motionmatchmethod-property"></a>\_Propiedad MOTIONMATCHMETHOD de MFPKEY

Especifica el método que se va a utilizar para la coincidencia de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad se puede establecer en uno de los valores siguientes.



| Value | Método usado                       |
|-------|-----------------------------------|
| 0     | suma de diferencias absolutas (SAD) |
| 1     | Hadamard                          |
| -1    | Adaptativo macrobloque: adaptable.              |



 

La suma de diferencias absolutas (SAD) es un método más rápido pero menos preciso que la transformación Hadamard. La transformación Hadamard es más precisa pero es computacionalmente intensiva. El modo de adaptación adaptativo macrobloque proporciona un compromiso razonable entre los dos métodos mediante la elección dinámica entre las dos transformaciones y la selección de la transformación Hadamard solo cuando sea necesario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




