---
title: Elemento repite (triggerBaseType)
description: Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento repite Programador de tareas
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491669"
---
# <a name="repetition-triggerbasetype-element"></a>Elemento repite (triggerBaseType)

Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

El tipo complejo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) define el elemento **repite** .

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



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                   | Tipo     | Descripción                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   | duration | Especifica cuánto tiempo se repite el patrón.<br/>                                                              |
| [**Interval**](taskschedulerschema-interval-repetitiontype-element.md)                   | duration | Especifica la cantidad de tiempo entre cada reinicio de la tarea.<br/>                                           |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean  | Especifica que las instancias en ejecución de la tarea se detienen al final de la duración del patrón de repetición.<br/> |



## <a name="remarks"></a>Observaciones

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces. Las cinco repeticiones se pueden definir con el siguiente patrón.

1.  Una tarea comienza al principio del primer minuto.
2.  La siguiente tarea comienza al final del primer minuto.
3.  La siguiente tarea comienza al final del segundo minuto.
4.  La siguiente tarea comienza al final del tercer minuto.
5.  La siguiente tarea comienza al final del cuarto minuto.

**Windows Server 2003, Windows XP y windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.

**Windows Vista, Windows 7, Windows server 2008, Windows 8 y Windows server 2012:** Normalmente, el establecimiento de la duración de repetición en un múltiplo exacto del intervalo produce los números descritos anteriormente. Sin embargo, en ciertas condiciones de carga pesada, es posible que se agote el tiempo de espera antes de que TaskScheduler pueda iniciar el intervalo de tareas final.

Para el desarrollo de scripting, el patrón de repetición se especifica mediante la propiedad [**Trigger. repite**](trigger-repetition.md) heredada por todos los objetos de desencadenador.

En el desarrollo de C++, el patrón de repetición se especifica mediante la propiedad [**ITRigger:: repite**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) que heredan todas las interfaces del desencadenador.

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de desencadenador de arranque que especifica un patrón de repetición para un desencadenador.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
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

 

 





