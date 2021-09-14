---
title: Elemento Delay (registrationTriggerType)
description: Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
keywords:
- Delay, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073408"
---
# <a name="delay-registrationtriggertype-element"></a>Elemento Delay (registrationTriggerType)

Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

El tipo complejo [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) define el elemento **Delay.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                     | Derivado de                                                                               | Descripción                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el retraso del desencadenador de registro se especifica mediante la [**propiedad RegistrationTrigger.Delay.**](registrationtrigger-delay.md)

Para el desarrollo de C++, el retraso del desencadenador de registro se especifica mediante la [**propiedad IRegistrationTrigger::D elay.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay)

## <a name="examples"></a>Ejemplos

El xml siguiente define un retraso del desencadenador de registro que permite un retraso de 5 minutos entre el momento en que se registra la tarea y el momento en que se inicia la tarea.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



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

 

 





