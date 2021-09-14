---
title: Elemento Task
description: Define la tarea que realiza el servicio Programador de tareas trabajo.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Elemento Task Programador de tareas
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968627"
---
# <a name="task-element"></a>Elemento Task

Define la tarea que realiza el servicio Programador de tareas trabajo.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Tipo                                                                                 | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Acciones**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Especifica las acciones realizadas por la tarea.<br/>                                                                             |
| [**Data**](taskschedulerschema-data-tasktype-element.md)                         | [**Datatype**](taskschedulerschema-datatype-complextype.md)                         | Especifica los datos de suma asociados a la tarea, pero el servicio de Programador de tareas de otro modo.<br/>         |
| [**Entidades de seguridad**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Especifica los contextos de seguridad que se pueden usar para ejecutar la tarea.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.<br/>                                                 |
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Especifica los desencadenadores que inician la tarea.<br/>                                                                              |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**ITaskDefinition.**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)

Para el desarrollo de scripts, vea [**TaskDefinition**](taskdefinition.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





