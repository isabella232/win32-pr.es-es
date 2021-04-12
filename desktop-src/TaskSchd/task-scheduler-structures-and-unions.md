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
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="bf4ad-105">Programador de tareas estructuras y uniones</span><span class="sxs-lookup"><span data-stu-id="bf4ad-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="bf4ad-106">En esta sección se describen las estructuras y las uniones usadas por las API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="bf4ad-107">Programador de tareas 1,0 usan todas las estructuras y uniones siguientes.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="bf4ad-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="bf4ad-108">Name</span></span>                                               | <span data-ttu-id="bf4ad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf4ad-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf4ad-110">**DIARIO**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="bf4ad-111">Define el intervalo, en días, en el que se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="bf4ad-112">**MONTHLYDATE**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="bf4ad-113">Define el día del mes en que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="bf4ad-114">**MONTHLYDOW**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="bf4ad-115">Define las fechas en las que la tarea se ejecuta por mes, semana y día de la semana.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="bf4ad-116">**\_desencadenador de tarea**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="bf4ad-117">Define las horas para ejecutar un [*elemento de trabajo*](w.md)programado.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="bf4ad-118">**\_Unión de tipo de desencadenador \_**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="bf4ad-119">Define la programación de invocación del desencadenador dentro del miembro de **tipo** de una estructura de [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="bf4ad-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="bf4ad-120">**SEMANA**</span><span class="sxs-lookup"><span data-stu-id="bf4ad-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="bf4ad-121">Define el intervalo, en semanas, entre las invocaciones de una tarea.</span><span class="sxs-lookup"><span data-stu-id="bf4ad-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




