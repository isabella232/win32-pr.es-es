---
description: Se han definido varios subtipos para vídeo DV. Cada una tiene un código FOURCC y un valor GUID correspondiente. No se admiten todos estos formatos; Vea la sección Comentarios para obtener más información.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Subtipos de vídeo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680735"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="223b5-105">Subtipos de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="223b5-105">DV Video Subtypes</span></span>

<span data-ttu-id="223b5-106">Se han definido varios subtipos para vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="223b5-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="223b5-107">Cada una tiene un código FOURCC y un valor GUID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="223b5-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="223b5-108">No se admiten todos estos formatos; Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="223b5-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="223b5-109">Formatos de consumidor</span><span class="sxs-lookup"><span data-stu-id="223b5-109">Consumer Formats</span></span>



| <span data-ttu-id="223b5-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="223b5-110">FOURCC</span></span> | <span data-ttu-id="223b5-111">GUID</span><span class="sxs-lookup"><span data-stu-id="223b5-111">GUID</span></span>               | <span data-ttu-id="223b5-112">Velocidad de datos</span><span class="sxs-lookup"><span data-stu-id="223b5-112">Data Rate</span></span> | <span data-ttu-id="223b5-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b5-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="223b5-114">'dvsl'</span><span class="sxs-lookup"><span data-stu-id="223b5-114">'dvsl'</span></span> | <span data-ttu-id="223b5-115">MEDIASUBTYPE \_ DVSL</span><span class="sxs-lookup"><span data-stu-id="223b5-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="223b5-116">12,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-116">12.5 Mbps</span></span> | <span data-ttu-id="223b5-117">SD-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="223b5-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="223b5-118">'dvsd'</span><span class="sxs-lookup"><span data-stu-id="223b5-118">'dvsd'</span></span> | <span data-ttu-id="223b5-119">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="223b5-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="223b5-120">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-120">25 Mbps</span></span>   | <span data-ttu-id="223b5-121">SDL-DVCR (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="223b5-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="223b5-122">'dvhd'</span><span class="sxs-lookup"><span data-stu-id="223b5-122">'dvhd'</span></span> | <span data-ttu-id="223b5-123">MEDIASUBTYPE \_ dvhd</span><span class="sxs-lookup"><span data-stu-id="223b5-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="223b5-124">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-124">50 Mbps</span></span>   | <span data-ttu-id="223b5-125">HD-DVCR (1125-60 o 1250-50)</span><span class="sxs-lookup"><span data-stu-id="223b5-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="223b5-126">Consulte IEC-61834 para obtener más información acerca de estos formatos.</span><span class="sxs-lookup"><span data-stu-id="223b5-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="223b5-127">Formatos profesionales</span><span class="sxs-lookup"><span data-stu-id="223b5-127">Professional Formats</span></span>



| <span data-ttu-id="223b5-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="223b5-128">FOURCC</span></span> | <span data-ttu-id="223b5-129">GUID</span><span class="sxs-lookup"><span data-stu-id="223b5-129">GUID</span></span>               | <span data-ttu-id="223b5-130">Velocidad de datos</span><span class="sxs-lookup"><span data-stu-id="223b5-130">Data Rate</span></span> | <span data-ttu-id="223b5-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b5-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="223b5-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="223b5-132">'dv25'</span></span> | <span data-ttu-id="223b5-133">MEDIASUBTYPE \_ DV25</span><span class="sxs-lookup"><span data-stu-id="223b5-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="223b5-134">25 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-134">25 Mbps</span></span>   | <span data-ttu-id="223b5-135">DVCPRO 25 (525-60 o 625-50).</span><span class="sxs-lookup"><span data-stu-id="223b5-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="223b5-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="223b5-136">'dv50'</span></span> | <span data-ttu-id="223b5-137">MEDIASUBTYPE \_ DV50</span><span class="sxs-lookup"><span data-stu-id="223b5-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="223b5-138">50 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-138">50 Mbps</span></span>   | <span data-ttu-id="223b5-139">DVCPRO 50 (525-60 o 625-50)</span><span class="sxs-lookup"><span data-stu-id="223b5-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="223b5-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="223b5-140">'dvh1'</span></span> | <span data-ttu-id="223b5-141">MEDIASUBTYPE \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="223b5-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="223b5-142">100 Mbps</span><span class="sxs-lookup"><span data-stu-id="223b5-142">100 Mbps</span></span>  | <span data-ttu-id="223b5-143">DVCPRO 100 (1080/60i, 1080/50i o 720/60P)</span><span class="sxs-lookup"><span data-stu-id="223b5-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="223b5-144">Consulte SMPTE 314M para obtener más información sobre DV25 y DV50, y SMPTE 370M para obtener más información sobre dvh1.</span><span class="sxs-lookup"><span data-stu-id="223b5-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="223b5-145">Varios</span><span class="sxs-lookup"><span data-stu-id="223b5-145">Miscellaneous</span></span>

