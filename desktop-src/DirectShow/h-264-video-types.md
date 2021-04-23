---
description: Tipos de vídeo H.264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H.264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692a751e197e2e7bbb088b30dd2a3f5f199d56de
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909023"
---
# <a name="h264-video-types"></a><span data-ttu-id="efbb6-103">Tipos de vídeo H.264</span><span class="sxs-lookup"><span data-stu-id="efbb6-103">H.264 Video Types</span></span>

<span data-ttu-id="efbb6-104">Los siguientes subtipos multimedia se definen para el vídeo H.264.</span><span class="sxs-lookup"><span data-stu-id="efbb6-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="efbb6-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="efbb6-105">Subtype</span></span>                | <span data-ttu-id="efbb6-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="efbb6-106">FOURCC</span></span> | <span data-ttu-id="efbb6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="efbb6-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="efbb6-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="efbb6-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="efbb6-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="efbb6-109">'AVC1'</span></span> | <span data-ttu-id="efbb6-110">Secuencia de bits H.264 sin códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="efbb6-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="efbb6-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="efbb6-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="efbb6-112">'H264'</span><span class="sxs-lookup"><span data-stu-id="efbb6-112">'H264'</span></span> | <span data-ttu-id="efbb6-113">Secuencia de bits H.264 con códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="efbb6-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="efbb6-114">**MEDIASUBTYPE \_ h264**</span><span class="sxs-lookup"><span data-stu-id="efbb6-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="efbb6-115">'h264'</span><span class="sxs-lookup"><span data-stu-id="efbb6-115">'h264'</span></span> | <span data-ttu-id="efbb6-116">Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="efbb6-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="efbb6-117">**MEDIASUBTYPE \_ X264**</span><span class="sxs-lookup"><span data-stu-id="efbb6-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="efbb6-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="efbb6-118">'X264'</span></span> | <span data-ttu-id="efbb6-119">Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="efbb6-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="efbb6-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="efbb6-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="efbb6-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="efbb6-121">'x264'</span></span> | <span data-ttu-id="efbb6-122">Equivalente a **MEDIASUBTYPE \_ H264**, con un FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="efbb6-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="efbb6-123">Estos GUID de subtipo se declaran en wmcodecdsp.h.</span><span class="sxs-lookup"><span data-stu-id="efbb6-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="efbb6-124">La principal diferencia entre estos tipos de medios es la presencia de códigos de inicio en la secuencia de bits.</span><span class="sxs-lookup"><span data-stu-id="efbb6-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="efbb6-125">Si el subtipo es **MEDIASUBTYPE \_ AVC1,** la secuencia de bits no contiene códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="efbb6-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="efbb6-126">Secuencia de bits H.264 con códigos de inicio</span><span class="sxs-lookup"><span data-stu-id="efbb6-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="efbb6-127">Las secuencias de bits H.264 que se transmiten a través del aire, que se encuentran en secuencias de transporte o programas MPEG-2, o que se graban en HD-DVD, tienen el formato descrito en el anexo B de ITU-T Rec. H.264.</span><span class="sxs-lookup"><span data-stu-id="efbb6-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="efbb6-128">Según esta especificación, el flujo de bits consta de una secuencia de unidades de capa de abstracción de red (NALUs), cada una de las cuales tiene un prefijo de código de inicio igual a 0x000001 o 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="efbb6-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="efbb6-129">Cuando los códigos de inicio están presentes en la secuencia de bits, se usa el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="efbb6-129">When start codes are present in the bitstream, the following media type is used:</span></span>



| <span data-ttu-id="efbb6-130">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="efbb6-130">Label</span></span> | <span data-ttu-id="efbb6-131">Value</span><span class="sxs-lookup"><span data-stu-id="efbb6-131">Value</span></span> |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbb6-132">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="efbb6-132">Major type</span></span>  | <span data-ttu-id="efbb6-133">**VÍDEO \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="efbb6-133">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="efbb6-134">Subtipos</span><span class="sxs-lookup"><span data-stu-id="efbb6-134">Subtypes</span></span>    | <span data-ttu-id="efbb6-135">**MEDIASUBTYPE \_ H264,** **MEDIASUBTYPE \_ h264,** **MEDIASUBTYPE \_ X264** o **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="efbb6-135">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="efbb6-136">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="efbb6-136">Format type</span></span> | <span data-ttu-id="efbb6-137">**FORMAT \_ VideoInfo,** **FORMAT \_ VideoInfo2,** **FORMAT \_ MPEG2Video** o **GUID \_ NULL**</span><span class="sxs-lookup"><span data-stu-id="efbb6-137">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="efbb6-138">Si el tipo de formato es **GUID \_ NULL,** no hay ninguna estructura de formato presente.</span><span class="sxs-lookup"><span data-stu-id="efbb6-138">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="efbb6-139">Cuando la secuencia de bits contiene códigos de inicio, cualquiera de los tipos de formato enumerados aquí es suficiente, ya que el descodificador no requiere ninguna información adicional para analizar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="efbb6-139">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="efbb6-140">El flujo de bits ya contiene toda la información necesaria para el descodificador y los códigos de inicio permiten al descodificador localizar el inicio de cada NALU.</span><span class="sxs-lookup"><span data-stu-id="efbb6-140">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="efbb6-141">Los subtipos siguientes son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="efbb6-141">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="efbb6-142">Secuencia de bits H.264 sin códigos de inicio</span><span class="sxs-lookup"><span data-stu-id="efbb6-142">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="efbb6-143">El formato de contenedor MP4 almacena datos H.264 sin códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="efbb6-143">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="efbb6-144">En su lugar, cada NALU tiene el prefijo de un campo de longitud, que proporciona la longitud de NALU en bytes.</span><span class="sxs-lookup"><span data-stu-id="efbb6-144">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="efbb6-145">El tamaño del campo de longitud puede variar, pero normalmente es de 1, 2 o 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="efbb6-145">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="efbb6-146">Cuando los códigos de inicio no están presentes en la secuencia de bits, se usa el siguiente tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="efbb6-146">When start codes are not present in the bitstream, the following media type is used.</span></span>



