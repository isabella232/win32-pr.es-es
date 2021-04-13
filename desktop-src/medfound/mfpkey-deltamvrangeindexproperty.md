---
description: Especifica el método utilizado para codificar la información del vector de movimiento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: Propiedad MFPKEY_DELTAMVRANGEINDEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544926"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>\_Propiedad DELTAMVRANGEINDEX de MFPKEY

Especifica el método utilizado para codificar la información del vector de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Si se establece esta propiedad, el codificador aumenta el intervalo de vector de movimiento Delta en los campos. La información del vector de movimiento solo es válida para los campos entrelazados.

Esta propiedad se puede establecer en uno de los valores siguientes:



| Value | Descripción                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Use el intervalo de vector de movimiento Delta existente.                                          |
| 1     | Doble el intervalo del vector de movimiento Delta en la dirección horizontal.                    |
| 2     | Duplique el intervalo del vector de movimiento Delta en dirección vertical.                      |
| 3     | Duplique el intervalo del vector de movimiento Delta en las direcciones horizontal y vertical. |



 

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

 

 




