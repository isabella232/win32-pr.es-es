---
title: ejemplo (SM4-ASM)
description: Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada. | ejemplo (SM4-ASM)
ms.assetid: 9055D3EE-FD4A-418C-A743-D12E8BDF69FF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397aba4a165f13721e73f87da82cff3e8918e33b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003655"
---
# <a name="sample-sm4---asm"></a><span data-ttu-id="fcbf8-104">ejemplo (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fcbf8-104">sample (sm4 - asm)</span></span>

<span data-ttu-id="fcbf8-105">Muestrea los datos del elemento o la textura especificados utilizando la dirección especificada y el modo de filtrado identificado por la muestra especificada.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="fcbf8-106">ejemplo \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler</span><span class="sxs-lookup"><span data-stu-id="fcbf8-106">sample\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="fcbf8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="fcbf8-107">Item</span></span>                                                                                                               | <span data-ttu-id="fcbf8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fcbf8-108">Description</span></span>                                                                                        |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbf8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fcbf8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="fcbf8-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-110">\[in\] The address of the result of the operation.</span></span><br/>                                      |
| <span data-ttu-id="fcbf8-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="fcbf8-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="fcbf8-112">\[en \] un conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="fcbf8-113">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-113">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="fcbf8-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="fcbf8-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="fcbf8-115">\[en \] un registro de textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-115">\[in\] A texture register.</span></span> <span data-ttu-id="fcbf8-116">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-116">For more information, see the **Remarks** section.</span></span><br/>           |
| <span data-ttu-id="fcbf8-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span><span class="sxs-lookup"><span data-stu-id="fcbf8-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="fcbf8-118">\[en \] un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-118">\[in\] A sampler register.</span></span> <span data-ttu-id="fcbf8-119">Para más información, vea la sección **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-119">For more information, see the **Remarks** section.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="fcbf8-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcbf8-120">Remarks</span></span>

<span data-ttu-id="fcbf8-121">Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea de búferes.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-121">The source data may come from any Resource Type, other than Buffers.</span></span>

