---
title: Elemento Data (taskType)
description: Define los datos de suma asociados a la tarea, pero el servicio de Programador de tareas de otro modo.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Datos de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071040"
---
# <a name="data-tasktype-element"></a>Elemento Data (taskType)

Define los datos de suma asociados a la tarea, pero el servicio de Programador de tareas de otro modo.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

El **elemento Data** se define mediante el tipo complejo [**taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas trabajo.<br/> |



## <a name="remarks"></a>Observaciones

Como ejemplo de este tipo de datos, el servicio Registros y alertas de rendimiento usa esta propiedad como contenedor de almacenamiento para la consulta de contador de rendimiento asociada a una tarea.

Para el desarrollo de C++, los datos de una tarea se especifican mediante la [**propiedad Data de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

En el desarrollo de scripting, los datos de una tarea se especifican mediante la [**propiedad TaskDefinition.Data.**](taskdefinition-data.md)

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

 

 





