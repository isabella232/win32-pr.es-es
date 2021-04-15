---
description: Especifica un número entre 0 y 100 que indica el equilibrio entre la calidad de codificación y la velocidad de codificación.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709077"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="b81b9-103">\_Atributo QUALITYVSSPEED de TRANSCODE MF \_</span><span class="sxs-lookup"><span data-stu-id="b81b9-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="b81b9-104">Especifica un número entre 0 y 100 que indica el equilibrio entre la calidad de codificación y la velocidad de codificación.</span><span class="sxs-lookup"><span data-stu-id="b81b9-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="b81b9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b81b9-105">Data type</span></span>

<span data-ttu-id="b81b9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b81b9-106">**UINT32**</span></span>

<span data-ttu-id="b81b9-107">El valor de esta propiedad tiene el siguiente intervalo.</span><span class="sxs-lookup"><span data-stu-id="b81b9-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="b81b9-108">Value</span><span class="sxs-lookup"><span data-stu-id="b81b9-108">Value</span></span>                                                                          | <span data-ttu-id="b81b9-109">Significado</span><span class="sxs-lookup"><span data-stu-id="b81b9-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="b81b9-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b81b9-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="b81b9-111">Codificación más rápida y de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="b81b9-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="b81b9-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="b81b9-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="b81b9-113">Codificación más lenta y de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="b81b9-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="b81b9-114">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b81b9-114">Get/set</span></span>

<span data-ttu-id="b81b9-115">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b81b9-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b81b9-116">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b81b9-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b81b9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b81b9-117">Remarks</span></span>

<span data-ttu-id="b81b9-118">Este atributo tiene el mismo valor GUID que la propiedad [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definida para [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), y tiene la misma interpretación.</span><span class="sxs-lookup"><span data-stu-id="b81b9-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="b81b9-119">La aplicación puede establecer este atributo en el perfil de transcodificación antes de generar la topología de transcodificación para códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b81b9-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="b81b9-120">El valor debe estar en el intervalo comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="b81b9-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="b81b9-121">En el flujo de vídeo, el generador de topología de transcodificación asigna un valor al valor especificado por la aplicación y proporciona el valor asignado a la propiedad **MFPKEY \_ COMPLEXITYEX** del codificador.</span><span class="sxs-lookup"><span data-stu-id="b81b9-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="b81b9-122">Los valores inferiores permiten al codificador usar algoritmos de codificación menos complicados.</span><span class="sxs-lookup"><span data-stu-id="b81b9-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="b81b9-123">El uso de algoritmos más sencillos produce una salida de menor calidad, pero el proceso de codificación es más rápido y requiere menos capacidad de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b81b9-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="b81b9-124">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b81b9-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81b9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b81b9-125">Requirements</span></span>



| <span data-ttu-id="b81b9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81b9-126">Requirement</span></span> | <span data-ttu-id="b81b9-127">Value</span><span class="sxs-lookup"><span data-stu-id="b81b9-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b81b9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b81b9-128">Header</span></span><br/> | <dl> <span data-ttu-id="b81b9-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b81b9-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81b9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b81b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81b9-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b81b9-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b81b9-132">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="b81b9-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="b81b9-133">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="b81b9-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
