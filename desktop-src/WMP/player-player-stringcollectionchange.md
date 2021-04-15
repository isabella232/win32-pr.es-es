---
title: Evento Player. StringCollectionChange
description: El evento StringCollectionChange se produce cuando cambia una colección de cadenas. | Evento Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Media Player StringCollectionChange de eventos de Windows
- Evento StringCollectionChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento StringCollectionChange
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
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708259"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="fd47f-107">Evento Player. StringCollectionChange</span><span class="sxs-lookup"><span data-stu-id="fd47f-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="fd47f-108">El evento StringCollectionChange se produce cuando cambia una colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="fd47f-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd47f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd47f-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="fd47f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd47f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd47f-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="fd47f-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="fd47f-112">Objeto **StringCollection** que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fd47f-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="fd47f-113">*change*</span><span class="sxs-lookup"><span data-stu-id="fd47f-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="fd47f-114">Número (largo) que indica el tipo de cambio que se produjo en la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="fd47f-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="fd47f-115">Incluye uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fd47f-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="fd47f-116">Number</span><span class="sxs-lookup"><span data-stu-id="fd47f-116">Number</span></span> | <span data-ttu-id="fd47f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd47f-117">Description</span></span>                        |
| <span data-ttu-id="fd47f-118">0</span><span class="sxs-lookup"><span data-stu-id="fd47f-118">0</span></span>      | <span data-ttu-id="fd47f-119">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fd47f-119">Unknown.</span></span> <span data-ttu-id="fd47f-120">(No es un valor válido)</span><span class="sxs-lookup"><span data-stu-id="fd47f-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="fd47f-121">1</span><span class="sxs-lookup"><span data-stu-id="fd47f-121">1</span></span>      | <span data-ttu-id="fd47f-122">Se insertó un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd47f-122">An item was inserted.</span></span>              |
| <span data-ttu-id="fd47f-123">2</span><span class="sxs-lookup"><span data-stu-id="fd47f-123">2</span></span>      | <span data-ttu-id="fd47f-124">La colección de cadenas ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fd47f-124">The string collection changed.</span></span>     |
| <span data-ttu-id="fd47f-125">3</span><span class="sxs-lookup"><span data-stu-id="fd47f-125">3</span></span>      | <span data-ttu-id="fd47f-126">Se eliminó un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd47f-126">An item was deleted.</span></span>               |
| <span data-ttu-id="fd47f-127">4</span><span class="sxs-lookup"><span data-stu-id="fd47f-127">4</span></span>      | <span data-ttu-id="fd47f-128">Se borró la colección de cadenas.</span><span class="sxs-lookup"><span data-stu-id="fd47f-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="fd47f-129">5</span><span class="sxs-lookup"><span data-stu-id="fd47f-129">5</span></span>      | <span data-ttu-id="fd47f-130">Se están iniciando las actualizaciones masivas.</span><span class="sxs-lookup"><span data-stu-id="fd47f-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="fd47f-131">6</span><span class="sxs-lookup"><span data-stu-id="fd47f-131">6</span></span>      | <span data-ttu-id="fd47f-132">Las actualizaciones masivas han finalizado.</span><span class="sxs-lookup"><span data-stu-id="fd47f-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="fd47f-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="fd47f-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="fd47f-134">Número (largo) que contiene el índice del elemento de colección de cadenas que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fd47f-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd47f-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd47f-135">Return value</span></span>

<span data-ttu-id="fd47f-136">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="fd47f-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd47f-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd47f-137">Remarks</span></span>

<span data-ttu-id="fd47f-138">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="fd47f-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd47f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd47f-139">Requirements</span></span>



| <span data-ttu-id="fd47f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd47f-140">Requirement</span></span> | <span data-ttu-id="fd47f-141">Value</span><span class="sxs-lookup"><span data-stu-id="fd47f-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd47f-142">Versión</span><span class="sxs-lookup"><span data-stu-id="fd47f-142">Version</span></span><br/> | <span data-ttu-id="fd47f-143">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="fd47f-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="fd47f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd47f-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd47f-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd47f-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd47f-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd47f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd47f-147">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="fd47f-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="fd47f-148">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="fd47f-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





