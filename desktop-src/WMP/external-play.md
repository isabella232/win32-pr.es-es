---
title: External. Play (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método play indica a Windows Media Player que reproduzca un conjunto de elementos multimedia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- método play Windows Media Player
- método play Windows Media Player, clase externa
- Clase externa Windows Media Player, método play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698581"
---
# <a name="externalplay-method"></a><span data-ttu-id="f86d4-108">External. Play (método)</span><span class="sxs-lookup"><span data-stu-id="f86d4-108">External.play method</span></span>

> [!Note]  
> <span data-ttu-id="f86d4-109">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="f86d4-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f86d4-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f86d4-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f86d4-111">El método **Play** indica a Windows Media Player que reproduzca un conjunto de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="f86d4-111">The **play** method instructs Windows Media Player to play a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86d4-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f86d4-112">Syntax</span></span>


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a><span data-ttu-id="f86d4-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f86d4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f86d4-114">*LibraryLocationType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f86d4-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f86d4-115">Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de los elementos multimedia que se van a reproducir.</span><span class="sxs-lookup"><span data-stu-id="f86d4-115">A [library location constant](library-location-constants.md) that specifies the type of the media items to be played.</span></span> <span data-ttu-id="f86d4-116">Por ejemplo, CPAlbumID especifica que se reproducirán uno o más álbumes.</span><span class="sxs-lookup"><span data-stu-id="f86d4-116">For example, CPAlbumID specifies that one or more albums are to be played.</span></span>

</dd> <dt>

<span data-ttu-id="f86d4-117">*LibraryLocationIDs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f86d4-117">*LibraryLocationIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f86d4-118">**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se van a reproducir.</span><span class="sxs-lookup"><span data-stu-id="f86d4-118">**String** containing the identifiers, delimited by semicolons, of the media items to be played.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f86d4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f86d4-119">Return value</span></span>

<span data-ttu-id="f86d4-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f86d4-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f86d4-121">Requirements</span></span>



| <span data-ttu-id="f86d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f86d4-122">Requirement</span></span> | <span data-ttu-id="f86d4-123">Value</span><span class="sxs-lookup"><span data-stu-id="f86d4-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f86d4-124">Versión</span><span class="sxs-lookup"><span data-stu-id="f86d4-124">Version</span></span><br/> | <span data-ttu-id="f86d4-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="f86d4-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f86d4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f86d4-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f86d4-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f86d4-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86d4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f86d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86d4-129">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f86d4-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





