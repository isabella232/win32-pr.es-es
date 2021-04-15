---
title: Propiedad principal. nivel
description: En el caso de scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Programador de tareas de la propiedad nivel
- Propiedad nivel Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad nivel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534293"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="2ebda-106">Propiedad principal. nivel</span><span class="sxs-lookup"><span data-stu-id="2ebda-106">Principal.RunLevel property</span></span>

<span data-ttu-id="2ebda-107">En el caso de scripting, obtiene o establece el identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2ebda-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="2ebda-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2ebda-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebda-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ebda-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="2ebda-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2ebda-110">Property value</span></span>

<span data-ttu-id="2ebda-111">El identificador que se usa para especificar el nivel de privilegios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2ebda-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="2ebda-112">Value</span><span class="sxs-lookup"><span data-stu-id="2ebda-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="2ebda-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2ebda-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="2ebda-114"><dt>**Tarea \_ de NIVEL \_ Lua**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2ebda-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="2ebda-115">Las tareas se ejecutarán con los privilegios mínimos (LUA).</span><span class="sxs-lookup"><span data-stu-id="2ebda-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="2ebda-116"><dt>**Tarea \_ de NIVEL \_ más alto**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2ebda-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2ebda-117">Las tareas se ejecutarán con los privilegios más altos.</span><span class="sxs-lookup"><span data-stu-id="2ebda-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="2ebda-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ebda-118">Remarks</span></span>

<span data-ttu-id="2ebda-119">Si una tarea se registra mediante la cuenta de \\ Administrador de Builtin o las cuentas de sistema local o de servicio local, se omitirá la propiedad **nivel** .</span><span class="sxs-lookup"><span data-stu-id="2ebda-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="2ebda-120">También se omitirá el valor de propiedad si el control de cuentas de usuario (UAC) está desactivado.</span><span class="sxs-lookup"><span data-stu-id="2ebda-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="2ebda-121">Si una tarea se registra mediante el grupo de administradores para el contexto de seguridad de la tarea, también debe establecer la propiedad [**nivel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) en la **tarea \_ nivel \_ más alta** si desea ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="2ebda-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="2ebda-122">Para obtener más información, vea [contextos de seguridad para tareas](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="2ebda-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebda-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ebda-123">Requirements</span></span>



| <span data-ttu-id="2ebda-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebda-124">Requirement</span></span> | <span data-ttu-id="2ebda-125">Value</span><span class="sxs-lookup"><span data-stu-id="2ebda-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebda-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ebda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebda-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ebda-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2ebda-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ebda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebda-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ebda-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ebda-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2ebda-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ebda-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ebda-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ebda-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ebda-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebda-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ebda-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebda-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ebda-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebda-135">**Principal**</span><span class="sxs-lookup"><span data-stu-id="2ebda-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





