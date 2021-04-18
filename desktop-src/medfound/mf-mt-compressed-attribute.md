---
description: Especifica para un tipo de medio si se comprimen los datos multimedia.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544342"
---
# <a name="mf_mt_compressed-attribute"></a><span data-ttu-id="151ee-103">\_ \_ Atributo comprimido MF MT</span><span class="sxs-lookup"><span data-stu-id="151ee-103">MF\_MT\_COMPRESSED attribute</span></span>

<span data-ttu-id="151ee-104">Especifica para un tipo de medio si se comprimen los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="151ee-104">Specifies for a media type whether the media data is compressed.</span></span>

## <a name="data-type"></a><span data-ttu-id="151ee-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="151ee-105">Data type</span></span>

<span data-ttu-id="151ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="151ee-106">**UINT32**</span></span>

<span data-ttu-id="151ee-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="151ee-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="151ee-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="151ee-108">Remarks</span></span>

<span data-ttu-id="151ee-109">Si este atributo es **true**, el tipo de medio es un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="151ee-109">If this attribute is **TRUE**, the media type is a compressed format.</span></span> <span data-ttu-id="151ee-110">De lo contrario, el tipo de medio se descomprime o no se conoce el tipo de compresión.</span><span class="sxs-lookup"><span data-stu-id="151ee-110">Otherwise, either the media type is uncompressed or the compression type is not known.</span></span>

<span data-ttu-id="151ee-111">No se garantiza que este atributo esté establecido en **true** para todos los formatos comprimidos, por lo que las aplicaciones no deben confiar normalmente en este atributo.</span><span class="sxs-lookup"><span data-stu-id="151ee-111">This attribute is not guaranteed to be set to **TRUE** for all compressed formats, so applications should generally not rely this attribute.</span></span> <span data-ttu-id="151ee-112">La forma más confiable de determinar si un formato está comprimido es mantener una lista de formatos conocidos.</span><span class="sxs-lookup"><span data-stu-id="151ee-112">The most reliable way to determine whether a format is compressed is to maintain a list of known formats.</span></span> <span data-ttu-id="151ee-113">Si una aplicación no reconoce un formato, tal y como se especifica en el atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) , no debe suponer nada sobre la compresión del formato.</span><span class="sxs-lookup"><span data-stu-id="151ee-113">If an application does not recognize a format, as specified in the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute, it should not assume anything about the compression of the format.</span></span>

<span data-ttu-id="151ee-114">Para determinar si un formato utiliza la compresión temporal (lo que significa que algunos ejemplos se calculan como deltas de los ejemplos anteriores), compruebe el atributo [**\_ independiente MF MT \_ All \_ Samples \_**](mf-mt-all-samples-independent-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="151ee-114">To determine whether a format uses temporal compression (meaning that some samples are computed as deltas from earlier samples), check the [**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) attribute.</span></span>

<span data-ttu-id="151ee-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="151ee-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="151ee-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="151ee-116">Requirements</span></span>



| <span data-ttu-id="151ee-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="151ee-117">Requirement</span></span> | <span data-ttu-id="151ee-118">Value</span><span class="sxs-lookup"><span data-stu-id="151ee-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="151ee-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="151ee-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="151ee-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="151ee-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="151ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="151ee-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="151ee-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="151ee-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="151ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="151ee-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="151ee-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="151ee-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="151ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="151ee-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="151ee-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="151ee-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="151ee-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="151ee-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="151ee-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="151ee-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="151ee-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="151ee-130">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="151ee-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




