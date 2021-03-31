---
title: Elemento ValueQueries (eventTriggerType)
description: Contiene una secuencia de elementos, cada uno de los cuales contiene un nombre y un valor de consulta XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Programador de tareas del elemento ValueQueries
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996084"
---
# <a name="valuequeries-eventtriggertype-element"></a>Elemento ValueQueries (eventTriggerType)

Contiene una secuencia de elementos, cada uno de los cuales contiene un nombre y un valor de consulta XPath. Las consultas se aplican a un evento devuelto desde la suscripción de eventos especificada en el elemento [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . El nombre del valor de consulta XPath se puede usar como una variable en la sección de acción de una tarea.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

El elemento **ValueQueries** se define mediante el tipo complejo de [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                      | Derivado de                                                                 | Descripción                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando se produce un evento del sistema.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, consulte la [**propiedad ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Para el desarrollo de scripts, consulte [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de evento mediante este elemento, vea [ejemplo de desencadenador de eventos (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

