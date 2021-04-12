---
title: Ejemplo de finalización de una tarea
description: Puede finalizar una tarea mientras se está ejecutando mediante una llamada a IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271316"
---
# <a name="terminating-a-task-example"></a>Ejemplo de finalización de una tarea

Puede finalizar una tarea mientras se está ejecutando mediante una llamada a [**IScheduledWorkItem:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

En el procedimiento siguiente se describe cómo finalizar una tarea si se está ejecutando.

**Para finalizar una tarea si se está ejecutando**

1.  Llame a [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto programador de tareas. (En este ejemplo se da por supuesto que el servicio Programador de tareas se está ejecutando).
2.  Llame a [**ITaskScheduler:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la interfaz [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "test Task").
3.  Llame a **ITask:: getStatus** para averiguar si la tarea se está ejecutando. (Tenga en cuenta que [**getStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).
4.  Compruebe el estado de la tarea y, a continuación, llame a **ITask:: Terminate** si se está ejecutando la tarea. (Tenga en cuenta que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)).



| Para obtener un ejemplo de código de                | Vea                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Comprobar el estado de una tarea conocida | [Ejemplo de código de C/C++: finalizar una tarea](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de Programador de tareas 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 