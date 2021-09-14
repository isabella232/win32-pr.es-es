---
description: Especifica el método utilizado para codificar la información del vector de movimiento.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257607"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>Propiedad DELTAMVRANGEINDEX de MFPKEY \_

Especifica el método utilizado para codificar la información del vector de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Si se establece esta propiedad, el codificador aumenta el intervalo de vectores de movimiento delta en los campos. La información del vector de movimiento solo es válida para los campos entrelazados.

Esta propiedad puede establecerse en uno de los siguientes valores:



| Value | Descripción                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Use el intervalo de vectores de movimiento delta existente.                                          |
| 1     | Doble el intervalo de vectores de movimiento delta en la dirección horizontal.                    |
| 2     | Doble el intervalo de vectores de movimiento delta en la dirección vertical.                      |
| 3     | Duplica el intervalo de vectores de movimiento delta en las direcciones horizontal y vertical. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




