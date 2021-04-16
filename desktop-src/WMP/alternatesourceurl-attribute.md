---
title: Atributo AlternateSourceURL
description: El atributo AlternateSourceURL es un localizador uniforme de recursos para el elemento multimedia que actúa como alternativa a los atributos DLNASourceURI y SourceURL.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- AlternateSourceURL Media Player de Windows
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699691"
---
# <a name="alternatesourceurl-attribute"></a><span data-ttu-id="75b2a-104">Atributo AlternateSourceURL</span><span class="sxs-lookup"><span data-stu-id="75b2a-104">AlternateSourceURL Attribute</span></span>

<span data-ttu-id="75b2a-105">El atributo **AlternateSourceURL** es un localizador uniforme de recursos para el elemento multimedia que actúa como alternativa a los atributos [**DLNASourceURI**](dlnasourceuri-attribute.md) y [**SourceURL**](sourceurl-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="75b2a-105">The **AlternateSourceURL** attribute is a uniform resource locator for the media item that serves as an alternative to the [**DLNASourceURI**](dlnasourceuri-attribute.md) and [**SourceURL**](sourceurl-attribute.md) attributes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="75b2a-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="75b2a-106">Applies To</span></span>

-   [<span data-ttu-id="75b2a-107">**Elementos de audio**</span><span class="sxs-lookup"><span data-stu-id="75b2a-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="75b2a-108">**Elementos de fotografía**</span><span class="sxs-lookup"><span data-stu-id="75b2a-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="75b2a-109">**Elementos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="75b2a-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="75b2a-110">**Elementos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="75b2a-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="75b2a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75b2a-111">Remarks</span></span>

<span data-ttu-id="75b2a-112">Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="75b2a-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="75b2a-113">Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica.</span><span class="sxs-lookup"><span data-stu-id="75b2a-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="75b2a-114">Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="75b2a-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="75b2a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b2a-115">Requirements</span></span>



| <span data-ttu-id="75b2a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b2a-116">Requirement</span></span> | <span data-ttu-id="75b2a-117">Value</span><span class="sxs-lookup"><span data-stu-id="75b2a-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="75b2a-118">Versión</span><span class="sxs-lookup"><span data-stu-id="75b2a-118">Version</span></span><br/> | <span data-ttu-id="75b2a-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="75b2a-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75b2a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="75b2a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b2a-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="75b2a-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