<span data-ttu-id="fcbf8-122">*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo, como valores de punto flotante que hacen referencia al espacio normalizado en la textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-122">*srcAddress* provides the set of texture coordinates needed to perform the sample, as floating point values referencing normalized space in the texture.</span></span> <span data-ttu-id="fcbf8-123">Los modos de ajuste de direcciones (Wrap/Mirror/Clamp/Border, etc.) se aplican a las coordenadas de textura fuera del \[ intervalo 0... 1 \] , se toman de los Estados de muestra \# y se aplican después de que se aplique cualquier desplazamiento de dirección a las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-123">Address wrapping modes (wrap/mirror/clamp/border etc.) are applied for texture coordinates outside \[0...1\] range, taken from the sampler state (s\#), and applied after any address offset is applied to texture coordinates.</span></span>

<span data-ttu-id="fcbf8-124">*srcResource* es un registro de textura (t \# ).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-124">*srcResource* is a texture register (t\#).</span></span> <span data-ttu-id="fcbf8-125">Esto es simplemente un marcador de posición para una textura, incluido el tipo de datos devuelto del recurso que se muestra.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-125">This is simply a placeholder for a texture, including the return data type of the resource being sampled.</span></span> <span data-ttu-id="fcbf8-126">Toda esta información se declara en el preámbulo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-126">All of this information is declared in the Shader preamble.</span></span> <span data-ttu-id="fcbf8-127">El recurso real que se va a muestrear se enlaza al sombreador externamente en la ranura \# (para t \# ).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-127">The actual resource to be sampled is bound to the Shader externally at slot \# (for t\#).</span></span>

<span data-ttu-id="fcbf8-128">*srcSampler* es un registro de muestra.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-128">*srcSampler* is a sampler register (s).</span></span> <span data-ttu-id="fcbf8-129">Esto es simplemente un marcador de posición para una colección de controles de filtrado, como los controles de punto frente a lineal, mipmapping y ajuste de direcciones.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-129">This is simply a placeholder for a collection of filtering controls such as point vs. linear, mipmapping and address wrapping controls.</span></span>

<span data-ttu-id="fcbf8-130">El conjunto de información necesario para que el hardware realice el muestreo se divide en dos partes ortogonales.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-130">The set of information required for the hardware to perform sampling is split into two orthogonal pieces.</span></span> <span data-ttu-id="fcbf8-131">En primer lugar, el registro de textura proporciona información de tipo de datos de origen, como por ejemplo, información sobre si la textura contiene datos SRGB.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-131">First, the texture register provides source data type information including, for example, information about whether the texture contains SRGB data.</span></span> <span data-ttu-id="fcbf8-132">También hace referencia a la memoria real que se muestra.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-132">It also references the actual memory being sampled.</span></span> <span data-ttu-id="fcbf8-133">En segundo lugar, el registro de muestra define el modo de filtrado que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-133">Second, the sampler register defines the filtering mode to apply.</span></span>

### <a name="array-resources"></a><span data-ttu-id="fcbf8-134">Recursos de matriz</span><span class="sxs-lookup"><span data-stu-id="fcbf8-134">Array Resources</span></span>

<span data-ttu-id="fcbf8-135">En el caso de las matrices Texture1D, el componente *srcAddress* g (pos-swizzle) selecciona en qué segmento de la matriz se va a capturar.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-135">For Texture1D Arrays, the *srcAddress* g component (POS-swizzle) selects which Array Slice to fetch from.</span></span> <span data-ttu-id="fcbf8-136">Siempre se trata como un valor de punto flotante escalado, en lugar del espacio normalizado para las coordenadas de textura estándar, y se aplica una operación de ida a vuelta más cercana al valor, seguida de una abrazadera al intervalo de BufferArray disponible.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-136">This is always treated as a scaled float value, rather than the normalized space for standard texture coordinates, and a round-to-nearest even is applied on the value, followed by a clamp to the available BufferArray range.</span></span>

<span data-ttu-id="fcbf8-137">En el caso de las matrices de Texture2D, el componente b de *srcAddress* (pos-swizzle) selecciona el segmento de matriz del que se va a capturar; de lo contrario, se usa la misma semántica descrita para las matrices de Texture1D.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-137">For Texture2D Arrays, the *srcAddress* b component (POS-swizzle) selects which Array Slice to fetch from, otherwise using the same semantics described for Texture1D Arrays .</span></span>

### <a name="address-offset"></a><span data-ttu-id="fcbf8-138">Desplazamiento de dirección</span><span class="sxs-lookup"><span data-stu-id="fcbf8-138">Address Offset</span></span>

<span data-ttu-id="fcbf8-139">El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura para el ejemplo se van a desplazar por un conjunto de valores de constantes de tipo entero de espacio de textura inmediato proporcionado.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-139">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the sample are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="fcbf8-140">Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-140">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="fcbf8-141">Este modificador se define para todos los recursos, incluidas las matrices Texture1D/2D y Texture3D, pero no está definido para TextureCube.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-141">This modifier is defined for all Resources, including Texture1D/2D Arrays and Texture3D, but it is undefined for TextureCube.</span></span>

<span data-ttu-id="fcbf8-142">El hardware puede aprovechar el conocimiento inmediato de que un recorrido de una determinada superficie de textura sobre una ubicación común se realiza mediante un conjunto de instrucciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-142">Hardware can take advantage of immediate knowledge that a traversal over some footprint of texels about a common location is being performed by a set of sample instructions.</span></span> <span data-ttu-id="fcbf8-143">Esto se puede transmitir mediante \_ aoffimmi (u, v, w).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-143">This can be conveyed using \_aoffimmi(u,v,w).</span></span>

<span data-ttu-id="fcbf8-144">Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura, con respecto a cada miplevel al que se tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-144">The offsets are added to the texture coordinates, in texel space, relative to each miplevel being accessed.</span></span> <span data-ttu-id="fcbf8-145">Por lo tanto, aunque las coordenadas de textura se proporcionan como valores Float normalizados, el desplazamiento aplica un desplazamiento de entero de espacio textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-145">So even though texture coordinates are provided as normalized float values, the offset applies a texel-space integer offset.</span></span>

<span data-ttu-id="fcbf8-146">Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-146">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="fcbf8-147">\_los componentes de aoffimmi v, w se omiten para Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-147">\_aoffimmi v,w components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="fcbf8-148">\_el componente aoffimmi w se omite para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-148">\_aoffimmi w component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="fcbf8-149">Los modos de ajuste de direcciones (Wrap, Mirror, Clamp/Border, etc.) de los Estados de muestra \# se aplican después de que se aplique cualquier desplazamiento de dirección a las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-149">Address wrapping modes (wrap/mirror/clamp/border etc.) from the sampler state (s\#) are applied after any address offset is applied to texture coordinates.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="fcbf8-150">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbf8-150">Return Type Control</span></span>

<span data-ttu-id="fcbf8-151">El formato de los datos que devuelve el ejemplo al registro de destino viene determinado por el formato de recursos (formato de DXGI \_ \* ) enlazado al parámetro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-151">The data format returned by the sample to the destination register is determined by the resource format (DXGI\_FORMAT\*) bound to the *srcResource* parameter (t\#).</span></span> <span data-ttu-id="fcbf8-152">Por ejemplo, si el t especificado \# estaba enlazado con un recurso con el formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, la operación de muestreo convertirá el textura muestreado de gamma 2,0 a 1,0, aplicará el filtrado y el resultado se escribirá en el registro de destino como valores de punto flotante en el intervalo \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-152">For example, if the specified t\# was bound with a resource with format DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB, then the sampling operation will convert sampled texels from gamma 2.0 to 1.0, apply filtering, and the result will written to the destination register as floating point values in the range \[0..1\].</span></span>

<span data-ttu-id="fcbf8-153">Los valores devueltos son los vectores 4 (con valores predeterminados específicos del formato para los componentes que no están presentes en el formato).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-153">Returned values are 4-vectors (with format-specific defaults for components not present in the format).</span></span> <span data-ttu-id="fcbf8-154">El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá del ejemplo de textura o filtro, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-154">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture sample/filter, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="fcbf8-155">Cuando **Sample** Lee un valor float de 32 bits en un registro de 32 bits, con muestreo de punto (sin filtrado), puede o no vaciar los valores desnormalizados, pero de lo contrario no se modifican los números.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-155">When **sample** reads a 32-bit float value into a 32-bit register, with point sampling (no filtering), it may or may not flush denormal values, but otherwise numbers are unmodified.</span></span> <span data-ttu-id="fcbf8-156">Si la incertidumbre con valores desnormalizados de muestreo de puntos es un problema para una aplicación, use la instrucción [LD](ld--sm4---asm-.md) , que garantiza que los valores float de 32 bits se lean sin modificar.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-156">If the uncertainty with point sampling denormal values is an issue for an application,use the [ld](ld--sm4---asm-.md) instruction, which guarantees that 32-bit float values are read unmodified.</span></span>

### <a name="lod-calculation"></a><span data-ttu-id="fcbf8-157">Cálculo de LOD</span><span class="sxs-lookup"><span data-stu-id="fcbf8-157">LOD Calculation</span></span>

<span data-ttu-id="fcbf8-158">Para obtener información detallada sobre cómo se calculan los derivados en el proceso de determinación de LOD para el filtrado, vea [derive \_ RTX](deriv-rtx--sm4---asm-.md) y [derive \_ propiedad](deriv-rty--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-158">For details on how derivatives are calculated in the process of determining LOD for filtering, see [deriv\_rtx](deriv-rtx--sm4---asm-.md) and [deriv\_rty](deriv-rty--sm4---asm-.md).</span></span> <span data-ttu-id="fcbf8-159">La instrucción de **ejemplo** calcula implícitamente los derivados de las coordenadas de textura usando la misma definición que usan las instrucciones de sombreador **derivadas** .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-159">The **sample** instruction implicitly computes derivatives on the texture coordinates using the same definition that the **deriv** Shader instructions use.</span></span> <span data-ttu-id="fcbf8-160">Esto no se aplica a las instrucciones de [ejemplo \_ l](sample-l--sm4---asm-.md) o [ \_ d](sample-d--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-160">This does not apply to [sample\_l](sample-l--sm4---asm-.md) or [sample\_d](sample-d--sm4---asm-.md) instructions.</span></span> <span data-ttu-id="fcbf8-161">En el caso de estas instrucciones, la aplicación proporciona directamente el LOD o los derivados.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-161">For those instructions, LOD or derivatives are provided directly by the application.</span></span>

<span data-ttu-id="fcbf8-162">En el caso de la instrucción de **ejemplo** , las implementaciones pueden optar por compartir el mismo cálculo de LOD en los 4 píxeles de una marca de 2x2 (pero sin área más grande) o realizar cálculos de LOD por píxel.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-162">For the **sample** instruction, implementations can choose to share the same LOD calculation across all 4 pixels in a 2x2 stamp (but no larger area), or perform per-pixel LOD calculations.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="fcbf8-163">Detalles varios</span><span class="sxs-lookup"><span data-stu-id="fcbf8-163">Miscellaneous Details</span></span>

<span data-ttu-id="fcbf8-164">Para buffer & Texture1D, se omiten los componentes *srcAddress* . GBA (pos-swizzle).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-164">For Buffer & Texture1D, *srcAddress* .gba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="fcbf8-165">En el caso de las matrices Texture1D, se omiten los componentes de *srcAddress* . BA (pos-swizzle).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-165">For Texture1D Arrays, *srcAddress* .ba components (POS-swizzle) are ignored.</span></span> <span data-ttu-id="fcbf8-166">En el caso de Texture2Ds, se omite el componente *srcAddress* . a (pos-swizzle).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-166">For Texture2Ds, *srcAddress* .a component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="fcbf8-167">La captura de una ranura de entrada que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-167">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="fcbf8-168">Restricciones</span><span class="sxs-lookup"><span data-stu-id="fcbf8-168">Restrictions</span></span>

-   <span data-ttu-id="fcbf8-169">*srcResource* debe ser un \# registro t.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-169">*srcResource* must be a t\# register.</span></span> <span data-ttu-id="fcbf8-170">*srcResource* no puede ser ConstantBuffer, que no se puede enlazar a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-170">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="fcbf8-171">*srcSampler* debe ser un \# registro s.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-171">*srcSampler* must be an s\# register.</span></span>
-   <span data-ttu-id="fcbf8-172">No se permite el direccionamiento relativo en *srcResource* o *srcSampler* .</span><span class="sxs-lookup"><span data-stu-id="fcbf8-172">Relative addressing on *srcResource* or *srcSampler* is not permitted.</span></span>
-   <span data-ttu-id="fcbf8-173">*srcAddress* debe ser un registro Temp (r \# /X \# ), constantBuffer (CB \# ), INPUT (v \# ) o un valor inmediato (s).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-173">*srcAddress* must be a temp (r\#/x\#), constantBuffer (cb\#), input (v\#) register or immediate value(s).</span></span>
-   <span data-ttu-id="fcbf8-174">*dest* debe ser un registro Temp (r \# /x \# ) o Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="fcbf8-174">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>
-   <span data-ttu-id="fcbf8-175">\_aoffimmi (u, v, w) no se permite para TextureCubes.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-175">\_aoffimmi(u,v,w) is not permitted for TextureCubes.</span></span>

<span data-ttu-id="fcbf8-176">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fcbf8-176">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fcbf8-177">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fcbf8-177">Vertex Shader</span></span> | <span data-ttu-id="fcbf8-178">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fcbf8-178">Geometry Shader</span></span> | <span data-ttu-id="fcbf8-179">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fcbf8-179">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="fcbf8-180">x</span><span class="sxs-lookup"><span data-stu-id="fcbf8-180">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fcbf8-181">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fcbf8-181">Minimum Shader Model</span></span>

<span data-ttu-id="fcbf8-182">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fcbf8-182">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fcbf8-183">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fcbf8-183">Shader Model</span></span>                                              | <span data-ttu-id="fcbf8-184">Compatible</span><span class="sxs-lookup"><span data-stu-id="fcbf8-184">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fcbf8-185">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fcbf8-185">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fcbf8-186">sí</span><span class="sxs-lookup"><span data-stu-id="fcbf8-186">yes</span></span>       |
| [<span data-ttu-id="fcbf8-187">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fcbf8-187">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fcbf8-188">sí</span><span class="sxs-lookup"><span data-stu-id="fcbf8-188">yes</span></span>       |
| [<span data-ttu-id="fcbf8-189">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fcbf8-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fcbf8-190">sí</span><span class="sxs-lookup"><span data-stu-id="fcbf8-190">yes</span></span>       |
| [<span data-ttu-id="fcbf8-191">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcbf8-191">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fcbf8-192">no</span><span class="sxs-lookup"><span data-stu-id="fcbf8-192">no</span></span>        |
| [<span data-ttu-id="fcbf8-193">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcbf8-193">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fcbf8-194">no</span><span class="sxs-lookup"><span data-stu-id="fcbf8-194">no</span></span>        |
| [<span data-ttu-id="fcbf8-195">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcbf8-195">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fcbf8-196">no</span><span class="sxs-lookup"><span data-stu-id="fcbf8-196">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fcbf8-197">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fcbf8-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcbf8-198">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fcbf8-198">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





