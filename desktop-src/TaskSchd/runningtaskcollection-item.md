---
title: RunningTaskCollection. Item (propiedad)
description: Para el scripting, obtiene la tarea especificada de la colección.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto RunningTaskCollection
- Programador de tareas de objeto RunningTaskCollection, propiedad Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150609"
---
# <a name="runningtaskcollectionitem-property"></a><span data-ttu-id="e64bc-106">RunningTaskCollection. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e64bc-106">RunningTaskCollection.Item property</span></span>

<span data-ttu-id="e64bc-107">Para el scripting, obtiene la tarea especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="e64bc-107">For scripting, gets the specified task from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e64bc-108">Syntax</span></span>


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a><span data-ttu-id="e64bc-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e64bc-109">Property value</span></span>

<span data-ttu-id="e64bc-110">Objeto [**RunningTask**](runningtask.md) que contiene el contexto solicitado.</span><span class="sxs-lookup"><span data-stu-id="e64bc-110">A [**RunningTask**](runningtask.md) object that contains the requested context.</span></span>

## <a name="remarks"></a><span data-ttu-id="e64bc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e64bc-111">Remarks</span></span>

<span data-ttu-id="e64bc-112">Las colecciones se basan en 1.</span><span class="sxs-lookup"><span data-stu-id="e64bc-112">Collections are 1-based.</span></span> <span data-ttu-id="e64bc-113">En otras palabras, el índice del primer elemento de la colección es 1.</span><span class="sxs-lookup"><span data-stu-id="e64bc-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e64bc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e64bc-114">Requirements</span></span>



| <span data-ttu-id="e64bc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64bc-115">Requirement</span></span> | <span data-ttu-id="e64bc-116">Value</span><span class="sxs-lookup"><span data-stu-id="e64bc-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e64bc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e64bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e64bc-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e64bc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e64bc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e64bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e64bc-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e64bc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e64bc-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e64bc-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e64bc-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e64bc-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e64bc-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e64bc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e64bc-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64bc-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e64bc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e64bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64bc-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e64bc-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





