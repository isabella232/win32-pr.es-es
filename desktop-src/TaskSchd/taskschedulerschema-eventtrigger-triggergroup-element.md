---
title: Elemento EventTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- desencadenador de evento Programador de tareas, elemento
- Elemento EventTrigger Programador de tareas
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492071"
---
# <a name="eventtrigger-triggergroup-element"></a>Elemento EventTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

El elemento **EventTrigger** está definido por [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                              | Tipo                                                                     | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Retraso (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.<br/>                                |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Suscripción (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Especifica la consulta XPath que identifica el evento que activa el desencadenador.<br/>                                             |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                           |
|------|------|---------------------------------------|
| Identificador   | id   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Se puede crear un máximo de 500 tareas con suscripciones de eventos. Una suscripción de eventos que consulta diversos eventos se puede usar para desencadenar una tarea que utiliza la misma acción en respuesta a los eventos que se registran.

Para el desarrollo de scripts, el objeto [**EventTrigger**](eventtrigger.md) define un desencadenador de eventos.

En el desarrollo de C++, un desencadenador de eventos se define mediante la interfaz [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que utiliza un desencadenador de eventos, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

