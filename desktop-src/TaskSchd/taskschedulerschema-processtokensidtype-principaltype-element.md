---
title: Elemento ProcessTokenSidType (principalType)
description: Especifica el tipo de identificación de seguridad de proceso (SID) de la tarea.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Elemento ProcessTokenSidType Programador de tareas
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b89da903ee3d0814f2c6d599e1418886efc414a129dd7197282fc66e9e7d78d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125725"
---
# <a name="processtokensidtype-principaltype-element"></a>Elemento ProcessTokenSidType (principalType)

Especifica el tipo de identificación de seguridad de proceso (SID) de la tarea.

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

El tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) define el elemento **ProcessTokenSidType.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, el tipo de SID de proceso se especifica mediante la propiedad [**IPrincipal2::P rocessTokenSidType.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype)

## <a name="examples"></a>Ejemplos

El xml siguiente define el tipo de SID de proceso de la tarea.


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





