---
description: Contiene las entradas de la paleta para un tipo de medio de vídeo. Use este atributo para los formatos de vídeo de paleta, como RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dcfc596ae463cf642cc462da1c73dc641356d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648319"
---
# <a name="mf_mt_palette-attribute"></a><span data-ttu-id="6d290-104">\_Atributo MF MT \_ Palette</span><span class="sxs-lookup"><span data-stu-id="6d290-104">MF\_MT\_PALETTE attribute</span></span>

<span data-ttu-id="6d290-105">Contiene las entradas de la paleta para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6d290-105">Contains the palette entries for a video media type.</span></span> <span data-ttu-id="6d290-106">Use este atributo para los formatos de vídeo de paleta, como RGB 8.</span><span class="sxs-lookup"><span data-stu-id="6d290-106">Use this attribute for palettized video formats, such as RGB 8.</span></span>

## <a name="data-type"></a><span data-ttu-id="6d290-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6d290-107">Data type</span></span>

<span data-ttu-id="6d290-108">Byte array</span><span class="sxs-lookup"><span data-stu-id="6d290-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6d290-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d290-109">Remarks</span></span>

<span data-ttu-id="6d290-110">Los datos del atributo son una matriz de uniones [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) .</span><span class="sxs-lookup"><span data-stu-id="6d290-110">The attribute data is an array of [**MFPaletteEntry**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry) unions.</span></span>

<span data-ttu-id="6d290-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6d290-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d290-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d290-112">Requirements</span></span>



| <span data-ttu-id="6d290-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d290-113">Requirement</span></span> | <span data-ttu-id="6d290-114">Value</span><span class="sxs-lookup"><span data-stu-id="6d290-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d290-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d290-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6d290-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6d290-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6d290-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d290-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6d290-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6d290-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6d290-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d290-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d290-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d290-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d290-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d290-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d290-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6d290-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6d290-123">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6d290-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6d290-124">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="6d290-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6d290-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6d290-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6d290-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="6d290-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




