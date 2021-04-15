---
title: Evento Player. MediaCollectionMediaRemoved
description: El evento MediaCollectionMediaRemoved se produce cuando se quita un elemento multimedia de la biblioteca local. | Evento Player. MediaCollectionMediaRemoved
ms.assetid: a1df6faf-38dc-4f5f-8f8a-953c91ea026c
keywords:
- Media Player MediaCollectionMediaRemoved de eventos de Windows
- Evento MediaCollectionMediaRemoved de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionMediaRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionMediaRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72af5fe4c5e90effeb34745ea71e3edb457da357
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709241"
---
# <a name="playermediacollectionmediaremoved-event"></a><span data-ttu-id="d8f59-107">Evento Player. MediaCollectionMediaRemoved</span><span class="sxs-lookup"><span data-stu-id="d8f59-107">Player.MediaCollectionMediaRemoved event</span></span>

<span data-ttu-id="d8f59-108">El evento MediaCollectionMediaRemoved se produce cuando se quita un elemento multimedia de la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="d8f59-108">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f59-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8f59-109">Syntax</span></span>


```JScript
Player.MediaCollectionMediaRemoved(
  pdispMedia
)
```



## <a name="parameters"></a><span data-ttu-id="d8f59-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8f59-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f59-111">*pdispMedia*</span><span class="sxs-lookup"><span data-stu-id="d8f59-111">*pdispMedia*</span></span> 
</dt> <dd>

<span data-ttu-id="d8f59-112">Objeto **multimedia** que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="d8f59-112">**Media** object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f59-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8f59-113">Return value</span></span>

<span data-ttu-id="d8f59-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="d8f59-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8f59-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8f59-115">Remarks</span></span>

<span data-ttu-id="d8f59-116">Este evento solo se produce para la biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="d8f59-116">This event only occurs for the local library.</span></span>

<span data-ttu-id="d8f59-117">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d8f59-117">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f59-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8f59-118">Requirements</span></span>



| <span data-ttu-id="d8f59-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8f59-119">Requirement</span></span> | <span data-ttu-id="d8f59-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8f59-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f59-121">Versión</span><span class="sxs-lookup"><span data-stu-id="d8f59-121">Version</span></span><br/> | <span data-ttu-id="d8f59-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d8f59-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="d8f59-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8f59-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8f59-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8f59-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f59-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8f59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f59-126">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="d8f59-126">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="d8f59-127">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="d8f59-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="d8f59-128">**Player. mediaCollection**</span><span class="sxs-lookup"><span data-stu-id="d8f59-128">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





