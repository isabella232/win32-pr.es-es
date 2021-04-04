---
description: Tipos de vídeo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997628"
---
# <a name="h264-video-types"></a><span data-ttu-id="0172e-103">Tipos de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="0172e-103">H.264 Video Types</span></span>

<span data-ttu-id="0172e-104">Los siguientes subtipos de medios se definen para el vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="0172e-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="0172e-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="0172e-105">Subtype</span></span>                | <span data-ttu-id="0172e-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="0172e-106">FOURCC</span></span> | <span data-ttu-id="0172e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0172e-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="0172e-108">**MEDIASUBTYPE \_ avc1**</span><span class="sxs-lookup"><span data-stu-id="0172e-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="0172e-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="0172e-109">'AVC1'</span></span> | <span data-ttu-id="0172e-110">H. 264 fragmentada sin códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="0172e-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="0172e-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="0172e-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="0172e-112">H264</span><span class="sxs-lookup"><span data-stu-id="0172e-112">'H264'</span></span> | <span data-ttu-id="0172e-113">H. 264 fragmentada con códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="0172e-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="0172e-114">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="0172e-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="0172e-115">H264</span><span class="sxs-lookup"><span data-stu-id="0172e-115">'h264'</span></span> | <span data-ttu-id="0172e-116">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente.</span><span class="sxs-lookup"><span data-stu-id="0172e-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="0172e-117">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="0172e-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="0172e-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="0172e-118">'X264'</span></span> | <span data-ttu-id="0172e-119">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente.</span><span class="sxs-lookup"><span data-stu-id="0172e-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="0172e-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="0172e-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="0172e-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="0172e-121">'x264'</span></span> | <span data-ttu-id="0172e-122">Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diferente.</span><span class="sxs-lookup"><span data-stu-id="0172e-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="0172e-123">Estos GUID de subtipos se declaran en wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="0172e-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="0172e-124">La diferencia principal entre estos tipos de medios es la presencia de códigos de inicio en el fragmentada.</span><span class="sxs-lookup"><span data-stu-id="0172e-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="0172e-125">Si el subtipo es **MEDIASUBTYPE \_ avc1**, el fragmentada no contiene códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="0172e-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="0172e-126">H. 264 fragmentada con códigos de inicio</span><span class="sxs-lookup"><span data-stu-id="0172e-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="0172e-127">Los bitstreams de H. 264 que se transmiten a través del aire o que se encuentran en flujos de programa o transporte MPEG-2, o grabados en HD-DVD, se formatean como se describe en el Anexo B de ITU-T Rec. H. 264.</span><span class="sxs-lookup"><span data-stu-id="0172e-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="0172e-128">Según esta especificación, fragmentada consta de una secuencia de unidades de capa de abstracción de red (NALUs), cada una de las cuales tiene como prefijo un código de inicio igual a 0x000001 o 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="0172e-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="0172e-129">Cuando los códigos de inicio están presentes en fragmentada, se usa el siguiente tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="0172e-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0172e-130">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="0172e-130">Major type</span></span>  | <span data-ttu-id="0172e-131">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0172e-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="0172e-132">Subtipos</span><span class="sxs-lookup"><span data-stu-id="0172e-132">Subtypes</span></span>    | <span data-ttu-id="0172e-133">**MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** o **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="0172e-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="0172e-134">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="0172e-134">Format type</span></span> | <span data-ttu-id="0172e-135">**Formato \_ Videoinfo**, **format \_ VideoInfo2**, **format \_ MPEG2Video** o **GUID \_ null**</span><span class="sxs-lookup"><span data-stu-id="0172e-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="0172e-136">Si el tipo de formato es **GUID \_ null**, no hay ninguna estructura de formato presente.</span><span class="sxs-lookup"><span data-stu-id="0172e-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="0172e-137">Cuando fragmentada contiene códigos de inicio, cualquiera de los tipos de formato enumerados aquí es suficiente, porque el descodificador no requiere ninguna información adicional para analizar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0172e-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="0172e-138">El fragmentada ya contiene toda la información que necesita el descodificador y los códigos de inicio permiten al descodificador localizar el inicio de cada NALU.</span><span class="sxs-lookup"><span data-stu-id="0172e-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="0172e-139">Los siguientes subtipos son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="0172e-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="0172e-140">H. 264 fragmentada sin códigos de inicio</span><span class="sxs-lookup"><span data-stu-id="0172e-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="0172e-141">El formato de contenedor MP4 almacena datos de H. 264 sin códigos de inicio.</span><span class="sxs-lookup"><span data-stu-id="0172e-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="0172e-142">En su lugar, cada NALU tiene como prefijo un campo de longitud, que proporciona la longitud de NALU en bytes.</span><span class="sxs-lookup"><span data-stu-id="0172e-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="0172e-143">El tamaño del campo de longitud puede variar, pero suele ser de 1, 2 o 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="0172e-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="0172e-144">Cuando los códigos de inicio no están presentes en fragmentada, se usa el siguiente tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="0172e-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="0172e-145">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="0172e-145">Major type</span></span>  | <span data-ttu-id="0172e-146">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0172e-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="0172e-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="0172e-147">Subtype</span></span>     | <span data-ttu-id="0172e-148">**MEDIASUBTYPE \_ avc1**</span><span class="sxs-lookup"><span data-stu-id="0172e-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="0172e-149">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="0172e-149">Format type</span></span> | <span data-ttu-id="0172e-150">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="0172e-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="0172e-151">El bloque Format es una estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="0172e-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="0172e-152">Esta estructura se debe rellenar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="0172e-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="0172e-153">**HDR**: una estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que describe el fragmentada.</span><span class="sxs-lookup"><span data-stu-id="0172e-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="0172e-154">No hay ninguna tabla de colores presente después de la parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de la estructura y **biClrUsed** debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0172e-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="0172e-155">**dwStartTimeCode**: no se usa.</span><span class="sxs-lookup"><span data-stu-id="0172e-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="0172e-156">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="0172e-156">Set to zero.</span></span>
-   <span data-ttu-id="0172e-157">**cbSequenceHeader**: la longitud de la matriz de **dwSequenceHeader** en bytes.</span><span class="sxs-lookup"><span data-stu-id="0172e-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="0172e-158">**dwProfile**: especifica el perfil H. 264.</span><span class="sxs-lookup"><span data-stu-id="0172e-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="0172e-159">**dwLevel**: especifica el nivel H. 264.</span><span class="sxs-lookup"><span data-stu-id="0172e-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="0172e-160">**dwFlags**: el número de bytes usados para el campo de longitud que aparece antes de cada **Nalu**.</span><span class="sxs-lookup"><span data-stu-id="0172e-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="0172e-161">El campo de longitud indica el tamaño de los siguientes NALU en bytes.</span><span class="sxs-lookup"><span data-stu-id="0172e-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="0172e-162">Por ejemplo, si **dwFlags** es 4, cada Nalu va precedido de un campo de longitud de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="0172e-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="0172e-163">Los valores válidos son 1, 2 y 4.</span><span class="sxs-lookup"><span data-stu-id="0172e-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="0172e-164">**dwSequenceHeader**: una matriz de bytes que puede contener el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="0172e-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="0172e-165">El contenedor MP4 podría contener conjuntos de parámetros de secuencia (SPS) o conjuntos de parámetros de imagen (PPS) como unidades NAL especiales en encabezados de archivo o en una secuencia independiente (distinta de la secuencia de vídeo).</span><span class="sxs-lookup"><span data-stu-id="0172e-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="0172e-166">Cuando se establece el formato, el tipo de medio puede especificar las unidades de SPS y de PPS NAL en la matriz **dwSequenceHeader** .</span><span class="sxs-lookup"><span data-stu-id="0172e-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="0172e-167">Si **cbSequenceHeader** es mayor que cero, **dwSequenceHeader** es el inicio de una matriz de bytes que contiene SPS y PPS NALUs, delimitado por campos de longitud de 2 bytes, todo ello en el orden de bytes de la red (Big-endian).</span><span class="sxs-lookup"><span data-stu-id="0172e-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="0172e-168">Es posible tener SPS y PPS, solo uno de estos tipos, o ninguno.</span><span class="sxs-lookup"><span data-stu-id="0172e-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="0172e-169">El tipo real de cada NALU se puede determinar mediante el examen del campo de **\_ \_ tipo de unidad nal** del mismo Nalu.</span><span class="sxs-lookup"><span data-stu-id="0172e-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="0172e-170">Cuando se usa este tipo de medio, cada ejemplo multimedia se inicia al principio de un NALU y las unidades NAL no abarcan los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="0172e-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="0172e-171">Esto permite que el descodificador se recupere de los datos dañados o ejemplos quitados.</span><span class="sxs-lookup"><span data-stu-id="0172e-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



