---
title: Programador de tareas tipos enumerados
description: Enumera las enumeraciones usadas por las API de Programador de tareas.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Programador de tareas de Programador de tareas, referencia, tipos enumerados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533615"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="83bce-104">Programador de tareas tipos enumerados</span><span class="sxs-lookup"><span data-stu-id="83bce-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="83bce-105">Describe los tipos enumerados que definen las constantes utilizadas por las API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="83bce-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="83bce-106">Los siguientes tipos enumerados se introducen en Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="83bce-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="83bce-107">Enumeración</span><span class="sxs-lookup"><span data-stu-id="83bce-107">Enumeration</span></span>                                                                  | <span data-ttu-id="83bce-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="83bce-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83bce-109">**\_tipo de acción de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="83bce-110">Define el tipo de acciones que puede realizar una tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="83bce-111">**compatibilidad de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="83bce-112">Define qué versiones de Programador de tareas o el comando AT con el que es compatible la tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="83bce-113">**creación de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="83bce-114">Define cómo el servicio Programador de tareas crea, actualiza o deshabilita la tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="83bce-115">**\_marcas de enumeración de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="83bce-116">Define cómo el Programador de tareas enumera a través de las tareas registradas.</span><span class="sxs-lookup"><span data-stu-id="83bce-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="83bce-117">**\_Directiva de instancias de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="83bce-118">Define cómo el Programador de tareas controla las instancias existentes de la tarea cuando inicia una nueva instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="83bce-119">**TIPO de inicio de sesión de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="83bce-120">Define la técnica de inicio de sesión necesaria para ejecutar una tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="83bce-121">**TIPO de PROCESSTOKENSID de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="83bce-122">Define los tipos de SID de proceso que pueden usar las tareas.</span><span class="sxs-lookup"><span data-stu-id="83bce-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="83bce-123">**\_marcas de ejecución de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="83bce-124">Define cómo se ejecuta una tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="83bce-125">**\_tipo de nivel de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="83bce-126">Define las marcas de elevación de LUA que especifican con qué nivel de privilegios se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="83bce-127">**\_tipo de \_ cambio de estado de sesión de tarea \_ \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="83bce-128">Define qué tipos de Terminal Server cambio de estado de sesión puede usar para desencadenar la inicio de una tarea.</span><span class="sxs-lookup"><span data-stu-id="83bce-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="83bce-129">**Estado de la tarea \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="83bce-130">Define los diferentes Estados en los que puede estar una tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="83bce-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="83bce-131">**\_Tipo2 de desencadenador de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="83bce-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="83bce-132">Define el tipo de desencadenadores que las tareas pueden usar.</span><span class="sxs-lookup"><span data-stu-id="83bce-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="83bce-133">Las enumeraciones de Programador de tareas 1,0 solo están disponibles en los sistemas operativos Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="83bce-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="83bce-134">Están en desuso en Windows Vista y pueden quitarse completamente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="83bce-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="83bce-135">En su lugar, use las enumeraciones Programador de tareas 2,0 enumeradas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="83bce-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="83bce-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83bce-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83bce-137">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="83bce-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="83bce-138">Referencia de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="83bce-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




