---
title: Elemento ProcessTokenSidType (principalType)
description: Especifica el tipo de identificación de seguridad (SID) del proceso de la tarea.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Programador de tareas del elemento ProcessTokenSidType
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150603"
---
# <a name="processtokensidtype-principaltype-element"></a>Elemento ProcessTokenSidType (principalType)

Especifica el tipo de identificación de seguridad (SID) del proceso de la tarea.

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

El elemento **ProcessTokenSidType** se define mediante el tipo complejo de [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                  | Derivado de                                                           | Descripción                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica las credenciales de seguridad para una entidad de seguridad.<br/> |



## <a name="remarks"></a>Observaciones

En el desarrollo de C++, el tipo de SID de proceso se especifica mediante la propiedad [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define el tipo de SID del proceso de la tarea.


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
</Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





