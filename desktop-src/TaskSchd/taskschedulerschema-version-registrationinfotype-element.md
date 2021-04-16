---
title: Elemento version (registrationInfoType)
description: Especifica el número de versión de la tarea.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento version Programador de tareas
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685880"
---
# <a name="version-registrationinfotype-element"></a>Elemento version (registrationInfoType)

Especifica el número de versión de la tarea.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

El elemento **version** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, la versión de una tarea se especifica mediante la propiedad [**RegistrationInfo. version**](registrationinfo-version.md) .

En el desarrollo de C++, la versión de una tarea se especifica mediante la propiedad [**IRegistrationInfo:: version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define la versión de una tarea.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





