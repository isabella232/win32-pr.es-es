---
title: Elemento Version (registrationInfoType)
description: Especifica el número de versión de la tarea.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento Version Programador de tareas
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168833"
---
# <a name="version-registrationinfotype-element"></a>Elemento Version (registrationInfoType)

Especifica el número de versión de la tarea.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

El **tipo** complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento Version.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, la versión de una tarea se especifica mediante [**la propiedad RegistrationInfo.Version.**](registrationinfo-version.md)

Para el desarrollo de C++, la versión de una tarea se especifica mediante [**la propiedad IRegistrationInfo::Version.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version)

## <a name="examples"></a>Ejemplos

El xml siguiente define la versión de una tarea.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





