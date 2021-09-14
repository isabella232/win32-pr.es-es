---
title: Elemento LogonTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- desencadenador logon, elemento XML
- Elemento LogonTrigger Programador de tareas
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259191"
---
# <a name="logontrigger-triggergroup-element"></a>Elemento LogonTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

El **elemento LogonTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)                         | duration                                                                 | Cantidad de tiempo entre el momento en que el usuario inicia sesión y el momento en que se inicia la tarea.<br/>                                              |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo en que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |
| [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)                       | string                                                                   | Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.<br/>                                      |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, se especifica un desencadenador de inicio de sesión mediante el [**objeto LogonTrigger.**](logontrigger.md)

Para el desarrollo de C++, se especifica un desencadenador de inicio de sesión mediante la [**interfaz ILogonTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)

Los elementos secundarios enumerados anteriormente se definen mediante los tipos de elementos complejos [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) y [**logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md) Estos elementos deben agregarse en la secuencia que se muestra a continuación.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Delay (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Atributos

El atributo que se muestra a continuación se define mediante los tipos de elementos complejos [**triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md)

-   Identificador: identificador del desencadenador.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa un desencadenador de inicio de sesión, vea Ejemplo de desencadenador de inicio de [sesión (XML).](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





