---
title: Propiedad Principal.Id
description: En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Propiedad ID Programador de tareas
- Propiedad ID Programador de tareas, objeto principal
- Programador de tareas de objeto principal, propiedad ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422488"
---
# <a name="principalid-property"></a><span data-ttu-id="148b0-106">Propiedad Principal.Id</span><span class="sxs-lookup"><span data-stu-id="148b0-106">Principal.Id property</span></span>

<span data-ttu-id="148b0-107">En el caso de scripting, obtiene o establece el identificador de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="148b0-107">For scripting, gets or sets the identifier of the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="148b0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="148b0-108">Syntax</span></span>


```VB
Principal.Id As String
```



## <a name="property-value"></a><span data-ttu-id="148b0-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="148b0-109">Property value</span></span>

<span data-ttu-id="148b0-110">El identificador de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="148b0-110">The identifier of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="148b0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="148b0-111">Remarks</span></span>

<span data-ttu-id="148b0-112">Este identificador también se utiliza al especificar la propiedad [**ActionCollection. Context**](actioncollection-context.md) .</span><span class="sxs-lookup"><span data-stu-id="148b0-112">This identifier is also used when specifying the [**ActionCollection.Context**](actioncollection-context.md) property.</span></span>

<span data-ttu-id="148b0-113">Al leer o escribir XML para una tarea, el identificador de la entidad de seguridad se especifica en el atributo ID del elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="148b0-113">When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="148b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="148b0-114">Requirements</span></span>



| <span data-ttu-id="148b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="148b0-115">Requirement</span></span> | <span data-ttu-id="148b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="148b0-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="148b0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="148b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="148b0-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="148b0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="148b0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="148b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="148b0-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="148b0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="148b0-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="148b0-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="148b0-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="148b0-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="148b0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="148b0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148b0-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="148b0-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="148b0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="148b0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148b0-126">**ActionCollection. Context**</span><span class="sxs-lookup"><span data-stu-id="148b0-126">**ActionCollection.Context**</span></span>](actioncollection-context.md)
</dt> <dt>

[<span data-ttu-id="148b0-127">**Principal**</span><span class="sxs-lookup"><span data-stu-id="148b0-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="148b0-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="148b0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





