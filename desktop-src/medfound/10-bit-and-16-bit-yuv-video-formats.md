---
description: En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para la captura, el procesamiento y la visualización de vídeo en el sistema operativo Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: Formatos de vídeo YUV de 10 y 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154467"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="1cb91-103">Formatos de vídeo YUV de 10 y 16 bits</span><span class="sxs-lookup"><span data-stu-id="1cb91-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="1cb91-104">En este tema se describen los formatos YUV de 10 y 16 bits que se recomiendan para la captura, el procesamiento y la visualización de vídeo en el sistema operativo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1cb91-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="1cb91-105">Este tema contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="1cb91-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1cb91-106">Información general</span><span class="sxs-lookup"><span data-stu-id="1cb91-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="1cb91-107">Códigos FOURCC para YUV de 10 bits y de 16 bits</span><span class="sxs-lookup"><span data-stu-id="1cb91-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="1cb91-108">Definiciones de Surface</span><span class="sxs-lookup"><span data-stu-id="1cb91-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="1cb91-109">formatos de 4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="1cb91-110">formatos de 4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="1cb91-111">formatos de 4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="1cb91-112">Formatos YUV preferidos</span><span class="sxs-lookup"><span data-stu-id="1cb91-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="1cb91-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb91-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="1cb91-114">Información general</span><span class="sxs-lookup"><span data-stu-id="1cb91-114">Overview</span></span>

