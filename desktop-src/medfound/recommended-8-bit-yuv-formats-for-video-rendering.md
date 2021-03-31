---
description: Formatos YUV de 8 bits recomendados para la representación de vídeo
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Formatos YUV de 8 bits recomendados para la representación de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811569"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="287f5-103">Formatos YUV de 8 bits recomendados para la representación de vídeo</span><span class="sxs-lookup"><span data-stu-id="287f5-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="287f5-104">Gary Sullivan y Stephen Estrop</span><span class="sxs-lookup"><span data-stu-id="287f5-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="287f5-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="287f5-105">Microsoft Corporation</span></span>

<span data-ttu-id="287f5-106">2002 de abril, actualizado el 2008 de noviembre</span><span class="sxs-lookup"><span data-stu-id="287f5-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="287f5-107">En este tema se describen los formatos de color YUV de 8 bits que se recomiendan para la representación de vídeo en el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="287f5-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="287f5-108">En este artículo se presentan técnicas para la conversión entre formatos YUV y RGB, y también se proporcionan técnicas para el muestreo de formatos YUV.</span><span class="sxs-lookup"><span data-stu-id="287f5-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="287f5-109">Este artículo está destinado a cualquier persona que trabaje con la descodificación o representación de vídeo YUV en Windows.</span><span class="sxs-lookup"><span data-stu-id="287f5-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="287f5-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="287f5-110">Introduction</span></span>

