---
description: Especifica el método utilizado para codificar la información del vector de movimiento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113345"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>Propiedad MFPKEY \_ DELTAMVRANGEINDEX

Especifica el método utilizado para codificar la información del vector de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Si se establece esta propiedad, el codificador aumenta el intervalo de vectores de movimiento delta en los campos. La información del vector de movimiento solo es válida para los campos entrelazados.

Esta propiedad puede establecerse en uno de los valores siguientes:



| Valor | Descripción                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Use el intervalo de vectores de movimiento delta existente.                                          |
| 1     | Duplica el intervalo de vectores de movimiento delta en la dirección horizontal.                    |
| 2     | Duplica el intervalo de vectores de movimiento delta en la dirección vertical.                      |
| 3     | Duplica el intervalo de vectores de movimiento delta en las direcciones horizontal y vertical. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