<span data-ttu-id="1cb91-115">Estos formatos usan una representación de punto fijo tanto para el canal de luminancia como para los canales croma (C'b y C'r).</span><span class="sxs-lookup"><span data-stu-id="1cb91-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="1cb91-116">Los valores de ejemplo son valores de 8 bits escalados, con un factor de escala de 2 ^ (n − 8), donde n es 10 o 16, según las secciones 7.7-7.8 y 7.11-7.12 de SMPTE 274M.</span><span class="sxs-lookup"><span data-stu-id="1cb91-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="1cb91-117">Las conversiones de precisión se pueden realizar mediante desplazamientos de bits simples.</span><span class="sxs-lookup"><span data-stu-id="1cb91-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="1cb91-118">Por ejemplo, si el punto blanco de un formato de 8 bits es 235, el formato de 10 bits correspondiente tiene un punto blanco en 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="1cb91-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="1cb91-119">Las representaciones de 16 bits que se describen aquí usan valores de **palabra** Little-Endian para cada canal.</span><span class="sxs-lookup"><span data-stu-id="1cb91-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="1cb91-120">Los formatos de 10 bits también usan 16 bits para cada canal, con los 6 bits inferiores establecidos en cero, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![diagrama que muestra la representación de 10 bits](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="1cb91-122">Dado que las representaciones de 10 bits y de 16 bits del mismo formato YUV tienen el mismo diseño de memoria, es posible convertir una representación de 10 bits en una representación de 16 sin pérdida de precisión.</span><span class="sxs-lookup"><span data-stu-id="1cb91-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="1cb91-123">También es posible convertir una representación de 16 bits en una representación de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="1cb91-124">(Los formatos Y416 y Y410 son una excepción a esta regla general, sin embargo, porque no comparten el mismo diseño de memoria).</span><span class="sxs-lookup"><span data-stu-id="1cb91-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="1cb91-125">Cuando el hardware gráfico Lee una superficie que contiene una representación de 10 bits, debe omitir los 6 bits de orden inferior de cada canal.</span><span class="sxs-lookup"><span data-stu-id="1cb91-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="1cb91-126">Sin embargo, si una superficie contiene datos válidos de 16 bits, debe identificarse como una superficie de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="1cb91-127">En los formatos que contienen alfa, un píxel completamente transparente tiene un valor alfa de cero y un píxel completamente opaco tiene un valor alfa de (2 ^ n) – 1, donde n es el número de bits alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb91-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="1cb91-128">Se supone que alfa es un valor lineal que se aplica a cada componente después de que el componente se haya convertido en su forma lineal normalizada.</span><span class="sxs-lookup"><span data-stu-id="1cb91-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="1cb91-129">En el caso de las imágenes de la memoria de vídeo, el controlador de gráficos selecciona la alineación de memoria de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1cb91-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="1cb91-130">La superficie debe estar alineada con **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="1cb91-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="1cb91-131">Es decir, se garantiza que las líneas individuales dentro de una superficie empiezan en un límite de 32 bits, aunque la alineación puede ser superior a 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="1cb91-132">El origen (0,0) siempre es la esquina superior izquierda de la superficie.</span><span class="sxs-lookup"><span data-stu-id="1cb91-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="1cb91-133">Para los fines de esta documentación, el término *U* es equivalente a *CB* y el término *V* es equivalente a *CR*.</span><span class="sxs-lookup"><span data-stu-id="1cb91-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="1cb91-134">Códigos FOURCC para YUV de 10 bits y de 16 bits</span><span class="sxs-lookup"><span data-stu-id="1cb91-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="1cb91-135">Los códigos FOURCC para los formatos descritos aquí usan la Convención siguiente:</span><span class="sxs-lookup"><span data-stu-id="1cb91-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="1cb91-136">Si el formato es plano, el primer carácter del código FOURCC es ' P '.</span><span class="sxs-lookup"><span data-stu-id="1cb91-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="1cb91-137">Si el formato es empaquetado, el primer carácter es ' Y '.</span><span class="sxs-lookup"><span data-stu-id="1cb91-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="1cb91-138">El segundo carácter del código FOURCC viene determinado por el muestreo de croma, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="1cb91-139">Muestreo de croma</span><span class="sxs-lookup"><span data-stu-id="1cb91-139">Chroma sampling</span></span> | <span data-ttu-id="1cb91-140">Letra de código FOURCC</span><span class="sxs-lookup"><span data-stu-id="1cb91-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="1cb91-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-141">4:4:4</span></span>           | <span data-ttu-id="1cb91-142">4</span><span class="sxs-lookup"><span data-stu-id="1cb91-142">'4'</span></span>                |
    | <span data-ttu-id="1cb91-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-143">4:2:2</span></span>           | <span data-ttu-id="1cb91-144">dos</span><span class="sxs-lookup"><span data-stu-id="1cb91-144">'2'</span></span>                |
    | <span data-ttu-id="1cb91-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="1cb91-145">4:2:1</span></span>           | <span data-ttu-id="1cb91-146">'1'</span><span class="sxs-lookup"><span data-stu-id="1cb91-146">'1'</span></span>                |
    | <span data-ttu-id="1cb91-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-147">4:2:0</span></span>           | <span data-ttu-id="1cb91-148">"0"</span><span class="sxs-lookup"><span data-stu-id="1cb91-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="1cb91-149">Los dos caracteres finales de FOURCC indican el número de bits por canal, ' 16 ' para 16 bits o ' 10 ' para 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="1cb91-150">Con este esquema, se han definido los siguientes códigos FOURCC.</span><span class="sxs-lookup"><span data-stu-id="1cb91-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="1cb91-151">En este momento no se han definido formatos 4:2:1 para el formato YUV de 10 bits o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="1cb91-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="1cb91-152">FOURCC</span></span> | <span data-ttu-id="1cb91-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cb91-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="1cb91-154">P016</span><span class="sxs-lookup"><span data-stu-id="1cb91-154">P016</span></span>   | <span data-ttu-id="1cb91-155">Planar, 4:2:0, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="1cb91-156">P010</span><span class="sxs-lookup"><span data-stu-id="1cb91-156">P010</span></span>   | <span data-ttu-id="1cb91-157">Planar, 4:2:0, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="1cb91-158">P216</span><span class="sxs-lookup"><span data-stu-id="1cb91-158">P216</span></span>   | <span data-ttu-id="1cb91-159">Planar, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="1cb91-160">P210</span><span class="sxs-lookup"><span data-stu-id="1cb91-160">P210</span></span>   | <span data-ttu-id="1cb91-161">Planar, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="1cb91-162">Y216</span><span class="sxs-lookup"><span data-stu-id="1cb91-162">Y216</span></span>   | <span data-ttu-id="1cb91-163">Empaquetado, 4:2:2, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="1cb91-164">Y210</span><span class="sxs-lookup"><span data-stu-id="1cb91-164">Y210</span></span>   | <span data-ttu-id="1cb91-165">Empaquetado, 4:2:2, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="1cb91-166">Y416</span><span class="sxs-lookup"><span data-stu-id="1cb91-166">Y416</span></span>   | <span data-ttu-id="1cb91-167">Empaquetado, 4:4:4, 16 bits</span><span class="sxs-lookup"><span data-stu-id="1cb91-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="1cb91-168">Y410</span><span class="sxs-lookup"><span data-stu-id="1cb91-168">Y410</span></span>   | <span data-ttu-id="1cb91-169">Empaquetado, 4:4:4, 10 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="1cb91-170">Los GUID de subtipo también se han definido a partir de estos FOURCCs; vea [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1cb91-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="1cb91-171">Definiciones de Surface</span><span class="sxs-lookup"><span data-stu-id="1cb91-171">Surface Definitions</span></span>

