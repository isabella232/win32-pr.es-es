---
title: Programador de tareas interfaces 1.0
description: Las interfaces que se describen en los temas siguientes proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2033c78594c0f4ef1d9f871275f425ef5189240ed7b432266464343cf86e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975035"
---
# <a name="task-scheduler-10-interfaces"></a>Programador de tareas interfaces 1.0

\[\[Esta API puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto. Use las [interfaces Programador de tareas 2.0 o](task-scheduler-2-0-interfaces.md) Programador de tareas tipos enumerados [de 2.0](task-scheduler-2-0-enumerated-types.md) en su lugar. \]\]

Las interfaces que se describen en los temas siguientes proporcionan acceso mediante programación a la funcionalidad que está disponible en el Programador de tareas que se usa en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.

Estos temas contienen una descripción de la interfaz, una lista de las propiedades y métodos definidos por la interfaz y comentarios sobre las circunstancias especiales que deben tenerse en cuenta al usar la interfaz.


Las interfaces siguientes se presentan en Programador de tareas 1.0.



| Interfaz                                        | Descripción                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Proporciona los métodos para enumerar las tareas en la [*carpeta Tareas programadas*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Proporciona los métodos para acceder a la configuración de la hoja de propiedades de una tarea.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Proporciona los métodos para administrar elementos [*de trabajo específicos.*](w.md)                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Proporciona los métodos para ejecutar tareas, obtener o establecer información de tareas y finalizar tareas. Se deriva de la interfaz [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) y hereda todos los métodos de esa interfaz. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Proporciona los métodos para programar tareas.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Proporciona los métodos para acceder a los desencadenadores y establecer los desencadenadores de una tarea. Los desencadenadores especifican las horas de inicio de la tarea, los criterios de repetición y otros parámetros que controlan cuándo se ejecuta una tarea.                                                     |



 

 

 




