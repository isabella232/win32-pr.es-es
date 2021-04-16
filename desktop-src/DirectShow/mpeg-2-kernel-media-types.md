---
description: En el caso de varios GUID de tipo de medios MPEG-2, el DDK de Windows define nombres que difieren de los nombres que se usan en DirectShow. En la tabla siguiente se muestran los nombres de DirectShow (definidos en Ksuuids. h) y los nombres de modo kernel correspondientes (definidos en Ksmedia. h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipos de medios de kernel MPEG-2 (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b03e6d3cbc32c987110ceac98e6aeef6617d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690674"
---
# <a name="mpeg-2-kernel-media-types"></a><span data-ttu-id="e5812-104">Tipos de medios de kernel MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e5812-104">MPEG-2 Kernel Media Types</span></span>

<span data-ttu-id="e5812-105">En el caso de varios GUID de tipo de medios MPEG-2, el DDK de Windows define nombres que difieren de los nombres que se usan en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e5812-105">For several MPEG-2 media type GUIDs, the Windows DDK defines names that differ from the names used in DirectShow.</span></span> <span data-ttu-id="e5812-106">En la tabla siguiente se muestran los nombres de DirectShow (definidos en Ksuuids. h) y los nombres de modo kernel correspondientes (definidos en Ksmedia. h).</span><span class="sxs-lookup"><span data-stu-id="e5812-106">The following table shows the DirectShow names (defined in Ksuuids.h) and the corresponding kernel-mode names (defined in Ksmedia.h).</span></span>



| <span data-ttu-id="e5812-107">Nombre en Ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="e5812-107">Name in Ksuuids.h</span></span>              | <span data-ttu-id="e5812-108">Nombre en Ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="e5812-108">Name in Ksmedia.h</span></span>                          |
|--------------------------------|--------------------------------------------|
| <span data-ttu-id="e5812-109">DAR formato a \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="e5812-109">FORMAT\_WaveFormatEx</span></span>           | <span data-ttu-id="e5812-110">KSDATAFORMAT ( \_ especificador) \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="e5812-110">KSDATAFORMAT\_SPECIFIER\_WAVEFORMATEX</span></span>      |
| <span data-ttu-id="e5812-111">FORMATO \_ MPEG2Video</span><span class="sxs-lookup"><span data-stu-id="e5812-111">FORMAT\_MPEG2Video</span></span>             | <span data-ttu-id="e5812-112">Vídeo de paraKSDATAFORMAT \_ Specifier \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e5812-112">KSDATAFORMAT\_SPECIFIER\_MPEG2\_VIDEO</span></span>      |
| <span data-ttu-id="e5812-113">MEDIASUBTYPE \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="e5812-113">MEDIASUBTYPE\_ATSC\_SI</span></span>         | <span data-ttu-id="e5812-114">subtipo de KSDATAFORMAT de \_ \_ ATSC \_ si</span><span class="sxs-lookup"><span data-stu-id="e5812-114">KSDATAFORMAT\_SUBTYPE\_ATSC\_SI</span></span>            |
| <span data-ttu-id="e5812-115">MEDIASUBTYPE \_ Dolby \_ AC3</span><span class="sxs-lookup"><span data-stu-id="e5812-115">MEDIASUBTYPE\_DOLBY\_AC3</span></span>       | <span data-ttu-id="e5812-116">KSDATAFORMAT \_ SubType \_ AC3 \_ audio</span><span class="sxs-lookup"><span data-stu-id="e5812-116">KSDATAFORMAT\_SUBTYPE\_AC3\_AUDIO</span></span>          |
| <span data-ttu-id="e5812-117">MEDIASUBTYPE \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="e5812-117">MEDIASUBTYPE\_DVB\_SI</span></span>          | <span data-ttu-id="e5812-118">subtipo de KSDATAFORMAT \_ \_ DVB \_ si</span><span class="sxs-lookup"><span data-stu-id="e5812-118">KSDATAFORMAT\_SUBTYPE\_DVB\_SI</span></span>             |
| <span data-ttu-id="e5812-119">MEDIASUBTYPE \_ DVD \_ LPCM \_ audio</span><span class="sxs-lookup"><span data-stu-id="e5812-119">MEDIASUBTYPE\_DVD\_LPCM\_AUDIO</span></span> | <span data-ttu-id="e5812-120">KSDATAFORMAT \_ SubType \_ LPCM \_ audio</span><span class="sxs-lookup"><span data-stu-id="e5812-120">KSDATAFORMAT\_SUBTYPE\_LPCM\_AUDIO</span></span>         |
| <span data-ttu-id="e5812-121">\_Audio MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-121">MEDIASUBTYPE\_MPEG2\_AUDIO</span></span>     | <span data-ttu-id="e5812-122">KSDATAFORMAT \_ SubType \_ MPEG2 \_ audio</span><span class="sxs-lookup"><span data-stu-id="e5812-122">KSDATAFORMAT\_SUBTYPE\_MPEG2\_AUDIO</span></span>        |
| <span data-ttu-id="e5812-123">\_Programa MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-123">MEDIASUBTYPE\_MPEG2\_PROGRAM</span></span>   | <span data-ttu-id="e5812-124">\_Tipo de KSDATAFORMAT estático \_ \_ \_ programa MPEG2</span><span class="sxs-lookup"><span data-stu-id="e5812-124">STATIC\_KSDATAFORMAT\_TYPE\_MPEG2\_PROGRAM</span></span> |
| <span data-ttu-id="e5812-125">\_Transporte MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-125">MEDIASUBTYPE\_MPEG2\_TRANSPORT</span></span> | <span data-ttu-id="e5812-126">KSDATAFORMAT \_ tipo \_ de \_ transporte MPEG2</span><span class="sxs-lookup"><span data-stu-id="e5812-126">KSDATAFORMAT\_TYPE\_MPEG2\_TRANSPORT</span></span>       |
| <span data-ttu-id="e5812-127">\_Vídeo MPEG2 de MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-127">MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>     | <span data-ttu-id="e5812-128">Vídeo de KSDATAFORMAT \_ SubType \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e5812-128">KSDATAFORMAT\_SUBTYPE\_MPEG2\_VIDEO</span></span>        |
| <span data-ttu-id="e5812-129">\_Secciones de MPEG2 de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-129">MEDIATYPE\_MPEG2\_SECTIONS</span></span>     | <span data-ttu-id="e5812-130">KSDATAFORMAT \_ tipos de texto \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="e5812-130">KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>        |
| <span data-ttu-id="e5812-131">Audio de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-131">MEDIATYPE\_Audio</span></span>               | <span data-ttu-id="e5812-132">KSDATAFORMAT \_ tipo \_ audio</span><span class="sxs-lookup"><span data-stu-id="e5812-132">KSDATAFORMAT\_TYPE\_AUDIO</span></span>                  |
| <span data-ttu-id="e5812-133">\_PES MPEG2 \_ PE</span><span class="sxs-lookup"><span data-stu-id="e5812-133">MEDIATYPE\_MPEG2\_PES</span></span>          | <span data-ttu-id="e5812-134">KSDATAFORMAT \_ Type \_ MPEG2 \_ PES</span><span class="sxs-lookup"><span data-stu-id="e5812-134">KSDATAFORMAT\_TYPE\_MPEG2\_PES</span></span>             |
| <span data-ttu-id="e5812-135">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="e5812-135">MEDIATYPE\_Video</span></span>               | <span data-ttu-id="e5812-136">\_vídeo de tipo KSDATAFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="e5812-136">KSDATAFORMAT\_TYPE\_VIDEO</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="e5812-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5812-137">Requirements</span></span>



| <span data-ttu-id="e5812-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5812-138">Requirement</span></span> | <span data-ttu-id="e5812-139">Value</span><span class="sxs-lookup"><span data-stu-id="e5812-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5812-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5812-140">Header</span></span><br/> | <dl> <span data-ttu-id="e5812-141"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5812-141"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5812-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5812-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5812-143">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="e5812-143">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




