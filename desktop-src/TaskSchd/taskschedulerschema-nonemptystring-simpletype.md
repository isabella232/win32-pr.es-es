---
title: Tipo simple de nonEmptyStringType
description: Define los valores utilizados para una cadena de texto que no está vacía.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Programador de tareas de tipo simple nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422438"
---
# <a name="nonemptystringtype-simple-type"></a>Tipo simple de nonEmptyStringType

Define los valores utilizados para una cadena de texto que no está vacía.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valores de enumeración

El tipo simple **nonEmptyString** define el siguiente valor.



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| 1     | La cadena contiene al menos un carácter.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





