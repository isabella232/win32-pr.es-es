---
description: Contiene un GUID de formato de DirectShow para un tipo de medio.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360513"
---
# <a name="mf_mt_am_format_type-attribute"></a><span data-ttu-id="97639-103">MF \_ MT \_ AM \_ \_ atributo de tipo Format</span><span class="sxs-lookup"><span data-stu-id="97639-103">MF\_MT\_AM\_FORMAT\_TYPE attribute</span></span>

<span data-ttu-id="97639-104">Contiene un GUID de formato de DirectShow para un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="97639-104">Contains a DirectShow format GUID for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="97639-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="97639-105">Data type</span></span>

<span data-ttu-id="97639-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="97639-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="97639-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97639-107">Remarks</span></span>

<span data-ttu-id="97639-108">Este atributo se puede establecer cuando un tipo de medio de DirectShow se convierte en un tipo de medio Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="97639-108">This attribute might be set when a DirectShow media type is converted into a Media Foundation media type.</span></span> <span data-ttu-id="97639-109">El atributo indica el tipo de formato de DirectShow original.</span><span class="sxs-lookup"><span data-stu-id="97639-109">The attribute indicates the original DirectShow format type.</span></span> <span data-ttu-id="97639-110">El valor corresponde al miembro FormatType de la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="97639-110">The value corresponds to the formattype member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="97639-111">En el caso de un formato de audio, el atributo de [**\_ datos de \_ usuario \_ MF MT**](mf-mt-user-data-attribute.md) podría contener el bloque de formato original, si no se reconoció el tipo de formato DirectShow.</span><span class="sxs-lookup"><span data-stu-id="97639-111">For an audio format, the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute might contain the original format block, if the DirectShow format type was not recognized.</span></span>

<span data-ttu-id="97639-112">No establezca este atributo en un tipo de medio a menos que esté convirtiendo una estructura de formato de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="97639-112">Do not set this attribute on a media type unless you are converting a DirectShow format structure.</span></span>

<span data-ttu-id="97639-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="97639-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="97639-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97639-114">Requirements</span></span>



| <span data-ttu-id="97639-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="97639-115">Requirement</span></span> | <span data-ttu-id="97639-116">Value</span><span class="sxs-lookup"><span data-stu-id="97639-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97639-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97639-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97639-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="97639-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97639-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97639-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97639-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="97639-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="97639-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97639-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="97639-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="97639-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97639-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="97639-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97639-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97639-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="97639-125">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="97639-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="97639-126">Conversiones de tipos de medios</span><span class="sxs-lookup"><span data-stu-id="97639-126">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="97639-127">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="97639-127">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="97639-128">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="97639-128">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="97639-129">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="97639-129">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="97639-130">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="97639-130">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="97639-131">**MFCreateMediaTypeFromRepresentation**</span><span class="sxs-lookup"><span data-stu-id="97639-131">**MFCreateMediaTypeFromRepresentation**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
