---
title: Elemento subscription (eventTriggerType)
description: Especifica la consulta XPath que identifica el evento que activa el desencadenador.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Elemento subscription Programador de tareas
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803974"
---
# <a name="subscription-eventtriggertype-element"></a>Elemento subscription (eventTriggerType)

Especifica la consulta XPath que identifica el evento que activa el desencadenador.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

El tipo complejo [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) define el elemento **subscription** .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, la suscripción de eventos se especifica mediante la propiedad [**EventTrigger. subscription**](eventtrigger-subscription.md) .

En el desarrollo de C++, la suscripción de eventos se especifica mediante la propiedad [**IEventTrigger:: subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

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

 

 





