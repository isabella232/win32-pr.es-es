---
description: Hay dos maneras de codificar mapas de texturas que presentan una transparencia más compleja.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Texturas con canales alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568374"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="2ca7c-103">Texturas con canales alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="2ca7c-104">Hay dos maneras de codificar mapas de texturas que presentan una transparencia más compleja.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="2ca7c-105">En cada caso, un bloque que describe la transparencia precede al bloque de 64 bits ya descrito.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="2ca7c-106">La transparencia se representa como un mapa de bits 4x4 con 4 bits por píxel (codificación explícita) o con menos bits y interpolación lineal que es análogo a lo que se usa para la codificación de colores.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="2ca7c-107">El bloque de transparencia y el bloque de color están organizados tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="2ca7c-108">Dirección de palabra</span><span class="sxs-lookup"><span data-stu-id="2ca7c-108">Word address</span></span> | <span data-ttu-id="2ca7c-109">bloque 64 bits</span><span class="sxs-lookup"><span data-stu-id="2ca7c-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="2ca7c-110">3:0</span><span class="sxs-lookup"><span data-stu-id="2ca7c-110">3:0</span></span>          | <span data-ttu-id="2ca7c-111">Bloque de transparencia</span><span class="sxs-lookup"><span data-stu-id="2ca7c-111">Transparency block</span></span>                |
| <span data-ttu-id="2ca7c-112">7:4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-112">7:4</span></span>          | <span data-ttu-id="2ca7c-113">Bloque de 64 bits descrito anteriormente</span><span class="sxs-lookup"><span data-stu-id="2ca7c-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="2ca7c-114">Codificación de textura explícita</span><span class="sxs-lookup"><span data-stu-id="2ca7c-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="2ca7c-115">En el caso de la codificación de texturas explícita (formatos DXT2 y DXT3), los componentes alfa de textura que describen la transparencia se codifican en un mapa de bits 4x4 con 4 bits por textura.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="2ca7c-116">Estos cuatro bits se pueden lograr a través de una gran variedad de medios, como la interpolación o el uso de los cuatro bits más significativos de los datos alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="2ca7c-117">Sin embargo, se usan tal y como están, sin ningún tipo de interpolación.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="2ca7c-118">En el diagrama siguiente se muestra un bloque de transparencia de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-118">The following diagram shows a 64-bit transparency block.</span></span>

![diagrama de un bloque de transparencia de 64 bits](images/colors4.png)

