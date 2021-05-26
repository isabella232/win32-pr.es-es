---
title: Evento Player.StringCollectionChange
description: El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas. | Evento Player.StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange Reproductor de Windows Media
- Evento StringCollectionChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a61b8e1e09e749579f323d506371138b0d9b59
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424095"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="db344-107">Evento Player.StringCollectionChange</span><span class="sxs-lookup"><span data-stu-id="db344-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="db344-108">El evento StringCollectionChange tiene lugar cuando cambia una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="db344-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="db344-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db344-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="db344-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db344-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db344-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="db344-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="db344-112">**Objeto StringCollection** que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="db344-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="db344-113">*change*</span><span class="sxs-lookup"><span data-stu-id="db344-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="db344-114">Número (long) que indica el tipo de cambio que se produjo en la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="db344-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="db344-115">Incluye uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="db344-115">Includes one of the following values.</span></span>



| <span data-ttu-id="db344-116">Number</span><span class="sxs-lookup"><span data-stu-id="db344-116">Number</span></span> | <span data-ttu-id="db344-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="db344-117">Description</span></span>                        |
|--------|------------------------------------|
| <span data-ttu-id="db344-118">0</span><span class="sxs-lookup"><span data-stu-id="db344-118">0</span></span>      | <span data-ttu-id="db344-119">desconocida.</span><span class="sxs-lookup"><span data-stu-id="db344-119">Unknown.</span></span> <span data-ttu-id="db344-120">(No es un valor válido)</span><span class="sxs-lookup"><span data-stu-id="db344-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="db344-121">1</span><span class="sxs-lookup"><span data-stu-id="db344-121">1</span></span>      | <span data-ttu-id="db344-122">Se insertó un elemento.</span><span class="sxs-lookup"><span data-stu-id="db344-122">An item was inserted.</span></span>              |
| <span data-ttu-id="db344-123">2</span><span class="sxs-lookup"><span data-stu-id="db344-123">2</span></span>      | <span data-ttu-id="db344-124">La colección de cadenas ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="db344-124">The string collection changed.</span></span>     |
| <span data-ttu-id="db344-125">3</span><span class="sxs-lookup"><span data-stu-id="db344-125">3</span></span>      | <span data-ttu-id="db344-126">Se eliminó un elemento.</span><span class="sxs-lookup"><span data-stu-id="db344-126">An item was deleted.</span></span>               |
| <span data-ttu-id="db344-127">4</span><span class="sxs-lookup"><span data-stu-id="db344-127">4</span></span>      | <span data-ttu-id="db344-128">Se ha borrado la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="db344-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="db344-129">5</span><span class="sxs-lookup"><span data-stu-id="db344-129">5</span></span>      | <span data-ttu-id="db344-130">Las actualizaciones masivas comienzan.</span><span class="sxs-lookup"><span data-stu-id="db344-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="db344-131">6</span><span class="sxs-lookup"><span data-stu-id="db344-131">6</span></span>      | <span data-ttu-id="db344-132">Las actualizaciones masivas han finalizado.</span><span class="sxs-lookup"><span data-stu-id="db344-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="db344-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="db344-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="db344-134">Número (long) que contiene el índice del elemento de colección de cadenas que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="db344-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db344-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db344-135">Return value</span></span>

<span data-ttu-id="db344-136">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="db344-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db344-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db344-137">Remarks</span></span>

<span data-ttu-id="db344-138">**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="db344-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="db344-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db344-139">Requirements</span></span>



| <span data-ttu-id="db344-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="db344-140">Requirement</span></span> | <span data-ttu-id="db344-141">Valor</span><span class="sxs-lookup"><span data-stu-id="db344-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db344-142">Versión</span><span class="sxs-lookup"><span data-stu-id="db344-142">Version</span></span><br/> | <span data-ttu-id="db344-143">Reproductor de Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="db344-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="db344-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db344-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="db344-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db344-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db344-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="db344-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db344-147">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="db344-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="db344-148">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="db344-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





