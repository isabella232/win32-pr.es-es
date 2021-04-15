---
title: ActionCollection. Item (propiedad)
description: En el caso de scripting, obtiene una acción especificada de la colección.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Propiedad del elemento Programador de tareas
- Propiedad Item Programador de tareas, objeto ActionCollection
- Programador de tareas de objeto ActionCollection, propiedad Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422490"
---
# <a name="actioncollectionitem-property"></a><span data-ttu-id="e7393-106">ActionCollection. Item (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e7393-106">ActionCollection.Item property</span></span>

<span data-ttu-id="e7393-107">En el caso de scripting, obtiene una acción especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="e7393-107">For scripting, gets a specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7393-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7393-108">Syntax</span></span>


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a><span data-ttu-id="e7393-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e7393-109">Property value</span></span>

<span data-ttu-id="e7393-110">Objeto de [**acción**](action.md) que representa la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="e7393-110">An [**Action**](action.md) object that represents the requested action.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7393-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7393-111">Remarks</span></span>

<span data-ttu-id="e7393-112">Las colecciones se basan en 1.</span><span class="sxs-lookup"><span data-stu-id="e7393-112">Collections are 1-based.</span></span> <span data-ttu-id="e7393-113">En otras palabras, el índice del primer elemento de la colección es 1.</span><span class="sxs-lookup"><span data-stu-id="e7393-113">In other words, the index for the first item in the collection is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7393-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7393-114">Requirements</span></span>



| <span data-ttu-id="e7393-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7393-115">Requirement</span></span> | <span data-ttu-id="e7393-116">Value</span><span class="sxs-lookup"><span data-stu-id="e7393-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7393-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7393-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7393-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7393-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e7393-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7393-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7393-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7393-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e7393-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e7393-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7393-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7393-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7393-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7393-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7393-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7393-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7393-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7393-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7393-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e7393-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e7393-127">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="e7393-127">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