<span data-ttu-id="1cb91-172">En esta sección se describe el diseño de memoria de cada formato.</span><span class="sxs-lookup"><span data-stu-id="1cb91-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="1cb91-173">En las descripciones siguientes, el término **palabra** hace referencia a un valor de 16 bits Little-endian y el término **DWORD** hace referencia a un valor little-endian de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="1cb91-174">formatos de 4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-174">4:2:0 Formats</span></span>

<span data-ttu-id="1cb91-175">Se definen dos formatos 4:2:0, con los códigos FOURCC P016 y P010.</span><span class="sxs-lookup"><span data-stu-id="1cb91-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="1cb91-176">Comparten el mismo diseño de memoria, pero P016 usa 16 bits por canal y P010 usa 10 bits por canal.</span><span class="sxs-lookup"><span data-stu-id="1cb91-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="1cb91-177">P016 y P010</span><span class="sxs-lookup"><span data-stu-id="1cb91-177">P016 and P010</span></span>

<span data-ttu-id="1cb91-178">En estos dos formatos, todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de **palabras** con un número par de líneas.</span><span class="sxs-lookup"><span data-stu-id="1cb91-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="1cb91-179">El intervalo de superficie puede ser mayor que el ancho del plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="1cb91-180">Esta matriz va seguida inmediatamente por una matriz de **palabras** que contiene ejemplos intercalados y de V, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagrama que muestra el diseño de píxeles de P016 y P010](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="1cb91-182">Si la matriz de U-V combinada se dirige como una matriz de **DWORD** s, la palabra menos significativa (LSW) contiene el valor U y la palabra más significativa (MSW) contiene el valor V.</span><span class="sxs-lookup"><span data-stu-id="1cb91-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="1cb91-183">El intervalo del plano U-V combinado es igual que el intervalo del plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="1cb91-184">El plano U-V tiene la mitad de tantas líneas como el plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="1cb91-185">Estos dos formatos son los formatos de píxel plano de 4:2:0 preferidos para las representaciones YUV de precisión superior.</span><span class="sxs-lookup"><span data-stu-id="1cb91-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="1cb91-186">Se espera que sean un requisito intermedio para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo 4:2:0 de 10 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="1cb91-187">formatos de 4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-187">4:2:2 Formats</span></span>

<span data-ttu-id="1cb91-188">Se definen cuatro formatos de 4:2:2, dos planos y dos empaquetados.</span><span class="sxs-lookup"><span data-stu-id="1cb91-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="1cb91-189">Tienen los siguientes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="1cb91-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="1cb91-190">P216</span><span class="sxs-lookup"><span data-stu-id="1cb91-190">P216</span></span>
-   <span data-ttu-id="1cb91-191">P210</span><span class="sxs-lookup"><span data-stu-id="1cb91-191">P210</span></span>
-   <span data-ttu-id="1cb91-192">Y216</span><span class="sxs-lookup"><span data-stu-id="1cb91-192">Y216</span></span>
-   <span data-ttu-id="1cb91-193">Y210</span><span class="sxs-lookup"><span data-stu-id="1cb91-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="1cb91-194">P216 y P210</span><span class="sxs-lookup"><span data-stu-id="1cb91-194">P216 and P210</span></span>

