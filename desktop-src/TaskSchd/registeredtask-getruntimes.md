---
title: RegisteredTask. GetRunTimes, método
description: En el caso de scripting, obtiene las veces que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Método GetRunTimes Programador de tareas
- Método GetRunTimes Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método GetRunTimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534888"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="d7027-106">RegisteredTask. GetRunTimes, método</span><span class="sxs-lookup"><span data-stu-id="d7027-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="d7027-107">En el caso de scripting, obtiene las veces que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d7027-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7027-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7027-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="d7027-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7027-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7027-110">*Inicio* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d7027-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7027-111">La hora de inicio de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d7027-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="d7027-112">*fin* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d7027-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7027-113">La hora de finalización de la consulta.</span><span class="sxs-lookup"><span data-stu-id="d7027-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="d7027-114">*recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7027-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7027-115">El número de horas programadas que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="d7027-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="d7027-116">*rgstTaskTimes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7027-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7027-117">Las horas programadas en las que se ejecutará la tarea.</span><span class="sxs-lookup"><span data-stu-id="d7027-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7027-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7027-118">Return value</span></span>

<span data-ttu-id="d7027-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7027-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7027-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7027-120">Remarks</span></span>

<span data-ttu-id="d7027-121">Si la tarea registrada contiene desencadenadores que se deshabilitan de forma individual, estos desencadenadores todavía afectarán a la siguiente hora de ejecución programada que se devuelva aunque estén deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="d7027-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7027-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7027-122">Requirements</span></span>



| <span data-ttu-id="d7027-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7027-123">Requirement</span></span> | <span data-ttu-id="d7027-124">Value</span><span class="sxs-lookup"><span data-stu-id="d7027-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7027-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7027-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7027-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7027-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d7027-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7027-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7027-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7027-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7027-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d7027-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7027-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7027-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7027-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7027-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7027-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7027-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7027-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7027-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7027-134">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="d7027-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d7027-135">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="d7027-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





