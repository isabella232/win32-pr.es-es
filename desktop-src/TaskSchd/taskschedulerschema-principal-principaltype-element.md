---
title: Elemento principal (principalType)
description: Especifica las credenciales de seguridad para una entidad de seguridad.
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
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685882"
---
# <a name="principal-principaltype-element"></a>Elemento principal (principalType)

Especifica las credenciales de seguridad para una entidad de seguridad. Estas credenciales definen el contexto de seguridad en el que se ejecuta una tarea.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

El elemento **principal** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                               | Derivado de                                                             | Descripción                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Entidades de seguridad**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Especifica las entidades de seguridad asociadas a la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                      | Tipo                                                          | Descripción                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Especifica el identificador del grupo de usuarios necesario para ejecutar tareas asociadas a la entidad de seguridad.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Especifica el método de inicio de sesión de seguridad necesario para ejecutar las tareas asociadas a la entidad de seguridad.<br/>  |
| [**Deberían**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Especifica el identificador de usuario necesario para ejecutar tareas asociadas a la entidad de seguridad.<br/>              |



## <a name="attributes"></a>Atributos



| Nombre | Tipo | Descripción                                        |
|------|------|----------------------------------------------------|
| Identificador   | id   | Identificador de la definición de la entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, las credenciales de seguridad de una entidad de seguridad se especifican mediante el objeto [**principal**](principal.md) .

En el desarrollo de C++, las credenciales de seguridad de una entidad de seguridad se especifican mediante la interfaz [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .

Los elementos secundarios enumerados anteriormente se definen mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) . Para obtener información sobre la secuenciación de estos elementos secundarios, vea [**principalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define una entidad de seguridad con un identificador de usuario.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



En el código XML siguiente se define una entidad de seguridad con un identificador de grupo.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





