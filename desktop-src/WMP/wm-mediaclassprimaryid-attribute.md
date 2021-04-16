---
title: Atributo WM/MediaClassPrimaryID
description: El atributo WM/MediaClassPrimaryID es un GUID que especifica una de las clases de medios principales música, audio no musical, vídeo u otros.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Media Player de Windows de atributos de WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708713"
---
# <a name="wmmediaclassprimaryid-attribute"></a><span data-ttu-id="a57cb-104">Atributo WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="a57cb-104">WM/MediaClassPrimaryID Attribute</span></span>

<span data-ttu-id="a57cb-105">El atributo **WM/MediaClassPrimaryID** es un GUID que especifica una de las clases de medios principales: música, audio no musical, vídeo u otros.</span><span class="sxs-lookup"><span data-stu-id="a57cb-105">The **WM/MediaClassPrimaryID** attribute is a GUID specifying one of the primary media classes: music, non-music audio, video, or other.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a57cb-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a57cb-106">Applies To</span></span>

-   [<span data-ttu-id="a57cb-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="a57cb-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="a57cb-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="a57cb-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="a57cb-109">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="a57cb-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="a57cb-110">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="a57cb-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="a57cb-111">Reproducción</span><span class="sxs-lookup"><span data-stu-id="a57cb-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="a57cb-112">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="a57cb-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="a57cb-113">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="a57cb-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="a57cb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a57cb-114">Remarks</span></span>

<span data-ttu-id="a57cb-115">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="a57cb-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="a57cb-116">**MediaClassPrimaryID** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="a57cb-116">**MediaClassPrimaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="a57cb-117">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMMediaClassPrimaryID.</span><span class="sxs-lookup"><span data-stu-id="a57cb-117">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassPrimaryID.</span></span>

<span data-ttu-id="a57cb-118">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a57cb-118">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a57cb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a57cb-119">Requirements</span></span>



| <span data-ttu-id="a57cb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a57cb-120">Requirement</span></span> | <span data-ttu-id="a57cb-121">Value</span><span class="sxs-lookup"><span data-stu-id="a57cb-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57cb-122">Versión</span><span class="sxs-lookup"><span data-stu-id="a57cb-122">Version</span></span><br/> | <span data-ttu-id="a57cb-123">Windows Media Player 9 series o posterior (el elemento de fotografía solo se admite en Windows Media Player 10 o posterior)</span><span class="sxs-lookup"><span data-stu-id="a57cb-123">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a57cb-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a57cb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57cb-125">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="a57cb-125">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





