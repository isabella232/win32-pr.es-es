---
title: Lista de reproducción. getNextSelectedItem
description: El método getNextSelectedItem recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Windows Media Player de lista de reproducción. getNextSelectedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708230"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="c432c-104">Lista de reproducción. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="c432c-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="c432c-105">El método **getNextSelectedItem** recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c432c-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="c432c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c432c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c432c-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="c432c-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="c432c-108">**Número** (**largo**) que indica el índice del elemento que se va a buscar después de.</span><span class="sxs-lookup"><span data-stu-id="c432c-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c432c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c432c-109">Return Value</span></span>

<span data-ttu-id="c432c-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c432c-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c432c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c432c-111">Remarks</span></span>

<span data-ttu-id="c432c-112">Cuando no hay más elementos seleccionados, este método devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="c432c-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="c432c-113">Este método se ha reemplazado por **getNextSelectedItem2**, que admite listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="c432c-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c432c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c432c-114">Requirements</span></span>



| <span data-ttu-id="c432c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c432c-115">Requirement</span></span> | <span data-ttu-id="c432c-116">Value</span><span class="sxs-lookup"><span data-stu-id="c432c-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c432c-117">Versión</span><span class="sxs-lookup"><span data-stu-id="c432c-117">Version</span></span><br/> | <span data-ttu-id="c432c-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c432c-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c432c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c432c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c432c-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="c432c-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="c432c-121">**Lista de reproducción. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="c432c-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





