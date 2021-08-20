---
title: Elemento GroupId (principalType)
description: Especifica el identificador del grupo de usuarios necesario para ejecutar esas tareas asociadas a la entidad de seguridad.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Elemento GroupId Programador de tareas
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131844"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (principalType)

Especifica el identificador del grupo de usuarios necesario para ejecutar esas tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

El **elemento GroupId** se define mediante el [**tipo complejo principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Comentarios

No se puede especificar un identificador de grupo y un identificador de usuario al mismo tiempo. Especifique los elementos [**UserId**](taskschedulerschema-userid-principaltype-element.md) **o GroupId,** pero no ambos.

Para el desarrollo de scripts, el identificador de grupo de la entidad de seguridad se especifica mediante la [**propiedad Principal.GroupId.**](principal-groupid.md)

Para el desarrollo de C++, el identificador de grupo de la entidad de seguridad se especifica mediante la [**propiedad IPrincipal::GroupId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML para una tarea que usa este elemento, vea Ejemplo de desencadenador de inicio de [sesión (XML).](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





