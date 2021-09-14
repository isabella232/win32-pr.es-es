---
title: Elemento StopAtDurationEnd (repetitionType)
description: Especifica que una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición.
ms.assetid: 4e34b5b2-ac93-4951-9de4-3e89614517d1
keywords:
- Elemento StopAtDurationEnd Programador de tareas
topic_type:
- apiref
api_name:
- StopAtDurationEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a95f15f3a62d05b9bc28dc9f50b924979e2b748c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968647"
---
# <a name="stopatdurationend-repetitiontype-element"></a>Elemento StopAtDurationEnd (repetitionType)

Especifica que una instancia en ejecución de la tarea se detiene al final de la duración del patrón de repetición. Esto solo es aplicable si se establecen repeticiones.

``` syntax
<xs:element name="StopAtDurationEnd"
 type="boolean"
 />
```

El **elemento StopAtDurationEnd** se define mediante el [**tipo complejo repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)

## <a name="parent-element"></a>Elemento primario

| Elemento | Derivado de | Descripción |
|-|-|-|
| [**Repetición**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica la frecuencia con la que se ejecuta la tarea y cuánto tiempo se repite el patrón de repetición después de iniciar la tarea.<br/> |

## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, esta configuración se especifica mediante la [**propiedad RepetitionPattern.StopAtDurationEnd.**](repetitionpattern-stopatdurationend.md)

Para el desarrollo de C++, esta configuración se especifica mediante la [**propiedad IRepetitionPattern::StopAtDurationEnd.**](/windows/win32/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend)

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |

## <a name="see-also"></a>Consulte también

[Programador de tareas de esquema](task-scheduler-schema-elements.md)

[Programador de tareas](task-scheduler-start-page.md)