<span data-ttu-id="287f5-111">Muchos formatos YUV se definen en todo el sector del vídeo.</span><span class="sxs-lookup"><span data-stu-id="287f5-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="287f5-112">En este artículo se identifican los formatos YUV de 8 bits que se recomiendan para la representación de vídeo en Windows.</span><span class="sxs-lookup"><span data-stu-id="287f5-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="287f5-113">Se recomienda a los proveedores de descodificadores y mostrar los proveedores que admitan los formatos descritos en este artículo.</span><span class="sxs-lookup"><span data-stu-id="287f5-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="287f5-114">En este artículo no se tratan otros usos del color YUV, como la fotografía todavía.</span><span class="sxs-lookup"><span data-stu-id="287f5-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="287f5-115">En los formatos descritos en este artículo se usa una ubicación de 8 bits por píxel para codificar el canal Y (también denominado canal de luminancia) y usar 8 bits por muestra para codificar cada ejemplo de croma U o V.</span><span class="sxs-lookup"><span data-stu-id="287f5-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="287f5-116">Sin embargo, la mayoría de los formatos YUV usan menos de 24 bits por píxel en promedio, ya que contienen menos muestras de usted y V que de Y. En este artículo no se tratan los formatos YUV con canales Y de 10 bits o superior.</span><span class="sxs-lookup"><span data-stu-id="287f5-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="287f5-117">Para los fines de este artículo, el término U es equivalente a CB y el término V es equivalente a CR.</span><span class="sxs-lookup"><span data-stu-id="287f5-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="287f5-118">En este artículo se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="287f5-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="287f5-119">[Muestreo YUV](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="287f5-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="287f5-120">Describe las técnicas de muestreo YUV más comunes.</span><span class="sxs-lookup"><span data-stu-id="287f5-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="287f5-121">[Definiciones de Surface](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="287f5-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="287f5-122">Describe los formatos YUV recomendados.</span><span class="sxs-lookup"><span data-stu-id="287f5-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="287f5-123">[Conversiones del espacio de colores y de la frecuencia de muestreo de croma](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="287f5-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="287f5-124">Proporciona algunas directrices para la conversión entre formatos YUV y RGB, y para la conversión entre distintos formatos YUV.</span><span class="sxs-lookup"><span data-stu-id="287f5-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="287f5-125">[Identificar formatos YUV en Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="287f5-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="287f5-126">Explica cómo describir los tipos de formato YUV en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="287f5-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="287f5-127">Muestreo YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-127">YUV Sampling</span></span>

<span data-ttu-id="287f5-128">Los canales de croma pueden tener una velocidad de muestreo inferior a la del canal de luminancia, sin ninguna pérdida dramática de calidad perceptual.</span><span class="sxs-lookup"><span data-stu-id="287f5-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="287f5-129">Una notación denominada "A:B: C" se usa para describir la frecuencia con la que se muestrean y las V en relación con Y:</span><span class="sxs-lookup"><span data-stu-id="287f5-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="287f5-130">4:4:4 significa que no hay una disminución de la resolución de los canales de croma.</span><span class="sxs-lookup"><span data-stu-id="287f5-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="287f5-131">4:2:2 significa una disminución de la resolución horizontal de 2:1, sin disminución de la resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="287f5-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="287f5-132">Cada línea de exploración contiene cuatro ejemplos Y por cada uno de los dos ejemplos U o V.</span><span class="sxs-lookup"><span data-stu-id="287f5-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="287f5-133">4:2:0 significa disminución de la reducción horizontal de 2:1, con una disminución de resolución de 2:1.</span><span class="sxs-lookup"><span data-stu-id="287f5-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="287f5-134">4:1:1 significa una disminución de la resolución horizontal de 4:1, sin disminución de la resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="287f5-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="287f5-135">Cada línea de exploración contiene cuatro ejemplos y para cada ejemplo de cada usuario y V.</span><span class="sxs-lookup"><span data-stu-id="287f5-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="287f5-136">el muestreo 4:1:1 es menos común que otros formatos y no se describe en detalle en este artículo.</span><span class="sxs-lookup"><span data-stu-id="287f5-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="287f5-137">En los diagramas siguientes se muestra cómo se muestrea el cromado para cada una de las tasas de reducción de la resolución.</span><span class="sxs-lookup"><span data-stu-id="287f5-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="287f5-138">Los ejemplos de luminancia se representan mediante una cruz y las muestras de croma se representan mediante un círculo.</span><span class="sxs-lookup"><span data-stu-id="287f5-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![Figura 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="287f5-141">La forma dominante de muestreo 4:2:2 se define en la recomendación de ITU-R BT. 601.</span><span class="sxs-lookup"><span data-stu-id="287f5-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="287f5-142">Hay dos variantes comunes del muestreo 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="287f5-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="287f5-143">Uno de ellos se usa en vídeo MPEG-2 y el otro se usa en MPEG-1 y en las recomendaciones de ITU-T H. 261 y H. 263.</span><span class="sxs-lookup"><span data-stu-id="287f5-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="287f5-144">En comparación con el esquema MPEG-1, es más fácil convertir entre el esquema MPEG-2 y las cuadrículas de muestreo definidas para los formatos 4:2:2 y 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="287f5-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="287f5-145">Por esta razón, se prefiere el esquema MPEG-2 en Windows y se debe considerar la interpretación predeterminada de los formatos 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="287f5-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="287f5-146">Definiciones de Surface</span><span class="sxs-lookup"><span data-stu-id="287f5-146">Surface Definitions</span></span>

<span data-ttu-id="287f5-147">En esta sección se describen los formatos YUV de 8 bits que se recomiendan para la representación de vídeo.</span><span class="sxs-lookup"><span data-stu-id="287f5-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="287f5-148">Estas se dividen en varias categorías:</span><span class="sxs-lookup"><span data-stu-id="287f5-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="287f5-149">formatos 4:4:4, 32 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="287f5-150">formatos de 4:2:2, 16 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="287f5-151">formatos de 4:2:0, 16 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="287f5-152">4:2:0 formatos, 12 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="287f5-153">En primer lugar, debe tener en cuenta los siguientes conceptos para comprender lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="287f5-154">*Origen* de la superficie.</span><span class="sxs-lookup"><span data-stu-id="287f5-154">*Surface origin*.</span></span> <span data-ttu-id="287f5-155">En el caso de los formatos YUV descritos en este artículo, el origen (0,0) siempre es la esquina superior izquierda de la superficie.</span><span class="sxs-lookup"><span data-stu-id="287f5-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="287f5-156">*STRIDE*.</span><span class="sxs-lookup"><span data-stu-id="287f5-156">*Stride*.</span></span> <span data-ttu-id="287f5-157">El paso de una superficie, a veces denominado paso, es el ancho de la superficie en bytes.</span><span class="sxs-lookup"><span data-stu-id="287f5-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="287f5-158">Dado un origen de superficie en la esquina superior izquierda, el intervalo siempre es positivo.</span><span class="sxs-lookup"><span data-stu-id="287f5-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="287f5-159">*Alineación*.</span><span class="sxs-lookup"><span data-stu-id="287f5-159">*Alignment*.</span></span> <span data-ttu-id="287f5-160">La alineación de una superficie es a discreción del controlador de pantalla de gráficos.</span><span class="sxs-lookup"><span data-stu-id="287f5-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="287f5-161">La superficie siempre debe estar alineada con DWORD; es decir, se garantiza que las líneas individuales dentro de la superficie se originen en un límite de 32 bits (DWORD).</span><span class="sxs-lookup"><span data-stu-id="287f5-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="287f5-162">Sin embargo, la alineación puede ser superior a 32 bits, en función de las necesidades del hardware.</span><span class="sxs-lookup"><span data-stu-id="287f5-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="287f5-163">Formato empaquetado frente al formato plano.</span><span class="sxs-lookup"><span data-stu-id="287f5-163">Packed format versus planar format.</span></span> <span data-ttu-id="287f5-164">Los formatos YUV se dividen en formatos *empaquetados* y formatos *planos* .</span><span class="sxs-lookup"><span data-stu-id="287f5-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="287f5-165">En un formato empaquetado, los componentes Y, U y V se almacenan en una sola matriz.</span><span class="sxs-lookup"><span data-stu-id="287f5-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="287f5-166">Los píxeles se organizan en grupos de macropixels, cuyo diseño depende del formato.</span><span class="sxs-lookup"><span data-stu-id="287f5-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="287f5-167">En un formato plano, los componentes Y, U y V se almacenan como tres planos independientes.</span><span class="sxs-lookup"><span data-stu-id="287f5-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="287f5-168">Cada uno de los formatos YUV descritos en este artículo tiene un código FOURCC asignado.</span><span class="sxs-lookup"><span data-stu-id="287f5-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="287f5-169">Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="287f5-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="287f5-170">4:4:4 (32 BPP)</span><span class="sxs-lookup"><span data-stu-id="287f5-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="287f5-171">AYUV</span><span class="sxs-lookup"><span data-stu-id="287f5-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="287f5-172">4:2:2 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="287f5-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="287f5-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="287f5-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="287f5-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="287f5-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="287f5-175">4:2:0 (16 BPP)</span><span class="sxs-lookup"><span data-stu-id="287f5-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="287f5-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="287f5-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="287f5-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="287f5-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="287f5-178">4:2:0 (12 BPP)</span><span class="sxs-lookup"><span data-stu-id="287f5-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="287f5-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="287f5-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="287f5-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="287f5-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="287f5-181">YV12</span><span class="sxs-lookup"><span data-stu-id="287f5-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="287f5-182">NV12</span><span class="sxs-lookup"><span data-stu-id="287f5-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="287f5-183">formatos 4:4:4, 32 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="287f5-184">AYUV</span><span class="sxs-lookup"><span data-stu-id="287f5-184">AYUV</span></span>

<span data-ttu-id="287f5-185">Se recomienda un solo formato 4:4:4, con el código FOURCC AYUV.</span><span class="sxs-lookup"><span data-stu-id="287f5-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="287f5-186">Se trata de un formato empaquetado, donde cada píxel se codifica como cuatro bytes consecutivos, organizados en la secuencia que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="287f5-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![Figura 2.](images/yuvformats01.gif)

<span data-ttu-id="287f5-189">Los bytes marcados como contienen valores para alfa.</span><span class="sxs-lookup"><span data-stu-id="287f5-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="287f5-190">formatos de 4:2:2, 16 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="287f5-191">Se recomiendan dos formatos 4:2:2, con los siguientes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="287f5-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="287f5-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="287f5-192">YUY2</span></span>
-   <span data-ttu-id="287f5-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="287f5-193">UYVY</span></span>

<span data-ttu-id="287f5-194">Ambos son formatos empaquetados, donde cada macropixel es dos píxeles codificados como cuatro bytes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="287f5-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="287f5-195">Esto da como resultado una disminución de la intensidad horizontal del croma en un factor de dos.</span><span class="sxs-lookup"><span data-stu-id="287f5-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="287f5-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="287f5-196">YUY2</span></span>

<span data-ttu-id="287f5-197">En el formato YUY2, los datos se pueden tratar como una matriz de valores **Char** sin signo, donde el primer byte contiene el primer ejemplo y, el segundo byte contiene el primer ejemplo de U (CB), el tercer byte contiene el segundo ejemplo y y el cuarto byte contiene el primer ejemplo V (CR), como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="287f5-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![Figura 3.](images/yuvformats02.gif)

<span data-ttu-id="287f5-200">Si la imagen se dirige como una matriz de valores de **palabra** Little-endian, la primera **palabra** contiene el primer ejemplo y en los bits menos significativos (LSBs) y el primer ejemplo de U (CB) en los bits más significativos (MSBs).</span><span class="sxs-lookup"><span data-stu-id="287f5-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="287f5-201">La segunda **palabra** contiene el segundo ejemplo y en el LSBs y el primer ejemplo V (CR) de MSBs.</span><span class="sxs-lookup"><span data-stu-id="287f5-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="287f5-202">YUY2 es el formato de 4:2:2 píxeles preferido para la aceleración de vídeo de Microsoft DirectX (DirectX VA).</span><span class="sxs-lookup"><span data-stu-id="287f5-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="287f5-203">Se espera que sea un requisito intermedio para los aceleradores de DirectX, que admiten vídeo de 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="287f5-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="287f5-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="287f5-204">UYVY</span></span>

<span data-ttu-id="287f5-205">Este formato es el mismo que el formato YUY2, excepto en que se invierte el orden de los bytes; es decir, se voltean los bytes de croma y luminancia (Figura 4).</span><span class="sxs-lookup"><span data-stu-id="287f5-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="287f5-206">Si la imagen se dirige como una matriz de dos valores de **palabra** Little-endian, la primera **palabra** contiene U en LSBs y Y0 en MSBs, y la segunda **palabra** contiene V en LSBs y Y1 en el MSBs.</span><span class="sxs-lookup"><span data-stu-id="287f5-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![Figura 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="287f5-209">formatos de 4:2:0, 16 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="287f5-210">Se recomiendan dos formatos de 4:2:0 16 bits por píxel (BPP), con los siguientes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="287f5-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="287f5-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="287f5-211">IMC1</span></span>
-   <span data-ttu-id="287f5-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="287f5-212">IMC3</span></span>

<span data-ttu-id="287f5-213">Ambos formatos YUV son formatos planos.</span><span class="sxs-lookup"><span data-stu-id="287f5-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="287f5-214">Los canales de croma se submuestran por un factor de dos en las dimensiones horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="287f5-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="287f5-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="287f5-215">IMC1</span></span>

<span data-ttu-id="287f5-216">Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo.</span><span class="sxs-lookup"><span data-stu-id="287f5-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="287f5-217">A continuación se muestran todos los ejemplos de V (CR) y, a continuación, todos los ejemplos de U (CB).</span><span class="sxs-lookup"><span data-stu-id="287f5-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="287f5-218">Los planos V y U tienen el mismo intervalo que el plano Y, lo que da lugar a áreas de memoria no utilizadas, tal como se muestra en la figura 5.</span><span class="sxs-lookup"><span data-stu-id="287f5-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="287f5-219">Los planos de ti y V deben comenzar en los límites de memoria que tengan un múltiplo de 16 líneas.</span><span class="sxs-lookup"><span data-stu-id="287f5-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="287f5-220">En la figura 5 se muestra el origen de usted y V para un fotograma de vídeo 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="287f5-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="287f5-221">La dirección inicial de los planos de ti y V se calcula de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="287f5-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="287f5-222">donde *py* es un puntero de byte al inicio de la matriz de memoria, tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="287f5-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![Figura 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="287f5-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="287f5-225">IMC3</span></span>

<span data-ttu-id="287f5-226">Este formato es idéntico a IMC1, excepto en que se intercambian los planos usted y V, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="287f5-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![Figura 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="287f5-229">4:2:0 formatos, 12 bits por píxel</span><span class="sxs-lookup"><span data-stu-id="287f5-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="287f5-230">Se recomiendan cuatro formatos 4:2:0 12-BPP, con los siguientes códigos FOURCC:</span><span class="sxs-lookup"><span data-stu-id="287f5-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="287f5-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="287f5-231">IMC2</span></span>
-   <span data-ttu-id="287f5-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="287f5-232">IMC4</span></span>
-   <span data-ttu-id="287f5-233">YV12</span><span class="sxs-lookup"><span data-stu-id="287f5-233">YV12</span></span>
-   <span data-ttu-id="287f5-234">NV12</span><span class="sxs-lookup"><span data-stu-id="287f5-234">NV12</span></span>

<span data-ttu-id="287f5-235">En todos estos formatos, los canales de croma se submuestran por un factor de dos en las dimensiones horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="287f5-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="287f5-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="287f5-236">IMC2</span></span>

<span data-ttu-id="287f5-237">Este formato es el mismo que el de IMC1, excepto por la diferencia siguiente: las líneas V (CR) y U (CB) se intercalan en los límites de medio STRIDE.</span><span class="sxs-lookup"><span data-stu-id="287f5-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="287f5-238">En otras palabras, cada línea de paso completo en el área de croma comienza con una línea de ejemplos de V, seguida de una línea de muestras de U que comienza en el siguiente límite de intervalo medio (Figura 7).</span><span class="sxs-lookup"><span data-stu-id="287f5-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="287f5-239">Este diseño hace un uso más eficaz del espacio de direcciones que IMC1.</span><span class="sxs-lookup"><span data-stu-id="287f5-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="287f5-240">Reduce el espacio de direcciones de croma en la mitad y, por tanto, el espacio de direcciones total en un 25 por ciento.</span><span class="sxs-lookup"><span data-stu-id="287f5-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="287f5-241">Entre los formatos 4:2:0, IMC2 es el segundo formato preferido, después de NV12.</span><span class="sxs-lookup"><span data-stu-id="287f5-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="287f5-242">En la imagen siguiente se ilustra este proceso.</span><span class="sxs-lookup"><span data-stu-id="287f5-242">The following image illustrates this process.</span></span>

![Figura 7.](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="287f5-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="287f5-245">IMC4</span></span>

<span data-ttu-id="287f5-246">Este formato es idéntico a IMC2, excepto que se intercambian las líneas U (CB) y V (CR), tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="287f5-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![Ilustración 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="287f5-249">YV12</span><span class="sxs-lookup"><span data-stu-id="287f5-249">YV12</span></span>

<span data-ttu-id="287f5-250">Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo.</span><span class="sxs-lookup"><span data-stu-id="287f5-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="287f5-251">Esta matriz va seguida inmediatamente de todos los ejemplos V (CR).</span><span class="sxs-lookup"><span data-stu-id="287f5-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="287f5-252">El paso del plano V es la mitad del intervalo del plano Y; y el plano V contiene la mitad de tantas líneas como el plano Y.</span><span class="sxs-lookup"><span data-stu-id="287f5-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="287f5-253">El plano V va seguido inmediatamente de todos los ejemplos de U (CB), con el mismo intervalo y número de líneas que el plano V, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="287f5-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![Ilustración 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="287f5-256">NV12</span><span class="sxs-lookup"><span data-stu-id="287f5-256">NV12</span></span>

<span data-ttu-id="287f5-257">Todos los ejemplos Y aparecen en primer lugar en la memoria como una matriz de valores **Char** sin signo con un número par de líneas.</span><span class="sxs-lookup"><span data-stu-id="287f5-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="287f5-258">El plano Y va seguido inmediatamente de una matriz de valores **Char** sin signo que contiene ejemplos empaquetados de U (CB) y V (CR).</span><span class="sxs-lookup"><span data-stu-id="287f5-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="287f5-259">Cuando la matriz de U-V combinada se dirige como una matriz de valores de **palabra** Little-endian, LSBs contiene los valores U y MSBs contiene los valores V.</span><span class="sxs-lookup"><span data-stu-id="287f5-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="287f5-260">NV12 es el formato preferido de 4:2:0 píxeles para DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="287f5-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="287f5-261">Se espera que sea un requisito intermedio para los aceleradores de DirectX, que admiten vídeo de 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="287f5-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="287f5-262">En la ilustración siguiente se muestra el plano y y la matriz que contiene ejemplos empaquetados y de V.</span><span class="sxs-lookup"><span data-stu-id="287f5-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![Figura 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="287f5-265">Conversiones del espacio de colores y de la frecuencia de muestreo de croma</span><span class="sxs-lookup"><span data-stu-id="287f5-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="287f5-266">En esta sección se proporcionan instrucciones para la conversión entre YUV y RGB, y para la conversión entre algunos formatos YUV diferentes.</span><span class="sxs-lookup"><span data-stu-id="287f5-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="287f5-267">Tenemos en cuenta dos esquemas de codificación RGB en esta sección: *RGB de 8 bits*, también conocido como sRGB o "RGB de imagen a gran escala", RGB de *estudio de vídeo* o "RGB con sala de cabezas".</span><span class="sxs-lookup"><span data-stu-id="287f5-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="287f5-268">Se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="287f5-268">These are defined as follows:</span></span>

-   <span data-ttu-id="287f5-269">El equipo RGB usa 8 bits para cada muestra de rojo, verde y azul.</span><span class="sxs-lookup"><span data-stu-id="287f5-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="287f5-270">El color negro se representa mediante R = G = B = 0 y el blanco se representa mediante R = G = B = 255.</span><span class="sxs-lookup"><span data-stu-id="287f5-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="287f5-271">Studio video RGB usa un número de bits N para cada muestra de rojo, verde y azul, donde N es 8 o más.</span><span class="sxs-lookup"><span data-stu-id="287f5-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="287f5-272">El vídeo RGB de Studio usa un factor de escala diferente del de equipo RGB y tiene un desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="287f5-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="287f5-273">El negro se representa mediante R = G = B = 16 \* 2 ^ (N-8) y el blanco se representa mediante r = G = B = 235 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="287f5-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="287f5-274">Sin embargo, los valores reales pueden quedar fuera de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="287f5-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="287f5-275">Studio video RGB es la definición de RGB preferida para el vídeo en Windows, mientras que el equipo RGB es la definición de RGB preferida para las aplicaciones que no son de vídeo.</span><span class="sxs-lookup"><span data-stu-id="287f5-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="287f5-276">En cualquier forma de RGB, las coordenadas de cromaticidad se especifican en ITU-R BT. 709 para la definición de los valores primarios de color RGB.</span><span class="sxs-lookup"><span data-stu-id="287f5-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="287f5-277">Las coordenadas (x, y) de R, G y B son (0,64, 0,33), (0,30, 0,60) y (0,15, 0,06), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="287f5-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="287f5-278">El blanco de referencia es D65 con coordenadas (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="287f5-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="287f5-279">La gamma nominal es de 1/0.45 (aproximadamente 2,2), con un gamma preciso definido en detalle en ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="287f5-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="287f5-280">**Conversión entre RGB y 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="287f5-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="287f5-281">En primer lugar, se describe la conversión entre RGB y 4:4:4 YUV.</span><span class="sxs-lookup"><span data-stu-id="287f5-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="287f5-282">Para convertir 4:2:0 o 4:2:2 YUV en RGB, se recomienda convertir los datos de YUV en 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="287f5-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="287f5-283">El formato AYUV, que es un formato 4:4:4, usa 8 bits cada uno para los ejemplos Y, U y V.</span><span class="sxs-lookup"><span data-stu-id="287f5-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="287f5-284">YUV también puede definirse con más de 8 bits por muestra para algunas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="287f5-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="287f5-285">Se han definido dos conversiones de YUV dominantes de RGB para vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="287f5-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="287f5-286">Ambos se basan en la especificación conocida como recomendación de ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="287f5-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="287f5-287">La primera conversión es el formato YUV anterior definido para el uso de 50 Hz en BT. 709.</span><span class="sxs-lookup"><span data-stu-id="287f5-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="287f5-288">Es igual que la relación especificada en la recomendación de ITU-R BT. 601, también conocida por su nombre anterior, CCIR 601.</span><span class="sxs-lookup"><span data-stu-id="287f5-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="287f5-289">Se debe considerar el formato YUV preferido para la resolución de TV de definición estándar (720 x 576) y el vídeo de menor resolución.</span><span class="sxs-lookup"><span data-stu-id="287f5-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="287f5-290">Se caracteriza por los valores de dos constantes *KR* y *KB*:</span><span class="sxs-lookup"><span data-stu-id="287f5-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="287f5-291">La segunda conversión es el formulario YUV más reciente definido para el uso de 60 Hz en BT. 709 y debe considerarse el formato preferido para las resoluciones de vídeo anteriores a SDTV.</span><span class="sxs-lookup"><span data-stu-id="287f5-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="287f5-292">Se caracteriza por valores diferentes para estas dos constantes:</span><span class="sxs-lookup"><span data-stu-id="287f5-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="287f5-293">La conversión de RGB a YUV se define a partir de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="287f5-294">Los valores YUV se obtienen de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="287f5-295">where</span><span class="sxs-lookup"><span data-stu-id="287f5-295">where</span></span>

-   <span data-ttu-id="287f5-296">M es el número de bits por muestra YUV (M >= 8).</span><span class="sxs-lookup"><span data-stu-id="287f5-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="287f5-297">Z es la variable de nivel negro.</span><span class="sxs-lookup"><span data-stu-id="287f5-297">Z is the black-level variable.</span></span> <span data-ttu-id="287f5-298">En el caso del equipo RGB, Z es igual a 0.</span><span class="sxs-lookup"><span data-stu-id="287f5-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="287f5-299">En Studio video RGB, Z \* es igual a 16 2 ^ (n-8), donde N es el número de bits por ejemplo RGB (n >= 8).</span><span class="sxs-lookup"><span data-stu-id="287f5-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="287f5-300">S es la variable de escalado.</span><span class="sxs-lookup"><span data-stu-id="287f5-300">S is the scaling variable.</span></span> <span data-ttu-id="287f5-301">En el caso del equipo RGB, S es igual a 255.</span><span class="sxs-lookup"><span data-stu-id="287f5-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="287f5-302">Para Studio video RGB, S es igual \* a 219 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="287f5-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="287f5-303">La función Floor (x) devuelve el número entero más grande menor o igual que x.</span><span class="sxs-lookup"><span data-stu-id="287f5-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="287f5-304">La función clip3 (x, y, z) se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="287f5-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="287f5-305">clip3 debe implementarse como una función en lugar de una macro de preprocesador; de lo contrario, se producirán varias evaluaciones de los argumentos.</span><span class="sxs-lookup"><span data-stu-id="287f5-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="287f5-306">El ejemplo Y representa el brillo, y los ejemplos de ti y V representan las desviaciones de color hacia el azul y el rojo, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="287f5-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="287f5-307">El intervalo nominal para Y es 16 \* 2 ^ (m-8) a 235 \* 2 ^ (M-8).</span><span class="sxs-lookup"><span data-stu-id="287f5-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="287f5-308">El color negro se representa como 16 \* 2 ^ (m-8) y el blanco se representa como 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="287f5-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="287f5-309">El intervalo nominal para usted y V son 16 \* 2 ^ (m-8) a 240 \* 2 ^ (M-8), con el valor 128 \* 2 ^ (m-8) que representa el croma neutro.</span><span class="sxs-lookup"><span data-stu-id="287f5-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="287f5-310">Sin embargo, los valores reales pueden estar fuera de estos intervalos.</span><span class="sxs-lookup"><span data-stu-id="287f5-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="287f5-311">En el caso de los datos de entrada con el formato de vídeo RGB de Studio, la operación de recorte es necesaria para mantener los valores de ti y V en el intervalo de 0 a (2 ^ M)-1.</span><span class="sxs-lookup"><span data-stu-id="287f5-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="287f5-312">Si la entrada es RGB de equipo, la operación de recorte no es necesaria, porque la fórmula de conversión no puede producir valores fuera de este intervalo.</span><span class="sxs-lookup"><span data-stu-id="287f5-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="287f5-313">Estas son las fórmulas exactas sin aproximación.</span><span class="sxs-lookup"><span data-stu-id="287f5-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="287f5-314">Todo lo que se muestra a continuación en este documento se deriva de estas fórmulas.</span><span class="sxs-lookup"><span data-stu-id="287f5-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="287f5-315">En esta sección se describen las conversiones siguientes:</span><span class="sxs-lookup"><span data-stu-id="287f5-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="287f5-316">Convertir RGB888 a YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="287f5-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="287f5-317">Conversión de YUV de 8 bits a RGB888</span><span class="sxs-lookup"><span data-stu-id="287f5-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="287f5-318">Conversión de 4:2:0 YUV a 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="287f5-319">Conversión de 4:2:2 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="287f5-320">Conversión de 4:2:0 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="287f5-321">Convertir RGB888 a YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="287f5-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="287f5-322">En el caso de la entrada RGB de equipo y la salida de 8 bits BT. 601, creemos que las fórmulas proporcionadas en la sección anterior se pueden aproximar razonablemente según lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="287f5-323">Estas fórmulas producen resultados de 8 bits mediante coeficientes que no requieren más de 8 bits de precisión (sin signo).</span><span class="sxs-lookup"><span data-stu-id="287f5-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="287f5-324">Los resultados intermedios requerirán hasta 16 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="287f5-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="287f5-325">Conversión de YUV de 8 bits a RGB888</span><span class="sxs-lookup"><span data-stu-id="287f5-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="287f5-326">En las fórmulas de RGB a YUV originales, una puede derivar las siguientes relaciones para BT. 601.</span><span class="sxs-lookup"><span data-stu-id="287f5-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="287f5-327">Por lo tanto, dado:</span><span class="sxs-lookup"><span data-stu-id="287f5-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="287f5-328">las fórmulas para convertir YUV en RGB pueden derivarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="287f5-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="287f5-329">donde `clip()` denota el recorte en un intervalo de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="287f5-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="287f5-330">Creemos que estas fórmulas se pueden aproximar razonablemente según lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="287f5-331">Estas fórmulas usan algunos coeficientes que requieren más de 8 bits de precisión para generar cada resultado de 8 bits, y los resultados intermedios requerirán más de 16 bits de precisión.</span><span class="sxs-lookup"><span data-stu-id="287f5-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="287f5-332">Para convertir 4:2:0 o 4:2:2 YUV en RGB, se recomienda convertir los datos de YUV en 4:4:4 YUV y, a continuación, convertir de 4:4:4 YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="287f5-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="287f5-333">En las secciones siguientes se presentan algunos métodos para convertir los formatos 4:2:0 y 4:2:2 a 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="287f5-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="287f5-334">Conversión de 4:2:0 YUV a 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="287f5-335">La conversión de 4:2:0 YUV a 4:2:2 YUV requiere una conversión vertical en un factor de dos.</span><span class="sxs-lookup"><span data-stu-id="287f5-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="287f5-336">En esta sección se describe un método de ejemplo para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="287f5-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="287f5-337">El método supone que las imágenes de vídeo son análisis progresivo.</span><span class="sxs-lookup"><span data-stu-id="287f5-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="287f5-338">El proceso de conversión de análisis entrelazado 4:2:0 a 4:2:2 presenta problemas atípicos y es difícil de implementar.</span><span class="sxs-lookup"><span data-stu-id="287f5-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="287f5-339">En este artículo no se aborda el problema de convertir el análisis entrelazado de 4:2:0 a 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="287f5-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="287f5-340">Permita que cada línea vertical de muestras de croma de entrada sea una matriz `Cin[]` que va de 0 a N-1.</span><span class="sxs-lookup"><span data-stu-id="287f5-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="287f5-341">La línea vertical correspondiente en la imagen de salida será una matriz `Cout[]` que va de 0 a 2N-1.</span><span class="sxs-lookup"><span data-stu-id="287f5-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="287f5-342">Para convertir cada línea vertical, realice el proceso siguiente:</span><span class="sxs-lookup"><span data-stu-id="287f5-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="287f5-343">donde clip () denota el recorte en un intervalo de \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="287f5-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="287f5-344">Las ecuaciones para controlar los bordes se pueden simplificar matemáticamente.</span><span class="sxs-lookup"><span data-stu-id="287f5-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="287f5-345">Se muestran en este formulario para mostrar el efecto de compresión en los bordes de la imagen.</span><span class="sxs-lookup"><span data-stu-id="287f5-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="287f5-346">En efecto, este método calcula cada valor que falta mediante la interpolación de la curva en los cuatro píxeles adyacentes, ponderada hacia los valores de los dos píxeles más cercanos (Figura 11).</span><span class="sxs-lookup"><span data-stu-id="287f5-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="287f5-347">El método de interpolación específico que se usa en este ejemplo genera muestras que faltan en posiciones de medio entero mediante un método conocido denominado Catmull-Rom interpolación, también conocido como interpolación de circunvolución cúbica.</span><span class="sxs-lookup"><span data-stu-id="287f5-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![Figura 11.](images/yuvformats14.gif)

<span data-ttu-id="287f5-350">En términos de procesamiento de señal, la conversión vertical debería incluir, idealmente, una compensación de desplazamiento de fase para tener en cuenta el desplazamiento vertical de medio píxel (con respecto a la cuadrícula de muestreo 4:2:2 de salida) entre las ubicaciones de las líneas de ejemplo 4:2:0 y la ubicación de cada otra línea de ejemplo 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="287f5-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="287f5-351">Sin embargo, si se introduce este desplazamiento, se aumentaría la cantidad de procesamiento necesaria para generar los ejemplos y se impedirá la reconstrucción de los ejemplos originales de 4:2:0 a partir de la imagen de 4:2:2 de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="287f5-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="287f5-352">También haría imposible descodificar el vídeo directamente en las superficies 4:2:2 y, a continuación, usar esas superficies como imágenes de referencia para descodificar imágenes posteriores en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="287f5-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="287f5-353">Por lo tanto, el método que se proporciona aquí no tiene en cuenta la alineación vertical precisa de los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="287f5-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="287f5-354">Hacer esto probablemente no es perjudicial visualmente en resoluciones de imagen razonablemente altas.</span><span class="sxs-lookup"><span data-stu-id="287f5-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="287f5-355">Si comienza con un vídeo de 4:2:0 que usa la cuadrícula de muestreo definida en el vídeo H. 261, H. 263 o MPEG-1, la fase de las muestras de croma 4:2:2 de salida también se desplazará con un desplazamiento horizontal de medio píxel en relación con el espaciado de la cuadrícula de muestreo de luminancia (un desplazamiento de cuarto de píxeles en relación con el espaciado de 4:2:2 la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="287f5-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="287f5-356">Sin embargo, el formato MPEG-2 del vídeo 4:2:0 probablemente se usa con más frecuencia en los equipos y no se ve afectado por este problema.</span><span class="sxs-lookup"><span data-stu-id="287f5-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="287f5-357">Además, es probable que la distinción no sea visualmente dañina en resoluciones de imagen razonablemente altas.</span><span class="sxs-lookup"><span data-stu-id="287f5-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="287f5-358">Si intenta corregir este problema, se creará el mismo tipo de problemas descritos para el desplazamiento de fase vertical.</span><span class="sxs-lookup"><span data-stu-id="287f5-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="287f5-359">Conversión de 4:2:2 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="287f5-360">La conversión de 4:2:2 YUV a 4:4:4 YUV requiere una conversión horizontal en un factor de dos.</span><span class="sxs-lookup"><span data-stu-id="287f5-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="287f5-361">El método descrito anteriormente para la conversión vertical se puede aplicar también a la conversión horizontal.</span><span class="sxs-lookup"><span data-stu-id="287f5-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="287f5-362">Para vídeo MPEG-2 e ITU-R BT. 601, este método generará ejemplos con la alineación de fase correcta.</span><span class="sxs-lookup"><span data-stu-id="287f5-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="287f5-363">Conversión de 4:2:0 YUV a 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="287f5-364">Para convertir 4:2:0 YUV en 4:4:4 YUV, puede seguir simplemente los dos métodos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="287f5-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="287f5-365">Convierta la imagen 4:2:0 a 4:2:2 y, a continuación, convierta la imagen 4:2:2 a 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="287f5-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="287f5-366">También puede cambiar el orden de los dos procesos de conversión, ya que el orden de operación no importa realmente la calidad visual del resultado.</span><span class="sxs-lookup"><span data-stu-id="287f5-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="287f5-367">Otros formatos YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-367">Other YUV Formats</span></span>

<span data-ttu-id="287f5-368">Otros formatos YUV menos comunes son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="287f5-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="287f5-369">AI44 es un formato YUV de paleta con 8 bits por muestra.</span><span class="sxs-lookup"><span data-stu-id="287f5-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="287f5-370">Cada ejemplo contiene un índice en los 4 bits más significativos (MSBs) y un valor alfa en 4 bits menos significativos (LSBs).</span><span class="sxs-lookup"><span data-stu-id="287f5-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="287f5-371">El índice hace referencia a una matriz de entradas de la paleta YUV, que debe definirse en el tipo de medio para el formato.</span><span class="sxs-lookup"><span data-stu-id="287f5-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="287f5-372">Este formato se usa principalmente para imágenes de subimagen.</span><span class="sxs-lookup"><span data-stu-id="287f5-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="287f5-373">NV11 es un formato plano 4:1:1 con 12 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="287f5-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="287f5-374">Los ejemplos Y aparecen en primer lugar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="287f5-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="287f5-375">El plano Y va seguido de una matriz de ejemplos empaquetados de U (CB) y V (CR).</span><span class="sxs-lookup"><span data-stu-id="287f5-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="287f5-376">Cuando la matriz de U-V combinada se dirige como una matriz de valores de **palabra** Little-endian, los ejemplos de u se incluyen en el LSBs de cada **palabra** y los ejemplos de V se incluyen en el MSBs.</span><span class="sxs-lookup"><span data-stu-id="287f5-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="287f5-377">(Este diseño de memoria es similar a NV12, aunque el muestreo de croma es diferente).</span><span class="sxs-lookup"><span data-stu-id="287f5-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="287f5-378">Y41P es un formato empaquetado de 4:1:1, con el usuario y V muestreados horizontalmente cada cuatro píxeles.</span><span class="sxs-lookup"><span data-stu-id="287f5-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="287f5-379">Cada macropixel contiene 8 píxeles en tres bytes, con el siguiente diseño de bytes: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="287f5-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="287f5-380">Y41T es idéntico a Y41P, excepto el bit menos significativo de cada ejemplo Y especifica la clave de croma (0 = transparente, 1 = opaca).</span><span class="sxs-lookup"><span data-stu-id="287f5-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="287f5-381">Y42T es idéntico a UYVY, excepto el bit menos significativo de cada ejemplo Y especifica la clave de croma (0 = transparente, 1 = opaca).</span><span class="sxs-lookup"><span data-stu-id="287f5-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="287f5-382">YVYU es equivalente a YUYV, excepto en que se intercambian los ejemplos de los que usted y V.</span><span class="sxs-lookup"><span data-stu-id="287f5-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="287f5-383">Identificar formatos YUV en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="287f5-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="287f5-384">Cada uno de los formatos YUV descritos en este artículo tiene un código FOURCC asignado.</span><span class="sxs-lookup"><span data-stu-id="287f5-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="287f5-385">Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="287f5-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="287f5-386">Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="287f5-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="287f5-387">Por ejemplo, la macro **MAKEFOURCC** se declara en mmsystem. h y la macro **FCC** se declara en Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="287f5-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="287f5-388">Úselos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="287f5-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="287f5-389">También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="287f5-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="287f5-390">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="287f5-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="287f5-391">Invertir el orden es necesario porque el sistema operativo Windows utiliza una arquitectura little-endian.</span><span class="sxs-lookup"><span data-stu-id="287f5-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="287f5-392">' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="287f5-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="287f5-393">En Media Foundation, los formatos se identifican mediante un GUID de tipo principal y un GUID de subtipo.</span><span class="sxs-lookup"><span data-stu-id="287f5-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="287f5-394">El tipo principal de los formatos de vídeo del equipo es siempre MFMediaType \_ video.</span><span class="sxs-lookup"><span data-stu-id="287f5-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="287f5-395">El subtipo se puede construir asignando el código FOURCC a un GUID, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="287f5-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="287f5-396">donde `XXXXXXXX` es el código FourCC.</span><span class="sxs-lookup"><span data-stu-id="287f5-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="287f5-397">Por lo tanto, el GUID del subtipo para YUY2 es:</span><span class="sxs-lookup"><span data-stu-id="287f5-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="287f5-398">Las constantes de los GUID de formato YUV más comunes se definen en el archivo de encabezado mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="287f5-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="287f5-399">Para obtener una lista de estas constantes, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="287f5-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="287f5-400">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="287f5-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="287f5-401">Acerca del vídeo YUV</span><span class="sxs-lookup"><span data-stu-id="287f5-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="287f5-402">Tipos de medios de vídeo</span><span class="sxs-lookup"><span data-stu-id="287f5-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



