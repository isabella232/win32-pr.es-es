---
title: Elemento Source (registrationInfoType)
description: Especifica de dónde se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Origen del elemento Programador de tareas
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf5532909e8f692aa2c438186a17cf9669170bb4a7d9666682d07ba8d4ea583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139168"
---
# <a name="source-registrationinfotype-element"></a>Elemento Source (registrationInfoType)

Especifica de dónde se originó la tarea. Por ejemplo, desde un componente, un servicio, una aplicación o un usuario.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

El **tipo** complejo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) define el elemento Source.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripting, el origen de una tarea se especifica mediante la [**propiedad RegistrationInfo.Source.**](registrationinfo-source.md)

Para el desarrollo de C++, el origen de una tarea se especifica mediante la [**propiedad IRegistrationInfo::Source.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source)

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

 

 





