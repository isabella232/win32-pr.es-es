---
title: External. selectedItemType
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Media Player de Windows externa. selectedItemType
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698577"
---
# <a name="externalselecteditemtype"></a><span data-ttu-id="18585-105">External. selectedItemType</span><span class="sxs-lookup"><span data-stu-id="18585-105">External.selectedItemType</span></span>

> [!Note]  
> <span data-ttu-id="18585-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="18585-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="18585-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="18585-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="18585-108">La propiedad **selectedItemType** recupera el tipo del elemento multimedia seleccionado actualmente en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="18585-108">The **selectedItemType** property retrieves the type of the media item that is currently selected in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="18585-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18585-109">Syntax</span></span>

<span data-ttu-id="18585-110">Window. external. selectedItemType ()</span><span class="sxs-lookup"><span data-stu-id="18585-110">window.external.selectedItemType()</span></span>

## <a name="possible-values"></a><span data-ttu-id="18585-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="18585-111">Possible Values</span></span>

<span data-ttu-id="18585-112">Esta propiedad es una **cadena** de solo lectura que contiene una de las [constantes de ubicación](library-location-constants.md)de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="18585-112">This property is a read-only **String** that contains one of the [library location constants](library-location-constants.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18585-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18585-113">Remarks</span></span>

<span data-ttu-id="18585-114">Esta propiedad se usa en combinación con la propiedad **external. selectedItemID** .</span><span class="sxs-lookup"><span data-stu-id="18585-114">This property is used in combination with the **External.selectedItemID** property.</span></span> <span data-ttu-id="18585-115">Por ejemplo, si **selectedItemType** es igual a CPTrackID, **SELECTEDITEMID** es el identificador de la pista seleccionada. Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="18585-115">For example, if **selectedItemType** is equal to CPTrackID, then **selectedItemID** is the ID of the selected track. For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="18585-116">Algunas vistas de Windows Media Player tienen un elemento multimedia determinado que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="18585-116">Certain views in Windows Media Player have a particular media item that is selected.</span></span> <span data-ttu-id="18585-117">Por ejemplo, supongamos que la vista actual representa un álbum.</span><span class="sxs-lookup"><span data-stu-id="18585-117">For example, suppose the current view represents an album.</span></span> <span data-ttu-id="18585-118">Un álbum es un contenedor de pistas, por lo que **selectedItemType** es igual a CPTrackID y **SELECTEDITEMID** es el identificador de la pista seleccionada. Otras vistas no tienen un elemento multimedia seleccionado.</span><span class="sxs-lookup"><span data-stu-id="18585-118">An album is a container of tracks, so **selectedItemType** is equal to CPTrackID, and **selectedItemID** is the ID of the selected track. Other views do not have a selected media item.</span></span> <span data-ttu-id="18585-119">Por ejemplo, si el usuario hace clic en el nodo raíz de la tienda en línea en el control de vista de árbol, Windows Media Player muestra una página de detección proporcionada por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="18585-119">For example, if the user clicks the online store's root node in the tree-view control, Windows Media Player displays a discovery page provided by the online store.</span></span> <span data-ttu-id="18585-120">El reproductor no muestra ningún contenedor de elementos multimedia en la interfaz de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="18585-120">The Player does not display any container of media items in the Player user interface.</span></span> <span data-ttu-id="18585-121">En ese caso, **selectedItemType** es igual a UnknownLocation y **selectedItemID** es igual a la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="18585-121">In that case, **selectedItemType** is equal to UnknownLocation, and **selectedItemID** is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="18585-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18585-122">Requirements</span></span>



| <span data-ttu-id="18585-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="18585-123">Requirement</span></span> | <span data-ttu-id="18585-124">Value</span><span class="sxs-lookup"><span data-stu-id="18585-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18585-125">Versión</span><span class="sxs-lookup"><span data-stu-id="18585-125">Version</span></span><br/> | <span data-ttu-id="18585-126">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="18585-126">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="18585-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18585-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="18585-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18585-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18585-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="18585-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18585-130">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="18585-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="18585-131">**External. selectedItemID**</span><span class="sxs-lookup"><span data-stu-id="18585-131">**External.selectedItemID**</span></span>](external-selecteditemid.md)
</dt> <dt>

[<span data-ttu-id="18585-132">**Ubicación y elemento seleccionado**</span><span class="sxs-lookup"><span data-stu-id="18585-132">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





