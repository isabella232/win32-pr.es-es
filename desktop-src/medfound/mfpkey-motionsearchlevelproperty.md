---
description: Especifica cómo se utiliza la información de color en las operaciones de búsqueda de movimiento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Propiedad MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082472"
---
# <a name="mfpkey_motionsearchlevel-property"></a>\_Propiedad MOTIONSEARCHLEVEL de MFPKEY

Especifica cómo se utiliza la información de color en las operaciones de búsqueda de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad se puede establecer en uno de los valores siguientes.



| Value | Información de vídeo usada                           |
|-------|--------------------------------------------------|
| 0     | Solo luminancia.                                       |
| 1     | Luminancia con intensidad de croma entero más próximo.                |
| 2     | Luminancia con intensidad de color verdadero.                           |
| -1    | Adaptativo macrobloque: adaptable con intensidad de croma real.            |
| -2    | Adaptativo macrobloque: adaptable con el cromado de entero más próximo. |



 

De forma predeterminada, el códec realiza la búsqueda de movimiento solo en el canal de luminancia. La inclusión de información de croma en la estimación de movimiento puede mejorar significativamente la calidad del vídeo codificado. La búsqueda de movimiento con luminancia y intensidad de croma real producirá la mejor calidad de vídeo, pero con el mayor costo de rendimiento. Los dos modos dinámicos (-1 y-2) y la luminancia con el modo de croma de entero más próximo proporcionarán un riesgo razonable entre calidad y rendimiento.

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

 

 




