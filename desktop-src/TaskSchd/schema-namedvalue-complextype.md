---
title: tipo complejo namedValue
description: Define un nombre asociado a un valor en un par nombre-valor.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- tipo complejo namedValue Programador de tareas
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886545"
---
# <a name="namedvalue-complex-type"></a>tipo complejo namedValue

Define un nombre asociado a un valor en un par nombre-valor.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



| Nombre | Tipo                                                                    | Descripción                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica el nombre asociado a un valor en un par nombre-valor. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





