---
description: Define la abertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715249"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a><span data-ttu-id="59826-103">\_Atributo de \_ \_ abertura de pantalla mínima MF MT \_</span><span class="sxs-lookup"><span data-stu-id="59826-103">MF\_MT\_MINIMUM\_DISPLAY\_APERTURE attribute</span></span>

<span data-ttu-id="59826-104">Define la abertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.</span><span class="sxs-lookup"><span data-stu-id="59826-104">Defines the display aperture, which is the region of a video frame that contains valid image data.</span></span>

## <a name="data-type"></a><span data-ttu-id="59826-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="59826-105">Data type</span></span>

<span data-ttu-id="59826-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="59826-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="59826-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59826-107">Remarks</span></span>

<span data-ttu-id="59826-108">El valor del atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="59826-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="59826-109">La abertura de pantalla mínima es la región que contiene la parte válida de la señal.</span><span class="sxs-lookup"><span data-stu-id="59826-109">The minimum display aperture is the region that contains the valid portion of the signal.</span></span> <span data-ttu-id="59826-110">Los píxeles que están fuera de la abertura contienen datos no válidos y no se deben mostrar.</span><span class="sxs-lookup"><span data-stu-id="59826-110">The pixels outside the aperture contain invalid data and should not be displayed.</span></span>

<span data-ttu-id="59826-111">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="59826-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="59826-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59826-112">Requirements</span></span>



| <span data-ttu-id="59826-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="59826-113">Requirement</span></span> | <span data-ttu-id="59826-114">Value</span><span class="sxs-lookup"><span data-stu-id="59826-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59826-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59826-115">Minimum supported client</span></span><br/> | <span data-ttu-id="59826-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="59826-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="59826-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="59826-117">Minimum supported server</span></span><br/> | <span data-ttu-id="59826-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="59826-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="59826-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59826-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="59826-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="59826-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59826-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="59826-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59826-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59826-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59826-123">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="59826-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="59826-124">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="59826-124">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="59826-125">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="59826-125">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="59826-126">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="59826-126">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="59826-127">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="59826-127">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="59826-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="59826-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="59826-129">**\_ \_ apertura geométrica de MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="59826-129">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="59826-130">**\_apertura de \_ \_ análisis panorámico MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="59826-130">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




