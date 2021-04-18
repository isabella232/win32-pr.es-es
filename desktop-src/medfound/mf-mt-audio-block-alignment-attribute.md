---
description: Alineación de bloque, en bytes, para un tipo de medio de audio. La alineación de bloque es la unidad atómica mínima de datos para el formato de audio.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: MF_MT_AUDIO_BLOCK_ALIGNMENT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706589"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="42f16-104">\_Atributo de \_ alineación de bloque de audio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="42f16-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="42f16-105">Alineación de bloque, en bytes, para un tipo de medio de audio.</span><span class="sxs-lookup"><span data-stu-id="42f16-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="42f16-106">La alineación de bloque es la unidad atómica mínima de datos para el formato de audio.</span><span class="sxs-lookup"><span data-stu-id="42f16-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="42f16-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="42f16-107">Data type</span></span>

<span data-ttu-id="42f16-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="42f16-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="42f16-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42f16-109">Remarks</span></span>

<span data-ttu-id="42f16-110">En el caso de los formatos de audio PCM, la alineación del bloque es igual al número de canales de audio multiplicado por el número de bytes por muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="42f16-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="42f16-111">Este atributo corresponde al miembro **nBlockAlign** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="42f16-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="42f16-112">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="42f16-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f16-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f16-113">Requirements</span></span>



| <span data-ttu-id="42f16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f16-114">Requirement</span></span> | <span data-ttu-id="42f16-115">Value</span><span class="sxs-lookup"><span data-stu-id="42f16-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42f16-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="42f16-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="42f16-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="42f16-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="42f16-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="42f16-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="42f16-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42f16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f16-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42f16-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f16-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f16-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42f16-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="42f16-124">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="42f16-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="42f16-125">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="42f16-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="42f16-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="42f16-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="42f16-127">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="42f16-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
