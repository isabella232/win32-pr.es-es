---
title: Evento Player. MediaCollectionMediaAdded
description: El evento MediaCollectionMediaAdded se produce cuando se agrega un elemento multimedia a la biblioteca local. | Evento Player. MediaCollectionMediaAdded
ms.assetid: 01696d28-e83b-4fd2-8e88-2871831b61e7
keywords:
- Media Player MediaCollectionMediaAdded de eventos de Windows
- Evento MediaCollectionMediaAdded de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionMediaAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18dd0536f508090c46f9fc5a9059c809f50091d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709132"
---
# <a name="playermediacollectionmediaadded-event"></a><span data-ttu-id="6d7b5-107">Evento Player. MediaCollectionMediaAdded</span><span class="sxs-lookup"><span data-stu-id="6d7b5-107">Player.MediaCollectionMediaAdded event</span></span>

<span data-ttu-id="6d7b5-108">El evento MediaCollectionMediaAdded se produce cuando se agrega un elemento multimedia a la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-108">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7b5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d7b5-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaAdded(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="6d7b5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d7b5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d7b5-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="6d7b5-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="6d7b5-112">Objeto **multimedia** que se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-112">**Media** object that was added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d7b5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d7b5-113">Return value</span></span>

<span data-ttu-id="6d7b5-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d7b5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d7b5-115">Remarks</span></span>

<span data-ttu-id="6d7b5-116">Este evento solo se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="6d7b5-117">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d7b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d7b5-118">Requirements</span></span>



| <span data-ttu-id="6d7b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d7b5-119">Requirement</span></span> | <span data-ttu-id="6d7b5-120">Value</span><span class="sxs-lookup"><span data-stu-id="6d7b5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7b5-121">Versión</span><span class="sxs-lookup"><span data-stu-id="6d7b5-121">Version</span></span><br/> | <span data-ttu-id="6d7b5-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="6d7b5-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="6d7b5-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d7b5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d7b5-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d7b5-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7b5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d7b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7b5-126">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6d7b5-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="6d7b5-127">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="6d7b5-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="6d7b5-128">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6d7b5-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





