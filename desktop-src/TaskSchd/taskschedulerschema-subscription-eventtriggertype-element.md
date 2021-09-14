---
title: Elemento Subscription (eventTriggerType)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968636"
---
# <a name="subscription-eventtriggertype-element"></a>Elemento Subscription (eventTriggerType)

Especifica la consulta XPath que identifica el evento que activa el desencadenador.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

El tipo complejo [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) define el elemento **Subscription.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, la propiedad [**EventTrigger.Subscription**](eventtrigger-subscription.md) especifica la suscripción de eventos.

Para el desarrollo de C++, la propiedad [**IEventTrigger::Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) especifica la suscripción de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





