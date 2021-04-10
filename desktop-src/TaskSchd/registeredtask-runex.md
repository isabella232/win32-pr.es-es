---
title: RegisteredTask. RunEx, método
description: En el caso de scripting, ejecuta la tarea registrada de inmediato usando las marcas especificadas y un identificador de sesión.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Método RunEx Programador de tareas
- Método RunEx Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150613"
---
# <a name="registeredtaskrunex-method"></a><span data-ttu-id="67611-106">RegisteredTask. RunEx, método</span><span class="sxs-lookup"><span data-stu-id="67611-106">RegisteredTask.RunEx method</span></span>

<span data-ttu-id="67611-107">En el caso de scripting, ejecuta la tarea registrada de inmediato usando las marcas especificadas y un identificador de sesión.</span><span class="sxs-lookup"><span data-stu-id="67611-107">For scripting, runs the registered task immediately using specified flags and a session identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="67611-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67611-108">Syntax</span></span>


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a><span data-ttu-id="67611-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67611-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67611-110">*parámetros* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67611-110">*params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67611-111">Los parámetros usados como valores en las acciones de la tarea.</span><span class="sxs-lookup"><span data-stu-id="67611-111">The parameters used as values in the task actions.</span></span> <span data-ttu-id="67611-112">Para no especificar ningún valor de parámetro para las acciones de tarea, establezca este parámetro en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="67611-112">To not specify any parameter values for the task actions, set this parameter to **Nothing**.</span></span> <span data-ttu-id="67611-113">De lo contrario, se puede especificar un valor de cadena único o una matriz de valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="67611-113">Otherwise, a single string value or an array of string values can be specified.</span></span>

<span data-ttu-id="67611-114">Los valores de cadena que especifique se emparejan con los nombres y se almacenan como pares de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="67611-114">The string values that you specify are paired with names and stored as name-value pairs.</span></span> <span data-ttu-id="67611-115">Si especifica un valor de cadena único, Arg0 será el nombre asignado al valor.</span><span class="sxs-lookup"><span data-stu-id="67611-115">If you specify a single string value, then Arg0 will be the name assigned to the value.</span></span> <span data-ttu-id="67611-116">El valor se puede usar en la acción de tarea donde se usa la variable $ (Arg0) en las propiedades de acción.</span><span class="sxs-lookup"><span data-stu-id="67611-116">The value can be used in the task action where the $(Arg0) variable is used in the action properties.</span></span>

<span data-ttu-id="67611-117">Si pasa valores como "0", "100" y "250" como una matriz de valores de cadena, "0" reemplazará las variables $ (Arg0), "100" reemplazará las variables $ (arg1) y "250" reemplazará las variables $ (arg2) utilizadas en las propiedades de la acción.</span><span class="sxs-lookup"><span data-stu-id="67611-117">If you pass in values such as "0", "100", and "250" as an array of string values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables used in the action properties.</span></span>

<span data-ttu-id="67611-118">Se puede especificar un máximo de 32 valores de cadena.</span><span class="sxs-lookup"><span data-stu-id="67611-118">A maximum of 32 string values can be specified.</span></span>

<span data-ttu-id="67611-119">Para obtener más información y una lista de las propiedades de acción que pueden usar las variables $ (Arg0), $ (arg1),..., $ (Arg32) en sus valores, vea [acciones de tarea](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="67611-119">For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see [Task Actions](task-actions.md).</span></span>

</dd> <dt>

<span data-ttu-id="67611-120">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="67611-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67611-121">Una constante de [ \_ \_ marcadores de ejecución de tareas](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define cómo se ejecuta la tarea.</span><span class="sxs-lookup"><span data-stu-id="67611-121">A [TASK\_RUN\_FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) constant that defines how the task is run.</span></span>

</dd> <dt>

<span data-ttu-id="67611-122">*SessionID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67611-122">*sessionID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67611-123">La sesión de Terminal Server en la que desea iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="67611-123">The terminal server session in which you want to launch the task.</span></span>

<span data-ttu-id="67611-124">Si la ejecución de la tarea \_ \_ usar la \_ \_ constante de ID. de sesión (0x4) no se pasa al parámetro *Flags* , se omite el valor especificado en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="67611-124">If the TASK\_RUN\_USE\_SESSION\_ID constant (0x4) is not passed into the *flags* parameter, then the value specified in this parameter is ignored.</span></span> <span data-ttu-id="67611-125">Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor de SessionID es menor o igual que 0, se devolverá un error de argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="67611-125">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.</span></span>

<span data-ttu-id="67611-126">Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor de SessionID es un identificador de sesión válido mayor que 0 y no se especifica ningún valor para el parámetro *User* , el servicio Programador de tareas intentará iniciar la tarea interactivamente como el usuario que ha iniciado sesión en la sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="67611-126">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is logged on to the specified session.</span></span>

<span data-ttu-id="67611-127">Si la ejecución de la tarea \_ \_ usar el \_ ID. de sesión \_ se pasa al parámetro *Flags* y el valor SessionID es un identificador de sesión válido mayor que 0 y se especifica un usuario en el parámetro *User* , el servicio Programador de tareas intentará iniciar la tarea interactivamente como el usuario especificado en el parámetro *User* .</span><span class="sxs-lookup"><span data-stu-id="67611-127">If the TASK\_RUN\_USE\_SESSION\_ID constant is passed into the *flags* parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the *user* parameter, then the Task Scheduler service will try to launch the task interactively as the user who is specified in the *user* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="67611-128">*runningTask* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67611-128">*runningTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67611-129">Objeto [**RunningTask**](runningtask.md) que define la nueva instancia de la tarea.</span><span class="sxs-lookup"><span data-stu-id="67611-129">A [**RunningTask**](runningtask.md) object that defines the new instance of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67611-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67611-130">Return value</span></span>

<span data-ttu-id="67611-131">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="67611-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67611-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67611-132">Remarks</span></span>

<span data-ttu-id="67611-133">Este método devolverá sin errores, pero la tarea no se ejecutará si la propiedad [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) se establece en false para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="67611-133">This method will return without error, but the task will not run if the [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) property is set to false for the registered task.</span></span>

## <a name="requirements"></a><span data-ttu-id="67611-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67611-134">Requirements</span></span>



| <span data-ttu-id="67611-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="67611-135">Requirement</span></span> | <span data-ttu-id="67611-136">Value</span><span class="sxs-lookup"><span data-stu-id="67611-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67611-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67611-137">Minimum supported client</span></span><br/> | <span data-ttu-id="67611-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67611-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67611-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67611-139">Minimum supported server</span></span><br/> | <span data-ttu-id="67611-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67611-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67611-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="67611-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="67611-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67611-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67611-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67611-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67611-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67611-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67611-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="67611-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67611-146">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="67611-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="67611-147">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="67611-147">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





