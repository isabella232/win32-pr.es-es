---
title: Interfaces Programador de tareas 1,0
description: Las interfaces que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104271921"
---
# <a name="task-scheduler-10-interfaces"></a>Interfaces Programador de tareas 1,0

\[\[Es posible que esta API se modifique o no esté disponible en versiones posteriores del sistema operativo o del producto. En su lugar, use las [Interfaces Programador de tareas 2,0](task-scheduler-2-0-interfaces.md) o los [tipos enumerados de programador de tareas 2,0](task-scheduler-2-0-enumerated-types.md) . \]\]

Las interfaces que se describen en los siguientes temas proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.

Estos temas contienen una descripción de la interfaz, una lista de las propiedades y los métodos definidos por la interfaz, así como comentarios sobre las circunstancias especiales que se deben anotar al usar la interfaz.


Las siguientes interfaces se incluyen en Programador de tareas 1,0.



| Interfaz                                        | Descripción                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Proporciona los métodos para enumerar las tareas de la [*carpeta tareas programadas*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Proporciona los métodos para tener acceso a la configuración de la hoja de propiedades de una tarea.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Proporciona los métodos para administrar [*elementos de trabajo*](w.md)específicos.                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Proporciona los métodos para ejecutar tareas, obtener o establecer información de tareas y finalizar tareas. Se deriva de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) y hereda todos los métodos de esa interfaz. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Proporciona los métodos para programar tareas.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Proporciona los métodos para tener acceso a los desencadenadores de una tarea y establecer su configuración. Los desencadenadores especifican las horas de inicio de la tarea, los criterios de repetición y otros parámetros que controlan Cuándo se ejecuta una tarea.                                                     |



 

 

 




