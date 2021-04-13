---
title: TriggerCollection. Remove (método)
description: En el caso de scripting, quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- desencadenadores Programador de tareas, quitar
- Quitar método Programador de tareas
- Quitar método Programador de tareas, objeto TriggerCollection
- Objeto TriggerCollection Programador de tareas, Remove (método)
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359720"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="ea4e9-107">TriggerCollection. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="ea4e9-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="ea4e9-108">En el caso de scripting, quita el desencadenador especificado de la colección de desencadenadores utilizada por la tarea.</span><span class="sxs-lookup"><span data-stu-id="ea4e9-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea4e9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea4e9-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="ea4e9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea4e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea4e9-111">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ea4e9-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea4e9-112">Índice del desencadenador que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="ea4e9-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea4e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea4e9-113">Return value</span></span>

<span data-ttu-id="ea4e9-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ea4e9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4e9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea4e9-115">Remarks</span></span>

<span data-ttu-id="ea4e9-116">Al quitar los elementos, tenga en cuenta que el índice del primer elemento de la colección es 1 y el índice del último elemento es el valor de la propiedad [**TriggerCollection. Count**](triggercollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4e9-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4e9-117">Requirements</span></span>



| <span data-ttu-id="ea4e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4e9-118">Requirement</span></span> | <span data-ttu-id="ea4e9-119">Value</span><span class="sxs-lookup"><span data-stu-id="ea4e9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4e9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4e9-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ea4e9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ea4e9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea4e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4e9-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea4e9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea4e9-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ea4e9-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea4e9-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e9-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea4e9-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea4e9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea4e9-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e9-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4e9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea4e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4e9-129">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="ea4e9-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





