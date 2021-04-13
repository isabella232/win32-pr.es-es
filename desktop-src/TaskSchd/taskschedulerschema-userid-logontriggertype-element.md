---
title: UserId (logonTriggerType), elemento
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535481"
---
# <a name="userid-logontriggertype-element"></a>UserId (logonTriggerType), elemento

Identificador del usuario. La tarea se inicia cuando este usuario inicia sesión en el equipo.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

El elemento **userid** se define mediante el tipo complejo [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Especifica un desencadenador que inicia una tarea cuando un usuario inicia sesión.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el identificador de usuario para el desencadenador logon se especifica mediante la propiedad [**LogonTrigger. userid**](logontrigger-userid.md) .

En el desarrollo de C++, el identificador de usuario para el desencadenador logon se especifica mediante la propiedad [**ILogonTrigger:: userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que especifica un desencadenador Logon, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





