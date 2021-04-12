---
description: Especifica la velocidad de bits de codificación de audio de la presentación, en bits por segundo. Este atributo se aplica a los descriptores de presentación.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: MF_PD_AUDIO_ENCODING_BITRATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277687"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a><span data-ttu-id="f3e6d-104">MF \_ PD \_ \_ atributo de velocidad de bits de codificación de audio \_</span><span class="sxs-lookup"><span data-stu-id="f3e6d-104">MF\_PD\_AUDIO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="f3e6d-105">Especifica la velocidad de bits de codificación de audio de la presentación, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-105">Specifies the audio encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="f3e6d-106">Este atributo se aplica a los descriptores de presentación.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3e6d-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f3e6d-107">Data type</span></span>

<span data-ttu-id="f3e6d-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f3e6d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3e6d-109">Remarks</span></span>

<span data-ttu-id="f3e6d-110">El atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-110">The attribute is optional.</span></span> <span data-ttu-id="f3e6d-111">Algunos formatos tienen esquemas de codificación más complejos que no se pueden resumir mediante este atributo.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="f3e6d-112">En el caso de los archivos de formato de sistema avanzado (ASF), los atributos siguientes describen colectivamente la velocidad de bits de codificación:</span><span class="sxs-lookup"><span data-stu-id="f3e6d-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="f3e6d-113">**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ de \_ velocidad de bits máxima**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="f3e6d-114">**\_velocidad de \_ \_ \_ bits promedio de \_ datos \_ ASF SD EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="f3e6d-115">**\_velocidad de \_ \_ bits de \_ datos Max SD ASF EXTSTRMPROP máx \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="f3e6d-116">**\_velocidad de \_ bits de ASF SD ASF \_ STREAMBITRATES \_**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="f3e6d-117">Los formatos de terceros pueden usar otros atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="f3e6d-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f3e6d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3e6d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3e6d-119">Requirements</span></span>



| <span data-ttu-id="f3e6d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e6d-120">Requirement</span></span> | <span data-ttu-id="f3e6d-121">Value</span><span class="sxs-lookup"><span data-stu-id="f3e6d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e6d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3e6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e6d-123">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f3e6d-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f3e6d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3e6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e6d-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f3e6d-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f3e6d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3e6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e6d-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e6d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e6d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3e6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e6d-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3e6d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3e6d-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f3e6d-131">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f3e6d-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3e6d-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f3e6d-133">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="f3e6d-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




