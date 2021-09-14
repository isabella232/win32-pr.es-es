---
title: Elemento Principals (taskType)
description: Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento Principals Programador de tareas
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968723"
---
# <a name="principals-tasktype-element"></a>Elemento Principals (taskType)

Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

El **elemento Principals** se define mediante el [**tipo complejo taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas trabajo.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                  | Tipo                                                                   | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Puede especificar hasta 32 entidades de seguridad para una tarea.

Para el desarrollo de scripting, las entidades de seguridad de una tarea se especifican mediante la [**propiedad TaskDefinition.Principal.**](taskdefinition-principal.md)

Para el desarrollo de C++, las entidades de seguridad de una tarea se especifican mediante la [**propiedad Principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Ejemplos

El siguiente XML define dos entidades de seguridad: un identificador de usuario y una entidad de seguridad de identificador de grupo para la tarea.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





