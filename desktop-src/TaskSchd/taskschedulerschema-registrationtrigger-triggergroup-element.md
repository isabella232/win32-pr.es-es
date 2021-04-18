---
title: Elemento RegistrationTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se registra la tarea.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Programador de tareas de desencadenador de registro, elemento XML
- Programador de tareas del elemento RegistrationTrigger
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686077"
---
# <a name="registrationtrigger-triggergroup-element"></a>Elemento RegistrationTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se registra la tarea.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

El elemento **RegistrationTrigger** se define mediante el tipo complejo de [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Retraso (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Especifica la cantidad de tiempo entre el momento en que se registra la tarea y el momento en que se inicia la tarea.<br/>                          |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                           |
|------|------|---------------------------------------|
| Identificador   | id   | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, se especifica un desencadenador de registro mediante el objeto [**RegistrationTrigger**](registrationtrigger.md) .

En el desarrollo de C++, se especifica un desencadenador de registro mediante la interfaz [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) . Estos elementos se deben agregar en la secuencia que se muestra a continuación.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Retraso (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de arranque, vea [ejemplo de desencadenador de registro (XML)](registration-trigger-example--xml-.md).

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

 

 





