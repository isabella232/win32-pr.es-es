---
description: En esta sección se enumeran los códigos de operación de trama binaria utilizados por las funciones GetROP2 y SetROP2. Los códigos de operación de trama definen cómo combina GDI los bits del lápiz seleccionado con los bits en el mapa de bits de destino.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operaciones de trama binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155701"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="cc1b2-104">Operaciones de trama binaria</span><span class="sxs-lookup"><span data-stu-id="cc1b2-104">Binary Raster Operations</span></span>

<span data-ttu-id="cc1b2-105">En esta sección se enumeran los códigos de operación de trama binaria utilizados por las funciones [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) y [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) .</span><span class="sxs-lookup"><span data-stu-id="cc1b2-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="cc1b2-106">Los códigos de operación de trama definen cómo combina GDI los bits del lápiz seleccionado con los bits en el mapa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="cc1b2-107">Cada código de operación de trama representa una operación booleana en la que se combinan los valores de los píxeles del lápiz seleccionado y el mapa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="cc1b2-108">A continuación se muestran los dos operandos utilizados en estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="cc1b2-109">Operando</span><span class="sxs-lookup"><span data-stu-id="cc1b2-109">Operand</span></span> | <span data-ttu-id="cc1b2-110">Significado</span><span class="sxs-lookup"><span data-stu-id="cc1b2-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="cc1b2-111">P</span><span class="sxs-lookup"><span data-stu-id="cc1b2-111">P</span></span>       | <span data-ttu-id="cc1b2-112">Pluma seleccionada</span><span class="sxs-lookup"><span data-stu-id="cc1b2-112">Selected pen</span></span>       |
| <span data-ttu-id="cc1b2-113">D</span><span class="sxs-lookup"><span data-stu-id="cc1b2-113">D</span></span>       | <span data-ttu-id="cc1b2-114">Mapa de bits de destino</span><span class="sxs-lookup"><span data-stu-id="cc1b2-114">Destination bitmap</span></span> |



 

<span data-ttu-id="cc1b2-115">A continuación se indican los operadores booleanos que se usan en estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="cc1b2-116">Operator</span><span class="sxs-lookup"><span data-stu-id="cc1b2-116">Operator</span></span> | <span data-ttu-id="cc1b2-117">Significado</span><span class="sxs-lookup"><span data-stu-id="cc1b2-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="cc1b2-118">a</span><span class="sxs-lookup"><span data-stu-id="cc1b2-118">a</span></span>        | <span data-ttu-id="cc1b2-119">AND bit a bit</span><span class="sxs-lookup"><span data-stu-id="cc1b2-119">Bitwise AND</span></span>                |
| <span data-ttu-id="cc1b2-120">n</span><span class="sxs-lookup"><span data-stu-id="cc1b2-120">n</span></span>        | <span data-ttu-id="cc1b2-121">NOT bit a bit (inversa)</span><span class="sxs-lookup"><span data-stu-id="cc1b2-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="cc1b2-122">o</span><span class="sxs-lookup"><span data-stu-id="cc1b2-122">o</span></span>        | <span data-ttu-id="cc1b2-123">OR bit a bit</span><span class="sxs-lookup"><span data-stu-id="cc1b2-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="cc1b2-124">x</span><span class="sxs-lookup"><span data-stu-id="cc1b2-124">x</span></span>        | <span data-ttu-id="cc1b2-125">Or exclusivo bit a bit (XOR)</span><span class="sxs-lookup"><span data-stu-id="cc1b2-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="cc1b2-126">Todas las operaciones booleanas se presentan en notación Polaco inversa.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="cc1b2-127">Por ejemplo, la siguiente operación reemplaza los valores de los píxeles en el mapa de bits de destino por una combinación de los valores de píxeles del lápiz y del pincel seleccionado:</span><span class="sxs-lookup"><span data-stu-id="cc1b2-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="cc1b2-128">Cada código de operación de trama es un entero de 32 bits cuya palabra de orden superior es un índice de operación booleano y cuya palabra de orden inferior es el código de operación.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="cc1b2-129">El índice de operación de 16 bits es un valor de 8 bits extendido con ceros que representa todos los resultados posibles que se derivan de la operación booleana con dos parámetros (en este caso, los valores de lápiz y destino).</span><span class="sxs-lookup"><span data-stu-id="cc1b2-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="cc1b2-130">Por ejemplo, los índices de operación de las operaciones DPo y DPan se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="cc1b2-131">P</span><span class="sxs-lookup"><span data-stu-id="cc1b2-131">P</span></span>   | <span data-ttu-id="cc1b2-132">D</span><span class="sxs-lookup"><span data-stu-id="cc1b2-132">D</span></span>   | <span data-ttu-id="cc1b2-133">DPo</span><span class="sxs-lookup"><span data-stu-id="cc1b2-133">DPo</span></span> | <span data-ttu-id="cc1b2-134">Dpan</span><span class="sxs-lookup"><span data-stu-id="cc1b2-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="cc1b2-135">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-135">0</span></span>   | <span data-ttu-id="cc1b2-136">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-136">0</span></span>   | <span data-ttu-id="cc1b2-137">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-137">0</span></span>   | <span data-ttu-id="cc1b2-138">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-138">1</span></span>    |
| <span data-ttu-id="cc1b2-139">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-139">0</span></span>   | <span data-ttu-id="cc1b2-140">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-140">1</span></span>   | <span data-ttu-id="cc1b2-141">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-141">1</span></span>   | <span data-ttu-id="cc1b2-142">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-142">1</span></span>    |
| <span data-ttu-id="cc1b2-143">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-143">1</span></span>   | <span data-ttu-id="cc1b2-144">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-144">0</span></span>   | <span data-ttu-id="cc1b2-145">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-145">1</span></span>   | <span data-ttu-id="cc1b2-146">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-146">1</span></span>    |
| <span data-ttu-id="cc1b2-147">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-147">1</span></span>   | <span data-ttu-id="cc1b2-148">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-148">1</span></span>   | <span data-ttu-id="cc1b2-149">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-149">1</span></span>   | <span data-ttu-id="cc1b2-150">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-150">0</span></span>    |



 

