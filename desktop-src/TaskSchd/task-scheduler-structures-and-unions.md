---
title: Programador de tareas estructuras y uniones
description: Enumera las estructuras y las uniones usadas por las API de Programador de tareas 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Programador de tareas Programador de tareas, referencia, estructuras y uniones
- desencadenadores Programador de tareas, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268388"
---
# <a name="task-scheduler-structures-and-unions"></a>Programador de tareas estructuras y uniones

En esta sección se describen las estructuras y las uniones usadas por las API de Programador de tareas.

Programador de tareas 1,0 usan todas las estructuras y uniones siguientes.



| Nombre                                               | Descripción                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**DIARIO**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Define el intervalo, en días, en el que se ejecuta una tarea.                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Define el día del mes en que se ejecutará la tarea.                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Define las fechas en las que la tarea se ejecuta por mes, semana y día de la semana.                                                     |
| [**\_desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Define las horas para ejecutar un [*elemento de trabajo*](w.md)programado.                                                  |
| [**\_Unión de tipo de desencadenador \_**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Define la programación de invocación del desencadenador dentro del miembro de **tipo** de una estructura de [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . |
| [**SEMANA**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Define el intervalo, en semanas, entre las invocaciones de una tarea.                                                                  |



 

 

 




