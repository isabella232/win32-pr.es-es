---
description: Define la abertura Pan/Scan, que es la 4&\# 215; 3 región del vídeo que se debe mostrar en el modo Pan/Scan.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: MF_MT_PAN_SCAN_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696640"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a><span data-ttu-id="f732a-103">MF \_ MT \_ pan \_ scan \_ abertura atributo</span><span class="sxs-lookup"><span data-stu-id="f732a-103">MF\_MT\_PAN\_SCAN\_APERTURE attribute</span></span>

<span data-ttu-id="f732a-104">Define la abertura Pan/Scan, que es la región de vídeo de 4 × 3 que se debe mostrar en el modo Pan/Scan.</span><span class="sxs-lookup"><span data-stu-id="f732a-104">Defines the pan/scan aperture, which is the 4×3 region of video that should be displayed in pan/scan mode.</span></span>

## <a name="data-type"></a><span data-ttu-id="f732a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f732a-105">Data type</span></span>

<span data-ttu-id="f732a-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="f732a-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="f732a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f732a-107">Remarks</span></span>

<span data-ttu-id="f732a-108">El valor del atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .</span><span class="sxs-lookup"><span data-stu-id="f732a-108">The attribute value is an [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) structure.</span></span>

<span data-ttu-id="f732a-109">Este atributo se usa para recortar el vídeo de pantalla panorámica a una relación de aspecto de 4:3.</span><span class="sxs-lookup"><span data-stu-id="f732a-109">This attribute is used to crop widescreen video to a 4:3 aspect ratio.</span></span> <span data-ttu-id="f732a-110">La abertura Pan/Scan solo se usa en el modo Pan/Scan, que se habilita estableciendo el atributo [**MF \_ MT \_ pan \_ scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="f732a-110">The pan/scan aperture is used only in pan/scan mode, which is enabled by setting the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="f732a-111">Si el modo de desplazamiento/exploración no está habilitado, use la abertura de la pantalla, especificada por el atributo [**MF \_ MT \_ Minimum \_ Display \_ abertura**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f732a-111">If pan/scan mode is not enabled, use the display aperture, specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="f732a-112">Si no se establece este atributo, se supone que la abertura de exploración o pan es todo el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f732a-112">If this attribute is not set, the pan/scan aperture is assumed to be the entire video frame.</span></span>

<span data-ttu-id="f732a-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f732a-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f732a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f732a-114">Requirements</span></span>



| <span data-ttu-id="f732a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f732a-115">Requirement</span></span> | <span data-ttu-id="f732a-116">Value</span><span class="sxs-lookup"><span data-stu-id="f732a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f732a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f732a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f732a-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f732a-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f732a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f732a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f732a-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f732a-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f732a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f732a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f732a-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f732a-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f732a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f732a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f732a-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f732a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f732a-125">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="f732a-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="f732a-126">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="f732a-126">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> <dt>

[<span data-ttu-id="f732a-127">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="f732a-127">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="f732a-128">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="f732a-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="f732a-129">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="f732a-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="f732a-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="f732a-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f732a-131">**\_ \_ apertura geométrica de MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="f732a-131">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="f732a-132">**\_ \_ apertura mínima de \_ pantalla MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="f732a-132">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="f732a-133">**examen de pan de MF \_ MT \_ \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="f732a-133">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




