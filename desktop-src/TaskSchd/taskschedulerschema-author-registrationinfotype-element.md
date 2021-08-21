---
title: Elemento Author (registrationInfoType)
description: Especifica el autor de la tarea.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Elemento Author Programador de tareas
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ef78038d262c6ba25880f6a2b6df5b628f5ddfa262e0ef31f121442e3085f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943252"
---
# <a name="author-registrationinfotype-element"></a>Elemento Author (registrationInfoType)

Especifica el autor de la tarea.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

El tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento **Author.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, el autor de la tarea se especifica mediante la [**propiedad RegistrationInfo.Author.**](registrationinfo-author.md)

Para el desarrollo de C++, el autor de la tarea se especifica mediante la [**propiedad IRegistrationInfo::Author.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author)

## <a name="examples"></a>Ejemplos

El siguiente XML define el autor de una tarea.


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





