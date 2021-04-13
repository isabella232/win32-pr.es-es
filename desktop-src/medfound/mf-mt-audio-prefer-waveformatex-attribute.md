---
description: Especifica la estructura de formato heredada preferida que se va a usar al convertir un tipo de medio de audio.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544350"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="b20c4-103">MF \_ MT \_ audio \_ preferida \_ atributo WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="b20c4-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="b20c4-104">Especifica la estructura de formato heredada preferida que se va a usar al convertir un tipo de medio de audio.</span><span class="sxs-lookup"><span data-stu-id="b20c4-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="b20c4-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b20c4-105">Data type</span></span>

<span data-ttu-id="b20c4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b20c4-106">**UINT32**</span></span>

<span data-ttu-id="b20c4-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="b20c4-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b20c4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b20c4-108">Remarks</span></span>

<span data-ttu-id="b20c4-109">Este atributo proporciona una sugerencia a la función [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="b20c4-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="b20c4-110">Si el atributo es **true**, la función convierte el tipo de medio de audio en una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) siempre que sea posible, en lugar de convertirlo en una estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b20c4-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="b20c4-111">La función [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) establece este atributo.</span><span class="sxs-lookup"><span data-stu-id="b20c4-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="b20c4-112">Puede invalidar el valor de este atributo, pero establecer este atributo en **true** no garantiza que un tipo de medio de audio se pueda convertir al formato de [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b20c4-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="b20c4-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b20c4-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20c4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b20c4-114">Requirements</span></span>



| <span data-ttu-id="b20c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20c4-115">Requirement</span></span> | <span data-ttu-id="b20c4-116">Value</span><span class="sxs-lookup"><span data-stu-id="b20c4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b20c4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b20c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b20c4-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="b20c4-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b20c4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b20c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b20c4-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b20c4-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b20c4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b20c4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b20c4-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b20c4-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20c4-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b20c4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20c4-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b20c4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b20c4-125">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b20c4-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b20c4-126">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b20c4-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b20c4-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b20c4-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b20c4-128">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="b20c4-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
