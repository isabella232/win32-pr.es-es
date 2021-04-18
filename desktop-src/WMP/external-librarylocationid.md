---
title: External. libraryLocationID
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Media Player de Windows externa. libraryLocationID
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698596"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="fb6cd-105">External. libraryLocationID</span><span class="sxs-lookup"><span data-stu-id="fb6cd-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="fb6cd-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fb6cd-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fb6cd-108">La propiedad **libraryLocationID** recupera el identificador del elemento multimedia específico que se muestra actualmente en la vista del reproductor.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="fb6cd-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="fb6cd-109">Possible Values</span></span>

<span data-ttu-id="fb6cd-110">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb6cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb6cd-111">Remarks</span></span>

<span data-ttu-id="fb6cd-112">Esta propiedad funciona en combinación con la propiedad [external. libraryLocationType](external-librarylocationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6cd-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="fb6cd-113">Por ejemplo, supongamos que **libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es igual a 3.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="fb6cd-114">Esto significa que la vista actual de Windows Media Player muestra el álbum que tiene un identificador de 3.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="fb6cd-115">Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="fb6cd-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="fb6cd-116">Algunas vistas de Windows Media Player están asociadas a un elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="fb6cd-117">Por ejemplo, si la vista actual representa un álbum individual, **libraryLocationType** es igual a CPAlbumID y **LIBRARYLOCATIONID** es el identificador del álbum.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="fb6cd-118">Otras vistas no están asociadas a ningún elemento multimedia determinado.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="fb6cd-119">Por ejemplo, si la vista actual representa todos los álbumes, **libraryLocationType** es igual a AllCPAlbumIDs, pero no hay ningún valor significativo que se pueda asignar a **libraryLocationID**.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="fb6cd-120">En los casos en los que la propiedad **libraryLocationID** no tiene ningún valor significativo, es igual a la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6cd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6cd-121">Requirements</span></span>



| <span data-ttu-id="fb6cd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6cd-122">Requirement</span></span> | <span data-ttu-id="fb6cd-123">Value</span><span class="sxs-lookup"><span data-stu-id="fb6cd-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6cd-124">Versión</span><span class="sxs-lookup"><span data-stu-id="fb6cd-124">Version</span></span><br/> | <span data-ttu-id="fb6cd-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="fb6cd-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb6cd-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb6cd-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb6cd-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6cd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb6cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6cd-129">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fb6cd-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fb6cd-130">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="fb6cd-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="fb6cd-131">**Ubicación y elemento seleccionado**</span><span class="sxs-lookup"><span data-stu-id="fb6cd-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





