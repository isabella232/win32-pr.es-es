---
title: ExecAction. arguments (propiedad)
description: En el caso de scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments (propiedad) Programador de tareas
- Propiedad arguments Programador de tareas, objeto ExecAction
- Programador de tareas de objeto ExecAction, propiedad arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996161"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="5c80e-106">ExecAction. arguments (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5c80e-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="5c80e-107">En el caso de scripting, obtiene o establece los argumentos asociados a la operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c80e-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c80e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c80e-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="5c80e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5c80e-109">Property value</span></span>

<span data-ttu-id="5c80e-110">Argumentos necesarios para la operación de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5c80e-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c80e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c80e-111">Remarks</span></span>

<span data-ttu-id="5c80e-112">Al leer o escribir XML, los argumentos de la operación de línea de comandos se especifican en el elemento [**arguments**](taskschedulerschema-arguments-exectype-element.md) del esquema programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="5c80e-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c80e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c80e-113">Requirements</span></span>



| <span data-ttu-id="5c80e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c80e-114">Requirement</span></span> | <span data-ttu-id="5c80e-115">Value</span><span class="sxs-lookup"><span data-stu-id="5c80e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c80e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c80e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c80e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5c80e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5c80e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c80e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c80e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c80e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c80e-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5c80e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c80e-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c80e-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c80e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c80e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c80e-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c80e-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c80e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c80e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c80e-125">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="5c80e-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="5c80e-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="5c80e-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





