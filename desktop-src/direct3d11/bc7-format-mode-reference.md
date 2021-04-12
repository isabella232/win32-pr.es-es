---
title: Referencia del modo de formato BC7
description: Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/22/2020
ms.locfileid: "104420120"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="06e1c-103">Referencia del modo de formato BC7</span><span class="sxs-lookup"><span data-stu-id="06e1c-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="06e1c-104">Esta documentación contiene una lista de los 8 modos de bloque y las asignaciones de bits para los bloques de formato de compresión de textura BC7.</span><span class="sxs-lookup"><span data-stu-id="06e1c-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="06e1c-105">Los colores de cada subconjunto dentro de un bloque se representan mediante dos colores de extremo explícitos y un conjunto de colores interpolados entre ellos.</span><span class="sxs-lookup"><span data-stu-id="06e1c-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="06e1c-106">Dependiendo de la precisión del índice del bloque, cada subconjunto puede tener 4, 8 o 16 colores posibles.</span><span class="sxs-lookup"><span data-stu-id="06e1c-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="06e1c-107">Modo 0</span><span class="sxs-lookup"><span data-stu-id="06e1c-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="06e1c-108">Modo 1</span><span class="sxs-lookup"><span data-stu-id="06e1c-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="06e1c-109">Modo 2</span><span class="sxs-lookup"><span data-stu-id="06e1c-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="06e1c-110">Modo 3</span><span class="sxs-lookup"><span data-stu-id="06e1c-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="06e1c-111">Modo 4</span><span class="sxs-lookup"><span data-stu-id="06e1c-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="06e1c-112">Modo 5</span><span class="sxs-lookup"><span data-stu-id="06e1c-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="06e1c-113">Modo 6</span><span class="sxs-lookup"><span data-stu-id="06e1c-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="06e1c-114">Modo 7</span><span class="sxs-lookup"><span data-stu-id="06e1c-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="06e1c-115">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="06e1c-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="06e1c-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06e1c-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="06e1c-117">Modo 0</span><span class="sxs-lookup"><span data-stu-id="06e1c-117">Mode 0</span></span>

<span data-ttu-id="06e1c-118">El modo de BC7 0 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-119">Solo componentes de color (no alfa)</span><span class="sxs-lookup"><span data-stu-id="06e1c-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="06e1c-120">3 subconjuntos por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-120">3 subsets per block</span></span>
-   <span data-ttu-id="06e1c-121">Puntos de conexión de RGBP 4.4.4.1 con un bit P único por punto de conexión</span><span class="sxs-lookup"><span data-stu-id="06e1c-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="06e1c-122">índices de 3 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-122">3-bit indices</span></span>
-   <span data-ttu-id="06e1c-123">16 particiones</span><span class="sxs-lookup"><span data-stu-id="06e1c-123">16 partitions</span></span>

![diseño de bits de modo 0](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="06e1c-125">Modo 1</span><span class="sxs-lookup"><span data-stu-id="06e1c-125">Mode 1</span></span>

<span data-ttu-id="06e1c-126">El modo de BC7 1 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-127">Solo componentes de color (no alfa)</span><span class="sxs-lookup"><span data-stu-id="06e1c-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="06e1c-128">2 subconjuntos por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-128">2 subsets per block</span></span>
-   <span data-ttu-id="06e1c-129">RGBP extremos de 6.6.6.1 con un bit P compartido por subconjunto)</span><span class="sxs-lookup"><span data-stu-id="06e1c-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="06e1c-130">índices de 3 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-130">3-bit indices</span></span>
-   <span data-ttu-id="06e1c-131">64 particiones</span><span class="sxs-lookup"><span data-stu-id="06e1c-131">64 partitions</span></span>

