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
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968648"
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



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea StateChange Property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Para el desarrollo de scripts, [**vea SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





