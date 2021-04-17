---
title: DisplayName (principalType), elemento
description: Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535500"
---
# <a name="displayname-principaltype-element"></a>DisplayName (principalType), elemento

Especifica el nombre de la entidad de seguridad que se muestra en la interfaz de usuario de Programador de tareas.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

El elemento **displayName** se define mediante el tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el nombre para mostrar de la entidad de seguridad se especifica mediante la propiedad [**principal. DisplayName**](principal-displayname.md) .

En el desarrollo de C++, el nombre para mostrar de la entidad de seguridad se especifica mediante la propiedad [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un con un identificador de grupo y un nombre para mostrar.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



En el código XML siguiente se define una entidad de seguridad mediante un identificador de usuario y un nombre para mostrar.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





