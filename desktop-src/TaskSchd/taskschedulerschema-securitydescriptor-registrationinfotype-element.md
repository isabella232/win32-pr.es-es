---
title: Elemento SecurityDescriptor (registrationInfoType)
description: Especifica el descriptor de seguridad de la tarea.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Elemento SecurityDescriptor Programador de tareas
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83742ebbbc6b8fb653610bf8e20c00094a3c8a3984123765adf6e953935c9011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099865"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>Elemento SecurityDescriptor (registrationInfoType)

Especifica el descriptor de seguridad de la tarea.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

El tipo complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento **SecurityDescriptor.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, el descriptor de seguridad de una tarea se especifica mediante la [**propiedad RegistrationInfo.SecurityDescriptor.**](registrationinfo-securitydescriptor.md)

Para el desarrollo de C++, el descriptor de seguridad de una tarea se especifica mediante la [**propiedad IRegistrationInfo::SecurityDescriptor.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor)

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

 

 





