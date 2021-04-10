---
title: Propiedad principal. UserId
description: En el caso de scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Propiedad UserId Programador de tareas
- Propiedad UserId Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150511"
---
# <a name="principaluserid-property"></a><span data-ttu-id="a1238-106">Propiedad principal. UserId</span><span class="sxs-lookup"><span data-stu-id="a1238-106">Principal.UserId property</span></span>

<span data-ttu-id="a1238-107">En el caso de scripting, obtiene o establece el identificador de usuario necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a1238-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1238-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1238-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="a1238-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a1238-109">Property value</span></span>

<span data-ttu-id="a1238-110">Identificador de usuario necesario para ejecutar la tarea.</span><span class="sxs-lookup"><span data-stu-id="a1238-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1238-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1238-111">Remarks</span></span>

<span data-ttu-id="a1238-112">No establezca esta propiedad si se especifica un identificador de grupo en la propiedad [**GROUPID**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="a1238-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="a1238-113">Al leer o escribir XML para una tarea, el identificador de usuario de la entidad de seguridad se especifica mediante el elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="a1238-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1238-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1238-114">Requirements</span></span>



| <span data-ttu-id="a1238-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1238-115">Requirement</span></span> | <span data-ttu-id="a1238-116">Value</span><span class="sxs-lookup"><span data-stu-id="a1238-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1238-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1238-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a1238-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1238-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a1238-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1238-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a1238-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1238-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1238-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a1238-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a1238-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1238-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1238-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1238-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1238-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1238-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1238-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1238-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1238-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="a1238-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a1238-127">**Principal**</span><span class="sxs-lookup"><span data-stu-id="a1238-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="a1238-128">**Entidad de seguridad. GroupId**</span><span class="sxs-lookup"><span data-stu-id="a1238-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





