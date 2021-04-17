---
title: External. libraryLocationType
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Media Player de Windows externa. libraryLocationType
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698595"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="0dacf-105">External. libraryLocationType</span><span class="sxs-lookup"><span data-stu-id="0dacf-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="0dacf-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="0dacf-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0dacf-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="0dacf-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0dacf-108">La propiedad **libraryLocationType** recupera una [constante de ubicación de biblioteca](library-location-constants.md) que indica el tipo de la vista actual en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0dacf-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="0dacf-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0dacf-109">Possible Values</span></span>

<span data-ttu-id="0dacf-110">Esta propiedad es una **cadena** de solo lectura que contiene una de las constantes de ubicación de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0dacf-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dacf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dacf-111">Remarks</span></span>

<span data-ttu-id="0dacf-112">Esta propiedad funciona en combinación con la propiedad [external. libraryLocationID](external-librarylocationid.md) .</span><span class="sxs-lookup"><span data-stu-id="0dacf-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="0dacf-113">Por ejemplo, supongamos que **libraryLocationType** es igual a CPAlbumID y **libraryLocationID** es igual a 3.</span><span class="sxs-lookup"><span data-stu-id="0dacf-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="0dacf-114">Esto significa que la vista actual de Windows Media Player muestra el álbum que tiene un identificador de 3.</span><span class="sxs-lookup"><span data-stu-id="0dacf-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="0dacf-115">Para obtener más información acerca de cómo Windows Media Player caracteriza las vistas del contenido de la tienda en línea, consulte [Ubicación y elemento seleccionado](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="0dacf-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dacf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dacf-116">Requirements</span></span>



| <span data-ttu-id="0dacf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dacf-117">Requirement</span></span> | <span data-ttu-id="0dacf-118">Value</span><span class="sxs-lookup"><span data-stu-id="0dacf-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0dacf-119">Versión</span><span class="sxs-lookup"><span data-stu-id="0dacf-119">Version</span></span><br/> | <span data-ttu-id="0dacf-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0dacf-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0dacf-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0dacf-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="0dacf-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dacf-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dacf-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dacf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dacf-124">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="0dacf-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="0dacf-125">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="0dacf-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="0dacf-126">**Ubicación y elemento seleccionado**</span><span class="sxs-lookup"><span data-stu-id="0dacf-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





