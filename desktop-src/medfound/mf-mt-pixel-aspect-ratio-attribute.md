---
description: Relación de aspecto de píxeles para un tipo de medio de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542158"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="63dc6-103">\_Atributo de \_ relación de aspecto de píxeles MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="63dc6-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="63dc6-104">Relación de aspecto de píxeles para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="63dc6-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="63dc6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="63dc6-105">Data type</span></span>

<span data-ttu-id="63dc6-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="63dc6-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="63dc6-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63dc6-107">Remarks</span></span>

<span data-ttu-id="63dc6-108">Los 32 bits superiores contienen el numerador de la relación de aspecto de píxeles y los 32 bits inferiores contienen el denominador.</span><span class="sxs-lookup"><span data-stu-id="63dc6-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="63dc6-109">El numerador es el componente horizontal de la relación de aspecto; el denominador es el componente vertical.</span><span class="sxs-lookup"><span data-stu-id="63dc6-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="63dc6-110">Para establecer este atributo, utilice la función [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="63dc6-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="63dc6-111">Para obtener este atributo, utilice la función [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="63dc6-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="63dc6-112">La relación de aspecto de píxeles describe la forma de los píxeles de la imagen de vídeo mostrada.</span><span class="sxs-lookup"><span data-stu-id="63dc6-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="63dc6-113">Establezca este atributo si la imagen tiene píxeles no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="63dc6-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="63dc6-114">Para que se muestre correctamente en un dispositivo de pantalla con píxeles cuadrados, la imagen se debe escalar mediante el inverso de la relación de aspecto de píxeles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="63dc6-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="63dc6-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="63dc6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="63dc6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63dc6-116">Requirements</span></span>



| <span data-ttu-id="63dc6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="63dc6-117">Requirement</span></span> | <span data-ttu-id="63dc6-118">Value</span><span class="sxs-lookup"><span data-stu-id="63dc6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63dc6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63dc6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63dc6-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="63dc6-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="63dc6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63dc6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63dc6-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="63dc6-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="63dc6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63dc6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63dc6-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="63dc6-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63dc6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="63dc6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63dc6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63dc6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63dc6-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="63dc6-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="63dc6-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63dc6-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63dc6-129">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="63dc6-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




