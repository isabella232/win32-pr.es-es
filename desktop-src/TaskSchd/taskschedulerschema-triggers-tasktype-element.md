---
title: Elemento Triggers (taskType)
description: Especifica los desencadenadores que inician la tarea.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Desencadenadores de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d067c9e315006c55e07e972e5616525750d8a383d7ed8294f7d39a6acf32caff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610889"
---
# <a name="triggers-tasktype-element"></a>Elemento Triggers (taskType)

Especifica los desencadenadores que inician la tarea.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

El tipo complejo **triggersType** define el elemento [**Triggers.**](taskschedulerschema-triggerstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas trabajo.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                     | Tipo                                                                                       | Descripción                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se arranca el sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando el equipo entra en estado de inactividad.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se registra la tarea.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.<br/>             |



## <a name="remarks"></a>Observaciones

Los elementos secundarios enumerados anteriormente se pueden agregar en cualquier orden.

Para el desarrollo de C++, los desencadenadores de una tarea se especifican mediante la [**propiedad Triggers de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).

Para el desarrollo de scripting, los desencadenadores de una tarea se especifican mediante la [**propiedad TaskDefinition.Triggers.**](taskdefinition-triggers.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador, vea [Ejemplo de desencadenador de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





