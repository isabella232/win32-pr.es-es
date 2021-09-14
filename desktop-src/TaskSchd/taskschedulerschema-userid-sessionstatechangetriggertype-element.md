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
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968563"
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



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea Propiedad UserId de ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid)

Para el desarrollo de scripts, [**vea SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





