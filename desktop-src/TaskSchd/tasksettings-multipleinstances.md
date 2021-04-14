---
title: Propiedad TaskSettings. MultipleInstances
description: En el caso de scripting, obtiene o establece la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Programador de tareas de la propiedad MultipleInstances
- Programador de tareas de la propiedad MultipleInstances, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533855"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="6125d-106">Propiedad TaskSettings. MultipleInstances</span><span class="sxs-lookup"><span data-stu-id="6125d-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="6125d-107">En el caso de scripting, obtiene o establece la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6125d-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="6125d-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6125d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6125d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6125d-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="6125d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6125d-110">Property value</span></span>

<span data-ttu-id="6125d-111">[**Tarea \_ de Constantes \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) de la Directiva de instancias.</span><span class="sxs-lookup"><span data-stu-id="6125d-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="6125d-112">Value</span><span class="sxs-lookup"><span data-stu-id="6125d-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="6125d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="6125d-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="6125d-114"><dt>**Tarea \_ de INSTANCIAS en \_ paralelo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6125d-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="6125d-115">Inicia una nueva instancia de mientras se ejecuta una instancia existente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6125d-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="6125d-116"><dt>**Tarea \_ de \_Cola de instancias**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6125d-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="6125d-117">Inicia una nueva instancia de la tarea después de que todas las demás instancias de la tarea se hayan completado.</span><span class="sxs-lookup"><span data-stu-id="6125d-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="6125d-118"><dt>**Tarea \_ de INSTANCIAS \_ omitir \_ nuevo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6125d-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="6125d-119">No inicia una nueva instancia de si se está ejecutando una instancia existente de la tarea.</span><span class="sxs-lookup"><span data-stu-id="6125d-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="6125d-120"><dt>**Tarea \_ de LAS instancias se \_ detienen 3 \_ existentes**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6125d-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="6125d-121">Detiene una instancia existente de la tarea antes de iniciar una nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="6125d-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="6125d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6125d-122">Remarks</span></span>

<span data-ttu-id="6125d-123">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="6125d-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6125d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6125d-124">Requirements</span></span>



| <span data-ttu-id="6125d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6125d-125">Requirement</span></span> | <span data-ttu-id="6125d-126">Value</span><span class="sxs-lookup"><span data-stu-id="6125d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6125d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6125d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6125d-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6125d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6125d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6125d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6125d-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6125d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6125d-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6125d-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="6125d-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6125d-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6125d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6125d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6125d-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6125d-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6125d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6125d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6125d-136">**\_Directiva de instancias de tarea \_**</span><span class="sxs-lookup"><span data-stu-id="6125d-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="6125d-137">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6125d-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





