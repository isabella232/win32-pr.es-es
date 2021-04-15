---
title: Query. beginNextGroup (método)
description: El método beginNextGroup comienza un nuevo grupo de condiciones. | Query. beginNextGroup (método)
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- método beginNextGroup de Windows Media Player
- método beginNextGroup de Windows Media Player, clase de consulta
- Clase de consulta de Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709070"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="61569-107">Query. beginNextGroup (método)</span><span class="sxs-lookup"><span data-stu-id="61569-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="61569-108">El método **beginNextGroup** comienza un nuevo grupo de condiciones.</span><span class="sxs-lookup"><span data-stu-id="61569-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="61569-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61569-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="61569-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61569-110">Parameters</span></span>

<span data-ttu-id="61569-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="61569-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61569-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61569-112">Return value</span></span>

<span data-ttu-id="61569-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61569-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61569-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61569-114">Remarks</span></span>

<span data-ttu-id="61569-115">El inicio de un nuevo grupo de condiciones implica que se ha completado el grupo de condiciones actual.</span><span class="sxs-lookup"><span data-stu-id="61569-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="61569-116">El nuevo grupo de condiciones siempre se concatena al grupo de condiciones anterior mediante la lógica o.</span><span class="sxs-lookup"><span data-stu-id="61569-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="61569-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61569-117">Requirements</span></span>



| <span data-ttu-id="61569-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="61569-118">Requirement</span></span> | <span data-ttu-id="61569-119">Value</span><span class="sxs-lookup"><span data-stu-id="61569-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61569-120">Versión</span><span class="sxs-lookup"><span data-stu-id="61569-120">Version</span></span><br/> | <span data-ttu-id="61569-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="61569-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="61569-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61569-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="61569-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61569-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61569-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="61569-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61569-125">**MediaCollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="61569-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="61569-126">**MediaCollection.getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="61569-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="61569-127">**MediaCollection.getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="61569-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="61569-128">**Query (objeto)**</span><span class="sxs-lookup"><span data-stu-id="61569-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="61569-129">**Consulta. addCondition**</span><span class="sxs-lookup"><span data-stu-id="61569-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





