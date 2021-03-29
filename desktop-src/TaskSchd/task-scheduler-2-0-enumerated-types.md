---
title: Tipos enumerados de Programador de tareas 2,0
description: Describe los tipos enumerados que definen las constantes utilizadas por las API de Programador de tareas 2,0.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359546"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="fb25e-103">Tipos enumerados de Programador de tareas 2,0</span><span class="sxs-lookup"><span data-stu-id="fb25e-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="fb25e-104">Describe los tipos enumerados que definen las constantes utilizadas por las API de Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="fb25e-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="fb25e-105">Los siguientes tipos enumerados se introducen en Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="fb25e-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="fb25e-106">Enumeración</span><span class="sxs-lookup"><span data-stu-id="fb25e-106">Enumeration</span></span>                                                                  | <span data-ttu-id="fb25e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb25e-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb25e-108">**\_tipo de acción de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="fb25e-109">Define el tipo de acciones que puede realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="fb25e-110">**compatibilidad de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="fb25e-111">Define qué versiones de Programador de tareas o el comando AT con el que es compatible la tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="fb25e-112">**creación de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="fb25e-113">Define cómo el servicio Programador de tareas crea, actualiza o deshabilita la tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="fb25e-114">**\_marcas de enumeración de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="fb25e-115">Define cómo el Programador de tareas enumera a través de las tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="fb25e-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="fb25e-116">**\_Directiva de instancias de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="fb25e-117">Define cómo el Programador de tareas controla las instancias existentes de la tarea cuando inicia una nueva instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="fb25e-118">**TIPO de inicio de sesión de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="fb25e-119">Define la técnica de inicio de sesión necesaria para ejecutar una tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="fb25e-120">**\_tipo de PROCESSTOKENSID de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="fb25e-121">Define los tipos de SID de proceso que pueden usar las tareas.</span><span class="sxs-lookup"><span data-stu-id="fb25e-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="fb25e-122">**\_marcas de ejecución de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="fb25e-123">Define cómo se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="fb25e-124">**\_tipo de nivel de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="fb25e-125">Define las marcas de elevación de LUA que especifican con qué nivel de privilegios se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="fb25e-126">**\_tipo de \_ cambio de estado de sesión de tarea \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="fb25e-127">Define qué tipos de Terminal Server cambio de estado de sesión puede usar para desencadenar la inicio de una tarea.</span><span class="sxs-lookup"><span data-stu-id="fb25e-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="fb25e-128">**Estado de la tarea \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="fb25e-129">Define los diferentes Estados en los que puede estar una tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="fb25e-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="fb25e-130">**\_Tipo2 de desencadenador de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="fb25e-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="fb25e-131">Define el tipo de desencadenadores que las tareas pueden usar.</span><span class="sxs-lookup"><span data-stu-id="fb25e-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="fb25e-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb25e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb25e-133">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="fb25e-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fb25e-134">Referencia de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="fb25e-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




