---
description: Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: MF_MT_VIDEO_NOMINAL_RANGE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678437"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="9c9ec-103">\_Atributo de \_ \_ intervalo nominal de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="9c9ec-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="9c9ec-104">Especifica el intervalo nominal de la información de color en un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="9c9ec-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c9ec-105">Data type</span></span>

<span data-ttu-id="9c9ec-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9c9ec-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9c9ec-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c9ec-107">Remarks</span></span>

<span data-ttu-id="9c9ec-108">El valor de este atributo es un miembro de la enumeración [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .</span><span class="sxs-lookup"><span data-stu-id="9c9ec-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="9c9ec-109">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="9c9ec-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="9c9ec-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="9c9ec-111">En el tipo de medio de salida, el \_ \_ intervalo nominal de vídeo MF MT \_ \_ se puede establecer con **MFNominalRange \_ 0 \_ 255** y **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="9c9ec-112">El codificador H. 264/AVC debe tratar **MFNominalRange \_ Unknown** como **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="9c9ec-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="9c9ec-113">El codificador H. 264/AVC debe rechazar un tipo de medio de salida cuando el \_ \_ intervalo nominal de vídeo de MF MT \_ \_ está establecido en **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** o en cualquier otro valor no definido en [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span><span class="sxs-lookup"><span data-stu-id="9c9ec-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9ec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c9ec-114">Requirements</span></span>



| <span data-ttu-id="9c9ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c9ec-115">Requirement</span></span> | <span data-ttu-id="9c9ec-116">Value</span><span class="sxs-lookup"><span data-stu-id="9c9ec-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9ec-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c9ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c9ec-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="9c9ec-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9c9ec-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c9ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c9ec-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="9c9ec-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9c9ec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c9ec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c9ec-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c9ec-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c9ec-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c9ec-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9ec-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c9ec-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c9ec-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c9ec-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9c9ec-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9c9ec-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9c9ec-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="9c9ec-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="9c9ec-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="9c9ec-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="9c9ec-129">Información de color ampliada</span><span class="sxs-lookup"><span data-stu-id="9c9ec-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




