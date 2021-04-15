---
description: Tipos de medios de demultiplexador MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipos de medios de demultiplexador MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689658"
---
# <a name="mpeg-2-demultiplexer-media-types"></a><span data-ttu-id="78df3-103">Tipos de medios de demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="78df3-103">MPEG-2 Demultiplexer Media Types</span></span>

<span data-ttu-id="78df3-104">El filtro de [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) reconoce los siguientes tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="78df3-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) filter recognizes the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="78df3-105">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="78df3-105">Input Types</span></span>

<span data-ttu-id="78df3-106">El tipo principal siempre es **el \_ flujo de MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="78df3-106">The major type is always **MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="78df3-107">El subtipo puede ser cualquiera de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="78df3-107">The subtype can be any of the following.</span></span>



| <span data-ttu-id="78df3-108">GUID</span><span class="sxs-lookup"><span data-stu-id="78df3-108">GUID</span></span>                                             | <span data-ttu-id="78df3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="78df3-109">Description</span></span>                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78df3-110">**Subtipo de KSDATAFORMAT de \_ \_ \_ transporte MPEG2 BDA \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-110">**KSDATAFORMAT\_SUBTYPE\_BDA\_MPEG2\_TRANSPORT**</span></span> | <span data-ttu-id="78df3-111">Secuencia de transporte de un filtro de dispositivo de la arquitectura de controlador de difusión (BDA).</span><span class="sxs-lookup"><span data-stu-id="78df3-111">Transport stream from a Broadcast Driver Architecture (BDA) device filter.</span></span> <span data-ttu-id="78df3-112">El desmultiplexador MPEG-2 trata este subtipo de manera idéntica a **MEDIASUBTYPE \_ MPEG2 \_ Transport**.</span><span class="sxs-lookup"><span data-stu-id="78df3-112">The MPEG-2 demultiplexer treats this subtype identically to **MEDIASUBTYPE\_MPEG2\_TRANSPORT**.</span></span>                                |
| <span data-ttu-id="78df3-113">**\_Programa MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-113">**MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>                 | <span data-ttu-id="78df3-114">Secuencia de programa</span><span class="sxs-lookup"><span data-stu-id="78df3-114">Program stream</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="78df3-115">**\_Transporte MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-115">**MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>               | <span data-ttu-id="78df3-116">Secuencia de transporte (TS), con paquetes de 188 bytes</span><span class="sxs-lookup"><span data-stu-id="78df3-116">Transport stream (TS), with 188-byte packets</span></span>                                                                                                                                                              |
| <span data-ttu-id="78df3-117">**\_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-117">**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**</span></span>       | <span data-ttu-id="78df3-118">Secuencia de transporte con paquetes "progresados".</span><span class="sxs-lookup"><span data-stu-id="78df3-118">Transport stream with "strided" packets.</span></span> <span data-ttu-id="78df3-119">Este subtipo indica que los paquetes de TS se pueden rellenar con bytes adicionales.</span><span class="sxs-lookup"><span data-stu-id="78df3-119">This subtype indicates that the TS packets may be padded with extra bytes.</span></span> <span data-ttu-id="78df3-120">Para obtener más información, [**consulte \_ \_ intervalo de transporte de MPEG2**](mpeg2-transport-stride.md).</span><span class="sxs-lookup"><span data-stu-id="78df3-120">For more information, see [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> |



 

<span data-ttu-id="78df3-121">En el caso de los paquetes de transporte más progresados (intervalo de transporte de MPEG2 de MEDIASUBTYPE), cada ejemplo de medio debe contener un número entero de paquetes de transporte, tal y como se describe en [**intervalo de \_ transporte \_ de MPEG2**](mpeg2-transport-stride.md).**\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-121">For strided transport packets (**MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE**), each media sample must contain an integral number of transport packets, as described in [**MPEG2\_TRANSPORT\_STRIDE**](mpeg2-transport-stride.md).</span></span> <span data-ttu-id="78df3-122">Para el resto de tipos de entrada, no hay restricciones en los límites de muestra; los paquetes individuales pueden abarcar los límites de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="78df3-122">For all other input types, there are no restrictions on sample boundaries; individual packets can span sample boundaries.</span></span>

### <a name="output-types"></a><span data-ttu-id="78df3-123">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="78df3-123">Output Types</span></span>

