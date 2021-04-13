---
description: Especifica si está habilitado el modo de panorámica o de recorrido.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545030"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a><span data-ttu-id="ec8be-103">\_Atributo MF MT de \_ \_ examen panorámico \_ habilitado</span><span class="sxs-lookup"><span data-stu-id="ec8be-103">MF\_MT\_PAN\_SCAN\_ENABLED attribute</span></span>

<span data-ttu-id="ec8be-104">Especifica si está habilitado el modo de panorámica o de recorrido.</span><span class="sxs-lookup"><span data-stu-id="ec8be-104">Specifies whether pan/scan mode is enabled.</span></span>

## <a name="data-type"></a><span data-ttu-id="ec8be-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ec8be-105">Data type</span></span>

<span data-ttu-id="ec8be-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ec8be-106">**UINT32**</span></span>

<span data-ttu-id="ec8be-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="ec8be-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8be-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec8be-108">Remarks</span></span>

<span data-ttu-id="ec8be-109">Si este atributo es **true**, solo se debe mostrar la región de Pan/Scan del vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec8be-109">If this attribute is **TRUE**, only the pan/scan region of the video should be displayed.</span></span> <span data-ttu-id="ec8be-110">La región de Pan/Scan se especifica mediante el atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8be-110">The pan/scan region is specified by the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="ec8be-111">Si este atributo es **falso** o no está establecido, se debe mostrar la abertura de pantalla completa del vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec8be-111">If this attribute is **FALSE** or not set, the entire display aperture of the video should be displayed.</span></span> <span data-ttu-id="ec8be-112">La abertura de pantalla se especifica mediante el atributo de [**\_ \_ \_ \_ abertura mínima de visualización MF MT**](mf-mt-minimum-display-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8be-112">The display aperture is specified by the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="ec8be-113">Si establece este atributo en **true**, establezca también el valor del atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8be-113">If you set this attribute to **TRUE**, also set the value of the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute.</span></span>

<span data-ttu-id="ec8be-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ec8be-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec8be-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec8be-115">Requirements</span></span>



| <span data-ttu-id="ec8be-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec8be-116">Requirement</span></span> | <span data-ttu-id="ec8be-117">Value</span><span class="sxs-lookup"><span data-stu-id="ec8be-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8be-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec8be-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8be-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ec8be-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ec8be-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec8be-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8be-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ec8be-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ec8be-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec8be-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8be-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec8be-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec8be-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec8be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8be-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec8be-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec8be-126">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ec8be-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ec8be-127">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ec8be-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ec8be-128">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ec8be-128">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ec8be-129">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="ec8be-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="ec8be-130">Relación de aspecto de la imagen</span><span class="sxs-lookup"><span data-stu-id="ec8be-130">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




