---
title: Lista de reproducción. setSelectedState2
description: El método setSelectedState2 establece el estado seleccionado del elemento con el índice especificado en el elemento de lista de reproducción.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Windows Media Player de lista de reproducción. setSelectedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661413"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="7c041-104">Lista de reproducción. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="7c041-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="7c041-105">El método **setSelectedState2** establece el estado seleccionado del elemento con el índice especificado en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="7c041-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="7c041-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c041-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c041-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="7c041-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="7c041-108">**Número** (**largo**) que indica el índice de un elemento de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="7c041-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="7c041-109"><span id="selected"></span><span id="SELECTED"></span>*seleccionadas*</span><span class="sxs-lookup"><span data-stu-id="7c041-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="7c041-110">**Valor booleano** que indica si el elemento especificado se va a seleccionar (true) o si no se ha seleccionado (false).</span><span class="sxs-lookup"><span data-stu-id="7c041-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c041-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c041-111">Return Value</span></span>

<span data-ttu-id="7c041-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7c041-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c041-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c041-113">Remarks</span></span>

<span data-ttu-id="7c041-114">Este método puede trabajar con listas de reproducción anidadas y reemplaza el método **setSelectedState** que no puede.</span><span class="sxs-lookup"><span data-stu-id="7c041-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="7c041-115">Puede establecer todos los elementos en el estado solicitado especificando 1 en el parámetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="7c041-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c041-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c041-116">Requirements</span></span>



| <span data-ttu-id="7c041-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c041-117">Requirement</span></span> | <span data-ttu-id="7c041-118">Value</span><span class="sxs-lookup"><span data-stu-id="7c041-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7c041-119">Versión</span><span class="sxs-lookup"><span data-stu-id="7c041-119">Version</span></span><br/> | <span data-ttu-id="7c041-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7c041-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c041-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c041-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c041-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="7c041-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="7c041-123">**Lista de reproducción. setSelectedState**</span><span class="sxs-lookup"><span data-stu-id="7c041-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





