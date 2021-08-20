---
title: Elemento Principal (principalType)
description: Especifica las credenciales de seguridad de una entidad de seguridad.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Elemento principal Programador de tareas
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8301371acc7624b4beb9b548191afa641ed267592b246cca7ba71ff170a9bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059783"
---
# <a name="principal-principaltype-element"></a>Elemento Principal (principalType)

Especifica las credenciales de seguridad de una entidad de seguridad. Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

El **tipo complejo principalType** define el [**elemento**](taskschedulerschema-principaltype-complextype.md) Principal.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                               | Derivado de                                                             | Descripción                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Entidades de seguridad**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Especifica las entidades de seguridad asociadas a la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                      | Tipo                                                          | Descripción                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Displayname**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Especifica el nombre de la entidad de seguridad que se muestra en la interfaz Programador de tareas usuario.<br/>                 |
| [**Groupid**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Especifica el identificador del grupo de usuarios necesario para ejecutar tareas asociadas a la entidad de seguridad.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Especifica el método de inicio de sesión de seguridad necesario para ejecutar esas tareas asociadas a la entidad de seguridad.<br/>  |
| [**Userid**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Especifica el identificador de usuario necesario para ejecutar tareas asociadas a la entidad de seguridad.<br/>              |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                                        |
|------|------|----------------------------------------------------|
| Identificador   | ID   | Identificador de la definición de entidad de seguridad.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, las credenciales de seguridad de una entidad de seguridad se especifican mediante el [**objeto Principal.**](principal.md)

Para el desarrollo de C++, las credenciales de seguridad de una entidad de seguridad se especifican mediante la [**interfaz IPrincipal.**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal)

Los elementos secundarios enumerados anteriormente se definen mediante el [**tipo complejo principalType.**](taskschedulerschema-principaltype-complextype.md) Para obtener información de secuenciación para estos elementos secundarios, vea [**principalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Ejemplos

El xml siguiente define una entidad de seguridad con un identificador de usuario.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



El xml siguiente define una entidad de seguridad con un identificador de grupo.


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
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

 

 