<span data-ttu-id="cc1b2-151">En la siguiente lista se describen los modos de dibujo y las operaciones booleanas que representan.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="cc1b2-152">Operación de trama</span><span class="sxs-lookup"><span data-stu-id="cc1b2-152">Raster operation</span></span> | <span data-ttu-id="cc1b2-153">Operación booleana</span><span class="sxs-lookup"><span data-stu-id="cc1b2-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="cc1b2-154">R2 \_ negro</span><span class="sxs-lookup"><span data-stu-id="cc1b2-154">R2\_BLACK</span></span>        | <span data-ttu-id="cc1b2-155">0</span><span class="sxs-lookup"><span data-stu-id="cc1b2-155">0</span></span>                 |
| <span data-ttu-id="cc1b2-156">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="cc1b2-157">P</span><span class="sxs-lookup"><span data-stu-id="cc1b2-157">P</span></span>                 |
| <span data-ttu-id="cc1b2-158">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="cc1b2-159">DPna</span><span class="sxs-lookup"><span data-stu-id="cc1b2-159">DPna</span></span>              |
| <span data-ttu-id="cc1b2-160">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="cc1b2-161">DPa</span><span class="sxs-lookup"><span data-stu-id="cc1b2-161">DPa</span></span>               |
| <span data-ttu-id="cc1b2-162">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="cc1b2-163">PDna</span><span class="sxs-lookup"><span data-stu-id="cc1b2-163">PDna</span></span>              |
| <span data-ttu-id="cc1b2-164">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="cc1b2-165">DPno</span><span class="sxs-lookup"><span data-stu-id="cc1b2-165">DPno</span></span>              |
| <span data-ttu-id="cc1b2-166">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="cc1b2-167">DPo</span><span class="sxs-lookup"><span data-stu-id="cc1b2-167">DPo</span></span>               |
| <span data-ttu-id="cc1b2-168">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="cc1b2-169">PDno</span><span class="sxs-lookup"><span data-stu-id="cc1b2-169">PDno</span></span>              |
| <span data-ttu-id="cc1b2-170">NOP de R2 \_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-170">R2\_NOP</span></span>          | <span data-ttu-id="cc1b2-171">D</span><span class="sxs-lookup"><span data-stu-id="cc1b2-171">D</span></span>                 |
| <span data-ttu-id="cc1b2-172">R2 \_ no</span><span class="sxs-lookup"><span data-stu-id="cc1b2-172">R2\_NOT</span></span>          | <span data-ttu-id="cc1b2-173">Dn</span><span class="sxs-lookup"><span data-stu-id="cc1b2-173">Dn</span></span>                |
| <span data-ttu-id="cc1b2-174">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="cc1b2-175">VPN</span><span class="sxs-lookup"><span data-stu-id="cc1b2-175">Pn</span></span>                |
| <span data-ttu-id="cc1b2-176">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="cc1b2-177">DPan</span><span class="sxs-lookup"><span data-stu-id="cc1b2-177">DPan</span></span>              |
| <span data-ttu-id="cc1b2-178">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="cc1b2-179">DPon</span><span class="sxs-lookup"><span data-stu-id="cc1b2-179">DPon</span></span>              |
| <span data-ttu-id="cc1b2-180">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="cc1b2-181">DPxn</span><span class="sxs-lookup"><span data-stu-id="cc1b2-181">DPxn</span></span>              |
| <span data-ttu-id="cc1b2-182">R2 \_ blanco</span><span class="sxs-lookup"><span data-stu-id="cc1b2-182">R2\_WHITE</span></span>        | <span data-ttu-id="cc1b2-183">1</span><span class="sxs-lookup"><span data-stu-id="cc1b2-183">1</span></span>                 |
| <span data-ttu-id="cc1b2-184">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-184">R2\_XORPEN</span></span>       | <span data-ttu-id="cc1b2-185">DPx</span><span class="sxs-lookup"><span data-stu-id="cc1b2-185">DPx</span></span>               |



 

