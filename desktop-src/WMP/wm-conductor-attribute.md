---
title: Atributo WM/conductor
description: El atributo WM/conductores es el nombre del conductor de la música.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Windows atributo de WM/conductores Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708734"
---
# <a name="wmconductor-attribute"></a><span data-ttu-id="28d59-104">Atributo WM/conductor</span><span class="sxs-lookup"><span data-stu-id="28d59-104">WM/Conductor Attribute</span></span>

<span data-ttu-id="28d59-105">El atributo **WM/conductores** es el nombre del conductor de la música.</span><span class="sxs-lookup"><span data-stu-id="28d59-105">The **WM/Conductor** attribute is the name of the conductor of the music.</span></span>

## <a name="applies-to"></a><span data-ttu-id="28d59-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="28d59-106">Applies To</span></span>

-   [<span data-ttu-id="28d59-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="28d59-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="28d59-108">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="28d59-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="28d59-109">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="28d59-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="28d59-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28d59-110">Remarks</span></span>

<span data-ttu-id="28d59-111">Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="28d59-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="28d59-112">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="28d59-112">This attribute may have multiple values.</span></span> <span data-ttu-id="28d59-113">Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="28d59-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="28d59-114">**Conductor** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="28d59-114">**Conductor** is an alias for this attribute.</span></span>

<span data-ttu-id="28d59-115">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMConductor.</span><span class="sxs-lookup"><span data-stu-id="28d59-115">The Windows Media Format SDK constant for this attribute is g\_wszWMConductor.</span></span>

<span data-ttu-id="28d59-116">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="28d59-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d59-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d59-117">Requirements</span></span>



| <span data-ttu-id="28d59-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d59-118">Requirement</span></span> | <span data-ttu-id="28d59-119">Value</span><span class="sxs-lookup"><span data-stu-id="28d59-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="28d59-120">Versión</span><span class="sxs-lookup"><span data-stu-id="28d59-120">Version</span></span><br/> | <span data-ttu-id="28d59-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="28d59-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d59-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="28d59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d59-123">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="28d59-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="28d59-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="28d59-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





