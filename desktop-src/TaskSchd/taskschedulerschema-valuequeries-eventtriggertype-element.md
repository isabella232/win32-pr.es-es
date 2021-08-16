---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una secuencia de elementos que contienen un nombre y un valor de consulta XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- ValueQueries, elemento Programador de tareas
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fecf58696618f1f0f359754bc29aa10680dd1717fe55ffe9fc3e87d0b361b76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355348"
---
# <a name="valuequeries-eventtriggertype-element"></a>Elemento ValueQueries (eventTriggerType)

Contiene una secuencia de elementos que contienen un nombre y un valor de consulta XPath. Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el [**elemento Subscription.**](taskschedulerschema-subscription-eventtriggertype-element.md) El nombre del valor de consulta XPath se puede usar como variable en la sección de acción de una tarea.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

El tipo complejo [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) define el elemento **ValueQueries.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                      | Derivado de                                                                 | Descripción                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad ValueQueries de IEventTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries)

Para el desarrollo de scripts, [**consulte EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de eventos mediante este elemento, vea Ejemplo de desencadenador de [eventos (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