<span data-ttu-id="cc1b2-186">Para un dispositivo monocromo, GDI asigna el valor cero a negro y el valor 1 a blanco.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="cc1b2-187">Si una aplicación intenta dibujar con un lápiz negro en un destino blanco mediante las operaciones de trama binaria disponibles, se producen los siguientes resultados.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="cc1b2-188">Operación de trama</span><span class="sxs-lookup"><span data-stu-id="cc1b2-188">Raster operation</span></span> | <span data-ttu-id="cc1b2-189">Resultado</span><span class="sxs-lookup"><span data-stu-id="cc1b2-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="cc1b2-190">R2 \_ negro</span><span class="sxs-lookup"><span data-stu-id="cc1b2-190">R2\_BLACK</span></span>        | <span data-ttu-id="cc1b2-191">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-191">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-192">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="cc1b2-193">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-193">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-194">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="cc1b2-195">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-195">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-196">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="cc1b2-197">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-197">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-198">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="cc1b2-199">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-199">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-200">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="cc1b2-201">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-201">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-202">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="cc1b2-203">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-203">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-204">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="cc1b2-205">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-205">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-206">NOP de R2 \_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-206">R2\_NOP</span></span>          | <span data-ttu-id="cc1b2-207">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-207">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-208">R2 \_ no</span><span class="sxs-lookup"><span data-stu-id="cc1b2-208">R2\_NOT</span></span>          | <span data-ttu-id="cc1b2-209">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-209">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-210">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="cc1b2-211">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-211">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-212">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="cc1b2-213">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-213">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-214">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="cc1b2-215">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-215">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-216">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="cc1b2-217">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-217">Visible black line</span></span> |
| <span data-ttu-id="cc1b2-218">R2 \_ blanco</span><span class="sxs-lookup"><span data-stu-id="cc1b2-218">R2\_WHITE</span></span>        | <span data-ttu-id="cc1b2-219">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-219">No visible line</span></span>    |
| <span data-ttu-id="cc1b2-220">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-220">R2\_XORPEN</span></span>       | <span data-ttu-id="cc1b2-221">No hay ninguna línea visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-221">No visible line</span></span>    |



 

