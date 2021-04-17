---
title: Lista de reproducción. itemMedia
description: El atributo itemMedia recupera el objeto multimedia correspondiente al índice especificado en el elemento de lista de reproducción.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Windows Media Player de lista de reproducción. itemMedia
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660543"
---
# <a name="playlistitemmedia"></a><span data-ttu-id="2ac80-104">Lista de reproducción. itemMedia</span><span class="sxs-lookup"><span data-stu-id="2ac80-104">PLAYLIST.itemMedia</span></span>

<span data-ttu-id="2ac80-105">El atributo **itemMedia** recupera el objeto **multimedia** correspondiente al índice especificado en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="2ac80-105">The **itemMedia** attribute retrieves the **Media** object corresponding to the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a><span data-ttu-id="2ac80-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2ac80-106">Possible Values</span></span>

<span data-ttu-id="2ac80-107">Este atributo es un objeto **multimedia** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2ac80-107">This attribute is a read-only **Media** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ac80-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ac80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac80-109"><span id="index"></span><span id="INDEX"></span>*ajustar*</span><span class="sxs-lookup"><span data-stu-id="2ac80-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="2ac80-110">**Número**(**largo**) que contiene el índice de un elemento de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2ac80-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ac80-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac80-111">Remarks</span></span>

<span data-ttu-id="2ac80-112">La propiedad **itemMedia** devolverá los objetos multimedia que se expanden en el elemento de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="2ac80-112">The **itemMedia** property will return media objects that are expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="2ac80-113">Por ejemplo, si hay una lista de reproducción que contiene tres clips multimedia que no se expanden en el elemento de **lista de reproducción** , **itemMedia**(0) devolverá la lista de reproducción como el objeto multimedia.</span><span class="sxs-lookup"><span data-stu-id="2ac80-113">For example, if there is a playlist that contains three media clips that is not expanded in the **PLAYLIST** element, **itemMedia**(0) will return the playlist as the media object.</span></span> <span data-ttu-id="2ac80-114">Si se expande la lista de reproducción, **itemMedia**(0) devolverá el primer clip multimedia en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="2ac80-114">If the playlist is expanded, **itemMedia**(0) will return the first media clip in the playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac80-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ac80-115">Requirements</span></span>



| <span data-ttu-id="2ac80-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac80-116">Requirement</span></span> | <span data-ttu-id="2ac80-117">Value</span><span class="sxs-lookup"><span data-stu-id="2ac80-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2ac80-118">Versión</span><span class="sxs-lookup"><span data-stu-id="2ac80-118">Version</span></span><br/> | <span data-ttu-id="2ac80-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2ac80-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ac80-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ac80-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac80-121">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="2ac80-121">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2ac80-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2ac80-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





