---
description: La velocidad de fotogramas máxima que admite un dispositivo de captura de vídeo, en fotogramas por segundo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: MF_MT_FRAME_RATE_RANGE_MAX atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001501"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a><span data-ttu-id="fd378-103">\_Atributo de \_ intervalo de velocidad de fotogramas MF MT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fd378-103">MF\_MT\_FRAME\_RATE\_RANGE\_MAX attribute</span></span>

<span data-ttu-id="fd378-104">La velocidad de fotogramas máxima que admite un dispositivo de captura de vídeo, en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="fd378-104">The maximum frame rate that is supported by a video capture device, in frames per second.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd378-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fd378-105">Data type</span></span>

<span data-ttu-id="fd378-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fd378-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="fd378-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="fd378-107">Get/set</span></span>

<span data-ttu-id="fd378-108">Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="fd378-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="fd378-109">Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="fd378-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd378-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd378-110">Remarks</span></span>

<span data-ttu-id="fd378-111">La velocidad de fotogramas se expresa como una proporción.</span><span class="sxs-lookup"><span data-stu-id="fd378-111">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="fd378-112">Los 32 superiores del valor del atributo contienen el numerador, y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="fd378-112">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="fd378-113">Por ejemplo, si la velocidad de fotogramas es de 30 fotogramas por segundo (FPS), la relación es 30/1.</span><span class="sxs-lookup"><span data-stu-id="fd378-113">For example, if the frame rate is 30 frames per second (fps), the ratio is 30/1.</span></span>

<span data-ttu-id="fd378-114">Si el dispositivo de captura informa de una velocidad de fotogramas máxima, el origen de medios establece este atributo en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fd378-114">If the capture device reports a maximum frame rate, the media source sets this attribute on the media type.</span></span> <span data-ttu-id="fd378-115">La velocidad de fotogramas mínima se indica en el atributo de [ \_ intervalo de velocidad de \_ fotogramas MF MT \_ \_ \_ min](mf-mt-frame-rate-range-min.md) .</span><span class="sxs-lookup"><span data-stu-id="fd378-115">The minimum frame rate is given in the [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attribute.</span></span> <span data-ttu-id="fd378-116">No se garantiza que el dispositivo admita todos los incrementos dentro de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="fd378-116">The device is not guaranteed to support every increment within this range.</span></span>

<span data-ttu-id="fd378-117">Para establecer la velocidad de fotogramas del dispositivo, modifique primero el valor del atributo de [**\_ \_ \_ velocidad de fotogramas MF MT**](mf-mt-frame-rate-attribute.md) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fd378-117">To set the device's frame rate, first modify the value of the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="fd378-118">A continuación, establezca el tipo de medio en el origen del medio.</span><span class="sxs-lookup"><span data-stu-id="fd378-118">Then set the media type on the media source.</span></span>

<span data-ttu-id="fd378-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fd378-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd378-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd378-120">Requirements</span></span>



| <span data-ttu-id="fd378-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd378-121">Requirement</span></span> | <span data-ttu-id="fd378-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd378-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd378-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd378-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fd378-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd378-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="fd378-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd378-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fd378-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd378-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fd378-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd378-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd378-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd378-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd378-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd378-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd378-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd378-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd378-131">Cómo establecer la velocidad de fotogramas de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fd378-131">How to Set the Video Capture Frame Rate</span></span>](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[<span data-ttu-id="fd378-132">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="fd378-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd378-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fd378-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fd378-134">\_intervalo de \_ velocidad de fotogramas MF MT \_ \_ \_ mín.</span><span class="sxs-lookup"><span data-stu-id="fd378-134">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




