---
title: Tipo complejo de sessionStateChangeTriggerType
description: Define los elementos que se usan para crear un desencadenador de tarea para la conexión o desconexión de la consola, la conexión remota o la desconexión o las notificaciones de bloqueo o desbloqueo de estación de trabajo.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- tipo complejo de sessionStateChangeTriggerType Programador de tareas
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359858"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Tipo complejo de sessionStateChangeTriggerType

Define los elementos que se usan para crear un desencadenador de tarea para la conexión o desconexión de la consola, la conexión remota o la desconexión o las notificaciones de bloqueo o desbloqueo de estación de trabajo.

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                      | Tipo                                                                                    | Descripción                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delay**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica un valor que indica la duración del retraso antes de que se inicie una tarea cuando se detecta un cambio de estado de sesión Terminal Server.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica el tipo de Terminal Server cambio de sesión que desencadenaría el inicio de una tarea.<br/>                                                     |
| [**Deberían**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica el usuario de la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.<br/>              |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





