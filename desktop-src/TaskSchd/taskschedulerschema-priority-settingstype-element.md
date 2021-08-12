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
ms.openlocfilehash: 11b71c88f63e7a3beb3c1c9ec8e1f3253bcd05a567ec5cd077f62175561ce2c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611897"
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

El **elemento Priority** se define mediante el tipo complejo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Observaciones

El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja. El valor predeterminado es 7. El tipo simple [**priorityType**](taskschedulerschema-prioritytype-simpletype.md) establece los valores mínimo y máximo. Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano, y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.

La acción de la tarea se inicia en un proceso con una prioridad que se basa en un valor priority class. Se usa un valor de nivel de prioridad (prioridad del subproceso) para las acciones de controlador COM, cuadro de mensaje y tarea de correo electrónico. Para obtener más información sobre los valores priority class y priority level, vea [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities). En la tabla siguiente se enumeran los valores posibles para el **elemento Priority** y los valores de Priority Class y Priority Level correspondientes.



| Prioridad de la tarea | Priority (clase)                 | Nivel de prioridad                   |
|---------------|--------------------------------|----------------------------------|
| 0             | CLASE \_ PRIORITY EN \_ TIEMPO REAL      | TIEMPO CRÍTICO \_ DE \_ PRIORIDAD DEL \_ SUBPROCESO |
| 1             | HIGH \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ MÁS ALTA DEL \_ SUBPROCESO        |
| 2             | ABOVE \_ NORMAL \_ PRIORITY \_ CLASS | PRIORIDAD \_ DEL SUBPROCESO POR ENCIMA DE LO \_ \_ NORMAL  |
| 3             | ABOVE \_ NORMAL \_ PRIORITY \_ CLASS | PRIORIDAD \_ DEL SUBPROCESO POR ENCIMA DE LO \_ \_ NORMAL  |
| 4             | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 5             | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 6             | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 7             | CLASE POR \_ \_ DEBAJO DE LA PRIORIDAD \_ NORMAL | PRIORIDAD \_ DEL SUBPROCESO POR \_ DEBAJO DE LO \_ NORMAL  |
| 8             | CLASE POR \_ \_ DEBAJO DE LA PRIORIDAD \_ NORMAL | PRIORIDAD \_ DEL SUBPROCESO POR \_ DEBAJO DE LO \_ NORMAL  |
| 9             | IDLE \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ MÁS BAJA DEL \_ SUBPROCESO         |
| 10            | IDLE \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ DE SUBPROCESO \_ INACTIVA           |



 

Para el desarrollo de C++, vea [**Priority Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_priority).

Para el desarrollo de scripts, [**vea TaskSettings.Priority**](tasksettings-priority.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

