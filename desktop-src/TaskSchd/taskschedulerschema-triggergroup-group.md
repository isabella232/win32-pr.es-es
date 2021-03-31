---
title: Grupo triggerGroup
description: Define el grupo de desencadenadores.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Programador de tareas triggerGroup
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151173"
---
# <a name="triggergroup-group"></a>Grupo triggerGroup

Define el grupo de desencadenadores.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                 | Tipo                                                                                                   | Descripción                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)                             | Desencadenador que inicia una tarea cuando se inicia el sistema.<br/>                                                |
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)                     | Desencadenador que inicia una tarea en función de una programación diaria, semanal, mensual o mensual (DOW).<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)                           | Desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/>                                               |
| [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)                             | Desencadenador que inicia una tarea cuando el equipo entra en un estado de inactividad.<br/>                                |
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)                           | Desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/>                                                      |
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)             | Desencadenador que inicia una tarea cuando se registra la tarea.<br/>                                              |
| [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Desencadenador que inicia una tarea cuando cambia el estado de una sesión de Terminal Server.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)                             | Desencadenador que inicia una tarea cuando se activa el desencadenador.<br/>                                            |



## <a name="remarks"></a>Observaciones

Al leer o escribir XML, los elementos definidos por este grupo son los elementos secundarios del elemento [**triggers**](taskschedulerschema-triggers-tasktype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