<span data-ttu-id="1cb91-195">En estos dos formatos planos, todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de **palabras** con un número par de líneas.</span><span class="sxs-lookup"><span data-stu-id="1cb91-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="1cb91-196">El intervalo de superficie puede ser mayor que el ancho del plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="1cb91-197">Esta matriz va seguida inmediatamente por una matriz de **palabras** que contiene ejemplos intercalados y de V, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![diagrama que muestra el diseño de píxeles de P216 y P210](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="1cb91-199">Si la matriz de U-V combinada se dirige como una matriz de **DWORD** s, LSW contiene el valor U y el MSW contiene el valor V.</span><span class="sxs-lookup"><span data-stu-id="1cb91-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="1cb91-200">El intervalo del plano U-V combinado es igual que el intervalo del plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="1cb91-201">El plano U-V tiene el mismo número de líneas que el plano Y.</span><span class="sxs-lookup"><span data-stu-id="1cb91-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="1cb91-202">Estos dos formatos son los formatos de píxel plano de 4:2:2 preferidos para las representaciones YUV de precisión superior.</span><span class="sxs-lookup"><span data-stu-id="1cb91-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="1cb91-203">Se espera que sean un requisito intermedio para los aceleradores de aceleración de vídeo de DirectX (DXVA) que admiten vídeo 4:2:2 de 10 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="1cb91-204">Y216 y Y210</span><span class="sxs-lookup"><span data-stu-id="1cb91-204">Y216 and Y210</span></span>