> [!Note]  
> <span data-ttu-id="2ca7c-120">El método de compresión de Direct3D usa los cuatro bits más significativos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="2ca7c-121">En las tablas siguientes se muestra cómo se distribuye la información alfa en la memoria, para cada palabra de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="2ca7c-122">Esta tabla contiene el diseño de la palabra 0.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="2ca7c-123">Bits</span><span class="sxs-lookup"><span data-stu-id="2ca7c-123">Bits</span></span>          | <span data-ttu-id="2ca7c-124">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ca7c-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="2ca7c-125">3:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="2ca7c-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="2ca7c-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="2ca7c-127">7:4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-127">7:4</span></span>           | <span data-ttu-id="2ca7c-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="2ca7c-129">11:8</span><span class="sxs-lookup"><span data-stu-id="2ca7c-129">11:8</span></span>          | <span data-ttu-id="2ca7c-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="2ca7c-131">15:12 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="2ca7c-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="2ca7c-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="2ca7c-133">\*bit menos significativo, bit más significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="2ca7c-134">Esta tabla contiene el diseño de la palabra 1.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="2ca7c-135">Bits</span><span class="sxs-lookup"><span data-stu-id="2ca7c-135">Bits</span></span>        | <span data-ttu-id="2ca7c-136">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ca7c-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ca7c-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-137">3:0 (LSB)</span></span>   | <span data-ttu-id="2ca7c-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="2ca7c-139">7:4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-139">7:4</span></span>         | <span data-ttu-id="2ca7c-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="2ca7c-141">11:8</span><span class="sxs-lookup"><span data-stu-id="2ca7c-141">11:8</span></span>        | <span data-ttu-id="2ca7c-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="2ca7c-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-143">15:12 (MSB)</span></span> | <span data-ttu-id="2ca7c-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="2ca7c-145">Esta tabla contiene el diseño de la palabra 2.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="2ca7c-146">Bits</span><span class="sxs-lookup"><span data-stu-id="2ca7c-146">Bits</span></span>        | <span data-ttu-id="2ca7c-147">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ca7c-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ca7c-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-148">3:0 (LSB)</span></span>   | <span data-ttu-id="2ca7c-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="2ca7c-150">7:4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-150">7:4</span></span>         | <span data-ttu-id="2ca7c-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="2ca7c-152">11:8</span><span class="sxs-lookup"><span data-stu-id="2ca7c-152">11:8</span></span>        | <span data-ttu-id="2ca7c-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="2ca7c-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-154">15:12 (MSB)</span></span> | <span data-ttu-id="2ca7c-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="2ca7c-156">Esta tabla contiene el diseño de la palabra 3.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="2ca7c-157">Bits</span><span class="sxs-lookup"><span data-stu-id="2ca7c-157">Bits</span></span>        | <span data-ttu-id="2ca7c-158">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ca7c-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="2ca7c-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-159">3:0 (LSB)</span></span>   | <span data-ttu-id="2ca7c-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="2ca7c-161">7:4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-161">7:4</span></span>         | <span data-ttu-id="2ca7c-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="2ca7c-163">11:8</span><span class="sxs-lookup"><span data-stu-id="2ca7c-163">11:8</span></span>        | <span data-ttu-id="2ca7c-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="2ca7c-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-165">15:12 (MSB)</span></span> | <span data-ttu-id="2ca7c-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="2ca7c-167">La diferencia entre DXT2 y DXT3 es que, en el formato DXT2, se supone que los datos de color se han multiplicado previamente por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="2ca7c-168">En el formato DXT3, se supone que el color no está premultiplicado por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="2ca7c-169">Estos dos formatos son necesarios porque, en la mayoría de los casos, en el momento en que se usa una textura, simplemente examinar los datos no es suficiente para determinar si los valores de color se han multiplicado por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="2ca7c-170">Dado que esta información es necesaria en tiempo de ejecución, los dos códigos FOURCC se utilizan para diferenciar estos casos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="2ca7c-171">Sin embargo, los datos y el método de interpolación que se usan para estos dos formatos son idénticos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="2ca7c-172">La comparación de color usada en DXT1 para determinar si el textura es transparente no se utiliza en este formato.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="2ca7c-173">Se supone que sin la comparación de color, los datos de color siempre se tratan como si estuviera en modo de 4 colores.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="2ca7c-174">En otras palabras, la instrucción if en la parte superior del código DXT1 debe ser la siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ca7c-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="2ca7c-175">Three-Bit interpolación alfa lineal</span><span class="sxs-lookup"><span data-stu-id="2ca7c-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="2ca7c-176">La codificación de transparencia para los formatos DXT4 y DXT5 se basa en un concepto similar a la codificación lineal utilizada para el color.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="2ca7c-177">Los valores alfa de 2 8 bits y un mapa de bits 4x4 con tres bits por píxel se almacenan en los primeros ocho bytes del bloque.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="2ca7c-178">Los valores alfa representativos se usan para interpolar valores alfa intermedios.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="2ca7c-179">Hay información adicional disponible en la forma en que se almacenan los dos valores alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="2ca7c-180">Si \_ el valor alfa 0 es mayor que el valor alfa \_ 1, la interpolación crea seis valores alfa intermedios.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="2ca7c-181">De lo contrario, se interpolan cuatro valores alfa intermedios entre los extremos alfa especificados.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="2ca7c-182">Los dos valores alfa implícitos adicionales son 0 (totalmente transparente) y 255 (totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="2ca7c-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="2ca7c-183">En el ejemplo de código siguiente se muestra este algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="2ca7c-184">El diseño de memoria del bloque alfa es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ca7c-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="2ca7c-185">Byte</span><span class="sxs-lookup"><span data-stu-id="2ca7c-185">Byte</span></span> | <span data-ttu-id="2ca7c-186">Alpha</span><span class="sxs-lookup"><span data-stu-id="2ca7c-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="2ca7c-187">0</span><span class="sxs-lookup"><span data-stu-id="2ca7c-187">0</span></span>    | <span data-ttu-id="2ca7c-188">Alfa \_ 0</span><span class="sxs-lookup"><span data-stu-id="2ca7c-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="2ca7c-189">1</span><span class="sxs-lookup"><span data-stu-id="2ca7c-189">1</span></span>    | <span data-ttu-id="2ca7c-190">Alfa \_ 1</span><span class="sxs-lookup"><span data-stu-id="2ca7c-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="2ca7c-191">2</span><span class="sxs-lookup"><span data-stu-id="2ca7c-191">2</span></span>    | <span data-ttu-id="2ca7c-192">\[0 \] \[ 2 \] (2 MSBs), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="2ca7c-193">3</span><span class="sxs-lookup"><span data-stu-id="2ca7c-193">3</span></span>    | <span data-ttu-id="2ca7c-194">\[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="2ca7c-195">4</span><span class="sxs-lookup"><span data-stu-id="2ca7c-195">4</span></span>    | <span data-ttu-id="2ca7c-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="2ca7c-197">5</span><span class="sxs-lookup"><span data-stu-id="2ca7c-197">5</span></span>    | <span data-ttu-id="2ca7c-198">\[2 \] \[ 2 \] (2 MSBs), \[ 2 1,2 \] \[ \] \[ \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="2ca7c-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="2ca7c-199">6</span><span class="sxs-lookup"><span data-stu-id="2ca7c-199">6</span></span>    | <span data-ttu-id="2ca7c-200">\[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="2ca7c-201">7</span><span class="sxs-lookup"><span data-stu-id="2ca7c-201">7</span></span>    | <span data-ttu-id="2ca7c-202">\[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSBs)</span><span class="sxs-lookup"><span data-stu-id="2ca7c-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="2ca7c-203">La diferencia entre DXT4 y DXT5 es que en el formato DXT4 se supone que los datos de color se han multiplicado previamente por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="2ca7c-204">En el formato DXT5, se supone que el color no se multiplica por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="2ca7c-205">Estos dos formatos son necesarios porque, en la mayoría de los casos, en el momento en que se usa una textura, simplemente examinar los datos no es suficiente para determinar si los valores de color se han multiplicado por alfa.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="2ca7c-206">Dado que esta información es necesaria en tiempo de ejecución, los dos códigos FOURCC se utilizan para diferenciar estos casos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="2ca7c-207">Sin embargo, los datos y el método de interpolación que se usan para estos dos formatos son idénticos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="2ca7c-208">La comparación de color usada en DXT1 para determinar si el textura es transparente no se utiliza con estos formatos.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="2ca7c-209">Se supone que sin la comparación de color, los datos de color siempre se tratan como si estuviera en modo de 4 colores.</span><span class="sxs-lookup"><span data-stu-id="2ca7c-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="2ca7c-210">En otras palabras, la instrucción if en la parte superior del código DXT1 debe ser:</span><span class="sxs-lookup"><span data-stu-id="2ca7c-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="2ca7c-211">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ca7c-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca7c-212">Recursos de textura comprimidos</span><span class="sxs-lookup"><span data-stu-id="2ca7c-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



