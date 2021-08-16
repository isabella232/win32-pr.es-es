---
title: Propiedad TaskSettings.Priority
description: Para el scripting, obtiene o establece el nivel de prioridad de la tarea.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Propiedad Priority Programador de tareas
- Propiedad Priority Programador de tareas , objeto TaskSettings
- Objeto TaskSettings Programador de tareas , propiedad Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b24c0281e8df314b070e0569176899b96071e1ef43caab17af4978e74f6b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354833"
---
# <a name="tasksettingspriority-property"></a>Propiedad TaskSettings.Priority

Para el scripting, obtiene o establece el nivel de prioridad de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valor de propiedad

Nivel de prioridad (0-10) de la tarea. El valor predeterminado es 7.

## <a name="remarks"></a>Comentarios

El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja. El valor predeterminado es 7. Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano, y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.

La acción de la tarea se inicia en un proceso con una prioridad que se basa en un valor priority class. Se usa un valor de nivel de prioridad (prioridad del subproceso) para las acciones de controlador COM, cuadro de mensaje y tarea de correo electrónico. Para obtener más información sobre los valores priority class y priority level, vea [Scheduling Priorities](/windows/desktop/ProcThread/scheduling-priorities). En la tabla siguiente se enumeran los valores posibles para el parámetro *priority* y los valores de Priority Class y Priority Level correspondientes.



| Prioridad de *la tarea* | Priority (clase)                 | Nivel de prioridad                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | CLASE \_ PRIORITY EN \_ TIEMPO REAL      | TIEMPO CRÍTICO \_ DE \_ PRIORIDAD DEL \_ SUBPROCESO |
| 1               | HIGH \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ MÁS ALTA DEL \_ SUBPROCESO        |
| 2               | ABOVE \_ NORMAL \_ PRIORITY \_ CLASS | PRIORIDAD \_ DEL SUBPROCESO POR ENCIMA DE LO \_ \_ NORMAL  |
| 3               | ABOVE \_ NORMAL \_ PRIORITY \_ CLASS | PRIORIDAD \_ DEL SUBPROCESO POR ENCIMA DE LO \_ \_ NORMAL  |
| 4               | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 5               | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 6               | NORMAL \_ PRIORITY \_ (CLASE)        | PRIORIDAD \_ NORMAL DEL \_ SUBPROCESO         |
| 7               | CLASE \_ POR \_ DEBAJO DE LA PRIORIDAD \_ NORMAL | PRIORIDAD \_ DEL SUBPROCESO POR \_ DEBAJO DE LO \_ NORMAL  |
| 8               | CLASE \_ POR \_ DEBAJO DE LA PRIORIDAD \_ NORMAL | PRIORIDAD \_ DEL SUBPROCESO POR \_ DEBAJO DE LO \_ NORMAL  |
| 9               | IDLE \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ MÁS BAJA DEL \_ SUBPROCESO         |
| 10              | IDLE \_ PRIORITY \_ (CLASE)          | PRIORIDAD \_ DE SUBPROCESO \_ INACTIVA           |



 

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) del Programador de tareas esquema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

