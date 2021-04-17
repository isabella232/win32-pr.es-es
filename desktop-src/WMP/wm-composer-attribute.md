---
title: Atributo WM/compositor
description: El atributo WM/compositor es el nombre del compositor de la música.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Media Player de Windows de atributo de WM/compositor
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708735"
---
# <a name="wmcomposer-attribute"></a><span data-ttu-id="4991f-104">Atributo WM/compositor</span><span class="sxs-lookup"><span data-stu-id="4991f-104">WM/Composer Attribute</span></span>

<span data-ttu-id="4991f-105">El atributo **WM/compositor** es el nombre del compositor de la música.</span><span class="sxs-lookup"><span data-stu-id="4991f-105">The **WM/Composer** attribute is the name of the composer of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4991f-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4991f-106">Applies To</span></span>

-   [<span data-ttu-id="4991f-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="4991f-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4991f-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="4991f-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="4991f-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="4991f-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="4991f-110">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="4991f-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4991f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4991f-111">Remarks</span></span>

<span data-ttu-id="4991f-112">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="4991f-112">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="4991f-113">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="4991f-113">This attribute may have multiple values.</span></span> <span data-ttu-id="4991f-114">Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="4991f-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="4991f-115">**Composer** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="4991f-115">**Composer** is an alias for this attribute.</span></span>

<span data-ttu-id="4991f-116">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMComposer.</span><span class="sxs-lookup"><span data-stu-id="4991f-116">The Windows Media Format SDK constant for this attribute is g\_wszWMComposer.</span></span>

<span data-ttu-id="4991f-117">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4991f-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4991f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4991f-118">Requirements</span></span>



| <span data-ttu-id="4991f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4991f-119">Requirement</span></span> | <span data-ttu-id="4991f-120">Value</span><span class="sxs-lookup"><span data-stu-id="4991f-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4991f-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4991f-121">Version</span></span><br/> | <span data-ttu-id="4991f-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4991f-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4991f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4991f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4991f-124">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="4991f-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="4991f-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="4991f-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





