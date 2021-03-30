---
title: TaskSettings. Compatibility (propiedad)
description: Para scripting, obtiene o establece un valor entero que indica la versión de Programador de tareas que una tarea es compatible con.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Programador de tareas de propiedades de compatibilidad
- Propiedad Compatibility Programador de tareas, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad Compatibility
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801760"
---
# <a name="tasksettingscompatibility-property"></a><span data-ttu-id="598db-106">TaskSettings. Compatibility (propiedad)</span><span class="sxs-lookup"><span data-stu-id="598db-106">TaskSettings.Compatibility property</span></span>

<span data-ttu-id="598db-107">Para scripting, obtiene o establece un valor entero que indica la versión de Programador de tareas que una tarea es compatible con.</span><span class="sxs-lookup"><span data-stu-id="598db-107">For scripting, gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.</span></span>

<span data-ttu-id="598db-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="598db-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="598db-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="598db-109">Syntax</span></span>


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a><span data-ttu-id="598db-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="598db-110">Property value</span></span>



| <span data-ttu-id="598db-111">Value</span><span class="sxs-lookup"><span data-stu-id="598db-111">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="598db-112">Significado</span><span class="sxs-lookup"><span data-stu-id="598db-112">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <span data-ttu-id="598db-113"><dt>**Tarea \_ de COMPATIBILIDAD \_ en**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="598db-113"><dt>**TASK\_COMPATIBILITY\_AT**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="598db-114">La tarea es compatible con el comando AT.</span><span class="sxs-lookup"><span data-stu-id="598db-114">The task is compatible with the AT command.</span></span><br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <span data-ttu-id="598db-115"><dt>**Tarea \_ de COMPATIBILIDAD \_ v1**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="598db-115"><dt>**TASK\_COMPATIBILITY\_V1**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="598db-116">La tarea es compatible con Programador de tareas 1,0.</span><span class="sxs-lookup"><span data-stu-id="598db-116">The task is compatible with Task Scheduler 1.0.</span></span><br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <span data-ttu-id="598db-117"><dt>**Tarea \_ de COMPATIBILIDAD \_ V2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="598db-117"><dt>**TASK\_COMPATIBILITY\_V2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="598db-118">La tarea es compatible con Programador de tareas 2,0.</span><span class="sxs-lookup"><span data-stu-id="598db-118">The task is compatible with Task Scheduler 2.0.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="598db-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="598db-119">Remarks</span></span>

<span data-ttu-id="598db-120">La compatibilidad de tareas, que se establece a través de la propiedad de [**compatibilidad**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , solo se debe establecer en compatibilidad de tareas \_ \_ v1 si es necesario tener acceso a una tarea o modificarla desde un equipo con Windows XP, Windows Server 2003 o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="598db-120">Task compatibility, which is set through the [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) property, should only be set to TASK\_COMPATIBILITY\_V1 if a task needs to be accessed or modified from a Windows XP, Windows Server 2003, or Windows 2000 computer.</span></span> <span data-ttu-id="598db-121">De lo contrario, se recomienda usar la compatibilidad con Programador de tareas 2,0 porque la tarea tendrá más características.</span><span class="sxs-lookup"><span data-stu-id="598db-121">Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.</span></span>

<span data-ttu-id="598db-122">Las tareas compatibles con el comando AT solo pueden tener un desencadenador de una vez.</span><span class="sxs-lookup"><span data-stu-id="598db-122">Tasks compatible with the AT command can only have one time trigger.</span></span>

<span data-ttu-id="598db-123">Las tareas compatibles con Programador de tareas 1,0 solo pueden tener un desencadenador de tiempo, un desencadenador de inicio de sesión o un desencadenador de arranque y la tarea solo puede tener una acción ejecutable.</span><span class="sxs-lookup"><span data-stu-id="598db-123">Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.</span></span>

<span data-ttu-id="598db-124">Para obtener más información sobre la compatibilidad de tareas, vea [novedades de programador de tareas](what-s-new-in-task-scheduler.md) y [tareas](tasks.md).</span><span class="sxs-lookup"><span data-stu-id="598db-124">For more information about task compatibility, see [What's New in Task Scheduler](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="598db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598db-125">Requirements</span></span>



| <span data-ttu-id="598db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="598db-126">Requirement</span></span> | <span data-ttu-id="598db-127">Value</span><span class="sxs-lookup"><span data-stu-id="598db-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="598db-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="598db-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="598db-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="598db-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="598db-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="598db-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="598db-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="598db-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="598db-133"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="598db-133"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="598db-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="598db-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598db-135"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="598db-135"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598db-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="598db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598db-137">**compatibilidad de tareas \_**</span><span class="sxs-lookup"><span data-stu-id="598db-137">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[<span data-ttu-id="598db-138">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="598db-138">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





