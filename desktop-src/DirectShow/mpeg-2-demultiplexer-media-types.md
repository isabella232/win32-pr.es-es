---
description: Tipos de medios de demultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de medios de demultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910003"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="7dff3-103">Tipos de medios de demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7dff3-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="7dff3-104">El [filtro Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) reconoce los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="7dff3-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="7dff3-105">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="7dff3-105">Input Types</span></span>

<span data-ttu-id="7dff3-106">El tipo principal es siempre **MEDIATYPE \_ Stream.**</span><span class="sxs-lookup"><span data-stu-id="7dff3-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="7dff3-107">El subtipo puede ser cualquiera de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="7dff3-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="7dff3-108">GUID</span><span class="sxs-lookup"><span data-stu-id="7dff3-108">GUID</span></span>                                             | <span data-ttu-id="7dff3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dff3-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dff3-110">**TRANSPORTE DE \_ \_ BDA \_ MPEG2 DEL SUBTIPO KSDATAFORMAT \_**</span><span class="sxs-lookup"><span data-stu-id="7dff3-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="7dff3-111">Flujo de transporte desde un filtro de dispositivo de arquitectura de controlador de difusión (BDA).</span><span class="sxs-lookup"><span data-stu-id="7dff3-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="7dff3-112">El demultiplexador MPEG-2 trata este subtipo de forma idéntica a **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT.**</span><span class="sxs-lookup"><span data-stu-id="7dff3-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="7dff3-113">**PROGRAMA \_ MPEG2 DE MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="7dff3-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="7dff3-114">Secuencia de programa</span><span class="sxs-lookup"><span data-stu-id="7dff3-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="7dff3-115">**TRANSPORTE DE MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="7dff3-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="7dff3-116">Secuencia de transporte (TS), con paquetes de 188 bytes</span><span class="sxs-lookup"><span data-stu-id="7dff3-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="7dff3-117">**MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="7dff3-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="7dff3-118">Flujo de transporte con paquetes "strided".</span><span class="sxs-lookup"><span data-stu-id="7dff3-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="7dff3-119">Este subtipo indica que los paquetes TS se pueden agregar con bytes adicionales.</span><span class="sxs-lookup"><span data-stu-id="7dff3-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="7dff3-120">Para obtener más información, [**vea MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="7dff3-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="7dff3-121">Para los paquetes de transporte strided **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE),** cada ejemplo multimedia debe contener un número entero de paquetes de transporte, como se describe en [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="7dff3-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="7dff3-122">Para todos los demás tipos de entrada, no hay ninguna restricción en los límites de ejemplo; los paquetes individuales pueden abarcar límites de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7dff3-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="7dff3-123">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="7dff3-123">Output Types</span></span>

<span data-ttu-id="7dff3-124">Demultiplexer MPEG-2 no valida los tipos de salida; El filtro de nivel inferior es responsable de analizar los datos que recibe del demultiplexor.</span><span class="sxs-lookup"><span data-stu-id="7dff3-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="7dff3-125">Sin embargo, los siguientes tipos se aceptan normalmente mediante filtros de bajada como salida del demultiplexor.</span><span class="sxs-lookup"><span data-stu-id="7dff3-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="7dff3-126">Secciones mpeg-2</span><span class="sxs-lookup"><span data-stu-id="7dff3-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7dff3-127">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="7dff3-127">Major Type</span></span></td>
<td><span data-ttu-id="7dff3-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="7dff3-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7dff3-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="7dff3-129">Subtype</span></span></td>
<td><span data-ttu-id="7dff3-130">Cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7dff3-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="7dff3-131"><strong>MEDIASUBTYPE_ATSC_SI:</strong>información del servicio ATSC.</span><span class="sxs-lookup"><span data-stu-id="7dff3-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="7dff3-132"><strong>MEDIASUBTYPE_DVB_SI:</strong>información del servicio DE VEZ.</span><span class="sxs-lookup"><span data-stu-id="7dff3-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="7dff3-133"><strong>MEDIASUBTYPE_ISDB_SI:</strong>Información del servicio de difusión digital de servicios integrados (ISDB).</span><span class="sxs-lookup"><span data-stu-id="7dff3-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="7dff3-134"><strong>MEDIASUBTYPE_MPEG2DATA:</strong>datos de sección MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="7dff3-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7dff3-135">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="7dff3-135">Format Type</span></span></td>
<td><span data-ttu-id="7dff3-136">None</span><span class="sxs-lookup"><span data-stu-id="7dff3-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="7dff3-137">VÍDEO MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7dff3-137">MPEG-2 Video</span></span>



| <span data-ttu-id="7dff3-138">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="7dff3-138">Label</span></span> | <span data-ttu-id="7dff3-139">Value</span><span class="sxs-lookup"><span data-stu-id="7dff3-139">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="7dff3-140">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="7dff3-140">Major type</span></span>       | <span data-ttu-id="7dff3-141">**VÍDEO \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="7dff3-141">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="7dff3-142">Subtype</span><span class="sxs-lookup"><span data-stu-id="7dff3-142">Subtype</span></span>          | <span data-ttu-id="7dff3-143">**VÍDEO DE MEDIASUBTYPE \_ MPEG2 \_**</span><span class="sxs-lookup"><span data-stu-id="7dff3-143">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="7dff3-144">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="7dff3-144">Format Type</span></span>      | <span data-ttu-id="7dff3-145">**FORMAT \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="7dff3-145">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="7dff3-146">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="7dff3-146">Format Structure</span></span> | [<span data-ttu-id="7dff3-147">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="7dff3-147">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="7dff3-148">MPEG-2 Audio</span><span class="sxs-lookup"><span data-stu-id="7dff3-148">MPEG-2 Audio</span></span>



| <span data-ttu-id="7dff3-149">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="7dff3-149">Label</span></span> | <span data-ttu-id="7dff3-150">Value</span><span class="sxs-lookup"><span data-stu-id="7dff3-150">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="7dff3-151">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="7dff3-151">Major type</span></span>       | <span data-ttu-id="7dff3-152">**MEDIATYPE \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="7dff3-152">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="7dff3-153">Subtype</span><span class="sxs-lookup"><span data-stu-id="7dff3-153">Subtype</span></span>          | <span data-ttu-id="7dff3-154">**MEDIASUBTYPE \_ MPEG2 \_ AUDIO**</span><span class="sxs-lookup"><span data-stu-id="7dff3-154">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="7dff3-155">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="7dff3-155">Format Type</span></span>      | <span data-ttu-id="7dff3-156">**FORMAT \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="7dff3-156">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="7dff3-157">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="7dff3-157">Format Structure</span></span> | <span data-ttu-id="7dff3-158">[**FORMA DE ONDAATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7dff3-158">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7dff3-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dff3-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dff3-160">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="7dff3-160">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
