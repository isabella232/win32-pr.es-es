---
description: El formato de textura DXT1 es para las texturas que son opacas o tienen un único color transparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Texturas alfa opacas y de 1 bit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104561886"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="c9a4b-103">Texturas alfa opacas y de 1 bit (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="c9a4b-104">El formato de textura DXT1 es para las texturas que son opacas o tienen un único color transparente.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="c9a4b-105">Para cada bloque alfa opaco o de 1 bit, se almacenan los valores de 2 16 bits (formato RGB 5:6:5) y un mapa de bits 4x4 con 2 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="c9a4b-106">Se suman los 64 bits para 16 textura, o cuatro bits por textura.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="c9a4b-107">En el mapa de bits de bloque, hay 2 bits por textura para seleccionar entre los cuatro colores, dos de los cuales se almacenan en los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="c9a4b-108">Los otros dos colores se derivan de estos colores almacenados mediante la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="c9a4b-109">Este diseño se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-109">This layout is shown in the following diagram.</span></span>

![diagrama del diseño de mapa de bits](images/colors1.png)

<span data-ttu-id="c9a4b-111">El formato alfa de 1 bit se distingue del formato opaco mediante la comparación de los valores de color de 2 16 bits almacenados en el bloque.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="c9a4b-112">Se tratan como enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="c9a4b-113">Si el primer color es mayor que el segundo, implica que solo se definen textura opacos.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="c9a4b-114">Esto significa que se usan cuatro colores para representar el textura.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="c9a4b-115">En la codificación de cuatro colores, hay dos colores derivados y los cuatro colores se distribuyen uniformemente en el espacio de colores RGB.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="c9a4b-116">Este formato es análogo al formato RGB 5:6:5.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="c9a4b-117">De lo contrario, para la transparencia alfa de 1 bit, se usan tres colores y el cuarto se reserva para representar textura transparentes.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="c9a4b-118">En la codificación de tres colores, hay un color derivado y el cuarto código de 2 bits se reserva para indicar un textura transparente (información alfa).</span><span class="sxs-lookup"><span data-stu-id="c9a4b-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="c9a4b-119">Este formato es análogo a RGBA 5:5:5:1, donde el bit final se usa para codificar la máscara alfa.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="c9a4b-120">En el ejemplo de código siguiente se muestra el algoritmo para decidir si la codificación de tres o cuatro colores está seleccionada:</span><span class="sxs-lookup"><span data-stu-id="c9a4b-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="c9a4b-121">Se recomienda establecer los componentes RGBA del píxel de transparencia en cero antes de la fusión.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="c9a4b-122">En las tablas siguientes se muestra el diseño de memoria para el bloque de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="c9a4b-123">Se supone que el primer índice corresponde a la coordenada y y el segundo corresponde a la coordenada x.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="c9a4b-124">Por ejemplo, textura \[ 1 \] \[ 2 \] hace referencia al píxel del mapa de texturas en (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="c9a4b-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="c9a4b-125">Esta tabla contiene el diseño de memoria para el bloque de 8 bytes (64 bits).</span><span class="sxs-lookup"><span data-stu-id="c9a4b-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="c9a4b-126">Dirección de palabra</span><span class="sxs-lookup"><span data-stu-id="c9a4b-126">Word address</span></span> | <span data-ttu-id="c9a4b-127">Palabra de 16 bits</span><span class="sxs-lookup"><span data-stu-id="c9a4b-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="c9a4b-128">0</span><span class="sxs-lookup"><span data-stu-id="c9a4b-128">0</span></span>            | <span data-ttu-id="c9a4b-129">Color \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9a4b-129">Color\_0</span></span>       |
| <span data-ttu-id="c9a4b-130">1</span><span class="sxs-lookup"><span data-stu-id="c9a4b-130">1</span></span>            | <span data-ttu-id="c9a4b-131">Color \_ 1</span><span class="sxs-lookup"><span data-stu-id="c9a4b-131">Color\_1</span></span>       |
| <span data-ttu-id="c9a4b-132">2</span><span class="sxs-lookup"><span data-stu-id="c9a4b-132">2</span></span>            | <span data-ttu-id="c9a4b-133">Bitmap (palabra \_ 0)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="c9a4b-134">3</span><span class="sxs-lookup"><span data-stu-id="c9a4b-134">3</span></span>            | <span data-ttu-id="c9a4b-135">Mapa de bits (palabra \_ 1)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="c9a4b-136">\_El color 0 y \_ el color 1, los colores de los dos extremos, se disponen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c9a4b-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="c9a4b-137">Bits</span><span class="sxs-lookup"><span data-stu-id="c9a4b-137">Bits</span></span>        | <span data-ttu-id="c9a4b-138">Color</span><span class="sxs-lookup"><span data-stu-id="c9a4b-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="c9a4b-139">4:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="c9a4b-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="c9a4b-140">Componente de color azul</span><span class="sxs-lookup"><span data-stu-id="c9a4b-140">Blue color component</span></span>  |
| <span data-ttu-id="c9a4b-141">10:5</span><span class="sxs-lookup"><span data-stu-id="c9a4b-141">10:5</span></span>        | <span data-ttu-id="c9a4b-142">Componente de color verde</span><span class="sxs-lookup"><span data-stu-id="c9a4b-142">Green color component</span></span> |
| <span data-ttu-id="c9a4b-143">15:11</span><span class="sxs-lookup"><span data-stu-id="c9a4b-143">15:11</span></span>       | <span data-ttu-id="c9a4b-144">Componente de color rojo</span><span class="sxs-lookup"><span data-stu-id="c9a4b-144">Red color component</span></span>   |



 

<span data-ttu-id="c9a4b-145">\*bit menos significativo</span><span class="sxs-lookup"><span data-stu-id="c9a4b-145">\*least-significant bit</span></span>

<span data-ttu-id="c9a4b-146">El mapa \_ de bits palabra 0 está diseñado de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c9a4b-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="c9a4b-147">Bits</span><span class="sxs-lookup"><span data-stu-id="c9a4b-147">Bits</span></span>          | <span data-ttu-id="c9a4b-148">Textura</span><span class="sxs-lookup"><span data-stu-id="c9a4b-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="c9a4b-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-149">1:0 (LSB)</span></span>     | <span data-ttu-id="c9a4b-150">Textura \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="c9a4b-151">3:2</span><span class="sxs-lookup"><span data-stu-id="c9a4b-151">3:2</span></span>           | <span data-ttu-id="c9a4b-152">Textura \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="c9a4b-153">5:4</span><span class="sxs-lookup"><span data-stu-id="c9a4b-153">5:4</span></span>           | <span data-ttu-id="c9a4b-154">Textura \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="c9a4b-155">7:6</span><span class="sxs-lookup"><span data-stu-id="c9a4b-155">7:6</span></span>           | <span data-ttu-id="c9a4b-156">Textura \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="c9a4b-157">9:8</span><span class="sxs-lookup"><span data-stu-id="c9a4b-157">9:8</span></span>           | <span data-ttu-id="c9a4b-158">Textura \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="c9a4b-159">11:10</span><span class="sxs-lookup"><span data-stu-id="c9a4b-159">11:10</span></span>         | <span data-ttu-id="c9a4b-160">Textura \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="c9a4b-161">13:12</span><span class="sxs-lookup"><span data-stu-id="c9a4b-161">13:12</span></span>         | <span data-ttu-id="c9a4b-162">Textura \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="c9a4b-163">15:14 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="c9a4b-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="c9a4b-164">Textura \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="c9a4b-165">\*bit más significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="c9a4b-166">El mapa \_ de bits de la palabra 1 se dispone de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c9a4b-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="c9a4b-167">Bits</span><span class="sxs-lookup"><span data-stu-id="c9a4b-167">Bits</span></span>        | <span data-ttu-id="c9a4b-168">Textura</span><span class="sxs-lookup"><span data-stu-id="c9a4b-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="c9a4b-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-169">1:0 (LSB)</span></span>   | <span data-ttu-id="c9a4b-170">Textura \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="c9a4b-171">3:2</span><span class="sxs-lookup"><span data-stu-id="c9a4b-171">3:2</span></span>         | <span data-ttu-id="c9a4b-172">Textura \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="c9a4b-173">5:4</span><span class="sxs-lookup"><span data-stu-id="c9a4b-173">5:4</span></span>         | <span data-ttu-id="c9a4b-174">Textura \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="c9a4b-175">7:6</span><span class="sxs-lookup"><span data-stu-id="c9a4b-175">7:6</span></span>         | <span data-ttu-id="c9a4b-176">Textura \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="c9a4b-177">9:8</span><span class="sxs-lookup"><span data-stu-id="c9a4b-177">9:8</span></span>         | <span data-ttu-id="c9a4b-178">Textura \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="c9a4b-179">11:10</span><span class="sxs-lookup"><span data-stu-id="c9a4b-179">11:10</span></span>       | <span data-ttu-id="c9a4b-180">Textura \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="c9a4b-181">13:12</span><span class="sxs-lookup"><span data-stu-id="c9a4b-181">13:12</span></span>       | <span data-ttu-id="c9a4b-182">Textura \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="c9a4b-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="c9a4b-183">15:14 (MSB)</span></span> | <span data-ttu-id="c9a4b-184">Textura \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="c9a4b-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="c9a4b-185">Ejemplo de codificación de color opaca</span><span class="sxs-lookup"><span data-stu-id="c9a4b-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="c9a4b-186">Como ejemplo de codificación opaca, supongamos que los colores rojo y negro están en el extremo.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="c9a4b-187">Rojo es el color \_ 0 y el negro es el color \_ 1.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="c9a4b-188">Hay cuatro colores interpolados que forman el degradado distribuido uniformemente entre ellos.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="c9a4b-189">Para determinar los valores para el mapa de bits 4x4, se usan los cálculos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c9a4b-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="c9a4b-190">El mapa de bits es similar al diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-190">The bitmap then looks like the following diagram.</span></span>

![Diagrama que muestra el diseño de mapa de bits expandido.](images/colors2.png)

<span data-ttu-id="c9a4b-192">Es similar a la siguiente serie de colores ilustrada.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="c9a4b-193">En una imagen, el píxel (0,0) aparece en la parte superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![Ilustración de un degradado opaco codificado](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="c9a4b-195">Ejemplo de codificación alfa de 1 bit</span><span class="sxs-lookup"><span data-stu-id="c9a4b-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="c9a4b-196">Este formato se selecciona cuando el entero de 16 bits sin signo, el color \_ 0, es menor que el entero de 16 bits sin signo, el color \_ 1.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="c9a4b-197">Un ejemplo de dónde se puede usar este formato es la salida de un árbol, que se muestra con un cielo azul.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="c9a4b-198">Algunos textura se pueden marcar como transparentes, mientras que tres tonalidades verdes siguen estando disponibles para las hojas.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="c9a4b-199">Dos colores corrigen los extremos y el tercero es un color interpolado.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="c9a4b-200">La siguiente ilustración es un ejemplo de este tipo de imagen.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-200">The following illustration is an example of such a picture.</span></span>

![Ilustración de la codificación alfa de 1 bit](images/greenthing.png)

<span data-ttu-id="c9a4b-202">Tenga en cuenta que cuando la imagen se muestra en blanco, textura se codificaría como transparente.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="c9a4b-203">Tenga en cuenta también que los componentes RGBA del textura transparente deben establecerse en cero antes de la combinación.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="c9a4b-204">La codificación de mapa de bits para los colores y la transparencia se determina mediante los cálculos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="c9a4b-205">El mapa de bits es similar al diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9a4b-205">The bitmap then looks like the following diagram.</span></span>

![diagrama del diseño de mapa de bits expandido](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="c9a4b-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9a4b-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9a4b-208">Recursos de textura comprimidos</span><span class="sxs-lookup"><span data-stu-id="c9a4b-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



