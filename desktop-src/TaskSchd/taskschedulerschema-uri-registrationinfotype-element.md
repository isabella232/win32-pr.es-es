---
title: Elemento URI (registrationInfoType)
description: Especifica el URI de la tarea.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Identificador de elemento URI Programador de tareas
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355608"
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



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, el URI de la tarea se especifica mediante la [**propiedad RegistrationInfo.URI.**](registrationinfo-uri.md)

Para el desarrollo de C++, el URI de la tarea se especifica mediante la [**propiedad IRegistrationInfo::URI.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





