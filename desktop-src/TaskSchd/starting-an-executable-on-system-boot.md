---
title: Iniciar un archivo ejecutable en el arranque del sistema
description: La escritura de una tarea que inicia un ejecutable cuando se arranca un sistema se realiza mediante la definición de un desencadenador de arranque y una acción ejecutable.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Programador de tareas ejemplos Programador de tareas, desencadenador de arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778114"
---
# <a name="starting-an-executable-on-system-boot"></a><span data-ttu-id="4c3ae-104">Iniciar un archivo ejecutable en el arranque del sistema</span><span class="sxs-lookup"><span data-stu-id="4c3ae-104">Starting an Executable on System Boot</span></span>

<span data-ttu-id="4c3ae-105">La escritura de una tarea que inicia un ejecutable cuando se arranca un sistema se realiza mediante la definición de un desencadenador de arranque y una acción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="4c3ae-105">Writing a task that starts an executable when a system is booted is done by defining a boot trigger and an executable action.</span></span>

## <a name="boot-trigger"></a><span data-ttu-id="4c3ae-106">Desencadenador de arranque</span><span class="sxs-lookup"><span data-stu-id="4c3ae-106">Boot Trigger</span></span>

<span data-ttu-id="4c3ae-107">Los desencadenadores de arranque se activan por su límite de inicio, pero no inician el ejecutable hasta que se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="4c3ae-107">Boot triggers are activated by their start boundary but they do not start the executable until the system is booted.</span></span> <span data-ttu-id="4c3ae-108">También puede especificar un tiempo de retraso en el desencadenador de arranque que especifica la cantidad de tiempo que transcurre entre el momento en que se arranca el sistema y el momento en que se inicia la tarea.</span><span class="sxs-lookup"><span data-stu-id="4c3ae-108">You can also specify a delay time in the boot trigger that specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="4c3ae-109">Se define mediante la propiedad [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) en la interfaz [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (objeto [**BootTrigger**](boottrigger.md) para scripting).</span><span class="sxs-lookup"><span data-stu-id="4c3ae-109">This is defined by the [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property in the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) interface ([**BootTrigger**](boottrigger.md) object for scripting).</span></span>

## <a name="boot-trigger-examples"></a><span data-ttu-id="4c3ae-110">Ejemplos de desencadenadores de arranque</span><span class="sxs-lookup"><span data-stu-id="4c3ae-110">Boot Trigger Examples</span></span>

<span data-ttu-id="4c3ae-111">En los siguientes ejemplos se inicia el Bloc de notas después de arrancar el sistema:</span><span class="sxs-lookup"><span data-stu-id="4c3ae-111">The following examples start Notepad after the system is booted:</span></span>

-   [<span data-ttu-id="4c3ae-112">Ejemplo de desencadenador de arranque (scripting)</span><span class="sxs-lookup"><span data-stu-id="4c3ae-112">Boot Trigger Example (Scripting)</span></span>](boot-trigger-example--scripting-.md)
-   [<span data-ttu-id="4c3ae-113">Ejemplo de desencadenador de arranque (C++)</span><span class="sxs-lookup"><span data-stu-id="4c3ae-113">Boot Trigger Example (C++)</span></span>](boot-trigger-example--c---.md)
-   [<span data-ttu-id="4c3ae-114">Ejemplo de desencadenador de arranque (XML)</span><span class="sxs-lookup"><span data-stu-id="4c3ae-114">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

## <a name="related-topics"></a><span data-ttu-id="4c3ae-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c3ae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c3ae-116">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="4c3ae-116">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




