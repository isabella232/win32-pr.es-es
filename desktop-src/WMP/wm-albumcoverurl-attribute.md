---
title: Atributo WM/AlbumCoverURL
description: El atributo WM/AlbumCoverURL es el localizador uniforme de recursos (URL) para carátulas de álbum o una imagen en miniatura.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- Media Player de Windows de atributos de WM/AlbumCoverURL
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708743"
---
# <a name="wmalbumcoverurl-attribute"></a><span data-ttu-id="7a2ab-104">Atributo WM/AlbumCoverURL</span><span class="sxs-lookup"><span data-stu-id="7a2ab-104">WM/AlbumCoverURL Attribute</span></span>

<span data-ttu-id="7a2ab-105">El atributo **WM/AlbumCoverURL** es el localizador uniforme de recursos (URL) para carátulas de álbum o una imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-105">The **WM/AlbumCoverURL** attribute is the uniform resource locator (URL) for album art or a thumbnail image.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7a2ab-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="7a2ab-106">Applies To</span></span>

-   [<span data-ttu-id="7a2ab-107">**Elementos de audio**</span><span class="sxs-lookup"><span data-stu-id="7a2ab-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7a2ab-108">**Elementos de fotografía**</span><span class="sxs-lookup"><span data-stu-id="7a2ab-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="7a2ab-109">**Elementos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="7a2ab-109">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7a2ab-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a2ab-110">Remarks</span></span>

<span data-ttu-id="7a2ab-111">Para un elemento de audio, este atributo es la dirección URL de la carátula del álbum.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-111">For an audio item, this attribute is the URL of the album art.</span></span> <span data-ttu-id="7a2ab-112">Para un elemento de foto o vídeo, este atributo es la dirección URL de una imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-112">For a photo or video item, this attribute is the URL of a thumbnail image.</span></span>

<span data-ttu-id="7a2ab-113">Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="7a2ab-114">Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="7a2ab-115">Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="7a2ab-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2ab-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2ab-116">Requirements</span></span>



| <span data-ttu-id="7a2ab-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2ab-117">Requirement</span></span> | <span data-ttu-id="7a2ab-118">Value</span><span class="sxs-lookup"><span data-stu-id="7a2ab-118">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="7a2ab-119">Versión</span><span class="sxs-lookup"><span data-stu-id="7a2ab-119">Version</span></span><br/> | <span data-ttu-id="7a2ab-120">Windows Media Player 12 o posterior.</span><span class="sxs-lookup"><span data-stu-id="7a2ab-120">Windows Media Player 12 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a2ab-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a2ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2ab-122">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="7a2ab-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





