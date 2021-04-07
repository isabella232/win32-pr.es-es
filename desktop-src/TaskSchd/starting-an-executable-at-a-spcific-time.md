---
title: Iniciar un archivo ejecutable en un momento específico
description: La escritura de una tarea que inicia un ejecutable en un momento determinado se realiza definiendo un desencadenador de tiempo y una acción ejecutable.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Programador de tareas ejemplos Programador de tareas, Time Trigger
- Programador de tareas ejemplos Programador de tareas, iniciar un archivo ejecutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903652"
---
# <a name="starting-an-executable-at-a-specific-time"></a><span data-ttu-id="0dc1d-105">Iniciar un archivo ejecutable en un momento específico</span><span class="sxs-lookup"><span data-stu-id="0dc1d-105">Starting an Executable at a Specific Time</span></span>

<span data-ttu-id="0dc1d-106">La escritura de una tarea que inicia un ejecutable en un momento determinado se realiza definiendo un desencadenador de tiempo y una acción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-106">Writing a task that starts an executable at a specific time is done by defining a time trigger and an executable action.</span></span>

## <a name="start-boundary"></a><span data-ttu-id="0dc1d-107">Límite de inicio</span><span class="sxs-lookup"><span data-stu-id="0dc1d-107">Start Boundary</span></span>

<span data-ttu-id="0dc1d-108">Es importante tener en cuenta que un desencadenador de tiempo es diferente de otros desencadenadores basados en tiempo en que se activa cuando el desencadenador se activa por su límite de inicio.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-108">It is important to note that a time trigger is different from other time-based triggers in that it is fired when the trigger is activated by its start boundary.</span></span> <span data-ttu-id="0dc1d-109">Los otros desencadenadores basados en el tiempo se activan por su límite de inicio, pero no comienzan a realizar sus acciones (en este caso, iniciar un ejecutable) hasta que se alcanza una fecha programada.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-109">Other time-based triggers are activated by their start boundary, but they do not start performing their actions (in this case starting an executable) until a scheduled date is reached.</span></span>

## <a name="time-trigger-examples"></a><span data-ttu-id="0dc1d-110">Ejemplos de desencadenadores Time</span><span class="sxs-lookup"><span data-stu-id="0dc1d-110">Time Trigger Examples</span></span>

<span data-ttu-id="0dc1d-111">En los siguientes ejemplos se inicia el Bloc de notas 30 segundos después de activar la tarea:</span><span class="sxs-lookup"><span data-stu-id="0dc1d-111">The following examples start Notepad 30 seconds after the task is activated:</span></span>

-   [<span data-ttu-id="0dc1d-112">Ejemplo de desencadenador de tiempo (C++)</span><span class="sxs-lookup"><span data-stu-id="0dc1d-112">Time Trigger Example (C++)</span></span>](time-trigger-example--c---.md)
-   [<span data-ttu-id="0dc1d-113">Ejemplo de desencadenador de tiempo (scripting)</span><span class="sxs-lookup"><span data-stu-id="0dc1d-113">Time Trigger Example (Scripting)</span></span>](time-trigger-example--scripting-.md)
-   [<span data-ttu-id="0dc1d-114">Ejemplo de desencadenador de tiempo (XML)</span><span class="sxs-lookup"><span data-stu-id="0dc1d-114">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="0dc1d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0dc1d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dc1d-116">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="0dc1d-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




