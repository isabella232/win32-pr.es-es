---
title: Elemento URI (registrationInfoType)
description: Especifica el URI de la tarea.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Elemento URI Programador de tareas
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be3f5782ba5fc02bc3309abfe337c029d0341667
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968571"
---
# <a name="uri-registrationinfotype-element"></a>Elemento URI (registrationInfoType)

Especifica el URI de la tarea. Este elemento se usa para especificar dónde se coloca la tarea registrada en la jerarquía de carpetas de tareas.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

El **elemento URI** se define mediante el tipo complejo [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripting, el URI de la tarea se especifica mediante la [**propiedad RegistrationInfo.URI.**](registrationinfo-uri.md)

Para el desarrollo de C++, el URI de la tarea se especifica mediante la [**propiedad IRegistrationInfo::URI.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





