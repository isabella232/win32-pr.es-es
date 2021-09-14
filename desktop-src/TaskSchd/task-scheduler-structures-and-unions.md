---
title: Programador de tareas y uniones
description: Enumera las estructuras y uniones usadas por las API Programador de tareas 1.0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Programador de tareas Programador de tareas , referencia, estructuras y uniones
- desencadenadores Programador de tareas , estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253395"
---
# <a name="task-scheduler-structures-and-unions"></a>Programador de tareas y uniones

En esta sección se describen las estructuras y las uniones que usan las API Programador de tareas de trabajo.

Todas las estructuras y uniones siguientes se usan en Programador de tareas 1.0.



| Nombre                                               | Descripción                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**DIARIO**](/windows/desktop/api/Mstask/ns-mstask-daily)                             | Define el intervalo, en días, en el que se ejecuta una tarea.                                                                          |
| [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | Define el día del mes en que se ejecutará la tarea.                                                                                 |
| [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | Define las fechas en las que la tarea se ejecuta por mes, semana y día de la semana.                                                     |
| [**DESENCADENADOR DE \_ TAREAS**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | Define las horas para ejecutar un elemento [*de trabajo programado.*](w.md)                                                  |
| [**TRIGGER \_ TYPE \_ UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | Define la programación de invocación del desencadenador dentro del **miembro Type** de una [**estructura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) |
| [**SEMANAL**](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | Define el intervalo, en semanas, entre las invocaciones de una tarea.                                                                  |



 

 

 




