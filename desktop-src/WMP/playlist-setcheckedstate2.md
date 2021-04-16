---
title: Lista de reproducción. setCheckedState2
description: El método setCheckedState2 establece el estado de activación del elemento con el índice especificado en el elemento de lista de reproducción.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Windows Media Player de lista de reproducción. setCheckedState2
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708213"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="9521e-104">Lista de reproducción. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="9521e-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="9521e-105">El método **setCheckedState2** establece el estado de activación del elemento con el índice especificado en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="9521e-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="9521e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9521e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9521e-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="9521e-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="9521e-108">**Número** (**largo**) que indica el índice del elemento de lista de reproducción que se va a activar o desactivar.</span><span class="sxs-lookup"><span data-stu-id="9521e-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="9521e-109"><span id="checked"></span><span id="CHECKED"></span>*incorpora*</span><span class="sxs-lookup"><span data-stu-id="9521e-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="9521e-110">**Valor booleano** que indica si el elemento especificado debe comprobarse (true) o desactivado (false).</span><span class="sxs-lookup"><span data-stu-id="9521e-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9521e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9521e-111">Return Value</span></span>

<span data-ttu-id="9521e-112">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="9521e-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9521e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9521e-113">Remarks</span></span>

<span data-ttu-id="9521e-114">Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **setCheckedState** , que no puede.</span><span class="sxs-lookup"><span data-stu-id="9521e-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="9521e-115">Puede establecer todos los elementos en el estado solicitado especificando 1 en el parámetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="9521e-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9521e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9521e-116">Requirements</span></span>



| <span data-ttu-id="9521e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9521e-117">Requirement</span></span> | <span data-ttu-id="9521e-118">Value</span><span class="sxs-lookup"><span data-stu-id="9521e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9521e-119">Versión</span><span class="sxs-lookup"><span data-stu-id="9521e-119">Version</span></span><br/> | <span data-ttu-id="9521e-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9521e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9521e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9521e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9521e-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="9521e-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="9521e-123">**Lista de reproducción. setCheckedState**</span><span class="sxs-lookup"><span data-stu-id="9521e-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





