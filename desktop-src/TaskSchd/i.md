---
title: I (Programador de tareas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533645"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="a7c15-103">I (Programador de tareas)</span><span class="sxs-lookup"><span data-stu-id="a7c15-103">I (Task Scheduler)</span></span>

<span data-ttu-id="a7c15-104">A B C D [E](e.md) F G H I J K L M N o [p](p.md) Q R [s](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a7c15-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a7c15-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condiciones de inactividad**</span><span class="sxs-lookup"><span data-stu-id="a7c15-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="a7c15-106">Un período de tiempo en el que no hay ninguna entrada de usuario en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a7c15-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="a7c15-107">Las condiciones de inactividad están asociadas a la hora de inicio programada para la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7c15-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="a7c15-108">Estas condiciones se establecen mediante una llamada a [**IScheduledWorkItem:: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span><span class="sxs-lookup"><span data-stu-id="a7c15-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="a7c15-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**desencadenadores inactivos**</span><span class="sxs-lookup"><span data-stu-id="a7c15-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="a7c15-110">Desencadenador basado en eventos que se desencadena cuando el equipo pasa a estar inactivo durante un período de tiempo específico.</span><span class="sxs-lookup"><span data-stu-id="a7c15-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="a7c15-111">Los desencadenadores inactivos se crean estableciendo \_ el \_ miembro de tipo de desencadenador de tarea de la estructura del [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) \_ \_ en desencadenador \_ de evento de tarea en \_ inactivo.</span><span class="sxs-lookup"><span data-stu-id="a7c15-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="a7c15-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tiempo de espera de inactividad**</span><span class="sxs-lookup"><span data-stu-id="a7c15-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="a7c15-113">Intervalo de tiempo (en minutos) utilizado por un desencadenador inactivo o una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="a7c15-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="a7c15-114">Los desencadenadores inactivos son desencadenadores basados en eventos que no están asociados a una hora programada.</span><span class="sxs-lookup"><span data-stu-id="a7c15-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="a7c15-115">Las condiciones de inactividad están asociadas a la hora de inicio programada para la tarea.</span><span class="sxs-lookup"><span data-stu-id="a7c15-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="a7c15-116">El tiempo de inactividad se establece mediante una llamada a [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span><span class="sxs-lookup"><span data-stu-id="a7c15-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




