---
title: Elemento de entidades de seguridad (taskType)
description: Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento de entidades de seguridad Programador de tareas
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996030"
---
# <a name="principals-tasktype-element"></a>Elemento de entidades de seguridad (taskType)

Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

El elemento de **entidades** de seguridad se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                                   | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Puede especificar hasta 32 entidades de seguridad para una tarea.

Para el desarrollo de scripting, las entidades de seguridad de una tarea se especifican mediante la propiedad [**TaskDefinition. principal**](taskdefinition-principal.md) .

En el desarrollo de C++, las entidades de seguridad de una tarea se especifican mediante la [**propiedad principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Ejemplos

En el código XML siguiente se definen dos entidades de seguridad: un identificador de usuario y una entidad de seguridad de identificador de grupo para la tarea.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





