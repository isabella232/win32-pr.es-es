---
title: Elemento TimeTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- Elemento TimeTrigger Programador de tareas
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968607"
---
# <a name="timetrigger-triggergroup-element"></a>Elemento TimeTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

El **elemento TimeTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo en que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador. Este elemento es obligatorio.<br/>                                    |



## <a name="attributes"></a>Atributos



| Nombre | Tipo       | Descripción                               |
|------|------------|-------------------------------------------|
| Identificador   | **string** | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

El [**elemento StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) es un elemento necesario para los desencadenadores time y calendar **(TimeTrigger** [**y CalendarTrigger).**](taskschedulerschema-calendartrigger-triggergroup-element.md)

Para el desarrollo de scripting, se especifica un desencadenador de tiempo mediante el [**objeto TimeTrigger.**](timetrigger.md)

Para el desarrollo de C++, se especifica un desencadenador de tiempo mediante la [**interfaz ITimeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)

Los elementos secundarios enumerados anteriormente se definen mediante los [**tipos de elementos complejos triggerBaseType.**](taskschedulerschema-triggerbasetype-complextype.md) Estos elementos deben agregarse en la secuencia que se muestra a continuación.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que especifica un desencadenador de hora, vea Ejemplo de desencadenador [de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





