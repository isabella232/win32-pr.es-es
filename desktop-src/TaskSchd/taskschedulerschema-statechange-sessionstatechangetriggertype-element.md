---
title: Elemento StateChange (sessionStateChangeTriggerType)
description: Contiene el tipo de cambio de sesión de Terminal Server que desencadenaría el inicio de una tarea.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- Elemento StateChange Programador de tareas
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356337"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>Elemento StateChange (sessionStateChangeTriggerType)

Contiene el tipo de cambio de sesión de Terminal Server que desencadenaría el inicio de una tarea.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

El tipo complejo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) define el elemento **StateChange.**

## <a name="parent-element"></a>Elemento primario



| Elemento                       | Derivado de                                                                                           | Descripción                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando una sesión de Terminal Server cambia de estado.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Para el desarrollo de scripts, [**vea SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





