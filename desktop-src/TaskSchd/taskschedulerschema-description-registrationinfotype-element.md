---
title: Elemento Description (registrationInfoType)
description: Especifica la descripción de la tarea.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Descripción, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6fef3012913eacfb8b8aa111793bd77255512d551bea0ab123d45b9caed6501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991395"
---
# <a name="description-registrationinfotype-element"></a>Elemento Description (registrationInfoType)

Especifica la descripción de la tarea.

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

El **elemento Description** se define mediante el tipo complejo [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, la descripción de una tarea se especifica mediante la [**propiedad RegistrationInfo.Description.**](registrationinfo-description.md)

Para el desarrollo de C++, la descripción de una tarea se especifica mediante la [**propiedad IRegistrationInfo::D escription.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description)

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

 

 