<span data-ttu-id="78df3-124">El desmultiplexador MPEG-2 no valida los tipos de salida; el filtro de nivel inferior es responsable de analizar los datos que recibe del desmultiplexador.</span><span class="sxs-lookup"><span data-stu-id="78df3-124">The MPEG-2 Demultiplexer does not validate output types; the downstream filter is responsible for parsing the data it receives from the demultiplexer.</span></span> <span data-ttu-id="78df3-125">Sin embargo, los filtros inferiores aceptan normalmente los siguientes tipos como resultado del desmultiplexador.</span><span class="sxs-lookup"><span data-stu-id="78df3-125">However, the following types are commonly accepted by downstream filters as output from the demultiplexer.</span></span>

### <a name="mpeg-2-sections"></a><span data-ttu-id="78df3-126">Secciones MPEG-2</span><span class="sxs-lookup"><span data-stu-id="78df3-126">MPEG-2 Sections</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="78df3-127">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="78df3-127">Major Type</span></span></td>
<td><span data-ttu-id="78df3-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span><span class="sxs-lookup"><span data-stu-id="78df3-128"><strong>MEDIATYPE_MPEG2_SECTIONS</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="78df3-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="78df3-129">Subtype</span></span></td>
<td><span data-ttu-id="78df3-130">Cualquiera de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="78df3-130">Any of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="78df3-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: información del servicio ATSC.</span><span class="sxs-lookup"><span data-stu-id="78df3-131"><strong>MEDIASUBTYPE_ATSC_SI</strong>: ATSC Service Information.</span></span></li>
<li><span data-ttu-id="78df3-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: información del servicio DVB.</span><span class="sxs-lookup"><span data-stu-id="78df3-132"><strong>MEDIASUBTYPE_DVB_SI</strong>: DVB Service Information.</span></span></li>
<li><span data-ttu-id="78df3-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: información del servicio de difusión digital de servicios integrados (ISDB).</span><span class="sxs-lookup"><span data-stu-id="78df3-133"><strong>MEDIASUBTYPE_ISDB_SI</strong>: Integrated Services Digital Broadcasting (ISDB) Service Information.</span></span></li>
<li><span data-ttu-id="78df3-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: datos de la sección MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="78df3-134"><strong>MEDIASUBTYPE_MPEG2DATA</strong>: MPEG-2 section data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="78df3-135">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="78df3-135">Format Type</span></span></td>
<td><span data-ttu-id="78df3-136">None</span><span class="sxs-lookup"><span data-stu-id="78df3-136">None</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a><span data-ttu-id="78df3-137">Vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="78df3-137">MPEG-2 Video</span></span>



|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="78df3-138">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="78df3-138">Major type</span></span>       | <span data-ttu-id="78df3-139">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-139">**MEDIATYPE\_Video**</span></span>                     |
| <span data-ttu-id="78df3-140">Subtype</span><span class="sxs-lookup"><span data-stu-id="78df3-140">Subtype</span></span>          | <span data-ttu-id="78df3-141">**\_Vídeo MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-141">**MEDIASUBTYPE\_MPEG2\_VIDEO**</span></span>           |
| <span data-ttu-id="78df3-142">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="78df3-142">Format Type</span></span>      | <span data-ttu-id="78df3-143">**FORMATO \_ MPEG2Video**</span><span class="sxs-lookup"><span data-stu-id="78df3-143">**FORMAT\_MPEG2Video**</span></span>                   |
| <span data-ttu-id="78df3-144">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="78df3-144">Format Structure</span></span> | [<span data-ttu-id="78df3-145">**MPEG2VIDEOINFO**</span><span class="sxs-lookup"><span data-stu-id="78df3-145">**MPEG2VIDEOINFO**</span></span>](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a><span data-ttu-id="78df3-146">Audio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="78df3-146">MPEG-2 Audio</span></span>



|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="78df3-147">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="78df3-147">Major type</span></span>       | <span data-ttu-id="78df3-148">**Audio de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-148">**MEDIATYPE\_Audio**</span></span>                 |
| <span data-ttu-id="78df3-149">Subtype</span><span class="sxs-lookup"><span data-stu-id="78df3-149">Subtype</span></span>          | <span data-ttu-id="78df3-150">**\_Audio MPEG2 de MEDIASUBTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="78df3-150">**MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span>       |
| <span data-ttu-id="78df3-151">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="78df3-151">Format Type</span></span>      | <span data-ttu-id="78df3-152">**DAR formato a \_ WaveFormatEx**</span><span class="sxs-lookup"><span data-stu-id="78df3-152">**FORMAT\_WaveFormatEx**</span></span>             |
| <span data-ttu-id="78df3-153">Estructura de formato</span><span class="sxs-lookup"><span data-stu-id="78df3-153">Format Structure</span></span> | <span data-ttu-id="78df3-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78df3-154">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="78df3-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78df3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78df3-156">Tipos de medios MPEG-2</span><span class="sxs-lookup"><span data-stu-id="78df3-156">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 
