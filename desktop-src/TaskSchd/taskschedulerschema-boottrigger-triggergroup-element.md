---
title: Elemento BootTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se arranca el sistema.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- boot trigger Programador de tareas , elemento XML
- Elemento BootTrigger Programador de tareas
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a9067c5e343db0e3bce0972dc89bfc9fd8857d34a3ff9bd9fd65909c019c2e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309575"
---
# <a name="boottrigger-triggergroup-element"></a>Elemento BootTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se arranca el sistema.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

El **elemento BootTrigger** se define mediante el [**tipo complejo bootTriggerType.**](taskschedulerschema-boottriggertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Especifica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.<br/>                            |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora en que se desactiva el desencadenador. El desencadenador no puede iniciar la tarea después de desactivarla.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo en que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |



## <a name="attributes"></a>Atributos



| Nombre | Tipo       | Descripción                               |
|------|------------|-------------------------------------------|
| Identificador   | **string** | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripts, el objeto [**BootTrigger**](boottrigger.md) define un desencadenador de arranque.

Para el desarrollo de C++, el objeto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) define un desencadenador de arranque.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que especifica un desencadenador de arranque, vea Ejemplo de desencadenador de [arranque (XML).](boot-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