<span data-ttu-id="223b5-146">En el archivo de encabezado UUID. h se definen dos subtipos de DV adicionales.</span><span class="sxs-lookup"><span data-stu-id="223b5-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="223b5-147">Estos se corresponden con los códigos FOURCC generados por determinados códecs DV; no se corresponden con ninguna de las normas DV definidas.</span><span class="sxs-lookup"><span data-stu-id="223b5-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="223b5-148">Estos subtipos están obsoletos y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="223b5-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="223b5-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="223b5-149">FOURCC</span></span> | <span data-ttu-id="223b5-150">GUID</span><span class="sxs-lookup"><span data-stu-id="223b5-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="223b5-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="223b5-151">'DVCS'</span></span> | <span data-ttu-id="223b5-152">MEDIASUBTYPE \_ DVCS</span><span class="sxs-lookup"><span data-stu-id="223b5-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="223b5-153">'DVSD'</span><span class="sxs-lookup"><span data-stu-id="223b5-153">'DVSD'</span></span> | <span data-ttu-id="223b5-154">MEDIASUBTYPE \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="223b5-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="223b5-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="223b5-155">Remarks</span></span>

<span data-ttu-id="223b5-156">En la tabla siguiente se muestran las tarifas de datos admitidas, en megabits por segundo (Mbps), para los controladores MSDV y UVC.</span><span class="sxs-lookup"><span data-stu-id="223b5-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="223b5-157">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="223b5-157">Operating System</span></span>                                                                 | <span data-ttu-id="223b5-158">Controlador MSDV (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="223b5-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="223b5-159">Controlador UVC</span><span class="sxs-lookup"><span data-stu-id="223b5-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="223b5-160">Windows XP Service Pack 1 o anterior</span><span class="sxs-lookup"><span data-stu-id="223b5-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="223b5-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="223b5-161">12.5, 25</span></span>                | <span data-ttu-id="223b5-162">No disponible</span><span class="sxs-lookup"><span data-stu-id="223b5-162">Not available</span></span> |
| <span data-ttu-id="223b5-163">Windows XP Service Pack 2 o posterior, Windows Server 2003 Service Pack 1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="223b5-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="223b5-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="223b5-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="223b5-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="223b5-165">12.5, 25</span></span>      |



 

<span data-ttu-id="223b5-166">En el caso de las secuencias de 25 Mbps, el comportamiento del controlador MSDV ha cambiado en Windows vista antes de Windows Vista, el controlador MSDV siempre establece el tipo de medio en MEDIASUBTYPE \_ DVSD para flujos de 25 Mbps, independientemente de si el origen es SDL-DVCR o DVCPRO 25.</span><span class="sxs-lookup"><span data-stu-id="223b5-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="223b5-167">No se usó el tipo de medio ' DV25 '.</span><span class="sxs-lookup"><span data-stu-id="223b5-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="223b5-168">A partir de Windows Vista, el controlador MSDV ahora distingue entre estos dos formatos.</span><span class="sxs-lookup"><span data-stu-id="223b5-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="223b5-169">Para SDL-DVCR, sigue usando el subtipo "DVSD".</span><span class="sxs-lookup"><span data-stu-id="223b5-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="223b5-170">En el caso de DVCPRO 25, ahora usa el subtipo ' DV25 '.</span><span class="sxs-lookup"><span data-stu-id="223b5-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="223b5-171">Los filtros de [divisor DV](dv-splitter-filter.md) de DirectShow y de [descodificador de vídeo DV](dv-video-decoder-filter.md) solo admiten los formatos SDL-DVCR.</span><span class="sxs-lookup"><span data-stu-id="223b5-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="223b5-172">Los datos pueden ser PAL o NTSC.</span><span class="sxs-lookup"><span data-stu-id="223b5-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="223b5-173">Pueden estar disponibles filtros o códecs de terceros que puedan analizar otros formatos DV, siempre que el controlador MSDV o UVC admita la velocidad de datos.</span><span class="sxs-lookup"><span data-stu-id="223b5-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="223b5-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="223b5-174">Requirements</span></span>



| <span data-ttu-id="223b5-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="223b5-175">Requirement</span></span> | <span data-ttu-id="223b5-176">Value</span><span class="sxs-lookup"><span data-stu-id="223b5-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="223b5-177">Encabezado</span><span class="sxs-lookup"><span data-stu-id="223b5-177">Header</span></span><br/> | <dl> <span data-ttu-id="223b5-178"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="223b5-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223b5-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="223b5-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223b5-180">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="223b5-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="223b5-181">Controlador MSDV</span><span class="sxs-lookup"><span data-stu-id="223b5-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="223b5-182">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="223b5-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




