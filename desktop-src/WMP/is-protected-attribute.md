---
title: Is_Protected atributo)
description: El \_ atributo is protected indica si el contenido está protegido mediante administración de derechos digitales (DRM).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Is_Protected Media Player de atributos de Windows
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691088"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="4e2ca-104">\_Atributo protegido</span><span class="sxs-lookup"><span data-stu-id="4e2ca-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="4e2ca-105">El atributo **is \_ Protected** indica si el contenido está protegido mediante administración de derechos digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="4e2ca-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="4e2ca-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="4e2ca-106">Applies To</span></span>

-   [<span data-ttu-id="4e2ca-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="4e2ca-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4e2ca-108">Archivos de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="4e2ca-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="4e2ca-109">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="4e2ca-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4e2ca-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e2ca-110">Remarks</span></span>

<span data-ttu-id="4e2ca-111">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="4e2ca-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="4e2ca-112">**DigitallySecure** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="4e2ca-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="4e2ca-113">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProtected.</span><span class="sxs-lookup"><span data-stu-id="4e2ca-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="4e2ca-114">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2ca-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2ca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e2ca-115">Requirements</span></span>



| <span data-ttu-id="4e2ca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2ca-116">Requirement</span></span> | <span data-ttu-id="4e2ca-117">Value</span><span class="sxs-lookup"><span data-stu-id="4e2ca-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4e2ca-118">Versión</span><span class="sxs-lookup"><span data-stu-id="4e2ca-118">Version</span></span><br/> | <span data-ttu-id="4e2ca-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4e2ca-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e2ca-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e2ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2ca-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="4e2ca-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





