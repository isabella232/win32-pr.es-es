---
title: principalsType Complex Type
description: Define el elemento secundario para el elemento Principals.
ms.assetid: a501534b-eb0f-480f-a2c9-d2015262a9a7
keywords:
- PrincipalsTipo de tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- principalsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa2aecd8ea71769b51792fcc5bd26ceca11309f43697037964a900d45c0d8254
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131746"
---
# <a name="principalstype-complex-type"></a>principalsType Complex Type

Define el elemento secundario para el [**elemento Principals.**](taskschedulerschema-principals-tasktype-element.md)

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
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





