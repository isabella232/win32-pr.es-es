---
title: Elemento Privilege (requiredPrivilegesType)
description: Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivo o cambiar la hora del sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Elemento Privilege Programador de tareas
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f181c2dbe21e31c752a44a4a3b0e27abd0f9396939c9a9dcee3127f796760527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758323"
---
# <a name="privilege-requiredprivilegestype-element"></a>Elemento Privilege (requiredPrivilegesType)

Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivo o cambiar la hora del sistema.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

El tipo complejo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) define el elemento **Privilege.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                             | Derivado de                                                                             | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, se tiene acceso a esta información a través de [**la propiedad IPrincipal2::RequiredPrivilege.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que especifica el derecho de una tarea para realizar diversas operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivo o cambiar la hora del sistema.


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

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





