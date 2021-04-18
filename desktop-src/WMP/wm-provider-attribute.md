---
title: Atributo WM/proveedor
description: El atributo WM/Provider es el nombre del proveedor de los valores de atributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Media Player de Windows de atributo de WM/proveedor
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718743"
---
# <a name="wmprovider-attribute"></a><span data-ttu-id="78f58-104">Atributo WM/proveedor</span><span class="sxs-lookup"><span data-stu-id="78f58-104">WM/Provider Attribute</span></span>

<span data-ttu-id="78f58-105">El atributo **WM/Provider** es el nombre del proveedor de los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="78f58-105">The **WM/Provider** attribute is the name of the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="78f58-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="78f58-106">Applies To</span></span>

-   [<span data-ttu-id="78f58-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="78f58-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="78f58-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="78f58-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="78f58-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="78f58-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="78f58-110">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="78f58-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="78f58-111">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="78f58-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="78f58-112">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="78f58-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="78f58-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78f58-113">Remarks</span></span>

<span data-ttu-id="78f58-114">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="78f58-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="78f58-115">**Metadatasource** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="78f58-115">**MetadataSource** is an alias for this attribute.</span></span>

<span data-ttu-id="78f58-116">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProvider.</span><span class="sxs-lookup"><span data-stu-id="78f58-116">The Windows Media Format SDK constant for this attribute is g\_wszWMProvider.</span></span>

<span data-ttu-id="78f58-117">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="78f58-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f58-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78f58-118">Requirements</span></span>



| <span data-ttu-id="78f58-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f58-119">Requirement</span></span> | <span data-ttu-id="78f58-120">Value</span><span class="sxs-lookup"><span data-stu-id="78f58-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78f58-121">Versión</span><span class="sxs-lookup"><span data-stu-id="78f58-121">Version</span></span><br/> | <span data-ttu-id="78f58-122">Windows Media Player 9 series o posterior (el elemento de fotografía solo se admite en Windows Media Player 10 o posterior)</span><span class="sxs-lookup"><span data-stu-id="78f58-122">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78f58-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="78f58-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f58-124">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="78f58-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





