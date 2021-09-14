---
title: Elemento Documentation (registrationInfoType)
description: Especifica cualquier documentación adicional para la tarea.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Elemento documentation Programador de tareas
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891508"
---
# <a name="documentation-registrationinfotype-element"></a>Elemento Documentation (registrationInfoType)

Especifica cualquier documentación adicional para la tarea.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

El **elemento Documentation** se define mediante el tipo complejo [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                           | Derivado de                                                                         | Descripción                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica información administrativa sobre la tarea, como el autor de la tarea y la fecha en que se registra la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Para las aplicaciones de scripting, se especifica documentación de tareas adicional mediante la [**propiedad RegistrationInfo.Documentation.**](registrationinfo-documentation.md)

En el caso de las aplicaciones de C++, se especifica documentación de tareas adicional mediante la [**propiedad IRegistrationInfo::D ocumentation.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





