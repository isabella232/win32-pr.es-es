---
title: Estructuras de desencadenador para Programador de tareas 1,0
description: Programador de tareas 1,0 utiliza varias estructuras para definir los criterios de un desencadenador.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075854"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="bca83-103">Estructuras de desencadenador para Programador de tareas 1,0</span><span class="sxs-lookup"><span data-stu-id="bca83-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="bca83-104">Programador de tareas 1,0 utiliza varias estructuras para definir los criterios de un desencadenador.</span><span class="sxs-lookup"><span data-stu-id="bca83-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="bca83-105">Para obtener más información sobre los desencadenadores de Programador de tareas 2,0, consulte [interfaces de desencadenador](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="bca83-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="bca83-106">Programador de tareas estructuras 1,0</span><span class="sxs-lookup"><span data-stu-id="bca83-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="bca83-107">En la ilustración siguiente se muestra la estructura del [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="bca83-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="bca83-108">Tiene tres miembros obligatorios (**wBeginYear**, **wBeginMonth** y **wBeginDay**) que se deben establecer al crear un nuevo desencadenador.</span><span class="sxs-lookup"><span data-stu-id="bca83-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="bca83-109">(Para saltar a la página de referencia de esta estructura, haga clic en el nombre de la estructura en la ilustración).</span><span class="sxs-lookup"><span data-stu-id="bca83-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![estructura del desencadenador de tarea](images/tsktri1.png)

<span data-ttu-id="bca83-111">Tenga en cuenta que el miembro **TriggerType** utiliza la enumeración de [**tipo de \_ desencadenador \_ de tarea**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y el miembro de **tipo** utiliza una estructura de **\_ \_ Unión de desencadenador de tarea** .</span><span class="sxs-lookup"><span data-stu-id="bca83-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="bca83-112">La enumeración del **\_ \_ tipo de desencadenador de tarea** se usa para especificar el tipo de desencadenador (tipos de desencadenador basados en eventos y tiempos).</span><span class="sxs-lookup"><span data-stu-id="bca83-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="bca83-113">La estructura de [**\_ \_ Unión de tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa para combinar las estructuras [**Daily**](/windows/desktop/api/Mstask/ns-mstask-daily), [**Weekly**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (Day of month) y [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (Day of Week) que se utilizan para especificar Cuándo se activará un desencadenador basado en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="bca83-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="bca83-114">Si **TriggerType** especifica un desencadenador de una vez o un desencadenador basado en eventos, se omite el miembro de **tipo** .</span><span class="sxs-lookup"><span data-stu-id="bca83-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="bca83-115">La estructura de [**\_ \_ Unión de tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se usa solo si el miembro **TriggerType** especifica un desencadenador de fecha diaria, semanal, día del mes o mensual.</span><span class="sxs-lookup"><span data-stu-id="bca83-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="bca83-116">Además, el valor del miembro de **tipo** indica qué miembro de la estructura [**de \_ \_ Unión del tipo de desencadenador**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bca83-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="bca83-117">En la ilustración siguiente se muestra la relación entre los valores de la enumeración de [**\_ \_ tipo de desencadenador de tarea**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) y los miembros de la estructura de **estructura de \_ tipo \_ de desencadenador** .</span><span class="sxs-lookup"><span data-stu-id="bca83-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="bca83-118">(Para saltar a las páginas de referencia de estas estructuras, haga clic en el nombre de la estructura en la ilustración).</span><span class="sxs-lookup"><span data-stu-id="bca83-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![relación entre los valores de enumeración de tipo de desencadenador de tarea y los miembros de la estructura de estructura tipo de desencadenador](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="bca83-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bca83-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bca83-121">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="bca83-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="bca83-122">Tipos de desencadenador</span><span class="sxs-lookup"><span data-stu-id="bca83-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="bca83-123">Interfaces de desencadenador</span><span class="sxs-lookup"><span data-stu-id="bca83-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




