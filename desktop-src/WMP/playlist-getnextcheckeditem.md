---
title: Lista de reproducción. getNextCheckedItem
description: El método getNextCheckedItem recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Windows Media Player de lista de reproducción. getNextCheckedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708233"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="e9972-104">Lista de reproducción. getNextCheckedItem</span><span class="sxs-lookup"><span data-stu-id="e9972-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="e9972-105">El método **getNextCheckedItem** recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="e9972-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="e9972-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9972-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="e9972-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="e9972-108">**Número** (**largo**) que indica el índice del elemento que se va a buscar después de.</span><span class="sxs-lookup"><span data-stu-id="e9972-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9972-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9972-109">Return Value</span></span>

<span data-ttu-id="e9972-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e9972-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9972-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9972-111">Remarks</span></span>

<span data-ttu-id="e9972-112">Cuando no hay más elementos marcados, este método devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="e9972-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="e9972-113">Este método se ha reemplazado por **getNextCheckedItem2**, que admite listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="e9972-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9972-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9972-114">Requirements</span></span>



| <span data-ttu-id="e9972-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9972-115">Requirement</span></span> | <span data-ttu-id="e9972-116">Value</span><span class="sxs-lookup"><span data-stu-id="e9972-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e9972-117">Versión</span><span class="sxs-lookup"><span data-stu-id="e9972-117">Version</span></span><br/> | <span data-ttu-id="e9972-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e9972-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9972-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9972-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9972-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="e9972-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e9972-121">**Lista de reproducción. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="e9972-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





