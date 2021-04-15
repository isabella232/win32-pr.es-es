---
title: Propiedad principal. GroupId
description: En el caso de scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Propiedad GroupId Programador de tareas
- Propiedad GroupId Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686085"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="2b948-106">Propiedad principal. GroupId</span><span class="sxs-lookup"><span data-stu-id="2b948-106">Principal.GroupId property</span></span>

<span data-ttu-id="2b948-107">En el caso de scripting, obtiene o establece el identificador del grupo de usuarios necesario para ejecutar las tareas que están asociadas a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b948-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b948-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b948-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="2b948-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b948-109">Property value</span></span>

<span data-ttu-id="2b948-110">Identificador del grupo de usuarios que está asociado a esta entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b948-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b948-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b948-111">Remarks</span></span>

<span data-ttu-id="2b948-112">No establezca esta propiedad si se especifica un identificador de usuario en la propiedad [**userid**](principal-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="2b948-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="2b948-113">Al leer o escribir XML para una tarea, el identificador de grupo de una entidad de seguridad se especifica en el elemento [**GROUPID**](taskschedulerschema-groupid-principaltype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="2b948-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b948-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b948-114">Requirements</span></span>



| <span data-ttu-id="2b948-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b948-115">Requirement</span></span> | <span data-ttu-id="2b948-116">Value</span><span class="sxs-lookup"><span data-stu-id="2b948-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b948-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b948-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b948-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2b948-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2b948-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b948-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b948-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b948-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b948-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2b948-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b948-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2b948-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2b948-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b948-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b948-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b948-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b948-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b948-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b948-126">**Deberían**</span><span class="sxs-lookup"><span data-stu-id="2b948-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="2b948-127">**Principal**</span><span class="sxs-lookup"><span data-stu-id="2b948-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="2b948-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="2b948-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





