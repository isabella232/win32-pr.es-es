---
title: RegisteredTask. SetSecurityDescriptor, método
description: En el caso de scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Método SetSecurityDescriptor Programador de tareas
- Método SetSecurityDescriptor Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, método SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150954"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="2da05-106">RegisteredTask. SetSecurityDescriptor, método</span><span class="sxs-lookup"><span data-stu-id="2da05-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="2da05-107">En el caso de scripting, establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="2da05-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da05-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2da05-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2da05-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2da05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da05-110">*SDDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2da05-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da05-111">Descriptor de seguridad que se usa como credenciales para la tarea registrada.</span><span class="sxs-lookup"><span data-stu-id="2da05-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="2da05-112">Si se deniega el acceso a la cuenta de sistema local a una tarea, el servicio de Programador de tareas puede generar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="2da05-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="2da05-113">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2da05-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da05-114">Marcas que especifican cómo establecer el descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2da05-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="2da05-115">\_ \_ Se puede especificar la tarea no agregar \_ \_ marca de ACE principal (0x10) de la enumeración de [**\_ creación de tareas**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .</span><span class="sxs-lookup"><span data-stu-id="2da05-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da05-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2da05-116">Return value</span></span>

<span data-ttu-id="2da05-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2da05-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da05-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2da05-118">Remarks</span></span>

<span data-ttu-id="2da05-119">Puede especificar la lista de control de acceso (ACL) en el descriptor de seguridad de una tarea con el fin de permitir o denegar el acceso de determinados usuarios y grupos a una tarea.</span><span class="sxs-lookup"><span data-stu-id="2da05-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da05-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da05-120">Requirements</span></span>



| <span data-ttu-id="2da05-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da05-121">Requirement</span></span> | <span data-ttu-id="2da05-122">Value</span><span class="sxs-lookup"><span data-stu-id="2da05-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da05-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2da05-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2da05-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2da05-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2da05-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2da05-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2da05-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2da05-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2da05-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2da05-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="2da05-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2da05-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2da05-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2da05-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2da05-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da05-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da05-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2da05-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da05-132">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="2da05-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="2da05-133">**TaskFolder. GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2da05-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="2da05-134">**RegisteredTask.SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2da05-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





