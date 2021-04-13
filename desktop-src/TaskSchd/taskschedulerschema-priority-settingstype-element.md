---
title: Elemento Priority (settingsType)
description: Especifica el nivel de prioridad de la tarea.
ms.assetid: 4885fffa-b7d9-4f5e-b6e8-6f18b01c2427
keywords:
- Elemento Priority Programador de tareas
topic_type:
- apiref
api_name:
- Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecda59ecbbe23550363fb30706d73bca54fcd925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422033"
---
# <a name="priority-settingstype-element"></a>Elemento Priority (settingsType)

Especifica el nivel de prioridad de la tarea.

``` syntax
<xs:element name="Priority"
    type="priorityType"
    default="7"
    minOccurs="0"
 />
```

El elemento de **prioridad** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja. El valor predeterminado es 7. Los valores mínimo y máximo se establecen mediante el tipo simple [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) . Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.

La acción de la tarea se inicia en un proceso con una prioridad basada en un valor de clase de prioridad. Un valor de nivel de prioridad (prioridad de subproceso) se usa para las acciones de tareas de correo electrónico, el cuadro de mensaje y el controlador COM. Para obtener más información sobre la clase de prioridad y los valores de nivel de prioridad, vea [programación de prioridades](/windows/desktop/ProcThread/scheduling-priorities). En la tabla siguiente se enumeran los valores posibles para el elemento **Priority** y los valores de nivel de prioridad y clase de prioridad correspondientes.



| Prioridad de la tarea | Priority (clase)                 | Nivel de prioridad                   |
|---------------|--------------------------------|----------------------------------|
| 0             | \_clase de prioridad en tiempo real \_      | tiempo de prioridad de subproceso \_ \_ \_ crítico |
| 1             | \_clase de prioridad alta \_          | prioridad de subproceso \_ \_ más alta        |
| 2             | POR encima de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por encima de lo \_ normal  |
| 3             | POR encima de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por encima de lo \_ normal  |
| 4             | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 5             | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 6             | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 7             | POR debajo de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por debajo de lo \_ normal  |
| 8             | POR debajo de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por debajo de lo \_ normal  |
| 9             | \_clase de prioridad INactiva \_          | prioridad de subproceso \_ \_ más baja         |
| 10            | \_clase de prioridad INactiva \_          | prioridad de subproceso \_ \_ inactiva           |



 

Para el desarrollo de C++, vea [**propiedad Priority de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Para el desarrollo de scripts, vea [**TaskSettings. Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

