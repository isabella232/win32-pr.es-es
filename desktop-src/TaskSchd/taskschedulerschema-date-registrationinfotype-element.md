---
title: Elemento Date (registrationInfoType)
description: Especifica la fecha y hora en que se registra la tarea.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Programador de tareas de elemento de fecha
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150604"
---
# <a name="date-registrationinfotype-element"></a>Elemento Date (registrationInfoType)

Especifica la fecha y hora en que se registra la tarea.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

El elemento **Date** se define mediante el tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica la información administrativa de la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, la fecha de registro de una tarea se especifica mediante la propiedad [**RegistrationInfo. Date**](registrationinfo-date.md) .

En el desarrollo de C++, la fecha de registro de una tarea se especifica mediante la propiedad [**IRegistrationInfo::D Alizar**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .

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

 

 





