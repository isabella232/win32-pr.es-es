---
title: Elemento EventTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- desencadenador de eventos Programador de tareas elemento ,
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
ms.openlocfilehash: 555c8683933b2242d119fc00f29c6d0a33188f6404ca48a00e8a127dd59aa791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424475"
---
# <a name="eventtrigger-triggergroup-element"></a>Elemento EventTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

El **elemento EventTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                              | Tipo                                                                     | Descripción                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Especifica la cantidad de tiempo entre el momento en que se produce el evento y el momento en que se inicia la tarea.<br/>                                |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Especifica la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**Suscripción (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Especifica la consulta XPath que identifica el evento que activa el desencadenador.<br/>                                             |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                           |
|------|------|---------------------------------------|
| Identificador   | ID   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Se puede crear un máximo de 500 tareas con suscripciones de eventos. Una suscripción de eventos que consulta diversos eventos se puede usar para desencadenar una tarea que usa la misma acción en respuesta a los eventos que se registran.

Para el desarrollo de scripts, el objeto [**EventTrigger**](eventtrigger.md) define un desencadenador de eventos.

Para el desarrollo de C++, la interfaz [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) define un desencadenador de eventos.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa un desencadenador de eventos, vea Ejemplo de desencadenador de [eventos (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

