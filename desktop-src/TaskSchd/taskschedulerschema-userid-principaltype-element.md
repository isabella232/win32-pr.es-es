---
title: Elemento UserId (principalType)
description: Especifica el identificador de usuario necesario para ejecutar esas tareas asociadas a la entidad de seguridad.
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
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959535"
---
# <a name="userid-principaltype-element"></a>Elemento UserId (principalType)

Especifica el identificador de usuario necesario para ejecutar esas tareas asociadas a la entidad de seguridad.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

El **elemento UserId** se define mediante el [**tipo complejo principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Comentarios

El **elemento UserId** y [**el elemento LogonType**](taskschedulerschema-logontype-principaltype-element.md) se usan juntos para definir el usuario necesario para ejecutar las tareas que usan esta entidad de seguridad.

No se puede especificar un identificador de usuario y un identificador de grupo al mismo tiempo. Especifique el **UserId o** el [**elemento GroupId,**](taskschedulerschema-groupid-principaltype-element.md) pero no ambos.

Para el desarrollo de scripting, el identificador de usuario se especifica mediante la [**propiedad Principal.UserId.**](principal-userid.md)

Para el desarrollo de C++, el identificador de usuario se especifica mediante la [**propiedad IPrincipal::UserId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)

## <a name="examples"></a>Ejemplos

El código XML siguiente define un principio mediante un identificador de usuario.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





