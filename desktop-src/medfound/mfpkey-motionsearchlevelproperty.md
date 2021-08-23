---
description: Especifica cómo se usa la información de color en las operaciones de búsqueda de movimiento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b53c6bf8f94b2b9817249d96cffbfa0da251dbbcb0545c141230de90f80485af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555424"
---
# <a name="mfpkey_motionsearchlevel-property"></a>Propiedad MFPKEY \_ MOTIONSEARCHLEVEL

Especifica cómo se usa la información de color en las operaciones de búsqueda de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Esta propiedad puede establecerse en uno de los valores siguientes.



| Value | Información de vídeo usada                           |
|-------|--------------------------------------------------|
| 0     | Solo luminancia.                                       |
| 1     | Luma con entero más próximo.                |
| 2     | Luminancia con intensidad de color verdadero.                           |
| -1    | Macroblock-adaptive with true crom.            |
| -2    | Macroblock-adaptive con integer integer más cercano. |



 

De forma predeterminada, el códec realiza la búsqueda de movimiento solo en el canal luma. La inclusión de la información de los colores en la estimación del movimiento puede mejorar significativamente la calidad del vídeo codificado. La búsqueda de movimiento con luma y true detector dará la mejor calidad de vídeo, pero con el mayor costo de rendimiento. Los dos modos dinámicos (-1 y -2) y el luma con el modo de estrella de entero más cercano proporcionarán compromisos razonables entre la calidad y el rendimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




