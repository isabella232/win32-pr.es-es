---
title: Lista de reproducción. itemPlaylist
description: El atributo itemPlaylist recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado del elemento de lista de reproducción.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Windows Media Player de lista de reproducción. itemPlaylist
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709210"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="b7aaa-104">Lista de reproducción. itemPlaylist</span><span class="sxs-lookup"><span data-stu-id="b7aaa-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="b7aaa-105">El atributo **itemPlaylist** recupera la lista de reproducción del elemento multimedia que se muestra en el índice especificado del elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="b7aaa-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="b7aaa-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="b7aaa-106">Possible Values</span></span>

<span data-ttu-id="b7aaa-107">Este atributo es un objeto de **lista de reproducción** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7aaa-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7aaa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7aaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7aaa-109"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="b7aaa-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="b7aaa-110">**Número**(**largo**) que contiene el índice de un elemento de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7aaa-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7aaa-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7aaa-111">Remarks</span></span>

<span data-ttu-id="b7aaa-112">La propiedad **itemPlaylist** devolverá el objeto de lista de reproducción que se expande en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="b7aaa-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="b7aaa-113">Por ejemplo, si hay dos listas de reproducción anidadas que no se expanden en el elemento de **lista de reproducción** y que contienen tres clips multimedia cada una, **itemPlaylist**(1) devolverá la lista de reproducción primaria que contiene las dos listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="b7aaa-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="b7aaa-114">Si se expande la segunda lista de reproducción, **itemPlaylist**(1) devolverá la segunda lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7aaa-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="b7aaa-115">Si se expanden ambas listas de reproducción, **itemPlaylist**(1) devolverá la primera lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b7aaa-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7aaa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7aaa-116">Requirements</span></span>



| <span data-ttu-id="b7aaa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7aaa-117">Requirement</span></span> | <span data-ttu-id="b7aaa-118">Value</span><span class="sxs-lookup"><span data-stu-id="b7aaa-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b7aaa-119">Versión</span><span class="sxs-lookup"><span data-stu-id="b7aaa-119">Version</span></span><br/> | <span data-ttu-id="b7aaa-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b7aaa-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7aaa-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7aaa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7aaa-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="b7aaa-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="b7aaa-123">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="b7aaa-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





