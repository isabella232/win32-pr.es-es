---
title: Acerca del Programador de tareas
description: El servicio Programador de tareas le permite realizar tareas automatizadas en un equipo seleccionado.
ms.assetid: 13816b8b-3090-4d17-86bb-8e632ca0cd37
keywords:
- Programador de tareas Programador de tareas, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6022546550efe32504dd0a3d12c94163e78214f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685574"
---
# <a name="about-the-task-scheduler"></a><span data-ttu-id="a94d4-104">Acerca del Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-104">About the Task Scheduler</span></span>

<span data-ttu-id="a94d4-105">El servicio Programador de tareas le permite realizar tareas automatizadas en un equipo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="a94d4-105">The Task Scheduler service allows you to perform automated tasks on a chosen computer.</span></span> <span data-ttu-id="a94d4-106">Con este servicio, puede programar cualquier programa para que se ejecute en un momento adecuado o cuando se produzca un evento específico.</span><span class="sxs-lookup"><span data-stu-id="a94d4-106">With this service, you can schedule any program to run at a convenient time for you or when a specific event occurs.</span></span> <span data-ttu-id="a94d4-107">El Programador de tareas supervisa el tiempo o los criterios de evento que elija y, a continuación, ejecuta la tarea cuando se cumplen esos criterios.</span><span class="sxs-lookup"><span data-stu-id="a94d4-107">The Task Scheduler monitors the time or event criteria that you choose and then executes the task when those criteria are met.</span></span>

## <a name="where-task-scheduler-is-installed"></a><span data-ttu-id="a94d4-108">Dónde está instalado Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-108">Where Task Scheduler is Installed</span></span>

<span data-ttu-id="a94d4-109">El Programador de tareas se instala automáticamente con varios sistemas operativos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a94d4-109">The Task Scheduler is automatically installed with several Microsoft operating systems.</span></span>

<span data-ttu-id="a94d4-110">Programador de tareas 1,0 se instala con los sistemas operativos Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a94d4-110">Task Scheduler 1.0 is installed with the Windows Server 2003, Windows XP, and Windows 2000 operating systems.</span></span>

<span data-ttu-id="a94d4-111">Programador de tareas 2,0 se instala con Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a94d4-111">Task Scheduler 2.0 is installed with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="a94d4-112">La API Programador de tareas 2,0 se debe usar en el desarrollo de aplicaciones que usan el servicio Programador de tareas en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a94d4-112">The Task Scheduler 2.0 API should be used in developing applications that use the Task Scheduler service on Windows Vista.</span></span> <span data-ttu-id="a94d4-113">Para obtener más información, vea [referencia de programador de tareas](task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a94d4-113">For more information, see [Task Scheduler Reference](task-scheduler-reference.md).</span></span>

<span data-ttu-id="a94d4-114">Programador de tareas se inicia cada vez que se inicia el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a94d4-114">Task Scheduler is started each time the operating system is started.</span></span> <span data-ttu-id="a94d4-115">Puede ejecutarse a través de la interfaz gráfica de usuario (GUI) de Programador de tareas o a través de la API de Programador de tareas descrita en este SDK.</span><span class="sxs-lookup"><span data-stu-id="a94d4-115">It can be run either through the Task Scheduler graphical user interface (GUI) or through the Task Scheduler API described in this SDK.</span></span>

## <a name="information-about-tasks"></a><span data-ttu-id="a94d4-116">Información acerca de las tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-116">Information about Tasks</span></span>

<span data-ttu-id="a94d4-117">Las tareas son el componente principal de la Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a94d4-117">Tasks are the main component of the Task Scheduler.</span></span> <span data-ttu-id="a94d4-118">Para obtener información sobre qué son las tareas y cuáles son sus componentes, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a94d4-118">For information on what tasks are and what their components are, see the following topics:</span></span>

-   [<span data-ttu-id="a94d4-119">Tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-119">Tasks</span></span>](tasks.md)
-   [<span data-ttu-id="a94d4-120">Acciones de tarea</span><span class="sxs-lookup"><span data-stu-id="a94d4-120">Task Actions</span></span>](task-actions.md)
-   [<span data-ttu-id="a94d4-121">Desencadenadores de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-121">Task Triggers</span></span>](task-triggers.md)
-   [<span data-ttu-id="a94d4-122">Información de registro de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-122">Task Registration Information</span></span>](task-registration-information.md)
-   [<span data-ttu-id="a94d4-123">Condiciones de inactividad de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-123">Task Idle Conditions</span></span>](task-idle-conditions.md)
-   [<span data-ttu-id="a94d4-124">Contextos de seguridad para tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-124">Security Contexts for Tasks</span></span>](security-contexts-for-running-tasks.md)
-   [<span data-ttu-id="a94d4-125">Repetir una tarea</span><span class="sxs-lookup"><span data-stu-id="a94d4-125">Repeating A Task</span></span>](repeating-a-task.md)
-   [<span data-ttu-id="a94d4-126">Mantenimiento automático</span><span class="sxs-lookup"><span data-stu-id="a94d4-126">Automatic Maintenance</span></span>](task-maintenence.md)

<span data-ttu-id="a94d4-127">Para obtener más información y ejemplos sobre cómo usar las interfaces de Programador de tareas, los objetos de scripting y XML, vea [usar el programador de tareas](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="a94d4-127">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a94d4-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a94d4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94d4-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a94d4-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




