---
description: Define el tipo que se usa para especificar valores válidos para el color de determinados elementos de un archivo XML de diario.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo simple ColorType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ColorType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 92b4f8db5626ec34c66c769f86afe1eac9d37940dce0374b1340430d3e62939d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009085"
---
# <a name="colortype-simple-type"></a>Tipo simple ColorType

Define el tipo que se usa para especificar valores válidos para el color de determinados elementos de un archivo XML de diario.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Comentarios

Un color puede ser un valor RGB hexadecimal con el formato \# RRGGBB. Debe coincidir con la siguiente expresión regular: \# \[ 0-9a-fA-F \] {6} . Por ejemplo: \# "4a79B5".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




