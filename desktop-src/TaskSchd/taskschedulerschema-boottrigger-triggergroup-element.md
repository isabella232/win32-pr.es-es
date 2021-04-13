---
title: Elemento BootTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- desencadenador de arranque Programador de tareas, elemento XML
- Programador de tareas del elemento BootTrigger
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359788"
---
# <a name="boottrigger-triggergroup-element"></a>Elemento BootTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando se inicia el sistema.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

El elemento **BootTrigger** se define mediante el tipo complejo de [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                        | Tipo                                                                     | Descripción                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Retraso (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Especifica la cantidad de tiempo entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.<br/>                            |
| [**Habilitado (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Especifica que el desencadenador está habilitado.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Especifica la fecha y hora de desactivación del desencadenador. El desencadenador no puede iniciar la tarea después de que se haya desactivado.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica la cantidad máxima de tiempo que el desencadenador puede iniciar la tarea.<br/>                                   |
| [**Repetición (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición una vez iniciada la tarea.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Especifica la fecha y hora en que se activa el desencadenador.<br/>                                                              |



## <a name="attributes"></a>Atributos



| Nombre | Tipo       | Descripción                               |
|------|------------|-------------------------------------------|
| Identificador   | **string** | Identificador del desencadenador.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, un desencadenador de arranque se define mediante el objeto [**BootTrigger**](boottrigger.md) .

En el desarrollo de C++, el objeto [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) define un desencadenador de arranque.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de arranque, vea [ejemplo de desencadenador de arranque (XML)](boot-trigger-example--xml-.md).

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

 

 





