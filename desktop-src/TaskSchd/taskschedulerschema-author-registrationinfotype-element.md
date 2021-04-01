---
title: Elemento Author (registrationInfoType)
description: Especifica el autor de la tarea.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Programador de tareas del elemento Author
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996610"
---
# <a name="author-registrationinfotype-element"></a>Elemento Author (registrationInfoType)

Especifica el autor de la tarea.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

El tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento **Author** .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el autor de la tarea se especifica mediante la propiedad [**RegistrationInfo. Author**](registrationinfo-author.md) .

En el desarrollo de C++, el autor de la tarea se especifica mediante la propiedad [**IRegistrationInfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define el autor de una tarea.


```XML
<RegistrationInfo>
    <Author></Author>
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

 

 