<span data-ttu-id="1cb91-205">En estos dos formatos empaquetados, cada par de píxeles se almacena como una matriz de cuatro **palabras**, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1cb91-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![diagrama que muestra el diseño de píxeles de Y216 y y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="1cb91-207">La primera **palabra** de la matriz contiene el primer ejemplo y del par, la segunda **palabra** contiene el ejemplo U, la tercera **palabra** contiene el segundo ejemplo y y la cuarta **palabra** contiene el ejemplo V.</span><span class="sxs-lookup"><span data-stu-id="1cb91-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="1cb91-208">Y210 es idéntico a Y216, salvo que cada ejemplo contiene solo 10 bits de datos significativos.</span><span class="sxs-lookup"><span data-stu-id="1cb91-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="1cb91-209">Los 6 bits menos significativos se establecen en cero, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="1cb91-210">formatos de 4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-210">4:4:4 Formats</span></span>

<span data-ttu-id="1cb91-211">Se definen dos formatos 4:4:4, con los códigos FOURCC Y410 y Y416.</span><span class="sxs-lookup"><span data-stu-id="1cb91-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="1cb91-212">Ambos son formatos empaquetados.</span><span class="sxs-lookup"><span data-stu-id="1cb91-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="1cb91-213">Y410</span><span class="sxs-lookup"><span data-stu-id="1cb91-213">Y410</span></span>

<span data-ttu-id="1cb91-214">Este formato es una representación de 10 bits empaquetada que incluye 2 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb91-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="1cb91-215">Cada píxel se codifica como un **DWORD** único con el diseño de memoria que se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="1cb91-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![diagrama que muestra el diseño de píxeles de y410.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="1cb91-217">Los bits 0-9 contienen el ejemplo U, bits 10-19 contienen el ejemplo Y, bits 20-29 contienen el ejemplo V y los bits 30-31 contienen el valor alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb91-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="1cb91-218">Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0x03.</span><span class="sxs-lookup"><span data-stu-id="1cb91-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="1cb91-219">Y416</span><span class="sxs-lookup"><span data-stu-id="1cb91-219">Y416</span></span>

<span data-ttu-id="1cb91-220">Este formato es una representación de 16 bits empaquetada que incluye 16 bits de alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb91-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="1cb91-221">Cada píxel se codifica como un par de **DWORD** s, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1cb91-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![diagrama que muestra el diseño de píxeles de y416.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="1cb91-223">Los bits 0-15 contienen el ejemplo U, bits 16-31 contienen el ejemplo Y, bits 32-47 contienen el ejemplo V y los bits 48-63 contienen el valor alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb91-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="1cb91-224">Para indicar que un píxel es totalmente opaco, una aplicación debe establecer los dos bits alfa iguales a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="1cb91-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="1cb91-225">Este formato está diseñado principalmente como un formato intermedio durante el procesamiento de imágenes para evitar la acumulación de errores.</span><span class="sxs-lookup"><span data-stu-id="1cb91-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="1cb91-226">Formatos YUV preferidos</span><span class="sxs-lookup"><span data-stu-id="1cb91-226">Preferred YUV Formats</span></span>

<span data-ttu-id="1cb91-227">En la tabla siguiente se enumeran los formatos YUV preferidos, incluidos los formatos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="1cb91-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="1cb91-228">Formato</span><span class="sxs-lookup"><span data-stu-id="1cb91-228">Format</span></span> | <span data-ttu-id="1cb91-229">Muestreo de croma</span><span class="sxs-lookup"><span data-stu-id="1cb91-229">Chroma sampling</span></span> | <span data-ttu-id="1cb91-230">Empaquetado o plano</span><span class="sxs-lookup"><span data-stu-id="1cb91-230">Packed or planar</span></span> | <span data-ttu-id="1cb91-231">Bits por canal</span><span class="sxs-lookup"><span data-stu-id="1cb91-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="1cb91-232">AYUV</span><span class="sxs-lookup"><span data-stu-id="1cb91-232">AYUV</span></span>   | <span data-ttu-id="1cb91-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-233">4:4:4</span></span>           | <span data-ttu-id="1cb91-234">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-234">Packed</span></span>           | <span data-ttu-id="1cb91-235">8</span><span class="sxs-lookup"><span data-stu-id="1cb91-235">8</span></span>                |
| <span data-ttu-id="1cb91-236">Y410</span><span class="sxs-lookup"><span data-stu-id="1cb91-236">Y410</span></span>   | <span data-ttu-id="1cb91-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-237">4:4:4</span></span>           | <span data-ttu-id="1cb91-238">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-238">Packed</span></span>           | <span data-ttu-id="1cb91-239">10</span><span class="sxs-lookup"><span data-stu-id="1cb91-239">10</span></span>               |
| <span data-ttu-id="1cb91-240">Y416</span><span class="sxs-lookup"><span data-stu-id="1cb91-240">Y416</span></span>   | <span data-ttu-id="1cb91-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-241">4:4:4</span></span>           | <span data-ttu-id="1cb91-242">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-242">Packed</span></span>           | <span data-ttu-id="1cb91-243">16</span><span class="sxs-lookup"><span data-stu-id="1cb91-243">16</span></span>               |
| <span data-ttu-id="1cb91-244">AI44</span><span class="sxs-lookup"><span data-stu-id="1cb91-244">AI44</span></span>   | <span data-ttu-id="1cb91-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="1cb91-245">4:4:4</span></span>           | <span data-ttu-id="1cb91-246">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-246">Packed</span></span>           | <span data-ttu-id="1cb91-247">Paleta</span><span class="sxs-lookup"><span data-stu-id="1cb91-247">Palettized</span></span>       |
| <span data-ttu-id="1cb91-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="1cb91-248">YUY2</span></span>   | <span data-ttu-id="1cb91-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-249">4:2:2</span></span>           | <span data-ttu-id="1cb91-250">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-250">Packed</span></span>           | <span data-ttu-id="1cb91-251">8</span><span class="sxs-lookup"><span data-stu-id="1cb91-251">8</span></span>                |
| <span data-ttu-id="1cb91-252">Y210</span><span class="sxs-lookup"><span data-stu-id="1cb91-252">Y210</span></span>   | <span data-ttu-id="1cb91-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-253">4:2:2</span></span>           | <span data-ttu-id="1cb91-254">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-254">Packed</span></span>           | <span data-ttu-id="1cb91-255">10</span><span class="sxs-lookup"><span data-stu-id="1cb91-255">10</span></span>               |
| <span data-ttu-id="1cb91-256">Y216</span><span class="sxs-lookup"><span data-stu-id="1cb91-256">Y216</span></span>   | <span data-ttu-id="1cb91-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-257">4:2:2</span></span>           | <span data-ttu-id="1cb91-258">Equipado</span><span class="sxs-lookup"><span data-stu-id="1cb91-258">Packed</span></span>           | <span data-ttu-id="1cb91-259">16</span><span class="sxs-lookup"><span data-stu-id="1cb91-259">16</span></span>               |
| <span data-ttu-id="1cb91-260">P210</span><span class="sxs-lookup"><span data-stu-id="1cb91-260">P210</span></span>   | <span data-ttu-id="1cb91-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-261">4:2:2</span></span>           | <span data-ttu-id="1cb91-262">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-262">Planar</span></span>           | <span data-ttu-id="1cb91-263">10</span><span class="sxs-lookup"><span data-stu-id="1cb91-263">10</span></span>               |
| <span data-ttu-id="1cb91-264">P216</span><span class="sxs-lookup"><span data-stu-id="1cb91-264">P216</span></span>   | <span data-ttu-id="1cb91-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="1cb91-265">4:2:2</span></span>           | <span data-ttu-id="1cb91-266">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-266">Planar</span></span>           | <span data-ttu-id="1cb91-267">16</span><span class="sxs-lookup"><span data-stu-id="1cb91-267">16</span></span>               |
| <span data-ttu-id="1cb91-268">NV12</span><span class="sxs-lookup"><span data-stu-id="1cb91-268">NV12</span></span>   | <span data-ttu-id="1cb91-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-269">4:2:0</span></span>           | <span data-ttu-id="1cb91-270">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-270">Planar</span></span>           | <span data-ttu-id="1cb91-271">8</span><span class="sxs-lookup"><span data-stu-id="1cb91-271">8</span></span>                |
| <span data-ttu-id="1cb91-272">P010</span><span class="sxs-lookup"><span data-stu-id="1cb91-272">P010</span></span>   | <span data-ttu-id="1cb91-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-273">4:2:0</span></span>           | <span data-ttu-id="1cb91-274">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-274">Planar</span></span>           | <span data-ttu-id="1cb91-275">10</span><span class="sxs-lookup"><span data-stu-id="1cb91-275">10</span></span>               |
| <span data-ttu-id="1cb91-276">P016</span><span class="sxs-lookup"><span data-stu-id="1cb91-276">P016</span></span>   | <span data-ttu-id="1cb91-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="1cb91-277">4:2:0</span></span>           | <span data-ttu-id="1cb91-278">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-278">Planar</span></span>           | <span data-ttu-id="1cb91-279">16</span><span class="sxs-lookup"><span data-stu-id="1cb91-279">16</span></span>               |
| <span data-ttu-id="1cb91-280">NV11</span><span class="sxs-lookup"><span data-stu-id="1cb91-280">NV11</span></span>   | <span data-ttu-id="1cb91-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="1cb91-281">4:1:1</span></span>           | <span data-ttu-id="1cb91-282">Trayectoria</span><span class="sxs-lookup"><span data-stu-id="1cb91-282">Planar</span></span>           | <span data-ttu-id="1cb91-283">8</span><span class="sxs-lookup"><span data-stu-id="1cb91-283">8</span></span>                |



 

<span data-ttu-id="1cb91-284">Se recomienda que si un objeto admite una profundidad de bits determinada y un esquema de muestreo de croma, debe admitir los formatos YUV correspondientes que se enumeran en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="1cb91-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="1cb91-285">(Los objetos podrían admitir formatos adicionales que no se enumeran aquí).</span><span class="sxs-lookup"><span data-stu-id="1cb91-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cb91-286">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cb91-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cb91-287">Formatos YUV de 8 bits recomendados para la representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="1cb91-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="1cb91-288">GUID de subtipo de vídeo</span><span class="sxs-lookup"><span data-stu-id="1cb91-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="1cb91-289">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="1cb91-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



