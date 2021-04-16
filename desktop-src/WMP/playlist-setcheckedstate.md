---
title: Lista de reproducción. setCheckedState
description: El método setCheckedState especifica que se comprueba el elemento indexado de la lista de reproducción.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Windows Media Player de lista de reproducción. setCheckedState
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708208"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="5a492-104">Lista de reproducción. setCheckedState</span><span class="sxs-lookup"><span data-stu-id="5a492-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="5a492-105">El método **setCheckedState** especifica que se comprueba el elemento indexado de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5a492-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="5a492-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a492-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a492-107"><span id="item"></span><span id="ITEM"></span>*movs*</span><span class="sxs-lookup"><span data-stu-id="5a492-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="5a492-108">**Número** (**largo**) que indica el índice del elemento de lista de reproducción que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="5a492-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a492-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a492-109">Return Value</span></span>

<span data-ttu-id="5a492-110">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="5a492-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a492-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a492-111">Remarks</span></span>

<span data-ttu-id="5a492-112">Puede establecer todos los elementos en el estado activado si especifica 1 en el parámetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="5a492-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="5a492-113">Este método se ha reemplazado por **setCheckedState2**, que admite listas de reproducción anidadas.</span><span class="sxs-lookup"><span data-stu-id="5a492-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a492-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a492-114">Requirements</span></span>



| <span data-ttu-id="5a492-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a492-115">Requirement</span></span> | <span data-ttu-id="5a492-116">Value</span><span class="sxs-lookup"><span data-stu-id="5a492-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5a492-117">Versión</span><span class="sxs-lookup"><span data-stu-id="5a492-117">Version</span></span><br/> | <span data-ttu-id="5a492-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5a492-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a492-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a492-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a492-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5a492-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="5a492-121">**Lista de reproducción. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="5a492-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





