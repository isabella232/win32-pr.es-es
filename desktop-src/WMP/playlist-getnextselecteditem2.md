---
title: Lista de reproducción. getNextSelectedItem2
description: El método getNextSelectedItem2 recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- Windows Media Player de lista de reproducción. getNextSelectedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708227"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="68339-104">Lista de reproducción. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="68339-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="68339-105">El método **getNextSelectedItem2** recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.</span><span class="sxs-lookup"><span data-stu-id="68339-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="68339-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68339-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68339-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="68339-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="68339-108">**Número** (**largo**) que indica el índice del elemento que se va a buscar después de.</span><span class="sxs-lookup"><span data-stu-id="68339-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68339-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68339-109">Return Value</span></span>

<span data-ttu-id="68339-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="68339-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="68339-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68339-111">Remarks</span></span>

<span data-ttu-id="68339-112">Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **getNextSelectedItem** , que no puede.</span><span class="sxs-lookup"><span data-stu-id="68339-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="68339-113">Pase 1 en el parámetro *Item* para buscar el primer elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="68339-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="68339-114">Cuando no hay ningún elemento seleccionado, se devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="68339-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="68339-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68339-115">Requirements</span></span>



| <span data-ttu-id="68339-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="68339-116">Requirement</span></span> | <span data-ttu-id="68339-117">Value</span><span class="sxs-lookup"><span data-stu-id="68339-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="68339-118">Versión</span><span class="sxs-lookup"><span data-stu-id="68339-118">Version</span></span><br/> | <span data-ttu-id="68339-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="68339-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68339-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="68339-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68339-121">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="68339-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="68339-122">**Lista de reproducción. getNextSelectedItem**</span><span class="sxs-lookup"><span data-stu-id="68339-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





