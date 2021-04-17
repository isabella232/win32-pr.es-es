---
title: PLAYLIST. itemCount
description: El atributo itemCount recupera el número de elementos que se muestran actualmente en el elemento de lista de reproducción.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Lista de reproducción. itemCount de Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661227"
---
# <a name="playlistitemcount"></a><span data-ttu-id="6c736-104">PLAYLIST. itemCount</span><span class="sxs-lookup"><span data-stu-id="6c736-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="6c736-105">El atributo **itemCount** recupera el número de elementos que se muestran actualmente en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="6c736-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="6c736-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6c736-106">Possible Values</span></span>

<span data-ttu-id="6c736-107">Este atributo es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="6c736-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c736-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c736-108">Remarks</span></span>

<span data-ttu-id="6c736-109">La propiedad **itemCount** contará el número total de elementos expandidos.</span><span class="sxs-lookup"><span data-stu-id="6c736-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="6c736-110">Por ejemplo, si hay dos listas de reproducción que contienen tres elementos multimedia cada uno, **itemCount** devolverá 2 si las listas de reproducción no se expanden.</span><span class="sxs-lookup"><span data-stu-id="6c736-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="6c736-111">Si solo se expande la primera lista de reproducción, **itemCount** devolverá 4.</span><span class="sxs-lookup"><span data-stu-id="6c736-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="6c736-112">Si se expanden ambas listas de reproducción, **itemCount** devolverá 6.</span><span class="sxs-lookup"><span data-stu-id="6c736-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c736-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c736-113">Requirements</span></span>



| <span data-ttu-id="6c736-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c736-114">Requirement</span></span> | <span data-ttu-id="6c736-115">Value</span><span class="sxs-lookup"><span data-stu-id="6c736-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="6c736-116">Versión</span><span class="sxs-lookup"><span data-stu-id="6c736-116">Version</span></span><br/> | <span data-ttu-id="6c736-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="6c736-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c736-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c736-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c736-119">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="6c736-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





