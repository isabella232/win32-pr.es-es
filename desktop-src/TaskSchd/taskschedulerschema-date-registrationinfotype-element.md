---
title: Elemento Date (registrationInfoType)
description: Especifica la fecha y hora en que se registra la tarea.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Elemento Date Programador de tareas
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071036"
---
# <a name="date-registrationinfotype-element"></a>Elemento Date (registrationInfoType)

Especifica la fecha y hora en que se registra la tarea.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

El **tipo** complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento Date.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, la fecha de registro de una tarea se especifica mediante la [**propiedad RegistrationInfo.Date.**](registrationinfo-date.md)

Para el desarrollo de C++, la fecha de registro de una tarea se especifica mediante la [**propiedad IRegistrationInfo::D ate.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date)

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

 

 





