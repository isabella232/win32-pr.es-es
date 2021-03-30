---
title: TriggerCollection. Item (propiedad)
description: En el caso de scripting, obtiene el desencadenador especificado de la colección.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto TriggerCollection
- Programador de tareas de objeto TriggerCollection, propiedad Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801730"
---
# <a name="triggercollectionitem-property"></a><span data-ttu-id="c6ccf-106">TriggerCollection. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c6ccf-106">TriggerCollection.Item property</span></span>

<span data-ttu-id="c6ccf-107">En el caso de scripting, obtiene el desencadenador especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="c6ccf-107">For scripting, gets the specified trigger from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ccf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6ccf-108">Syntax</span></span>


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a><span data-ttu-id="c6ccf-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c6ccf-109">Property value</span></span>

<span data-ttu-id="c6ccf-110">Objeto [**desencadenador**](trigger.md) que representa el desencadenador solicitado.</span><span class="sxs-lookup"><span data-stu-id="c6ccf-110">A [**Trigger**](trigger.md) object that represents the requested trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ccf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6ccf-111">Remarks</span></span>

<span data-ttu-id="c6ccf-112">Las colecciones se basan en 1.</span><span class="sxs-lookup"><span data-stu-id="c6ccf-112">Collections are 1-based.</span></span> <span data-ttu-id="c6ccf-113">En otras palabras, el índice del primer elemento de la colección es 1.</span><span class="sxs-lookup"><span data-stu-id="c6ccf-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6ccf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ccf-114">Requirements</span></span>



| <span data-ttu-id="c6ccf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ccf-115">Requirement</span></span> | <span data-ttu-id="c6ccf-116">Value</span><span class="sxs-lookup"><span data-stu-id="c6ccf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ccf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6ccf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ccf-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6ccf-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c6ccf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6ccf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ccf-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6ccf-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6ccf-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c6ccf-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6ccf-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6ccf-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6ccf-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6ccf-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ccf-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6ccf-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ccf-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6ccf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ccf-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="c6ccf-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





