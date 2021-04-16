---
description: Contiene la etiqueta de formato de onda original para una secuencia de audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678503"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a><span data-ttu-id="b9bc2-103">MF \_ MT \_ original \_ \_ atributo de etiqueta de formato de onda \_</span><span class="sxs-lookup"><span data-stu-id="b9bc2-103">MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute</span></span>

<span data-ttu-id="b9bc2-104">Contiene la etiqueta de formato de onda original para una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-104">Contains the original WAVE format tag for an audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9bc2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b9bc2-105">Data type</span></span>

<span data-ttu-id="b9bc2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b9bc2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b9bc2-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="b9bc2-107">Get/set</span></span>

<span data-ttu-id="b9bc2-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b9bc2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b9bc2-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b9bc2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b9bc2-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b9bc2-110">Applies to</span></span>

[<span data-ttu-id="b9bc2-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b9bc2-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b9bc2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9bc2-112">Remarks</span></span>

<span data-ttu-id="b9bc2-113">Dependiendo del archivo de origen, el origen de medios AVI podría establecer este atributo en los tipos de medios que ofrece.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-113">Depending on the source file, the AVI media source might set this attribute on the media types that it offers.</span></span>

<span data-ttu-id="b9bc2-114">Un archivo AVI contiene un encabezado de secuencia para cada flujo del archivo.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-114">An AVI file contains a stream header for each stream in the file.</span></span> <span data-ttu-id="b9bc2-115">El origen de medios AVI traduce el encabezado de secuencia en un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-115">The AVI media source translates the stream header into a media type.</span></span> <span data-ttu-id="b9bc2-116">En el caso de las secuencias de audio, el encabezado de flujo contiene una etiqueta de formato que identifica el formato de audio.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-116">For audio streams, the stream header contains a format tag that identifies the audio format.</span></span> <span data-ttu-id="b9bc2-117">(La etiqueta de formato se encuentra en el miembro **wFormatTag** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ). En la mayoría de los casos, el origen de medios AVI convierte la etiqueta de formato directamente en un GUID de subtipo, tal y como se describe en el tema [**GUID de subtipo de audio**](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b9bc2-117">(The format tag is contained in the **wFormatTag** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.) In most cases, the AVI media source converts the format tag directly to a subtype GUID, as described in the topic [**Audio Subtype GUIDs**](audio-subtype-guids.md).</span></span> <span data-ttu-id="b9bc2-118">En algunos casos, sin embargo, asigna la etiqueta de formato original a otra etiqueta de formato equivalente.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-118">In some cases, however, it maps the original format tag to another format tag that is equivalent.</span></span> <span data-ttu-id="b9bc2-119">Si es así, el origen de medios almacena la etiqueta de formato original en el tipo de medio mediante el \_ \_ atributo de etiqueta de formato de onda original MF MT \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b9bc2-119">If so, the media source stores the original format tag in the media type, using the MF\_MT\_ORIGINAL\_WAVE\_FORMAT\_TAG attribute.</span></span>

<span data-ttu-id="b9bc2-120">Las asignaciones de formato se almacenan en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="b9bc2-120">The format mappings are stored in the Registry under the following key:</span></span>

<span data-ttu-id="b9bc2-121">**HKEY \_ MediaFoundation \_ raíz de clases** \\  \\ **MapAudioFormatTag**</span><span class="sxs-lookup"><span data-stu-id="b9bc2-121">**HKEY\_CLASSES\_ROOT**\\**MediaFoundation**\\**MapAudioFormatTag**</span></span>

<span data-ttu-id="b9bc2-122">Cada entrada es un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b9bc2-122">Each entry is a **DWORD** value.</span></span> <span data-ttu-id="b9bc2-123">El nombre de la entrada es la representación decimal de la etiqueta de formato.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-123">The name of the entry is the decimal representation of the format tag.</span></span> <span data-ttu-id="b9bc2-124">El valor de la entrada es la etiqueta de formato equivalente.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-124">The value of the entry is the equivalent format tag.</span></span>

<span data-ttu-id="b9bc2-125">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b9bc2-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9bc2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9bc2-126">Requirements</span></span>



| <span data-ttu-id="b9bc2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9bc2-127">Requirement</span></span> | <span data-ttu-id="b9bc2-128">Value</span><span class="sxs-lookup"><span data-stu-id="b9bc2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bc2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9bc2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9bc2-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9bc2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9bc2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9bc2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9bc2-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9bc2-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b9bc2-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9bc2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9bc2-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9bc2-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9bc2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9bc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bc2-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9bc2-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9bc2-137">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="b9bc2-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
