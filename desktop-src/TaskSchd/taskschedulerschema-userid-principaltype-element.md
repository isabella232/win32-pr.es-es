---
title: UserId (principalType), elemento
description: Especifica el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422621"
---
# <a name="userid-principaltype-element"></a>UserId (principalType), elemento

Especifica el identificador de usuario necesario para ejecutar las tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

El elemento **userid** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

El elemento **userid** y el elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.

No se puede especificar un identificador de usuario y un identificador de grupo al mismo tiempo. Especifique el **userid** o el elemento [**GROUPID**](taskschedulerschema-groupid-principaltype-element.md) , pero no ambos.

Para el desarrollo de scripts, el identificador de usuario se especifica mediante la propiedad [**principal. userid**](principal-userid.md) .

En el desarrollo de C++, el identificador de usuario se especifica mediante la propiedad [**IPrincipal:: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un principio mediante un identificador de usuario.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





