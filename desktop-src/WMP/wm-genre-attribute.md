---
title: Atributo WM/Genre
description: El atributo WM/Genre es el género del contenido.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Media Player de atributos de WM/género de Windows
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708722"
---
# <a name="wmgenre-attribute"></a><span data-ttu-id="e00be-104">Atributo WM/Genre</span><span class="sxs-lookup"><span data-stu-id="e00be-104">WM/Genre Attribute</span></span>

<span data-ttu-id="e00be-105">El atributo **WM/Genre** es el género del contenido.</span><span class="sxs-lookup"><span data-stu-id="e00be-105">The **WM/Genre** attribute is the genre of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e00be-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e00be-106">Applies To</span></span>

-   [<span data-ttu-id="e00be-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="e00be-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e00be-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="e00be-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="e00be-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="e00be-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="e00be-110">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="e00be-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="e00be-111">DVDs</span><span class="sxs-lookup"><span data-stu-id="e00be-111">DVDs</span></span>](dvd-attributes.md)
-   [<span data-ttu-id="e00be-112">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="e00be-112">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="e00be-113">Reproducción</span><span class="sxs-lookup"><span data-stu-id="e00be-113">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="e00be-114">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="e00be-114">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e00be-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e00be-115">Remarks</span></span>

<span data-ttu-id="e00be-116">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="e00be-116">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="e00be-117">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="e00be-117">This attribute may have multiple values.</span></span> <span data-ttu-id="e00be-118">Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="e00be-118">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="e00be-119">**Genre** es un alias de este atributo.</span><span class="sxs-lookup"><span data-stu-id="e00be-119">**Genre** is an alias for this attribute.</span></span>

<span data-ttu-id="e00be-120">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMGenre.</span><span class="sxs-lookup"><span data-stu-id="e00be-120">The Windows Media Format SDK constant for this attribute is g\_wszWMGenre.</span></span>

<span data-ttu-id="e00be-121">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e00be-121">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00be-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00be-122">Requirements</span></span>



| <span data-ttu-id="e00be-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00be-123">Requirement</span></span> | <span data-ttu-id="e00be-124">Value</span><span class="sxs-lookup"><span data-stu-id="e00be-124">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e00be-125">Versión</span><span class="sxs-lookup"><span data-stu-id="e00be-125">Version</span></span><br/> | <span data-ttu-id="e00be-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e00be-126">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e00be-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="e00be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00be-128">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="e00be-128">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="e00be-129">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="e00be-129">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





