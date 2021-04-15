---
title: Lista de reproducción. getNextCheckedItem2
description: El método getNextCheckedItem2 recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Windows Media Player de lista de reproducción. getNextCheckedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708232"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="a76de-104">Lista de reproducción. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="a76de-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="a76de-105">El método **getNextCheckedItem2** recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a76de-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="a76de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a76de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a76de-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="a76de-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="a76de-108">**Número** (**largo**) que indica el índice del elemento que se va a buscar después de.</span><span class="sxs-lookup"><span data-stu-id="a76de-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a76de-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a76de-109">Return Value</span></span>

<span data-ttu-id="a76de-110">Este método devuelve un **número** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a76de-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a76de-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a76de-111">Remarks</span></span>

<span data-ttu-id="a76de-112">Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **getNextCheckedItem** , que no puede.</span><span class="sxs-lookup"><span data-stu-id="a76de-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="a76de-113">Pase 1 en el parámetro *Item* para buscar el primer elemento activado.</span><span class="sxs-lookup"><span data-stu-id="a76de-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="a76de-114">Cuando no hay más elementos marcados, este método devuelve 1.</span><span class="sxs-lookup"><span data-stu-id="a76de-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a76de-115">Requirements</span></span>



| <span data-ttu-id="a76de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a76de-116">Requirement</span></span> | <span data-ttu-id="a76de-117">Value</span><span class="sxs-lookup"><span data-stu-id="a76de-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="a76de-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a76de-118">Version</span></span><br/> | <span data-ttu-id="a76de-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a76de-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a76de-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a76de-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76de-121">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="a76de-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="a76de-122">**Lista de reproducción. getNextCheckedItem**</span><span class="sxs-lookup"><span data-stu-id="a76de-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





