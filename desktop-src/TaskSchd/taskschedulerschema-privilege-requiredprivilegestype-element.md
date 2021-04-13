---
title: Privilege (elemento requiredPrivilegesType)
description: Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.
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
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492280"
---
# <a name="privilege-requiredprivilegestype-element"></a>Privilege (elemento requiredPrivilegesType)

Especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

El elemento **Privilege** se define mediante el tipo complejo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                             | Derivado de                                                                             | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

En el desarrollo de C++, se tiene acceso a esta información a través de la propiedad [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que especifica el derecho de una tarea para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar controladores de dispositivos o cambiar la hora del sistema.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





