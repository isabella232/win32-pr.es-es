---
description: Especifica los elementos primarios de color personalizado para un tipo de medio de vídeo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: MF_MT_CUSTOM_VIDEO_PRIMARIES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707239"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="6a86d-103">\_ \_ \_ Atributo primario de vídeo \_ primario MF MT</span><span class="sxs-lookup"><span data-stu-id="6a86d-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="6a86d-104">Especifica los elementos primarios de color personalizado para un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a86d-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="6a86d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6a86d-105">Data type</span></span>

<span data-ttu-id="6a86d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6a86d-106">**UINT32**</span></span>

<span data-ttu-id="6a86d-107">Byte array</span><span class="sxs-lookup"><span data-stu-id="6a86d-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="6a86d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a86d-108">Remarks</span></span>

<span data-ttu-id="6a86d-109">Los datos de atributo son una estructura de los principales [**\_ \_ vídeos \_ personalizados de MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .</span><span class="sxs-lookup"><span data-stu-id="6a86d-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="6a86d-110">Este atributo especifica el volumen de color real del contenido o una pantalla.</span><span class="sxs-lookup"><span data-stu-id="6a86d-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="6a86d-111">Los descodificadores almacenan la información de maestro de volumen de CEA-861,3/SMPTE ST. 2086 en este atributo.</span><span class="sxs-lookup"><span data-stu-id="6a86d-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="6a86d-112">Tenga en cuenta que este atributo no reemplaza el atributo [**\_ \_ \_ primarios de vídeo MF MT**](mf-mt-video-primaries-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="6a86d-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="6a86d-113">Este atributo describe una sugerencia sobre el volumen de color del contenido, mientras que el **\_ \_ vídeo \_ primario MF MT** describe las principales colores en los que el contenido se codifica realmente (por ejemplo, el significado de 1,0 en los canales R/g/B de una representación de punto flotante).</span><span class="sxs-lookup"><span data-stu-id="6a86d-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="6a86d-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6a86d-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a86d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a86d-115">Requirements</span></span>



| <span data-ttu-id="6a86d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a86d-116">Requirement</span></span> | <span data-ttu-id="6a86d-117">Value</span><span class="sxs-lookup"><span data-stu-id="6a86d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a86d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a86d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a86d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a86d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a86d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a86d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a86d-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a86d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a86d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a86d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a86d-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a86d-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a86d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a86d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a86d-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a86d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a86d-126">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="6a86d-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a86d-127">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6a86d-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6a86d-128">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="6a86d-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6a86d-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6a86d-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




