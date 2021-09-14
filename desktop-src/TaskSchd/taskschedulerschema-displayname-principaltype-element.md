---
title: Elemento DisplayName (principalType)
description: Especifica el nombre de la entidad de seguridad que se muestra en la interfaz Programador de tareas usuario.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Programador de tareas
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891513"
---
# <a name="displayname-principaltype-element"></a>Elemento DisplayName (principalType)

Especifica el nombre de la entidad de seguridad que se muestra en la interfaz Programador de tareas usuario.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

El **elemento DisplayName** se define mediante el [**tipo complejo principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el nombre para mostrar de la entidad de seguridad se especifica mediante la [**propiedad Principal.DisplayName.**](principal-displayname.md)

Para el desarrollo de C++, el nombre para mostrar de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal::D isplayName.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname)

## <a name="examples"></a>Ejemplos

En el siguiente XML se define mediante un identificador de grupo y un nombre para mostrar.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



El código XML siguiente define una entidad de seguridad mediante un identificador de usuario y un nombre para mostrar.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





