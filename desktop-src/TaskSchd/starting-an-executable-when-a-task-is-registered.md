---
title: Iniciar un archivo ejecutable cuando se registra una tarea
description: La escritura de una tarea que inicia un ejecutable cuando se registra una tarea se realiza mediante la definición de un desencadenador de registro y una acción ejecutable.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Programador de tareas ejemplos Programador de tareas, desencadenador de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994341"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a><span data-ttu-id="7a9d3-104">Iniciar un archivo ejecutable cuando se registra una tarea</span><span class="sxs-lookup"><span data-stu-id="7a9d3-104">Starting an Executable When a Task is Registered</span></span>

<span data-ttu-id="7a9d3-105">La escritura de una tarea que inicia un ejecutable cuando se registra una tarea se realiza mediante la definición de un desencadenador de registro y una acción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-105">Writing a task that starts an executable when a task is registered is done by defining a registration trigger and an executable action.</span></span>

## <a name="registration-trigger"></a><span data-ttu-id="7a9d3-106">Desencadenador de registro</span><span class="sxs-lookup"><span data-stu-id="7a9d3-106">Registration Trigger</span></span>

<span data-ttu-id="7a9d3-107">Los desencadenadores de registro inician una tarea en cuanto se registra.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-107">Registration triggers start a task as soon as it is registered.</span></span> <span data-ttu-id="7a9d3-108">También puede especificar un retraso para el desencadenador de registro, que inicia una tarea después de un período de tiempo específico (retraso) una vez registrada la tarea.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-108">You can also specify a delay for the registration trigger, which starts a task after a specific amount of time (the delay) after the task is registered.</span></span> <span data-ttu-id="7a9d3-109">El retraso se especifica en la propiedad [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) de la interfaz [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) ([**RegistrationTrigger**](registrationtrigger.md) para scripting).</span><span class="sxs-lookup"><span data-stu-id="7a9d3-109">The delay is specified in the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property of the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface ([**RegistrationTrigger**](registrationtrigger.md) for scripting).</span></span>

> [!Note]  
> <span data-ttu-id="7a9d3-110">Cuando se actualiza una tarea con un desencadenador de registro, la tarea se ejecutará después de que se produzca la actualización.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-110">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

## <a name="registration-trigger-examples"></a><span data-ttu-id="7a9d3-111">Ejemplos de desencadenadores de registro</span><span class="sxs-lookup"><span data-stu-id="7a9d3-111">Registration Trigger Examples</span></span>

<span data-ttu-id="7a9d3-112">En los siguientes ejemplos se inicia el Bloc de notas cuando se registra una tarea:</span><span class="sxs-lookup"><span data-stu-id="7a9d3-112">The following examples start Notepad when a task is registered:</span></span>

-   [<span data-ttu-id="7a9d3-113">Ejemplo de desencadenador de registro (scripting)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-113">Registration Trigger Example (Scripting)</span></span>](registration-trigger-example--scripting-.md)
-   [<span data-ttu-id="7a9d3-114">Ejemplo de desencadenador de registro (C++)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-114">Registration Trigger Example (C++)</span></span>](registration-trigger-example--c---.md)
-   [<span data-ttu-id="7a9d3-115">Ejemplo de desencadenador de registro (XML)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-115">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="7a9d3-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a9d3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a9d3-117">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="7a9d3-117">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




