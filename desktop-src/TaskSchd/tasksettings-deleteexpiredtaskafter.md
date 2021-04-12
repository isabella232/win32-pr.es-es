---
title: Propiedad TaskSettings. DeleteExpiredTaskAfter
description: En el caso de scripting, obtiene o establece la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Programador de tareas de la propiedad DeleteExpiredTaskAfter
- Programador de tareas de la propiedad DeleteExpiredTaskAfter, objeto TaskSettings
- Programador de tareas de objeto TaskSettings, propiedad DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489850"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="99346-106">Propiedad TaskSettings. DeleteExpiredTaskAfter</span><span class="sxs-lookup"><span data-stu-id="99346-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="99346-107">En el caso de scripting, obtiene o establece la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.</span><span class="sxs-lookup"><span data-stu-id="99346-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="99346-108">Si no se especifica ningún valor para esta propiedad, el servicio Programador de tareas no eliminará la tarea.</span><span class="sxs-lookup"><span data-stu-id="99346-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="99346-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="99346-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99346-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99346-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="99346-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="99346-111">Property value</span></span>

<span data-ttu-id="99346-112">Una cadena que obtiene o establece la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.</span><span class="sxs-lookup"><span data-stu-id="99346-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="99346-113">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="99346-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="99346-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99346-114">Remarks</span></span>

<span data-ttu-id="99346-115">Una tarea expira una vez que se ha superado el límite final para todos los desencadenadores asociados a la tarea.</span><span class="sxs-lookup"><span data-stu-id="99346-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="99346-116">El límite final de un desencadenador se especifica mediante la propiedad [EndBoundary](trigger-endboundary.md) heredada por todos los objetos de desencadenador.</span><span class="sxs-lookup"><span data-stu-id="99346-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="99346-117">Al leer o escribir XML para una tarea, esta configuración se especifica en el elemento [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="99346-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="99346-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99346-118">Requirements</span></span>



| <span data-ttu-id="99346-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="99346-119">Requirement</span></span> | <span data-ttu-id="99346-120">Value</span><span class="sxs-lookup"><span data-stu-id="99346-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99346-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99346-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99346-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="99346-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99346-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99346-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99346-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="99346-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99346-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="99346-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="99346-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99346-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99346-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99346-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99346-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99346-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99346-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="99346-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99346-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="99346-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





