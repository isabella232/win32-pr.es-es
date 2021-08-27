---
title: Elemento SessionStateChangeTrigger (triggerGroup)
description: Especifica un desencadenador que inicia una tarea cuando una sesión de Terminal Server cambia de estado.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Elemento SessionStateChangeTrigger Programador de tareas
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099825"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Elemento SessionStateChangeTrigger (triggerGroup)

Especifica un desencadenador que inicia una tarea cuando una sesión de Terminal Server cambia de estado.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

El **elemento SessionStateChangeTrigger** se define mediante [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Desencadenadores**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Especifica los desencadenadores que inician la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                      | Tipo                                                                                    | Descripción                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica un valor que indica la longitud del retraso antes de que se inicia una tarea cuando se detecta un cambio de estado de sesión de Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica el tipo de cambio de sesión de Terminal Server que desencadenaría el inicio de una tarea.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica el usuario para la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.<br/>              |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, se especifica un desencadenador de cambio de estado de sesión mediante el [**objeto SessionStateChangeTrigger.**](sessionstatechangetrigger.md)

Para el desarrollo de C++, se especifica un desencadenador de cambio de estado de sesión mediante la [**interfaz ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





