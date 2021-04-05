---
title: ActionCollection. Remove (método)
description: En el caso de scripting, quita la acción especificada de la colección.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Quitar método Programador de tareas
- Quitar método Programador de tareas, objeto ActionCollection
- Objeto ActionCollection Programador de tareas, Remove (método)
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802996"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="6bc88-106">ActionCollection. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="6bc88-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="6bc88-107">En el caso de scripting, quita la acción especificada de la colección.</span><span class="sxs-lookup"><span data-stu-id="6bc88-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc88-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bc88-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="6bc88-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bc88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bc88-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6bc88-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bc88-111">Índice de la acción que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6bc88-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bc88-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bc88-112">Return value</span></span>

<span data-ttu-id="6bc88-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6bc88-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc88-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bc88-114">Remarks</span></span>

<span data-ttu-id="6bc88-115">Al quitar los elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y el índice del último elemento es el valor de la propiedad [**ActionCollection. Count**](actioncollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc88-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc88-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc88-116">Requirements</span></span>



| <span data-ttu-id="6bc88-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc88-117">Requirement</span></span> | <span data-ttu-id="6bc88-118">Value</span><span class="sxs-lookup"><span data-stu-id="6bc88-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc88-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bc88-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc88-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6bc88-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6bc88-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bc88-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc88-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6bc88-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bc88-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6bc88-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="6bc88-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6bc88-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6bc88-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6bc88-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bc88-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bc88-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc88-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bc88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc88-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6bc88-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="6bc88-129">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="6bc88-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





