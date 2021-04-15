---
title: TaskSettings.Exepropiedad cutionTimeLimit
description: En el caso de scripting, obtiene o establece la cantidad de tiempo que se permite completar la tarea.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Programador de tareas de la propiedad ExecutionTimeLimit
- Programador de tareas de la propiedad ExecutionTimeLimit, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686122"
---
# <a name="tasksettingsexecutiontimelimit-property"></a><span data-ttu-id="6be3d-106">TaskSettings.Exepropiedad cutionTimeLimit</span><span class="sxs-lookup"><span data-stu-id="6be3d-106">TaskSettings.ExecutionTimeLimit property</span></span>

<span data-ttu-id="6be3d-107">En el caso de scripting, obtiene o establece la cantidad de tiempo que se permite completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6be3d-107">For scripting, gets or sets the amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="6be3d-108">De forma predeterminada, se detendrá una tarea 72 horas después de que empiece a ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="6be3d-108">By default, a task will be stopped 72 hours after it starts to run.</span></span> <span data-ttu-id="6be3d-109">Puede cambiar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="6be3d-109">You can change this by changing this setting.</span></span>

<span data-ttu-id="6be3d-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6be3d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be3d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6be3d-111">Syntax</span></span>


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a><span data-ttu-id="6be3d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6be3d-112">Property value</span></span>

<span data-ttu-id="6be3d-113">Cantidad de tiempo que se permite completar la tarea.</span><span class="sxs-lookup"><span data-stu-id="6be3d-113">The amount of time that is allowed to complete the task.</span></span> <span data-ttu-id="6be3d-114">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="6be3d-114">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="6be3d-115">Un valor de PT0S permitirá que la tarea se ejecute indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="6be3d-115">A value of PT0S will enable the task to run indefinitely.</span></span> <span data-ttu-id="6be3d-116">Cuando este parámetro se establece en Nothing, el límite de tiempo de ejecución es infinito.</span><span class="sxs-lookup"><span data-stu-id="6be3d-116">When this parameter is set to Nothing, the execution time limit is infinite.</span></span>

## <a name="remarks"></a><span data-ttu-id="6be3d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6be3d-117">Remarks</span></span>

<span data-ttu-id="6be3d-118">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="6be3d-118">When reading or writing XML for a task, this setting is specified in the [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be3d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be3d-119">Requirements</span></span>



| <span data-ttu-id="6be3d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be3d-120">Requirement</span></span> | <span data-ttu-id="6be3d-121">Value</span><span class="sxs-lookup"><span data-stu-id="6be3d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6be3d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be3d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6be3d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6be3d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6be3d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be3d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6be3d-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6be3d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6be3d-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6be3d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6be3d-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6be3d-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6be3d-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6be3d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6be3d-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6be3d-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6be3d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6be3d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be3d-131">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6be3d-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