| <span data-ttu-id="efbb6-147">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="efbb6-147">Label</span></span> | <span data-ttu-id="efbb6-148">Value</span><span class="sxs-lookup"><span data-stu-id="efbb6-148">Value</span></span> |
|-------------|------------------------|
| <span data-ttu-id="efbb6-149">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="efbb6-149">Major type</span></span>  | <span data-ttu-id="efbb6-150">**Vídeo \_ DE MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="efbb6-150">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="efbb6-151">Subtype</span><span class="sxs-lookup"><span data-stu-id="efbb6-151">Subtype</span></span>     | <span data-ttu-id="efbb6-152">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="efbb6-152">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="efbb6-153">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="efbb6-153">Format type</span></span> | <span data-ttu-id="efbb6-154">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="efbb6-154">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="efbb6-155">El bloque de formato es una [**estructura MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)</span><span class="sxs-lookup"><span data-stu-id="efbb6-155">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="efbb6-156">Esta estructura debe rellenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="efbb6-156">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="efbb6-157">**hdr:** estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que describe la secuencia de bits.</span><span class="sxs-lookup"><span data-stu-id="efbb6-157">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="efbb6-158">No hay ninguna tabla de colores después de [**la parte BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la estructura y **biClrUsed** debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="efbb6-158">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="efbb6-159">**dwStartTimeCode:** no se usa.</span><span class="sxs-lookup"><span data-stu-id="efbb6-159">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="efbb6-160">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="efbb6-160">Set to zero.</span></span>
-   <span data-ttu-id="efbb6-161">**cbSequenceHeader:** longitud de la **matriz dwSequenceHeader** en bytes.</span><span class="sxs-lookup"><span data-stu-id="efbb6-161">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="efbb6-162">**dwProfile:** especifica el perfil H.264.</span><span class="sxs-lookup"><span data-stu-id="efbb6-162">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="efbb6-163">**dwLevel:** especifica el nivel H.264.</span><span class="sxs-lookup"><span data-stu-id="efbb6-163">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="efbb6-164">**dwFlags:** número de bytes usados para el campo de longitud que aparece antes de cada **NALU.**</span><span class="sxs-lookup"><span data-stu-id="efbb6-164">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="efbb6-165">El campo length indica el tamaño del siguiente NALU en bytes.</span><span class="sxs-lookup"><span data-stu-id="efbb6-165">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="efbb6-166">Por ejemplo, si **dwFlags** es 4, cada NALU va precedida de un campo de longitud de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="efbb6-166">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="efbb6-167">Los valores válidos son 1, 2 y 4.</span><span class="sxs-lookup"><span data-stu-id="efbb6-167">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="efbb6-168">**dwSequenceHeader:** matriz de bytes que puede contener NALUs de conjunto de parámetros de secuencia (SPS) y conjunto de parámetros de imagen (PPS).</span><span class="sxs-lookup"><span data-stu-id="efbb6-168">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="efbb6-169">El contenedor MP4 puede contener conjuntos de parámetros de secuencia (SPS) o conjuntos de parámetros de imagen (PPS) como unidades NAL especiales en encabezados de archivo o en una secuencia independiente (distinta de la secuencia de vídeo).</span><span class="sxs-lookup"><span data-stu-id="efbb6-169">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="efbb6-170">Cuando se establece el formato, el tipo de medio puede especificar unidades SPS y PPS NAL en la **matriz dwSequenceHeader.**</span><span class="sxs-lookup"><span data-stu-id="efbb6-170">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="efbb6-171">Si **cbSequenceHeader** es mayor que cero, **dwSequenceHeader** es el inicio de una matriz de bytes que contiene SPS y PPS NALUs, delimitado por campos de longitud de 2 bytes, todos en orden de bytes de red (big-endian).</span><span class="sxs-lookup"><span data-stu-id="efbb6-171">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="efbb6-172">Es posible tener SPS y PPS, solo uno de estos tipos o ninguno.</span><span class="sxs-lookup"><span data-stu-id="efbb6-172">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="efbb6-173">El tipo real de cada NALU se puede determinar examinando el campo de tipo de unidad **nal \_ \_** del propio NALU.</span><span class="sxs-lookup"><span data-stu-id="efbb6-173">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="efbb6-174">Cuando se usa este tipo de medio, cada ejemplo multimedia se inicia al principio de una NALU y las unidades NAL no abarcan muestras.</span><span class="sxs-lookup"><span data-stu-id="efbb6-174">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="efbb6-175">Esto permite al descodificador recuperarse de datos dañados o ejemplos eliminados.</span><span class="sxs-lookup"><span data-stu-id="efbb6-175">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



