---
title: Elemento GroupId (principalType)
description: Especifica el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.
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
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079635"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (principalType)

Especifica el identificador del grupo de usuarios necesario para ejecutar las tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

El elemento **GROUPID** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

No se puede especificar un identificador de grupo y un identificador de usuario al mismo tiempo. Especifique los elementos [**userid**](taskschedulerschema-userid-principaltype-element.md) o **GROUPID** , pero no ambos.

Para el desarrollo de scripts, el identificador de grupo de la entidad de seguridad se especifica mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .

En el desarrollo de C++, el identificador de grupo de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal:: GROUPID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea que usa este elemento, vea [ejemplo de desencadenador de inicio de sesión (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





