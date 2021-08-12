---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Especifica los privilegios que requiere la tarea.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Elemento RequiredPrivileges Programador de tareas
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e395a61aace07dccb27eab04d9c0299115c25f16d84cd42e3d607435478f8060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611492"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Elemento RequiredPrivileges (requiredPrivilegesType)

Especifica los privilegios que requiere la tarea.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

El tipo complejo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) define el elemento **RequiredPrivileges.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                  | Derivado de                                                           | Descripción                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, se tiene acceso a esta información a través de [**la propiedad IPrincipal2::RequiredPrivilege.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Ejemplos

El código XML siguiente define el uso de un identificador de grupo y los privilegios necesarios.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





