---
title: External. addToBasket (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. addToBasket (método)
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- método addToBasket de Windows Media Player
- método addToBasket de Windows Media Player, clase externa
- Clase externa Windows Media Player, método addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699873"
---
# <a name="externaladdtobasket-method"></a><span data-ttu-id="95270-107">External. addToBasket (método)</span><span class="sxs-lookup"><span data-stu-id="95270-107">External.addToBasket method</span></span>

> [!Note]  
> <span data-ttu-id="95270-108">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="95270-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="95270-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="95270-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="95270-110">El método **addToBasket** agrega elementos multimedia al panel lista (también denominado cesta) en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="95270-110">The **addToBasket** method adds media items to the list pane (also called the basket) in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="95270-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95270-111">Syntax</span></span>


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="95270-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95270-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95270-113">*ViewType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95270-113">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95270-114">**Cadena** que especifica el tipo de elemento que se va a agregar al panel lista.</span><span class="sxs-lookup"><span data-stu-id="95270-114">**String** that specifies the type of item being added to the list pane.</span></span> <span data-ttu-id="95270-115">El autor de la llamada debe establecer este parámetro en una de las siguientes [constantes de ubicación de biblioteca](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="95270-115">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="95270-116">CPListID</span><span class="sxs-lookup"><span data-stu-id="95270-116">CPListID</span></span>

<span data-ttu-id="95270-117">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="95270-117">CPTrackID</span></span>

<span data-ttu-id="95270-118">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="95270-118">CPAlbumID</span></span>

<span data-ttu-id="95270-119">CPArtist</span><span class="sxs-lookup"><span data-stu-id="95270-119">CPArtist</span></span>

<span data-ttu-id="95270-120">CPGenreID</span><span class="sxs-lookup"><span data-stu-id="95270-120">CPGenreID</span></span>

<span data-ttu-id="95270-121">CPAlbumSubGenreID</span><span class="sxs-lookup"><span data-stu-id="95270-121">CPAlbumSubGenreID</span></span>

<span data-ttu-id="95270-122">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="95270-122">CPRadioID</span></span>

</dd> <dt>

<span data-ttu-id="95270-123">*Viewid controles* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95270-123">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95270-124">**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos que se van a agregar al panel lista.</span><span class="sxs-lookup"><span data-stu-id="95270-124">**String** containing the IDs, delimited by semicolons, of the items to be added to the list pane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95270-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95270-125">Return value</span></span>

<span data-ttu-id="95270-126">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="95270-126">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95270-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95270-127">Requirements</span></span>



| <span data-ttu-id="95270-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="95270-128">Requirement</span></span> | <span data-ttu-id="95270-129">Value</span><span class="sxs-lookup"><span data-stu-id="95270-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95270-130">Versión</span><span class="sxs-lookup"><span data-stu-id="95270-130">Version</span></span><br/> | <span data-ttu-id="95270-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="95270-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="95270-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95270-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="95270-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95270-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95270-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="95270-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95270-135">**ExternalObject para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="95270-135">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="95270-136">**External. basketTitle**</span><span class="sxs-lookup"><span data-stu-id="95270-136">**External.basketTitle**</span></span>](external-baskettitle.md)
</dt> </dl>

 

 





