---
title: Lista de reproducción. setSelectedState
description: El método setSelectedState especifica que el elemento indexado de la lista de reproducción está seleccionado.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Windows Media Player de lista de reproducción. setSelectedState
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709263"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="d17cd-104">Lista de reproducción. setSelectedState</span><span class="sxs-lookup"><span data-stu-id="d17cd-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="d17cd-105">El método **setSelectedState** especifica que el elemento indexado de la lista de reproducción está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d17cd-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="d17cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d17cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17cd-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="d17cd-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="d17cd-108">**Número** (**largo**) que indica el índice de un elemento de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="d17cd-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d17cd-109">Return Value</span></span>

<span data-ttu-id="d17cd-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d17cd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d17cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d17cd-111">Remarks</span></span>

<span data-ttu-id="d17cd-112">Puede establecer todos los elementos en el estado seleccionado especificando 1 en el parámetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="d17cd-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="d17cd-113">Este método se ha reemplazado por **setSelectedState2**, que admite listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="d17cd-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="d17cd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d17cd-114">Requirements</span></span>



| <span data-ttu-id="d17cd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d17cd-115">Requirement</span></span> | <span data-ttu-id="d17cd-116">Value</span><span class="sxs-lookup"><span data-stu-id="d17cd-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d17cd-117">Versión</span><span class="sxs-lookup"><span data-stu-id="d17cd-117">Version</span></span><br/> | <span data-ttu-id="d17cd-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d17cd-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d17cd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d17cd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17cd-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="d17cd-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="d17cd-121">**Lista de reproducción. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="d17cd-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





