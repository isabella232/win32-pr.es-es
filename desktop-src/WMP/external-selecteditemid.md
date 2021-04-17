---
title: External. selectedItemID
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Media Player de Windows externa. selectedItemID
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698578"
---
# <a name="externalselecteditemid"></a><span data-ttu-id="7d332-105">External. selectedItemID</span><span class="sxs-lookup"><span data-stu-id="7d332-105">External.selectedItemID</span></span>

> [!Note]  
> <span data-ttu-id="7d332-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="7d332-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7d332-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="7d332-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7d332-108">La propiedad **selectedItemID** recupera el identificador del elemento multimedia seleccionado actualmente en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7d332-108">The **selectedItemID** property retrieves the identifier of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d332-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d332-109">Syntax</span></span>

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a><span data-ttu-id="7d332-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7d332-110">Possible Values</span></span>

<span data-ttu-id="7d332-111">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d332-111">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d332-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d332-112">Remarks</span></span>

<span data-ttu-id="7d332-113">Esta propiedad se usa en combinación con la propiedad [external. selectedItemType](external-selecteditemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="7d332-113">This property is used in combination with the [External.selectedItemType](external-selecteditemtype.md) property.</span></span> <span data-ttu-id="7d332-114">Por ejemplo, si **selectedItemType** es igual a CPTrackID, **SELECTEDITEMID** es el identificador de la pista seleccionada. Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="7d332-114">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="7d332-115">Algunas vistas de Windows Media Player tienen un elemento multimedia determinado que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7d332-115">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="7d332-116">Por ejemplo, supongamos que la vista actual representa un álbum.</span><span class="sxs-lookup"><span data-stu-id="7d332-116">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="7d332-117">Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **SELECTEDITEMID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7d332-117">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="7d332-118">Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Windows Media Player muestra una página de detección proporcionada por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="7d332-118">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="7d332-119">El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="7d332-119">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="7d332-120">En ese caso, **selectedItemType** es igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="7d332-120">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d332-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d332-121">Requirements</span></span>



| <span data-ttu-id="7d332-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d332-122">Requirement</span></span> | <span data-ttu-id="7d332-123">Value</span><span class="sxs-lookup"><span data-stu-id="7d332-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d332-124">Versión</span><span class="sxs-lookup"><span data-stu-id="7d332-124">Version</span></span><br/> | <span data-ttu-id="7d332-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7d332-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="7d332-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d332-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d332-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d332-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d332-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d332-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d332-129">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="7d332-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7d332-130">**External. selectedItemType**</span><span class="sxs-lookup"><span data-stu-id="7d332-130">**External.selectedItemType**</span></span>](external-selecteditemtype.md)
</dt> <dt>

[<span data-ttu-id="7d332-131">**Ubicación y elemento seleccionado**</span><span class="sxs-lookup"><span data-stu-id="7d332-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





