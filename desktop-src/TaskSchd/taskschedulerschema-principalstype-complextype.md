---
title: Tipo complejo de principalsType
description: Define el elemento secundario del elemento de entidades de seguridad.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- tipo complejo de principalsType Programador de tareas
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56cd26a4dff31ce86b218e5a4a2662d678327625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996029"
---
# <a name="principalstype-complex-type"></a>Tipo complejo de principalsType

Define el elemento secundario del elemento de [**entidades**](taskschedulerschema-principals-tasktype-element.md) de seguridad.

``` syntax
<xs:complexType name="principalsType">
    <xs:sequence>
        <xs:element name="Principal"
            type="principalType"
            maxOccurs="1"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                                   | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





