---
title: Elemento UserId (sessionStateChangeTriggerType)
description: Contiene el usuario para la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- UserId, elemento Programador de tareas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6f6ddaf196f83d727e4641df6e59375033eb60c076451d70866d9d227ca457d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355581"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>Elemento UserId (sessionStateChangeTriggerType)

Contiene el usuario para la sesión de Terminal Server. Cuando se detecta un cambio de estado de sesión para este usuario, se inicia una tarea.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

El tipo complejo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) define el elemento **UserId.**

## <a name="parent-element"></a>Elemento primario



| Elemento                       | Derivado de                                                                                           | Descripción                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando una sesión de Terminal Server cambia de estado.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad UserId de ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid)

Para el desarrollo de scripts, [**vea SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





