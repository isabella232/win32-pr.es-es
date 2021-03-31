---
title: Propiedad TaskSettings. Priority
description: En el caso de scripting, obtiene o establece el nivel de prioridad de la tarea.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Propiedad Priority Programador de tareas
- Propiedad Priority Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Priority
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
ms.openlocfilehash: 282c688d63bb21f2dc0bab43acde7f089fa960b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996027"
---
# <a name="tasksettingspriority-property"></a>Propiedad TaskSettings. Priority

En el caso de scripting, obtiene o establece el nivel de prioridad de la tarea.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valor de propiedad

Nivel de prioridad (0-10) de la tarea. El valor predeterminado es 7.

## <a name="remarks"></a>Observaciones

El nivel de prioridad 0 es la prioridad más alta y el nivel de prioridad 10 es la prioridad más baja. El valor predeterminado es 7. Los niveles de prioridad 7 y 8 se usan para las tareas en segundo plano y los niveles de prioridad 4, 5 y 6 se usan para las tareas interactivas.

La acción de la tarea se inicia en un proceso con una prioridad basada en un valor de clase de prioridad. Un valor de nivel de prioridad (prioridad de subproceso) se usa para las acciones de tareas de correo electrónico, el cuadro de mensaje y el controlador COM. Para obtener más información sobre la clase de prioridad y los valores de nivel de prioridad, vea [programación de prioridades](/windows/desktop/ProcThread/scheduling-priorities). En la tabla siguiente se enumeran los valores posibles para el parámetro *Priority* y los valores de nivel de prioridad y clase de prioridad correspondientes.



| *Prioridad* de la tarea | Priority (clase)                 | Nivel de prioridad                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | \_clase de prioridad en tiempo real \_      | tiempo de prioridad de subproceso \_ \_ \_ crítico |
| 1               | \_clase de prioridad alta \_          | prioridad de subproceso \_ \_ más alta        |
| 2               | POR encima de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por encima de lo \_ normal  |
| 3               | POR encima de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por encima de lo \_ normal  |
| 4               | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 5               | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 6               | \_clase de prioridad normal \_        | prioridad de subproceso \_ \_ normal         |
| 7               | POR debajo de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por debajo de lo \_ normal  |
| 8               | POR debajo de la \_ \_ clase de prioridad normal \_ | prioridad de subproceso \_ \_ por debajo de lo \_ normal  |
| 9               | \_clase de prioridad INactiva \_          | prioridad de subproceso \_ \_ más baja         |
| 10              | \_clase de prioridad INactiva \_          | prioridad de subproceso \_ \_ inactiva           |



 

Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

