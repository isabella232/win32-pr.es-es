---
title: Elemento UserId (logonTriggerType)
description: Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
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
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968567"
---
# <a name="userid-logontriggertype-element"></a>Elemento UserId (logonTriggerType)

Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

El **elemento UserId** se define mediante el tipo [**complejo logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el identificador de usuario para el desencadenador de inicio de sesión se especifica mediante la [**propiedad LogonTrigger.UserId.**](logontrigger-userid.md)

Para el desarrollo de C++, el identificador de usuario para el desencadenador de inicio de sesión se especifica mediante la [**propiedad ILogonTrigger::UserId.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador de inicio de sesión, vea Ejemplo de desencadenador de inicio de [sesión (XML).](logon-trigger-example--xml-.md)

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

 

 





