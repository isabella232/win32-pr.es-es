---
title: Propiedad Trigger.Id
description: Para el scripting, obtiene o establece el identificador del desencadenador.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Propiedad ID Programador de tareas
- Propiedad ID Programador de tareas, objeto desencadenador
- Objeto desencadenador Programador de tareas, propiedad ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533945"
---
# <a name="triggerid-property"></a><span data-ttu-id="b1f1d-106">Propiedad Trigger.Id</span><span class="sxs-lookup"><span data-stu-id="b1f1d-106">Trigger.Id property</span></span>

<span data-ttu-id="b1f1d-107">Para el scripting, obtiene o establece el identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b1f1d-107">For scripting, gets or sets the identifier for the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f1d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1f1d-108">Syntax</span></span>


```VB
Trigger.Id As String
```



## <a name="property-value"></a><span data-ttu-id="b1f1d-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b1f1d-109">Property value</span></span>

<span data-ttu-id="b1f1d-110">Identificador del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="b1f1d-110">The identifier for the trigger.</span></span> <span data-ttu-id="b1f1d-111">El Programador de tareas usa este identificador para el registro.</span><span class="sxs-lookup"><span data-stu-id="b1f1d-111">This identifier is used by the Task Scheduler for logging purposes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f1d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1f1d-112">Remarks</span></span>

<span data-ttu-id="b1f1d-113">Al leer o escribir XML para una tarea, el identificador del desencadenador se especifica en el atributo ID de los elementos de desencadenador individuales (por ejemplo, el atributo ID del elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="b1f1d-113">When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element) of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f1d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f1d-114">Requirements</span></span>



| <span data-ttu-id="b1f1d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f1d-115">Requirement</span></span> | <span data-ttu-id="b1f1d-116">Value</span><span class="sxs-lookup"><span data-stu-id="b1f1d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f1d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1f1d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f1d-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b1f1d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1f1d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1f1d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f1d-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1f1d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1f1d-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b1f1d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1f1d-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1f1d-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1f1d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1f1d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f1d-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1f1d-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1f1d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1f1d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f1d-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b1f1d-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





