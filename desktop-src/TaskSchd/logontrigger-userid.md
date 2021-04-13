---
title: LogonTrigger. UserId (propiedad)
description: En el caso de scripting, obtiene o establece el identificador del usuario.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Propiedad UserId Programador de tareas
- Propiedad UserId Programador de tareas, objeto LogonTrigger
- Programador de tareas de objeto LogonTrigger, propiedad UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422037"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="46ed3-106">LogonTrigger. UserId (propiedad)</span><span class="sxs-lookup"><span data-stu-id="46ed3-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="46ed3-107">En el caso de scripting, obtiene o establece el identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="46ed3-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ed3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46ed3-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="46ed3-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="46ed3-109">Property value</span></span>

<span data-ttu-id="46ed3-110">El identificador del usuario.</span><span class="sxs-lookup"><span data-stu-id="46ed3-110">The identifier of the user.</span></span> <span data-ttu-id="46ed3-111">Por ejemplo, "midominio \\ nombre" o para una cuenta local, "administrador".</span><span class="sxs-lookup"><span data-stu-id="46ed3-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="46ed3-112">Esta propiedad puede estar en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="46ed3-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="46ed3-113">Nombre de usuario o SID: la tarea se inicia cuando el usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="46ed3-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="46ed3-114">NULL: la tarea se inicia cuando cualquier usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="46ed3-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ed3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46ed3-115">Remarks</span></span>

<span data-ttu-id="46ed3-116">Si desea que una tarea se desencadene cuando un miembro de un grupo inicia sesión en el equipo en lugar de cuando un usuario específico inicia sesión, no asigne un valor a la propiedad **LogonTrigger. userid** .</span><span class="sxs-lookup"><span data-stu-id="46ed3-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="46ed3-117">En su lugar, cree un desencadenador Logon con una propiedad **LogonTrigger. userid** vacía y asigne un valor a la entidad de seguridad para la tarea mediante la propiedad [**principal. GROUPID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="46ed3-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="46ed3-118">Al leer o escribir XML para una tarea, el identificador de usuario de inicio de sesión se especifica mediante el elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="46ed3-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ed3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ed3-119">Requirements</span></span>



| <span data-ttu-id="46ed3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46ed3-120">Requirement</span></span> | <span data-ttu-id="46ed3-121">Value</span><span class="sxs-lookup"><span data-stu-id="46ed3-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46ed3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46ed3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="46ed3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46ed3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46ed3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46ed3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="46ed3-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="46ed3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46ed3-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="46ed3-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="46ed3-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="46ed3-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="46ed3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46ed3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46ed3-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46ed3-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ed3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="46ed3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ed3-131">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="46ed3-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="46ed3-132">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="46ed3-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