![diseño de bits de modo 1](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="06e1c-133">Modo 2</span><span class="sxs-lookup"><span data-stu-id="06e1c-133">Mode 2</span></span>

<span data-ttu-id="06e1c-134">El modo 2 de BC7 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-135">Solo componentes de color (no alfa)</span><span class="sxs-lookup"><span data-stu-id="06e1c-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="06e1c-136">3 subconjuntos por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-136">3 subsets per block</span></span>
-   <span data-ttu-id="06e1c-137">Extremos 5.5.5 RGB</span><span class="sxs-lookup"><span data-stu-id="06e1c-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="06e1c-138">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-138">2-bit indices</span></span>
-   <span data-ttu-id="06e1c-139">64 particiones</span><span class="sxs-lookup"><span data-stu-id="06e1c-139">64 partitions</span></span>

![diseño de bits de modo 2](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="06e1c-141">Modo 3</span><span class="sxs-lookup"><span data-stu-id="06e1c-141">Mode 3</span></span>

<span data-ttu-id="06e1c-142">El modo de BC7 3 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-143">Solo componentes de color (no alfa)</span><span class="sxs-lookup"><span data-stu-id="06e1c-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="06e1c-144">2 subconjuntos por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-144">2 subsets per block</span></span>
-   <span data-ttu-id="06e1c-145">Puntos de conexión de RGBP 7.7.7.1 con un bit P único por subconjunto)</span><span class="sxs-lookup"><span data-stu-id="06e1c-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="06e1c-146">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-146">2-bit indices</span></span>
-   <span data-ttu-id="06e1c-147">64 particiones</span><span class="sxs-lookup"><span data-stu-id="06e1c-147">64 partitions</span></span>

![diseño de modo de 3 bits](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="06e1c-149">Modo 4</span><span class="sxs-lookup"><span data-stu-id="06e1c-149">Mode 4</span></span>

<span data-ttu-id="06e1c-150">El modo de BC7 4 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-151">Componentes de color con componentes alfa independientes</span><span class="sxs-lookup"><span data-stu-id="06e1c-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="06e1c-152">1 subconjunto por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-152">1 subset per block</span></span>
-   <span data-ttu-id="06e1c-153">Extremos de color RGB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="06e1c-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="06e1c-154">puntos de conexión alfa de 6 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="06e1c-155">16 índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="06e1c-156">16 índices de 3 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="06e1c-157">rotación de componentes de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-157">2-bit component rotation</span></span>
-   <span data-ttu-id="06e1c-158">Selector de índice de 1 bit (si se usan los índices de 2 o 3 bits)</span><span class="sxs-lookup"><span data-stu-id="06e1c-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![diseño de modo 4 bits](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="06e1c-160">Modo 5</span><span class="sxs-lookup"><span data-stu-id="06e1c-160">Mode 5</span></span>

<span data-ttu-id="06e1c-161">El modo de BC7 5 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-162">Componentes de color con componentes alfa independientes</span><span class="sxs-lookup"><span data-stu-id="06e1c-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="06e1c-163">1 subconjunto por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-163">1 subset per block</span></span>
-   <span data-ttu-id="06e1c-164">Extremos de color RGB 7.7.7</span><span class="sxs-lookup"><span data-stu-id="06e1c-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="06e1c-165">puntos de conexión alfa de 8 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="06e1c-166">16 índices de color de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="06e1c-167">16 índices alfa de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="06e1c-168">rotación de componentes de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-168">2-bit component rotation</span></span>

![diseño de bits de modo 5](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="06e1c-170">Modo 6</span><span class="sxs-lookup"><span data-stu-id="06e1c-170">Mode 6</span></span>

<span data-ttu-id="06e1c-171">El modo de BC7 6 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-172">Componentes de color y alfa combinados</span><span class="sxs-lookup"><span data-stu-id="06e1c-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="06e1c-173">Un subconjunto por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-173">One subset per block</span></span>
-   <span data-ttu-id="06e1c-174">Puntos de conexión de color (y alfa) de RGBAP 7.7.7.7.1 (único P bits por extremo)</span><span class="sxs-lookup"><span data-stu-id="06e1c-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="06e1c-175">16 índices x 4 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-175">16 x 4-bit indices</span></span>

![diseño de modo de 6 bits](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="06e1c-177">Modo 7</span><span class="sxs-lookup"><span data-stu-id="06e1c-177">Mode 7</span></span>

<span data-ttu-id="06e1c-178">El modo de BC7 7 tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="06e1c-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="06e1c-179">Componentes de color y alfa combinados</span><span class="sxs-lookup"><span data-stu-id="06e1c-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="06e1c-180">2 subconjuntos por bloque</span><span class="sxs-lookup"><span data-stu-id="06e1c-180">2 subsets per block</span></span>
-   <span data-ttu-id="06e1c-181">Puntos de conexión de color (y alfa) de RGBAP 5.5.5.5.1 (único P bits por extremo)</span><span class="sxs-lookup"><span data-stu-id="06e1c-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="06e1c-182">índices de 2 bits</span><span class="sxs-lookup"><span data-stu-id="06e1c-182">2-bit indices</span></span>
-   <span data-ttu-id="06e1c-183">64 particiones</span><span class="sxs-lookup"><span data-stu-id="06e1c-183">64 partitions</span></span>

![diseño de bits de modo 7](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="06e1c-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06e1c-185">Remarks</span></span>

<span data-ttu-id="06e1c-186">El modo 8 (el byte menos significativo está establecido en 0x00).</span><span class="sxs-lookup"><span data-stu-id="06e1c-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="06e1c-187">No lo use en el codificador.</span><span class="sxs-lookup"><span data-stu-id="06e1c-187">Don't use it in your encoder.</span></span> <span data-ttu-id="06e1c-188">Si pasa este modo al hardware, se devuelve un bloque inicializado con ceros.</span><span class="sxs-lookup"><span data-stu-id="06e1c-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="06e1c-189">En BC7, puede codificar el componente alfa de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="06e1c-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="06e1c-190">Tipos de bloque sin codificación de componentes alfa explícita.</span><span class="sxs-lookup"><span data-stu-id="06e1c-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="06e1c-191">En estos bloques, los extremos de color tienen una codificación solo RGB, con el componente alfa descodificado en 1,0 para todos los textura.</span><span class="sxs-lookup"><span data-stu-id="06e1c-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="06e1c-192">Tipos de bloque con componentes de color y alfa combinados.</span><span class="sxs-lookup"><span data-stu-id="06e1c-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="06e1c-193">En estos bloques, los valores de color del punto de conexión se especifican en el formato RGBA y los valores del componente alfa se interpolan junto con los valores de color.</span><span class="sxs-lookup"><span data-stu-id="06e1c-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="06e1c-194">Tipos de bloque con componentes de color y alfa separados.</span><span class="sxs-lookup"><span data-stu-id="06e1c-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="06e1c-195">En estos bloques, los valores de color y alfa se especifican por separado, cada uno con su propio conjunto de índices.</span><span class="sxs-lookup"><span data-stu-id="06e1c-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="06e1c-196">Como resultado, tienen un vector efectivo y un canal escalar codificados por separado, donde el vector especifica normalmente los canales de color \[ R, G, B \] y el valor escalar especifica el canal alfa \[ a \] .</span><span class="sxs-lookup"><span data-stu-id="06e1c-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="06e1c-197">Para admitir este enfoque, se proporciona un campo de 2 bits independiente en la codificación, que permite la especificación de la codificación de canal independiente como un valor escalar.</span><span class="sxs-lookup"><span data-stu-id="06e1c-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="06e1c-198">Como resultado, el bloque puede tener una de las siguientes cuatro representaciones diferentes de esta codificación alfa (como se indica en el campo de 2 bits):</span><span class="sxs-lookup"><span data-stu-id="06e1c-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="06e1c-199">RGB \| A: canal alfa independiente</span><span class="sxs-lookup"><span data-stu-id="06e1c-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="06e1c-200">AGB \| R: canal de color "rojo" independiente</span><span class="sxs-lookup"><span data-stu-id="06e1c-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="06e1c-201">RAB \| G: canal de color verde independiente</span><span class="sxs-lookup"><span data-stu-id="06e1c-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="06e1c-202">RGA \| B: canal de color azul independiente</span><span class="sxs-lookup"><span data-stu-id="06e1c-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="06e1c-203">El descodificador vuelve a ordenar el orden del canal a RGBA después de la descodificación, por lo que el formato de bloque interno no es visible para el desarrollador.</span><span class="sxs-lookup"><span data-stu-id="06e1c-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="06e1c-204">Los negros con componentes de color y alfa independientes también tienen dos conjuntos de datos de índice: uno para el conjunto de canales de vectores y otro para el canal escalar.</span><span class="sxs-lookup"><span data-stu-id="06e1c-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="06e1c-205">(En el caso del modo 4, estos índices son de distintos anchos \[ 2 o 3 bits \] .</span><span class="sxs-lookup"><span data-stu-id="06e1c-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="06e1c-206">El modo 4 también contiene un selector de 1 bit que especifica si el vector o el canal escalar utiliza los índices de 3 bits).</span><span class="sxs-lookup"><span data-stu-id="06e1c-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="06e1c-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06e1c-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06e1c-208">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="06e1c-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




