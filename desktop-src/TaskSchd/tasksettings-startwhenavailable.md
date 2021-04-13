---
title: Propiedad TaskSettings. StartWhenAvailable
description: En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Programador de tareas de la propiedad StartWhenAvailable
- Programador de tareas de la propiedad StartWhenAvailable, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492256"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="ecbf2-106">Propiedad TaskSettings. StartWhenAvailable</span><span class="sxs-lookup"><span data-stu-id="ecbf2-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="ecbf2-107">En el caso de scripting, obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="ecbf2-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbf2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecbf2-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ecbf2-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ecbf2-110">Property value</span></span>

<span data-ttu-id="ecbf2-111">Si es true, la propiedad indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="ecbf2-112">El valor predeterminado es False.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbf2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecbf2-113">Remarks</span></span>

<span data-ttu-id="ecbf2-114">Esta propiedad solo se aplica a las tareas basadas en tiempo con un límite final o tareas basadas en el tiempo que se establecen para repetirse infinitamente.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="ecbf2-115">Las tareas que se inician después de que transcurra la hora programada (debido a que la propiedad [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) se establece en true) se ponen en cola en la cola del servicio Programador de tareas de las tareas y se inician después de un retraso.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="ecbf2-116">El retraso predeterminado es de 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="ecbf2-117">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="ecbf2-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbf2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecbf2-118">Requirements</span></span>



| <span data-ttu-id="ecbf2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecbf2-119">Requirement</span></span> | <span data-ttu-id="ecbf2-120">Value</span><span class="sxs-lookup"><span data-stu-id="ecbf2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbf2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecbf2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbf2-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecbf2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ecbf2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecbf2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbf2-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecbf2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecbf2-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ecbf2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ecbf2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ecbf2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ecbf2-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecbf2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecbf2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecbf2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbf2-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecbf2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbf2-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ecbf2-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





