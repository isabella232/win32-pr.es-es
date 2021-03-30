---
title: Elemento Data (taskType)
description: Define los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Programador de tareas de elementos de datos
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801771"
---
# <a name="data-tasktype-element"></a>Elemento Data (taskType)

Define los datos de suma que están asociados a la tarea, pero que no usa el servicio Programador de tareas.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

El elemento de **datos** se define mediante el tipo complejo de [**taskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define la tarea que realiza el servicio Programador de tareas.<br/> |



## <a name="remarks"></a>Observaciones

Como ejemplo de este tipo de datos, el servicio Registros y alertas de rendimiento usa esta propiedad como contenedor de almacenamiento para la consulta de contador de rendimiento asociada a una tarea.

En el desarrollo de C++, los datos de una tarea se especifican mediante la [**propiedad data de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

En el desarrollo de scripting, los datos de una tarea se especifican mediante la propiedad [**TaskDefinition. Data**](taskdefinition-data.md) .

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

 

 





