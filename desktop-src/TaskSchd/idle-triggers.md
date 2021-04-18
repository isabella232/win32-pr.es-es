---
title: Desencadenadores inactivos para Programador de tareas 1,0
description: Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelva inactivo. Hay varias condiciones que definen Cuándo un equipo pasa a estar inactivo, como cuando no se produce ninguna entrada de teclado o de mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685510"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="9fa7f-104">Desencadenadores inactivos para Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="9fa7f-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="9fa7f-105">Un desencadenador inactivo es un desencadenador basado en eventos que se desencadena un número específico de veces después de que el equipo se vuelva inactivo.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="9fa7f-106">Hay varias condiciones que definen Cuándo un equipo pasa a estar inactivo, como cuando no se produce ninguna entrada de teclado o de mouse.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="9fa7f-107">Los desencadenadores inactivos se crean especificando \_ el desencadenador de evento de tarea \_ \_ en \_ inactivo en el miembro de [**\_ \_ tipo de desencadenador**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) de tarea de la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="9fa7f-108">El desencadenador idle se activa cuando el sistema se queda inactivo durante el período de tiempo especificado por el tiempo de espera de inactividad del elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="9fa7f-109">Cuando \_ \_ se especifica desencadenador de evento \_ de tarea en \_ inactivo, se omiten los miembros **wStartHour**, **wStartMinute** y **Type** de la estructura del [**\_ desencadenador**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de la tarea.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="9fa7f-110">Puede establecer el tiempo de espera de inactividad de un elemento de trabajo llamando al método [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) .</span><span class="sxs-lookup"><span data-stu-id="9fa7f-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="9fa7f-111">Este método establece la cantidad de tiempo (en minutos) que el sistema debe permanecer inactivo antes de que se active el desencadenador y se ejecute el elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fa7f-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="9fa7f-112">Para recuperar el tiempo de inactividad de una tarea, llame al método [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .</span><span class="sxs-lookup"><span data-stu-id="9fa7f-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fa7f-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fa7f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fa7f-114">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="9fa7f-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




