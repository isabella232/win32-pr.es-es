---
title: Elemento StartBoundary (triggerBaseType)
description: Especifica la fecha y hora en que se activa el desencadenador.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Programador de tareas del elemento StartBoundary
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150044"
---
# <a name="startboundary-triggerbasetype-element"></a>Elemento StartBoundary (triggerBaseType)

Especifica la fecha y hora en que se activa el desencadenador.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

El elemento **StartBoundary** se define mediante el tipo complejo de [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                     | Derivado de                                                                               | Descripción                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se registra la tarea.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.<br/>             |



## <a name="remarks"></a>Observaciones

El **<StartBoundary>** elemento es un elemento necesario para los desencadenadores Time y Calendar ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) y [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).

Para el desarrollo de scripting, el límite final se especifica mediante la propiedad [**Trigger. StartBoundary**](trigger-startboundary.md) heredada por todos los objetos del desencadenador.

En el desarrollo de C++, el límite final se especifica mediante la propiedad [**ITrigger:: StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) heredada por todas las interfaces del desencadenador.

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de desencadenador de arranque que define un límite de inicio del 1 de enero de 2005:8:00 AM.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
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

 

 





