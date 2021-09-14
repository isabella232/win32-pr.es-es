---
title: Terminación de un ejemplo de tarea
description: Puede finalizar una tarea mientras se ejecuta llamando a IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068647"
---
# <a name="terminating-a-task-example"></a>Terminación de un ejemplo de tarea

Puede finalizar una tarea mientras se está ejecutando llamando a [**IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

En el procedimiento siguiente se describe cómo finalizar una tarea si se está ejecutando.

**Para finalizar una tarea si se está ejecutando**

1.  Llame a [**CoInitialize para**](/windows/win32/api/objbase/nf-objbase-coinitialize) inicializar la biblioteca COM y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener Programador de tareas objeto. (En este ejemplo se da por supuesto que Programador de tareas servicio está en ejecución).
2.  Llame [**a ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) para obtener la [**interfaz ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) del objeto de tarea. (Tenga en cuenta que en este ejemplo se obtiene la tarea "Tarea de prueba").
3.  Llame **a ITask::GetStatus** para averiguar si la tarea se está ejecutando. (Tenga en [**cuenta que GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) es un [**método IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)
4.  Compruebe el estado de la tarea y, a continuación, llame **a ITask::Terminate** si la tarea se está ejecutando. (Tenga en [**cuenta que Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) es un método [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) heredado por [**ITask).**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Para obtener un ejemplo de código de                | Vea                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Comprobación del estado de una tarea conocida | [Ejemplo de código de C/C++: Terminación de una tarea](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas ejemplos de 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 