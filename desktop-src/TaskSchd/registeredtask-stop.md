---
title: RegisteredTask. STOP (método)
description: En el caso de scripting, detiene la tarea registrada inmediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Detener método Programador de tareas
- Método STOP Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método STOP
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422577"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="9964c-106">RegisteredTask. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="9964c-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="9964c-107">En el caso de scripting, detiene la tarea registrada inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9964c-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="9964c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9964c-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="9964c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9964c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9964c-110">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9964c-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9964c-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9964c-111">Reserved.</span></span> <span data-ttu-id="9964c-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9964c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9964c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9964c-113">Return value</span></span>

<span data-ttu-id="9964c-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9964c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9964c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9964c-115">Remarks</span></span>

<span data-ttu-id="9964c-116">La función **RegisteredTask. Stop** detiene todas las instancias de la tarea.</span><span class="sxs-lookup"><span data-stu-id="9964c-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="9964c-117">Los usuarios de la cuenta del sistema pueden detener una tarea, los usuarios con privilegios de grupo de administradores pueden detener una tarea y, si un usuario tiene derechos para ejecutar y leer una tarea, el usuario puede detener la tarea.</span><span class="sxs-lookup"><span data-stu-id="9964c-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="9964c-118">Un usuario puede detener las instancias de tarea que se ejecutan con las mismas credenciales que la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="9964c-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="9964c-119">En todos los demás casos, se deniega el acceso al usuario para detener la tarea.</span><span class="sxs-lookup"><span data-stu-id="9964c-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="9964c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9964c-120">Requirements</span></span>



| <span data-ttu-id="9964c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9964c-121">Requirement</span></span> | <span data-ttu-id="9964c-122">Value</span><span class="sxs-lookup"><span data-stu-id="9964c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9964c-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9964c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9964c-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9964c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9964c-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9964c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9964c-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9964c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9964c-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9964c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="9964c-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9964c-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9964c-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9964c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9964c-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9964c-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9964c-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9964c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9964c-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="9964c-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





