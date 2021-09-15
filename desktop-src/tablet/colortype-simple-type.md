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
ms.openlocfilehash: 883c34f42f8d31f3581599445b398b93676d416b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468009"
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

## <a name="remarks"></a>Observaciones

Un color puede ser un valor RGB hexadecimal con el formato \# RRGGBB. Debe coincidir con la siguiente expresión regular: \# \[ 0-9a-fA-F \] {6} . Por ejemplo: \# "4a79B5".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




