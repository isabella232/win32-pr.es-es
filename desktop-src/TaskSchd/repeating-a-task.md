---
title: Repetir una tarea
description: Programador de tareas puede ejecutar una tarea cualquier número de veces después de que se desencadene un desencadenador.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- patrón de repetición Programador de tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357410"
---
# <a name="repeating-a-task"></a><span data-ttu-id="88084-104">Repetir una tarea</span><span class="sxs-lookup"><span data-stu-id="88084-104">Repeating A Task</span></span>

<span data-ttu-id="88084-105">Programador de tareas puede ejecutar una tarea cualquier número de veces después de que se desencadene un desencadenador.</span><span class="sxs-lookup"><span data-stu-id="88084-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="88084-106">Para ello, el desencadenador define un patrón de repetición que indica Programador de tareas cuánto tiempo debe continuar repitiendo la tarea y el intervalo de tiempo entre cada repetición de tarea.</span><span class="sxs-lookup"><span data-stu-id="88084-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="88084-107">Patrón de repetición</span><span class="sxs-lookup"><span data-stu-id="88084-107">Repetition Pattern</span></span>

<span data-ttu-id="88084-108">En la ilustración siguiente se muestra un patrón de repetición con una duración de 60 minutos y un intervalo de 25 minutos.</span><span class="sxs-lookup"><span data-stu-id="88084-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="88084-109">Tenga en cuenta que, en este caso, Programador de tareas ejecuta la tarea cuando se activa el desencadenador, vuelve a ejecutar la tarea después de 25 minutos y, a continuación, vuelve a ejecutar la tarea después de 50 minutos, según el valor de la [**propiedad StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) para scripting).</span><span class="sxs-lookup"><span data-stu-id="88084-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="88084-110">Si la propiedad **StopAtDurationEnd** está establecida en True, programador de tareas detiene la última instancia de la tarea si todavía se está ejecutando después de 60 minutos.</span><span class="sxs-lookup"><span data-stu-id="88084-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="88084-111">Si la propiedad **StopAtDurationEnd** se establece en false, la última instancia de la tarea se ejecuta independientemente de la duración.</span><span class="sxs-lookup"><span data-stu-id="88084-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![patrón de repetición de desencadenador](images/repetition-pattern.png)

<span data-ttu-id="88084-113">Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cinco veces.</span><span class="sxs-lookup"><span data-stu-id="88084-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="88084-114">Las cinco repeticiones se pueden definir con el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="88084-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="88084-115">Una tarea comienza al principio del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="88084-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="88084-116">La siguiente tarea comienza al final del primer minuto.</span><span class="sxs-lookup"><span data-stu-id="88084-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="88084-117">La siguiente tarea comienza al final del segundo minuto.</span><span class="sxs-lookup"><span data-stu-id="88084-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="88084-118">La siguiente tarea comienza al final del tercer minuto.</span><span class="sxs-lookup"><span data-stu-id="88084-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="88084-119">La siguiente tarea comienza al final del cuarto minuto.</span><span class="sxs-lookup"><span data-stu-id="88084-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="88084-120">**Windows Server 2003, Windows XP y windows 2000:** Si registra una tarea que contiene un desencadenador con un intervalo de repetición igual a un minuto y una duración de repetición igual a cuatro minutos, la tarea se iniciará cuatro veces.</span><span class="sxs-lookup"><span data-stu-id="88084-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="88084-121">Objetos, interfaces y elementos XML</span><span class="sxs-lookup"><span data-stu-id="88084-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="88084-122">Para el desarrollo de scripting, el patrón de repetición se define mediante el objeto [**RepetitionPattern**](repetitionpattern.md) .</span><span class="sxs-lookup"><span data-stu-id="88084-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="88084-123">En el desarrollo de C++, el patrón de repetición se define mediante la interfaz [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .</span><span class="sxs-lookup"><span data-stu-id="88084-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="88084-124">Al leer o escribir XML para una tarea, el patrón de repetición se especifica en el elemento [**repite**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="88084-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88084-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88084-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88084-126">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="88084-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




