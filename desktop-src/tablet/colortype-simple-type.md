---
description: Define el tipo que se utiliza para especificar los valores válidos para el color de determinados elementos de un archivo XML de diario.
ms.assetid: 10a19f28-d0aa-4126-b3f5-fde35fc5fdb0
title: Tipo simple de ColorType
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705446"
---
# <a name="colortype-simple-type"></a>Tipo simple de ColorType

Define el tipo que se utiliza para especificar los valores válidos para el color de determinados elementos de un archivo XML de diario.

``` syntax
<xs:simpleType name="ColorType">
    <xs:restriction
        base="string"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Observaciones

Un color puede ser un valor RGB hexadecimal con el formato \# RRGGBB. Debe coincidir con la siguiente expresión regular: \# \[ 0-9 – FA-F \] {6} . Por ejemplo: " \# 4a79B5".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



 

 