<span data-ttu-id="cc1b2-222">Para un dispositivo de color, GDI usa valores RGB para representar los colores del lápiz y el destino.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="cc1b2-223">Un valor de color RGB es un entero largo que contiene un campo de color rojo, verde y azul, cada uno de los cuales especifica la intensidad del color especificado.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="cc1b2-224">La intensidad oscila entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="cc1b2-225">Los valores se empaquetan en los tres bytes de orden inferior del entero largo.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="cc1b2-226">El color de un lápiz siempre es un color sólido, pero el color del destino puede ser una combinación de dos o tres colores.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="cc1b2-227">Si una aplicación intenta dibujar con un lápiz blanco en un destino azul mediante las operaciones binarias de tramas disponibles, se producirán los resultados siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc1b2-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="cc1b2-228">Operación de trama</span><span class="sxs-lookup"><span data-stu-id="cc1b2-228">Raster operation</span></span> | <span data-ttu-id="cc1b2-229">Resultado</span><span class="sxs-lookup"><span data-stu-id="cc1b2-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="cc1b2-230">R2 \_ negro</span><span class="sxs-lookup"><span data-stu-id="cc1b2-230">R2\_BLACK</span></span>        | <span data-ttu-id="cc1b2-231">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-231">Visible black line</span></span>     |
| <span data-ttu-id="cc1b2-232">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="cc1b2-233">Línea blanca visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-233">Visible white line</span></span>     |
| <span data-ttu-id="cc1b2-234">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="cc1b2-235">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-235">Visible black line</span></span>     |
| <span data-ttu-id="cc1b2-236">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="cc1b2-237">Línea azul invisible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-237">Invisible blue line</span></span>    |
| <span data-ttu-id="cc1b2-238">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="cc1b2-239">Línea visible de rojo/verde</span><span class="sxs-lookup"><span data-stu-id="cc1b2-239">Visible red/green line</span></span> |
| <span data-ttu-id="cc1b2-240">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="cc1b2-241">Línea azul invisible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-241">Invisible blue line</span></span>    |
| <span data-ttu-id="cc1b2-242">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="cc1b2-243">Línea blanca visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-243">Visible white line</span></span>     |
| <span data-ttu-id="cc1b2-244">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="cc1b2-245">Línea blanca visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-245">Visible white line</span></span>     |
| <span data-ttu-id="cc1b2-246">NOP de R2 \_</span><span class="sxs-lookup"><span data-stu-id="cc1b2-246">R2\_NOP</span></span>          | <span data-ttu-id="cc1b2-247">Línea azul invisible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-247">Invisible blue line</span></span>    |
| <span data-ttu-id="cc1b2-248">R2 \_ no</span><span class="sxs-lookup"><span data-stu-id="cc1b2-248">R2\_NOT</span></span>          | <span data-ttu-id="cc1b2-249">Línea visible de rojo/verde</span><span class="sxs-lookup"><span data-stu-id="cc1b2-249">Visible red/green line</span></span> |
| <span data-ttu-id="cc1b2-250">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="cc1b2-251">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-251">Visible black line</span></span>     |
| <span data-ttu-id="cc1b2-252">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="cc1b2-253">Línea visible de rojo/verde</span><span class="sxs-lookup"><span data-stu-id="cc1b2-253">Visible red/green line</span></span> |
| <span data-ttu-id="cc1b2-254">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="cc1b2-255">Línea negra visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-255">Visible black line</span></span>     |
| <span data-ttu-id="cc1b2-256">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="cc1b2-257">Línea azul invisible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-257">Invisible blue line</span></span>    |
| <span data-ttu-id="cc1b2-258">R2 \_ blanco</span><span class="sxs-lookup"><span data-stu-id="cc1b2-258">R2\_WHITE</span></span>        | <span data-ttu-id="cc1b2-259">Línea blanca visible</span><span class="sxs-lookup"><span data-stu-id="cc1b2-259">Visible white line</span></span>     |
| <span data-ttu-id="cc1b2-260">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="cc1b2-260">R2\_XORPEN</span></span>       | <span data-ttu-id="cc1b2-261">Línea visible de rojo/verde</span><span class="sxs-lookup"><span data-stu-id="cc1b2-261">Visible red/green line</span></span> |



 

 

 



