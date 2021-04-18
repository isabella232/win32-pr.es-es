---
title: RegisteredTask. Run (método)
description: En el caso de scripting, ejecuta la tarea registrada inmediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Ejecutar método Programador de tareas
- Método Run Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, Run (método)
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686127"
---
# <a name="registeredtaskrun-method"></a><span data-ttu-id="99299-106">RegisteredTask. Run (método)</span><span class="sxs-lookup"><span data-stu-id="99299-106">RegisteredTask.Run method</span></span>

<span data-ttu-id="99299-107">En el caso de scripting, ejecuta la tarea registrada inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="99299-107">For scripting, runs the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="99299-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99299-108">Syntax</span></span>


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="99299-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99299-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99299-110">*parámetros* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99299-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99299-111">Los parámetros usados como valores en las acciones de la tarea.</span><span class="sxs-lookup"><span data-stu-id="99299-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="99299-112">Para no especificar ningún valor de parámetro para las acciones de tarea, establezca este parámetro en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="99299-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="99299-113">De lo contrario, se puede especificar un valor de cadena único o una matriz de valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="99299-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="99299-114">Los valores de cadena que especifique se emparejan con los nombres y se almacenan como pares de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="99299-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="99299-115">Si especifica un valor de cadena único, Arg0 será el nombre asignado al valor.</span><span class="sxs-lookup"><span data-stu-id="99299-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="99299-116">El valor se puede usar en la acción de tarea donde se usa la variable $ (Arg0) en las propiedades de acción.</span><span class="sxs-lookup"><span data-stu-id="99299-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="99299-117">Si pasa valores como "0", "100" y "250" como una matriz de valores de cadena, "0" reemplazará las variables $ (Arg0), "100" reemplazará las variables $ (arg1) y "250" reemplazará las variables $ (arg2) utilizadas en las propiedades de la acción.</span><span class="sxs-lookup"><span data-stu-id="99299-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="99299-118">Se puede especificar un máximo de 32 valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="99299-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="99299-119">Para obtener más información y una lista de las propiedades de acción que pueden usar las variables $ (Arg0), $ (arg1),..., $ (Arg32) en sus valores, vea [acciones de tarea](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="99299-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="99299-120">*ppRunningTask* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99299-120">*ppRunningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99299-121">Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="99299-121">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99299-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99299-122">Return value</span></span>

<span data-ttu-id="99299-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="99299-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99299-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99299-124">Remarks</span></span>

<span data-ttu-id="99299-125">La función **RegisteredTask. Run** es equivalente a la función [**RegisteredTask. RunEx**](registeredtask-runex.md) con el parámetro flags igual a 0 y no se ha especificado ningún valor para el parámetro user.</span><span class="sxs-lookup"><span data-stu-id="99299-125">The **RegisteredTask.Run** function is equivalent to the [**RegisteredTask.RunEx**](registeredtask-runex.md) function with the flags parameter equal to 0 and nothing specified for the user parameter.</span></span>

<span data-ttu-id="99299-126">Este método devolverá sin errores, pero la tarea no se ejecutará si la propiedad [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) se establece en false para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="99299-126">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="99299-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99299-127">Requirements</span></span>



| <span data-ttu-id="99299-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99299-128">Requirement</span></span> | <span data-ttu-id="99299-129">Value</span><span class="sxs-lookup"><span data-stu-id="99299-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99299-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99299-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99299-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="99299-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99299-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99299-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99299-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="99299-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99299-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="99299-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="99299-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99299-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99299-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99299-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99299-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99299-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99299-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="99299-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99299-139">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="99299-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="99299-140">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="99299-140">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





