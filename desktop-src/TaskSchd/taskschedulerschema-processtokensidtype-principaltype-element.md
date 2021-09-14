---
title: Elemento ProcessTokenSidType (principalType)
description: Especifica el tipo de identificación de seguridad de proceso (SID) de la tarea.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Elemento ProcessTokenSidType Programador de tareas
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891484"
---
# <a name="processtokensidtype-principaltype-element"></a>Elemento ProcessTokenSidType (principalType)

Especifica el tipo de identificación de seguridad de proceso (SID) de la tarea.

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

El tipo complejo [**principalType**](taskschedulerschema-principaltype-complextype.md) define el elemento **ProcessTokenSidType.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad de una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, el tipo de SID de proceso se especifica mediante la propiedad [**IPrincipal2::P rocessTokenSidType.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype)

## <a name="examples"></a>Ejemplos

El xml siguiente define el tipo de SID de proceso de la tarea.


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





