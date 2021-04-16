---
title: External. Buy (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método Buy inicia la compra de un conjunto de elementos multimedia.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- comprar método Media Player Windows
- método Buy Windows Media Player, clase externa
- Clase externa Windows Media Player, método Buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699763"
---
# <a name="externalbuy-method"></a><span data-ttu-id="0c772-108">External. Buy (método)</span><span class="sxs-lookup"><span data-stu-id="0c772-108">External.buy method</span></span>

> [!Note]  
> <span data-ttu-id="0c772-109">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="0c772-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0c772-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="0c772-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0c772-111">El método **Buy** inicia la compra de un conjunto de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="0c772-111">The **buy** method initiates the purchase of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c772-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c772-112">Syntax</span></span>


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a><span data-ttu-id="0c772-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c772-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c772-114">*ViewType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c772-114">*ViewType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c772-115">**Cadena** que especifica el tipo de elemento que se va a adquirir.</span><span class="sxs-lookup"><span data-stu-id="0c772-115">**String** that specifies the type of item to be purchased.</span></span> <span data-ttu-id="0c772-116">El autor de la llamada debe establecer este parámetro en una de las siguientes [constantes de ubicación de biblioteca](library-location-constants.md):</span><span class="sxs-lookup"><span data-stu-id="0c772-116">The caller must set this parameter to one of the following [library location constants](library-location-constants.md):</span></span>

<span data-ttu-id="0c772-117">CPListID</span><span class="sxs-lookup"><span data-stu-id="0c772-117">CPListID</span></span>

<span data-ttu-id="0c772-118">CPTrackID</span><span class="sxs-lookup"><span data-stu-id="0c772-118">CPTrackID</span></span>

<span data-ttu-id="0c772-119">CPAlbumID</span><span class="sxs-lookup"><span data-stu-id="0c772-119">CPAlbumID</span></span>

</dd> <dt>

<span data-ttu-id="0c772-120">*Viewid controles* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0c772-120">*ViewIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c772-121">**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos que se van a adquirir.</span><span class="sxs-lookup"><span data-stu-id="0c772-121">**String** containing the IDs, delimited by semicolons, of the items to be purchased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c772-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c772-122">Return value</span></span>

<span data-ttu-id="0c772-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0c772-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c772-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c772-124">Requirements</span></span>



| <span data-ttu-id="0c772-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c772-125">Requirement</span></span> | <span data-ttu-id="0c772-126">Value</span><span class="sxs-lookup"><span data-stu-id="0c772-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c772-127">Versión</span><span class="sxs-lookup"><span data-stu-id="0c772-127">Version</span></span><br/> | <span data-ttu-id="0c772-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0c772-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0c772-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c772-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c772-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c772-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c772-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c772-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c772-132">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="0c772-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0c772-133">**External. download**</span><span class="sxs-lookup"><span data-stu-id="0c772-133">**External.download**</span></span>](external-download.md)
</dt> <dt>

[<span data-ttu-id="0c772-134">**IWMPContentPartner:: Buy**</span><span class="sxs-lookup"><span data-stu-id="0c772-134">**IWMPContentPartner::Buy**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[<span data-ttu-id="0c772-135">**Compra de contenido multimedia**</span><span class="sxs-lookup"><span data-stu-id="0c772-135">**Purchasing Media Content**</span></span>](purchasing-media-content.md)
</dt> </dl>

 

 





