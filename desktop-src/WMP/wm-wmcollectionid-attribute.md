---
title: Atributo WM/WMCollectionID
description: El atributo WM/WMCollectionID es un GUID que identifica la colección a la que pertenece el elemento.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Media Player de Windows de atributos de WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718855"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="11817-104">Atributo WM/WMCollectionID</span><span class="sxs-lookup"><span data-stu-id="11817-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="11817-105">El atributo **WM/WMCollectionID** es un GUID que identifica la colección a la que pertenece el elemento.</span><span class="sxs-lookup"><span data-stu-id="11817-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="11817-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="11817-106">Applies To</span></span>

-   [<span data-ttu-id="11817-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="11817-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="11817-108">Listas de reproducción de CD</span><span class="sxs-lookup"><span data-stu-id="11817-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="11817-109">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="11817-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="11817-110">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="11817-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="11817-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11817-111">Remarks</span></span>

<span data-ttu-id="11817-112">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="11817-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="11817-113">**WMCollectionID** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="11817-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="11817-114">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMCollectionID.</span><span class="sxs-lookup"><span data-stu-id="11817-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="11817-115">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="11817-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="11817-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11817-116">Requirements</span></span>



| <span data-ttu-id="11817-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="11817-117">Requirement</span></span> | <span data-ttu-id="11817-118">Value</span><span class="sxs-lookup"><span data-stu-id="11817-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="11817-119">Versión</span><span class="sxs-lookup"><span data-stu-id="11817-119">Version</span></span><br/> | <span data-ttu-id="11817-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="11817-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11817-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="11817-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11817-122">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="11817-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





