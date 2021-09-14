---
description: Especifica cómo se usa la información de color en las operaciones de búsqueda de movimiento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268900"
---
# <a name="mfpkey_motionsearchlevel-property"></a>Propiedad MFPKEY \_ MOTIONSEARCHLEVEL

Especifica cómo se usa la información de color en las operaciones de búsqueda de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad puede establecerse en uno de los valores siguientes.



| Value | Información de vídeo usada                           |
|-------|--------------------------------------------------|
| 0     | Solo luminancia.                                       |
| 1     | Luma con entero más próximo.                |
| 2     | Luminancia con intensidad de color verdadero.                           |
| -1    | Macroblock-adaptive con true croma.            |
| -2    | Macroblock-adaptive con integer integer más cercano. |



 

De forma predeterminada, el códec realiza la búsqueda de movimiento solo en el canal luma. La inclusión de la información de los colores en la estimación del movimiento puede mejorar significativamente la calidad del vídeo codificado. La búsqueda de movimiento con luma y true detector dará la mejor calidad de vídeo, pero con el mayor costo de rendimiento. Los dos modos dinámicos (-1 y -2) y el luma con el modo de estrella de entero más cercano proporcionarán compromisos razonables entre la calidad y el rendimiento.

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

 

 




