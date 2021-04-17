---
description: Especifica si un fotograma de vídeo desentrelazado se ha derivado del campo superior o del campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696886"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a><span data-ttu-id="68524-103">\_Atributo DerivedFromTopField de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="68524-103">MFSampleExtension\_DerivedFromTopField attribute</span></span>

<span data-ttu-id="68524-104">Especifica si un fotograma de vídeo desentrelazado se ha derivado del campo superior o del campo inferior.</span><span class="sxs-lookup"><span data-stu-id="68524-104">Specifies whether a deinterlaced video frame was derived from the upper field or the lower field.</span></span> <span data-ttu-id="68524-105">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="68524-105">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="68524-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="68524-106">Data type</span></span>

<span data-ttu-id="68524-107">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="68524-107">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="68524-108">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="68524-108">Get/set</span></span>

<span data-ttu-id="68524-109">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="68524-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="68524-110">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="68524-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="68524-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="68524-111">Applies to</span></span>

[<span data-ttu-id="68524-112">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="68524-112">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="68524-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68524-113">Remarks</span></span>

<span data-ttu-id="68524-114">Este atributo solo es válido para los ejemplos desentrelazados.</span><span class="sxs-lookup"><span data-stu-id="68524-114">This attribute is valid for deinterlaced samples only.</span></span> <span data-ttu-id="68524-115">Establezca este atributo si el marco se desentrelaza mediante la interpolación de uno de los campos.</span><span class="sxs-lookup"><span data-stu-id="68524-115">Set this attribute if the frame was deinterlaced by interpolating one of the fields.</span></span>

<span data-ttu-id="68524-116">Si el valor es **true**, el campo inferior se interpola a partir del campo superior.</span><span class="sxs-lookup"><span data-stu-id="68524-116">If the value is **TRUE**, the lower field was interpolated from the upper field.</span></span> <span data-ttu-id="68524-117">Si el valor es **false**, el campo superior se interpola a partir del campo inferior.</span><span class="sxs-lookup"><span data-stu-id="68524-117">If the value is **FALSE**, the upper field was interpolated from the lower field.</span></span>

<span data-ttu-id="68524-118">Si no se establece el atributo, el marco no se ha desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="68524-118">If the attribute is not set, the frame has not been deinterlaced.</span></span> <span data-ttu-id="68524-119">El marco es un fotograma progresivo verdadero o es un marco entrelazado.</span><span class="sxs-lookup"><span data-stu-id="68524-119">The frame is either a true progressive frame, or it is an interlaced frame.</span></span>

<span data-ttu-id="68524-120">Este atributo es informativo.</span><span class="sxs-lookup"><span data-stu-id="68524-120">This attribute is informational.</span></span> <span data-ttu-id="68524-121">Un desentrelazador de software podría establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="68524-121">A software deinterlacer could set this attribute.</span></span> <span data-ttu-id="68524-122">Si se establece este atributo, se proporciona una sugerencia que permite recuperar el campo original quitando las líneas de recorrido interpoladas.</span><span class="sxs-lookup"><span data-stu-id="68524-122">If this attribute is set, it provides a hint that you can recover the original field by dropping the interpolated scan lines.</span></span> <span data-ttu-id="68524-123">Por ejemplo, si el atributo es **true**, puede recuperar el campo superior original quitando el campo interpolado inferior.</span><span class="sxs-lookup"><span data-stu-id="68524-123">For example, if the attribute is **TRUE**, you can recover the original upper field by dropping the interpolated lower field.</span></span>

<span data-ttu-id="68524-124">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="68524-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68524-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68524-125">Requirements</span></span>



| <span data-ttu-id="68524-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="68524-126">Requirement</span></span> | <span data-ttu-id="68524-127">Value</span><span class="sxs-lookup"><span data-stu-id="68524-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68524-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68524-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68524-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="68524-129">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="68524-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68524-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68524-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="68524-131">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="68524-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68524-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="68524-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68524-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68524-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="68524-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68524-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68524-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68524-136">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="68524-136">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="68524-137">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="68524-137">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="68524-138">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="68524-138">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




