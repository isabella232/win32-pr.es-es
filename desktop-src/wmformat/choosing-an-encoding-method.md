---
title: Elección de un método de codificación
description: Elección de un método de codificación
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- perfiles, elegir métodos de codificación
- perfiles, métodos de codificación
- códecs, elegir métodos de codificación
- códecs, métodos de codificación
- perfiles, seleccionar métodos de codificación
- códecs, seleccionar métodos de codificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695300"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="6d789-109">Elección de un método de codificación</span><span class="sxs-lookup"><span data-stu-id="6d789-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="6d789-110">Algunos códecs, como el códec de Windows Media Video 9, admiten varios métodos de codificación.</span><span class="sxs-lookup"><span data-stu-id="6d789-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="6d789-111">El método de codificación que elija para un flujo dependerá de cómo se entregue la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6d789-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="6d789-112">En la tabla siguiente se describe cuándo usar los distintos métodos de codificación.</span><span class="sxs-lookup"><span data-stu-id="6d789-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="6d789-113">Método de codificación</span><span class="sxs-lookup"><span data-stu-id="6d789-113">Encoding method</span></span>                | <span data-ttu-id="6d789-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d789-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d789-115">1: pasar la velocidad de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="6d789-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="6d789-116">La única opción para el streaming en vivo.</span><span class="sxs-lookup"><span data-stu-id="6d789-116">The only option for live streaming.</span></span> <span data-ttu-id="6d789-117">Codifica en una velocidad de bits predecible y proporciona la calidad más baja de todos los métodos de codificación.</span><span class="sxs-lookup"><span data-stu-id="6d789-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="6d789-118">2-Pass CBR</span><span class="sxs-lookup"><span data-stu-id="6d789-118">2-pass CBR</span></span>                     | <span data-ttu-id="6d789-119">Use para los archivos que se transmitirán por secuencias a través de una red a un lector de cliente, pero que no se difunden desde un origen en directo.</span><span class="sxs-lookup"><span data-stu-id="6d789-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="6d789-120">Codifica en una velocidad de bits predecible, pero con mejor calidad que 1-Pass CBR.</span><span class="sxs-lookup"><span data-stu-id="6d789-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="6d789-121">1: pasar la velocidad de bits variable (VBR)</span><span class="sxs-lookup"><span data-stu-id="6d789-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="6d789-122">Use cuando necesite especificar la calidad de la salida codificada.</span><span class="sxs-lookup"><span data-stu-id="6d789-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="6d789-123">Ofrece la calidad más coherente de todos los métodos de codificación.</span><span class="sxs-lookup"><span data-stu-id="6d789-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="6d789-124">Use solo para archivos locales o para su descarga.</span><span class="sxs-lookup"><span data-stu-id="6d789-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="6d789-125">VBR de dos pasos: sin restricciones</span><span class="sxs-lookup"><span data-stu-id="6d789-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="6d789-126">Use cuando necesite especificar un ancho de banda, pero se aceptan las fluctuaciones en torno al ancho de banda especificado.</span><span class="sxs-lookup"><span data-stu-id="6d789-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="6d789-127">Solo para archivos locales o para descarga.</span><span class="sxs-lookup"><span data-stu-id="6d789-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="6d789-128">VBR de 2 pasos: restringido</span><span class="sxs-lookup"><span data-stu-id="6d789-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="6d789-129">Use en las mismas circunstancias que sin restricciones, pero cuando tenga que especificar una velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="6d789-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="6d789-130">Solo para archivos locales o para descarga.</span><span class="sxs-lookup"><span data-stu-id="6d789-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="6d789-131">En la tabla siguiente se enumeran los métodos de codificación que son compatibles con los códecs que se incluyen con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="6d789-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="6d789-132">Códec</span><span class="sxs-lookup"><span data-stu-id="6d789-132">Codec</span></span>                                  | <span data-ttu-id="6d789-133">CBR</span><span class="sxs-lookup"><span data-stu-id="6d789-133">CBR</span></span> | <span data-ttu-id="6d789-134">2-Pass CBR</span><span class="sxs-lookup"><span data-stu-id="6d789-134">2-pass CBR</span></span> | <span data-ttu-id="6d789-135">VBR</span><span class="sxs-lookup"><span data-stu-id="6d789-135">VBR</span></span> | <span data-ttu-id="6d789-136">VBR de 2 pasos</span><span class="sxs-lookup"><span data-stu-id="6d789-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="6d789-137">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6d789-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="6d789-138">X</span><span class="sxs-lookup"><span data-stu-id="6d789-138">X</span></span>   | <span data-ttu-id="6d789-139">X</span><span class="sxs-lookup"><span data-stu-id="6d789-139">X</span></span>          | <span data-ttu-id="6d789-140">X</span><span class="sxs-lookup"><span data-stu-id="6d789-140">X</span></span>   | <span data-ttu-id="6d789-141">X</span><span class="sxs-lookup"><span data-stu-id="6d789-141">X</span></span>          |
| <span data-ttu-id="6d789-142">Windows Media Audio 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="6d789-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="6d789-143">X</span><span class="sxs-lookup"><span data-stu-id="6d789-143">X</span></span>   | <span data-ttu-id="6d789-144">X</span><span class="sxs-lookup"><span data-stu-id="6d789-144">X</span></span>          | <span data-ttu-id="6d789-145">X</span><span class="sxs-lookup"><span data-stu-id="6d789-145">X</span></span>   | <span data-ttu-id="6d789-146">X</span><span class="sxs-lookup"><span data-stu-id="6d789-146">X</span></span>          |
| <span data-ttu-id="6d789-147">Pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6d789-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="6d789-148">X</span><span class="sxs-lookup"><span data-stu-id="6d789-148">X</span></span>   |            | <span data-ttu-id="6d789-149">X</span><span class="sxs-lookup"><span data-stu-id="6d789-149">X</span></span>   |            |
| <span data-ttu-id="6d789-150">Windows Media Audio 9 Voice</span><span class="sxs-lookup"><span data-stu-id="6d789-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="6d789-151">X</span><span class="sxs-lookup"><span data-stu-id="6d789-151">X</span></span>   |            |     |            |
| <span data-ttu-id="6d789-152">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="6d789-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="6d789-153">X</span><span class="sxs-lookup"><span data-stu-id="6d789-153">X</span></span>   | <span data-ttu-id="6d789-154">X</span><span class="sxs-lookup"><span data-stu-id="6d789-154">X</span></span>          | <span data-ttu-id="6d789-155">X</span><span class="sxs-lookup"><span data-stu-id="6d789-155">X</span></span>   | <span data-ttu-id="6d789-156">X</span><span class="sxs-lookup"><span data-stu-id="6d789-156">X</span></span>          |
| <span data-ttu-id="6d789-157">Windows Media Audio sin pérdida de</span><span class="sxs-lookup"><span data-stu-id="6d789-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="6d789-158">X</span><span class="sxs-lookup"><span data-stu-id="6d789-158">X</span></span>   |            |
| <span data-ttu-id="6d789-159">Imagen de Windows Media Video 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="6d789-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="6d789-160">X</span><span class="sxs-lookup"><span data-stu-id="6d789-160">X</span></span>   |            | <span data-ttu-id="6d789-161">X</span><span class="sxs-lookup"><span data-stu-id="6d789-161">X</span></span>   |            |
| <span data-ttu-id="6d789-162">Perfil avanzado de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6d789-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="6d789-163">X</span><span class="sxs-lookup"><span data-stu-id="6d789-163">X</span></span>   | <span data-ttu-id="6d789-164">X</span><span class="sxs-lookup"><span data-stu-id="6d789-164">X</span></span>          | <span data-ttu-id="6d789-165">X</span><span class="sxs-lookup"><span data-stu-id="6d789-165">X</span></span>   | <span data-ttu-id="6d789-166">X</span><span class="sxs-lookup"><span data-stu-id="6d789-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="6d789-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6d789-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d789-168">**Diseñar perfiles**</span><span class="sxs-lookup"><span data-stu-id="6d789-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="6d789-169">**Codificación de velocidad de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="6d789-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="6d789-170">**Codificación de dos pasos**</span><span class="sxs-lookup"><span data-stu-id="6d789-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="6d789-171">**Codificación de velocidad de bits variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="6d789-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




