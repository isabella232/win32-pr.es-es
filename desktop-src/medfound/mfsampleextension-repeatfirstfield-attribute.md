---
description: Especifica si se va a repetir el primer campo en un marco entrelazado. Este atributo se aplica a los ejemplos de medios.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155365"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a><span data-ttu-id="85aa4-104">\_Atributo RepeatFirstField de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="85aa4-104">MFSampleExtension\_RepeatFirstField attribute</span></span>

<span data-ttu-id="85aa4-105">Especifica si se va a repetir el primer campo en un marco entrelazado.</span><span class="sxs-lookup"><span data-stu-id="85aa4-105">Specifies whether to repeat the first field in an interlaced frame.</span></span> <span data-ttu-id="85aa4-106">Este atributo se aplica a los ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="85aa4-106">This attribute applies to media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="85aa4-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="85aa4-107">Data type</span></span>

<span data-ttu-id="85aa4-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="85aa4-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="85aa4-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="85aa4-109">Get/set</span></span>

<span data-ttu-id="85aa4-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="85aa4-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="85aa4-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="85aa4-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="85aa4-112">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="85aa4-112">Applies to</span></span>

[<span data-ttu-id="85aa4-113">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="85aa4-113">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="85aa4-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85aa4-114">Remarks</span></span>

<span data-ttu-id="85aa4-115">Si el valor es **false** o el atributo no está establecido, el primer campo no se repite.</span><span class="sxs-lookup"><span data-stu-id="85aa4-115">If the value is **FALSE** or the attribute is not set, the first field is not repeated.</span></span> <span data-ttu-id="85aa4-116">Si el valor es **true**, el primer campo se repite.</span><span class="sxs-lookup"><span data-stu-id="85aa4-116">If the value is **TRUE**, the first field is repeated.</span></span> <span data-ttu-id="85aa4-117">El valor **true** solo es válido cuando se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="85aa4-117">The value **TRUE** is valid only when the following conditions are true:</span></span>

-   <span data-ttu-id="85aa4-118">El tipo de medio es entrelazado y progresivo.</span><span class="sxs-lookup"><span data-stu-id="85aa4-118">The media type is mixed interlaced and progressive.</span></span> <span data-ttu-id="85aa4-119">(El atributo de atributo de [**\_ \_ \_ modo entrelazado MF MT**](mf-mt-interlace-mode-attribute.md) en el tipo de medio es **MFVideoInterlace \_ MixedInterlaceOrProgressive**).</span><span class="sxs-lookup"><span data-stu-id="85aa4-119">(The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute attribute on the media type is **MFVideoInterlace\_MixedInterlaceOrProgressive**.)</span></span>
-   <span data-ttu-id="85aa4-120">El marco es progresivo y el atributo [**\_ entrelazado MFSampleExtension**](mfsampleextension-interlaced-attribute.md) del ejemplo es **true**.</span><span class="sxs-lookup"><span data-stu-id="85aa4-120">The frame is progressive and the [**MFSampleExtension\_Interlaced**](mfsampleextension-interlaced-attribute.md) attribute on the sample is **TRUE**.</span></span>
-   <span data-ttu-id="85aa4-121">El atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) se establece en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="85aa4-121">The [**MFSampleExtension\_BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) attribute is set on the sample.</span></span> <span data-ttu-id="85aa4-122">El valor puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="85aa4-122">The value can be **TRUE** or **FALSE**.</span></span> <span data-ttu-id="85aa4-123">Este atributo determina el orden de los campos.</span><span class="sxs-lookup"><span data-stu-id="85aa4-123">The ordering of the fields is determined by this attribute.</span></span>

<span data-ttu-id="85aa4-124">Este atributo se utiliza para la telecine 3:2.</span><span class="sxs-lookup"><span data-stu-id="85aa4-124">This attribute is used for 3:2 pulldown.</span></span> <span data-ttu-id="85aa4-125">En la tabla siguiente se muestra el orden en que se muestran los campos.</span><span class="sxs-lookup"><span data-stu-id="85aa4-125">The following table shows the order in which fields are displayed.</span></span>



| <span data-ttu-id="85aa4-126">MFSampleExtension \_ RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="85aa4-126">MFSampleExtension\_RepeatFirstField</span></span> | <span data-ttu-id="85aa4-127">MFSampleExtension \_ BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="85aa4-127">MFSampleExtension\_BottomFieldFirst</span></span> | <span data-ttu-id="85aa4-128">Orden de los campos</span><span class="sxs-lookup"><span data-stu-id="85aa4-128">Field order</span></span>         |
|-------------------------------------|-------------------------------------|---------------------|
| <span data-ttu-id="85aa4-129">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-129">**TRUE**</span></span>                            | <span data-ttu-id="85aa4-130">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-130">**TRUE**</span></span>                            | <span data-ttu-id="85aa4-131">Inferior, superior, inferior</span><span class="sxs-lookup"><span data-stu-id="85aa4-131">Lower, upper, lower</span></span> |
| <span data-ttu-id="85aa4-132">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-132">**TRUE**</span></span>                            | <span data-ttu-id="85aa4-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-133">**FALSE**</span></span>                           | <span data-ttu-id="85aa4-134">Superior, inferior, superior</span><span class="sxs-lookup"><span data-stu-id="85aa4-134">Upper, lower, upper</span></span> |
| <span data-ttu-id="85aa4-135">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-135">**FALSE**</span></span>                           | <span data-ttu-id="85aa4-136">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-136">**TRUE**</span></span>                            | <span data-ttu-id="85aa4-137">Inferior, superior</span><span class="sxs-lookup"><span data-stu-id="85aa4-137">Lower, upper</span></span>        |
| <span data-ttu-id="85aa4-138">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-138">**FALSE**</span></span>                           | <span data-ttu-id="85aa4-139">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85aa4-139">**FALSE**</span></span>                           | <span data-ttu-id="85aa4-140">Superior, inferior</span><span class="sxs-lookup"><span data-stu-id="85aa4-140">Upper, lower</span></span>        |



 

<span data-ttu-id="85aa4-141">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="85aa4-141">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85aa4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85aa4-142">Requirements</span></span>



| <span data-ttu-id="85aa4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="85aa4-143">Requirement</span></span> | <span data-ttu-id="85aa4-144">Value</span><span class="sxs-lookup"><span data-stu-id="85aa4-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85aa4-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85aa4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="85aa4-146">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="85aa4-146">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="85aa4-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85aa4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="85aa4-148">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="85aa4-148">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="85aa4-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85aa4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="85aa4-150"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="85aa4-150"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85aa4-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="85aa4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85aa4-152">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85aa4-152">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85aa4-153">Atributos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="85aa4-153">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="85aa4-154">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="85aa4-154">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="85aa4-155">Entrelazado de vídeo</span><span class="sxs-lookup"><span data-stu-id="85aa4-155">Video Interlacing</span></span>](video-interlacing.md)
</dt> </dl>

 

 




