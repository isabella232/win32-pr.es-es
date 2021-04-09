---
title: Desencadenador. Enabled (propiedad)
description: En el caso de scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Propiedad Enabled Programador de tareas
- Propiedad habilitada Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411bc36dcf03933e2b4cee2f575aaec3b8133846
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996152"
---
# <a name="triggerenabled-property"></a><span data-ttu-id="b3d64-106">Desencadenador. Enabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b3d64-106">Trigger.Enabled property</span></span>

<span data-ttu-id="b3d64-107">En el caso de scripting, obtiene o establece un valor booleano que indica si el desencadenador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b3d64-107">For scripting, gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d64-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3d64-108">Syntax</span></span>


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b3d64-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b3d64-109">Property value</span></span>

<span data-ttu-id="b3d64-110">True si el desencadenador está habilitado; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="b3d64-110">True if the trigger is enabled; otherwise, false.</span></span> <span data-ttu-id="b3d64-111">El valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="b3d64-111">The default is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3d64-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3d64-112">Remarks</span></span>

<span data-ttu-id="b3d64-113">Al leer o escribir XML para una tarea, se especifica la propiedad Enabled mediante el elemento [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) del esquema de programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="b3d64-113">When reading or writing XML for a task, the enabled property is specified using the [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d64-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3d64-114">Requirements</span></span>



| <span data-ttu-id="b3d64-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3d64-115">Requirement</span></span> | <span data-ttu-id="b3d64-116">Value</span><span class="sxs-lookup"><span data-stu-id="b3d64-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d64-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d64-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d64-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3d64-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b3d64-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3d64-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d64-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3d64-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3d64-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b3d64-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3d64-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3d64-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3d64-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3d64-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3d64-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3d64-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3d64-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3d64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d64-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b3d64-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





