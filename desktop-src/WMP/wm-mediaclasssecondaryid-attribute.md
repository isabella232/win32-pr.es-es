---
title: Atributo WM/MediaClassSecondaryID
description: El atributo WM/MediaClassSecondaryID es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Media Player de Windows de atributos de WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708712"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="a69e0-104">Atributo WM/MediaClassSecondaryID</span><span class="sxs-lookup"><span data-stu-id="a69e0-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="a69e0-105">El atributo **WM/MediaClassSecondaryID** es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.</span><span class="sxs-lookup"><span data-stu-id="a69e0-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a69e0-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a69e0-106">Applies To</span></span>

-   [<span data-ttu-id="a69e0-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="a69e0-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="a69e0-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="a69e0-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="a69e0-109">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="a69e0-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="a69e0-110">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="a69e0-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="a69e0-111">Reproducción</span><span class="sxs-lookup"><span data-stu-id="a69e0-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="a69e0-112">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="a69e0-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="a69e0-113">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="a69e0-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="a69e0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a69e0-114">Remarks</span></span>

<span data-ttu-id="a69e0-115">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="a69e0-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="a69e0-116">En la tabla siguiente se enumeran los GUID admitidos y sus descripciones.</span><span class="sxs-lookup"><span data-stu-id="a69e0-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="a69e0-117">GUID</span><span class="sxs-lookup"><span data-stu-id="a69e0-117">GUID</span></span>                                 | <span data-ttu-id="a69e0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a69e0-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="a69e0-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="a69e0-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="a69e0-120">El objeto multimedia representa una lista de reproducción estática.</span><span class="sxs-lookup"><span data-stu-id="a69e0-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="a69e0-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="a69e0-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="a69e0-122">El objeto multimedia representa una lista de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="a69e0-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="a69e0-123">**MediaClassSecondaryID** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="a69e0-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="a69e0-124">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMMediaClassSecondaryID.</span><span class="sxs-lookup"><span data-stu-id="a69e0-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="a69e0-125">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a69e0-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a69e0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a69e0-126">Requirements</span></span>



| <span data-ttu-id="a69e0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a69e0-127">Requirement</span></span> | <span data-ttu-id="a69e0-128">Value</span><span class="sxs-lookup"><span data-stu-id="a69e0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a69e0-129">Versión</span><span class="sxs-lookup"><span data-stu-id="a69e0-129">Version</span></span><br/> | <span data-ttu-id="a69e0-130">El elemento de foto solo se admite en Windows Media Player 10 o posterior. el elemento de radio solo se admite en Windows Media Player 9 series todos los demás elementos se admiten en Windows Media Player series 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="a69e0-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a69e0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a69e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a69e0-132">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="a69e0-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





