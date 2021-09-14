---
title: Elemento StartBoundary (triggerBaseType)
description: Especifica la fecha y hora en que se activa el desencadenador.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- Elemento StartBoundary Programador de tareas
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46584659fbd14bc26981e220798a91c03e960e1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968651"
---
# <a name="startboundary-triggerbasetype-element"></a>Elemento StartBoundary (triggerBaseType)

Especifica la fecha y hora en que se activa el desencadenador.

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

El tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) define el elemento **StartBoundary.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                     | Derivado de                                                                               | Descripción                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se arranca el sistema.<br/>                 |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)         | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/>                |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando el equipo entra en estado inactivo.<br/> |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)               | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/>                       |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se registra la tarea.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                 | Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.<br/>             |



## <a name="remarks"></a>Observaciones

El **&lt; elemento &gt; StartBoundary** es un elemento necesario para los desencadenadores time y calendar [**&lt; (TimeTrigger &gt;**](taskschedulerschema-timetrigger-triggergroup-element.md) [**&lt; y CalendarTrigger). &gt;**](taskschedulerschema-calendartrigger-triggergroup-element.md)

Para el desarrollo de scripting, el límite final se especifica mediante la propiedad [**Trigger.StartBoundary**](trigger-startboundary.md) heredada por todos los objetos de desencadenador.

Para el desarrollo de C++, el límite final se especifica mediante la propiedad [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) heredada por todas las interfaces de desencadenador.

## <a name="examples"></a>Ejemplos

El siguiente XML define un elemento de desencadenador de arranque que define un límite de inicio del 1 de enero de 2005: 8:00 a. m.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





