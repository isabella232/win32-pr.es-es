---
description: Especifica si una secuencia de imágenes ASF es un tipo JPEG degradado.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908039"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a><span data-ttu-id="a4b34-103">MF \_ MT \_ Image \_ loss \_ tolerante (atributo)</span><span class="sxs-lookup"><span data-stu-id="a4b34-103">MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute</span></span>

<span data-ttu-id="a4b34-104">Especifica si una secuencia de imágenes ASF es un tipo JPEG degradado.</span><span class="sxs-lookup"><span data-stu-id="a4b34-104">Specifies whether an ASF image stream is a degradable JPEG type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4b34-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a4b34-105">Data type</span></span>

<span data-ttu-id="a4b34-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a4b34-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a4b34-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="a4b34-107">Get/set</span></span>

<span data-ttu-id="a4b34-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a4b34-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="a4b34-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="a4b34-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a4b34-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="a4b34-110">Applies to</span></span>

[<span data-ttu-id="a4b34-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a4b34-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="a4b34-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4b34-112">Remarks</span></span>

<span data-ttu-id="a4b34-113">Este atributo se aplica al tipo de medio para flujos de imagen en ASF.</span><span class="sxs-lookup"><span data-stu-id="a4b34-113">This attribute applies to the media type for image streams in ASF.</span></span> <span data-ttu-id="a4b34-114">Si el valor es **true**, la secuencia es un tipo de imagen JPEG degradado.</span><span class="sxs-lookup"><span data-stu-id="a4b34-114">If the value is **TRUE**, the stream is a degradable JPEG image type.</span></span> <span data-ttu-id="a4b34-115">De lo contrario, el flujo es un tipo de imagen JFIF.</span><span class="sxs-lookup"><span data-stu-id="a4b34-115">Otherwise, the stream is a JFIF image type.</span></span> <span data-ttu-id="a4b34-116">Para obtener más información sobre estos tipos de secuencias, vea la especificación ASF.</span><span class="sxs-lookup"><span data-stu-id="a4b34-116">For more information about these stream types, see the ASF specification.</span></span>

<span data-ttu-id="a4b34-117">Además del \_ atributo MF MT \_ Image \_ loss \_ tolerante, el tipo de medio para un flujo de imagen ASF contiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="a4b34-117">In addition to the MF\_MT\_IMAGE\_LOSS\_TOLERANT attribute, the media type for an ASF image stream contains the following attributes:</span></span>



| <span data-ttu-id="a4b34-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="a4b34-118">Attribute</span></span>                                                 | <span data-ttu-id="a4b34-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4b34-119">Description</span></span>                                |
|-----------------------------------------------------------|--------------------------------------------|
| [<span data-ttu-id="a4b34-120">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="a4b34-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="a4b34-121">Contiene el valor **MFMediaType \_ imagen**.</span><span class="sxs-lookup"><span data-stu-id="a4b34-121">Contains the value **MFMediaType\_Image**.</span></span> |
| [<span data-ttu-id="a4b34-122">**\_tamaño de \_ marco MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a4b34-122">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md) | <span data-ttu-id="a4b34-123">Proporciona el tamaño de la imagen en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a4b34-123">Gives the image size in pixels.</span></span>            |



 

<span data-ttu-id="a4b34-124">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a4b34-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b34-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b34-125">Requirements</span></span>



| <span data-ttu-id="a4b34-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b34-126">Requirement</span></span> | <span data-ttu-id="a4b34-127">Value</span><span class="sxs-lookup"><span data-stu-id="a4b34-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b34-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4b34-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b34-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a4b34-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a4b34-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4b34-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b34-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="a4b34-131">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a4b34-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4b34-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b34-133"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b34-133"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b34-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4b34-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b34-135">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a4b34-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a4b34-136">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="a4b34-136">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




