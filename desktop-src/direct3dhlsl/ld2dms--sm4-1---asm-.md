---
title: ld2dms (SM 4.1-ASM)
description: Lee ejemplos individuales de texturas de varios ejemplos bidimensionales.
ms.assetid: 8D92BFA8-4B22-46F3-876D-8D84BB3A96E7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9dd03b7c07f3fb25294dd0ad6aa382eb203560
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148997"
---
# <a name="ld2dms-sm41---asm"></a><span data-ttu-id="2c4c5-103">ld2dms (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-103">ld2dms (sm4.1 - asm)</span></span>

<span data-ttu-id="2c4c5-104">Lee ejemplos individuales de texturas de varios ejemplos bidimensionales.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-104">Reads individual samples out of 2-dimensional multi-sample textures.</span></span>



| <span data-ttu-id="2c4c5-105">ld2dms \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , sampleIndex (operando escalar)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-105">ld2dms\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], sampleIndex (scalar operand)</span></span> |
|------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2c4c5-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c4c5-106">Item</span></span>                                                                                                               | <span data-ttu-id="2c4c5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c4c5-107">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4c5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2c4c5-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="2c4c5-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-109">\[in\] The address of result of the operation.</span></span> <br/>                                                                 |
| <span data-ttu-id="2c4c5-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="2c4c5-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="2c4c5-111">\[en \] las coordenadas de textura necesarias para realizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-111">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                    |
| <span data-ttu-id="2c4c5-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="2c4c5-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="2c4c5-113">\[en \] un registro de textura (t \# ), que se debe haber declarado que identifica la textura o el búfer del que se va a capturar</span><span class="sxs-lookup"><span data-stu-id="2c4c5-113">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from</span></span><br/> |
| <span data-ttu-id="2c4c5-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span><span class="sxs-lookup"><span data-stu-id="2c4c5-114"><span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*</span></span><br/> | <span data-ttu-id="2c4c5-115">\[en \] Idendifies los ejemplos que se van a leer desde *srcResource*.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-115">\[in\] Idendifies the samples to read from *srcResource*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="2c4c5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c4c5-116">Remarks</span></span>

<span data-ttu-id="2c4c5-117">Esta instrucción es una alternativa simplificada a la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="2c4c5-118">Captura los datos de la textura especificada sin ningún filtro (por ejemplo, el muestreo de puntos) mediante el entero proporcionado *srcAddress* y *sampleIndex*.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-118">It fetches data from the specified Texture without any filtering (e.g. point sampling) using the provided integer *srcAddress* and *sampleIndex*.</span></span>

<span data-ttu-id="2c4c5-119">*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo en forma de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-119">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="2c4c5-120">Si *srcAddress* está fuera del intervalo \[ 0... ( \# textura en Dimension-1) \] , **ld2dms** siempre devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1.0 f/0x00000001) para los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-120">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="2c4c5-121">*sampleIndex* no tiene que ser un literal.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-121">*sampleIndex* does not have to be a literal.</span></span> <span data-ttu-id="2c4c5-122">No es necesario especificar el número de muestras múltiples en el recurso de textura y funciona con vistas de profundidad o de estarcido.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-122">The multi-sample count does not have to be specified on the texture resource, and it works with depth or stencil views.</span></span>

<span data-ttu-id="2c4c5-123">Una aplicación que desee tener un control más flexible sobre el comportamiento de la dirección fuera del intervalo debería usar la instrucción de **ejemplo** en su lugar, ya que respeta el comportamiento de la dirección, el reflejo, la abrazadera y el borde definidos como estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-123">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="2c4c5-124">*srcAddress. b* (post-swizzle) se omite para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-124">*srcAddress.b* (post-swizzle) is ignored for Texture2Ds.</span></span> <span data-ttu-id="2c4c5-125">Si el valor está fuera del intervalo de índices de matriz disponibles \[ 0... ( tamaño de matriz: 1) \] , **ld2dms** siempre devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1.0 f/0x00000001) para los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-125">If the value is out of the range of available array indices \[0...(array size-1)\], then **ld2dms** always returns 0 in all components present in the format of the resource, and defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

<span data-ttu-id="2c4c5-126">En el caso de las matrices Texture2D, *srcAddress. b* (post-swizzle) proporciona el índice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-126">For Texture2D Arrays, *srcAddress.b* (post-swizzle) provides the array index.</span></span> <span data-ttu-id="2c4c5-127">Oherwise tiene el mismo comportamiento que Texture2D.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-127">Oherwise it has the same behavior as Texture2D.</span></span>

<span data-ttu-id="2c4c5-128">*srcAddress. a* (post-swizzle) siempre se omite.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-128">*srcAddress.a* (post-swizzle) is always ignored.</span></span> <span data-ttu-id="2c4c5-129">El compilador de HLSL nunca generará nada.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-129">The HLSL compiler will never output anything there.</span></span>

<span data-ttu-id="2c4c5-130">*srcResource* es un registro de textura (t \# ) que se debe haber declarado (22.3.11), que identifica la textura de la que se va a capturar.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-130">*srcResource* is a texture register (t\#) which must have been declared(22.3.11), identifying which Texture to fetch from.</span></span>

<span data-ttu-id="2c4c5-131">La captura de t \# que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-131">Fetching from t\# that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="2c4c5-132">Desplazamiento de dirección</span><span class="sxs-lookup"><span data-stu-id="2c4c5-132">Address Offset</span></span>

<span data-ttu-id="2c4c5-133">El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura de **ld2dms** se van a desplazar mediante un conjunto de valores de constante de entero de espacio textura inmediato proporcionado.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld2dms** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="2c4c5-134">Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span>

<span data-ttu-id="2c4c5-135">Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-135">The offsets are added to the texture coordinates, in texel space.</span></span>

<span data-ttu-id="2c4c5-136">Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices Texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-136">Address offsets are not applied along the array axis of Texture1D/2D Arrays.</span></span>

<span data-ttu-id="2c4c5-137">Los componentes de *\_ aoffimmi v, w* se omiten para Texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-137">The *\_aoffimmi v,w* components are ignored for Texture1Ds.</span></span>

<span data-ttu-id="2c4c5-138">El componente *\_ aoffimmi w* se omite para Texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-138">The *\_aoffimmi w* component is ignored for Texture2Ds.</span></span>

<span data-ttu-id="2c4c5-139">Dado que las coordenadas de textura para **ld2dms** son enteros sin signo, si el desplazamiento hace que la dirección quede por debajo de cero, se ajustará a una dirección grande y se producirá un acceso fuera del límite, que es como **LD** devuelve 0 en todos los componentes presentes en el formato del recurso y los valores predeterminados (0, 0, 0, 1,0 f/0x00000001) para los componentes</span><span class="sxs-lookup"><span data-stu-id="2c4c5-139">Because the texture coordinates for **ld2dms** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access, which like **ld** returns 0 in all components present in the format of the resource, and the defaults (0,0,0,1.0f/0x00000001) for missing components.</span></span>

### <a name="sample-number"></a><span data-ttu-id="2c4c5-140">Número de muestra</span><span class="sxs-lookup"><span data-stu-id="2c4c5-140">Sample Number</span></span>

<span data-ttu-id="2c4c5-141">**ld2dms** está disponible para su uso en cualquier recurso.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-141">**ld2dms** is available for use on any resource.</span></span> <span data-ttu-id="2c4c5-142">**ld2dms** funciona de forma idéntica a **LD** , excepto en los recursos de multsample 2D, mediante el uso del operando de *sampleIndex* adicional (basado en 0) para identificar qué ejemplo se debe leer del recurso.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-142">**ld2dms** operates identically to **ld** except on 2D multsample resources, by using the additional (0-based) *sampleIndex* operand to identify which sample to read from the resource.</span></span>

<span data-ttu-id="2c4c5-143">El resultado de especificar un *sampleIndex* que supera el número de muestras del recurso es indefinido, pero no puede devolver datos fuera del espacio de direcciones del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-143">The result of specifying a *sampleIndex* that exceeds the number of samples in the resource is undefined, but cannot return data outside of the address space of the device context.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="2c4c5-144">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2c4c5-144">Return Type Control</span></span>

<span data-ttu-id="2c4c5-145">El formato de datos devuelto por **ld2dms** al registro de destino se determina de la misma manera que se describe para la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-145">The data format returned by **ld2dms** to the destination register is determined in the same way as described for the **sample** instruction.</span></span> <span data-ttu-id="2c4c5-146">Se basa en el formato enlazado al parámetro *srcResource* (t \# ).</span><span class="sxs-lookup"><span data-stu-id="2c4c5-146">It is based on the format bound to the *srcResource* parameter (t\#).</span></span>

<span data-ttu-id="2c4c5-147">Al igual que con la instrucción de **ejemplo** , los valores devueltos para **ld2dms** son de 4 vectores con valores predeterminados específicos del formato para los componentes que no están presentes en el formato.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-147">As with the **sample** instruction, returned values for **ld2dms** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="2c4c5-148">El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá de la carga de textura, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-148">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="2c4c5-149">Cuando **ld2dms** Lee un valor float de 32 bits en un registro de 32 bits, los bits no se tocan; es decir, los valores desnormalizados permanecen desnormalizados.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-149">When a 32-bit float value is read by **ld2dms** into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="2c4c5-150">Esto no es lo mismo que la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-150">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="2c4c5-151">Detalles varios</span><span class="sxs-lookup"><span data-stu-id="2c4c5-151">Miscellaneous Details</span></span>

<span data-ttu-id="2c4c5-152">Como no hay ningún filtrado asociado a esta instrucción, no se aplican conceptos como la diferencia de LOD.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-152">As there is no filtering associated with this instruction, concepts like LOD bias do not apply.</span></span> <span data-ttu-id="2c4c5-153">En consecuencia, no hay ningún parámetro *Samples \#* .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-153">Accordingly there is no *sampler s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="2c4c5-154">Restricciones</span><span class="sxs-lookup"><span data-stu-id="2c4c5-154">Restrictions</span></span>

-   <span data-ttu-id="2c4c5-155">*srcResource* debe ser un \# registro t y no un TextureCube, Texture1D o Texture1DArray.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-155">*srcResource* must be a t\# register, and not a TextureCube, Texture1D or Texture1DArray.</span></span> <span data-ttu-id="2c4c5-156">*srcResource* no puede ser ConstantBuffer, que no se puede enlazar a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-156">*srcResource* cannot be a ConstantBuffer, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="2c4c5-157">No se permite el direccionamiento relativo en *srcResource* .</span><span class="sxs-lookup"><span data-stu-id="2c4c5-157">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="2c4c5-158">*srcAddress* y *sampleIndex* deben ser un registro Temp (r \# /x \# ), Constant (CB \# ) o INPUT (v \# ).</span><span class="sxs-lookup"><span data-stu-id="2c4c5-158">*srcAddress* and *sampleIndex* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="2c4c5-159">*dest* debe ser un registro Temp (r \# /x \# ) o Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="2c4c5-159">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="2c4c5-160">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2c4c5-160">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2c4c5-161">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2c4c5-161">Vertex Shader</span></span> | <span data-ttu-id="2c4c5-162">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="2c4c5-162">Geometry Shader</span></span> | <span data-ttu-id="2c4c5-163">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2c4c5-163">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2c4c5-164">x</span><span class="sxs-lookup"><span data-stu-id="2c4c5-164">x</span></span>             | <span data-ttu-id="2c4c5-165">x</span><span class="sxs-lookup"><span data-stu-id="2c4c5-165">x</span></span>               | <span data-ttu-id="2c4c5-166">x</span><span class="sxs-lookup"><span data-stu-id="2c4c5-166">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2c4c5-167">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2c4c5-167">Minimum Shader Model</span></span>

<span data-ttu-id="2c4c5-168">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2c4c5-168">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2c4c5-169">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2c4c5-169">Shader Model</span></span>                                              | <span data-ttu-id="2c4c5-170">Compatible</span><span class="sxs-lookup"><span data-stu-id="2c4c5-170">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2c4c5-171">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2c4c5-171">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2c4c5-172">sí</span><span class="sxs-lookup"><span data-stu-id="2c4c5-172">yes</span></span>       |
| [<span data-ttu-id="2c4c5-173">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2c4c5-173">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2c4c5-174">sí</span><span class="sxs-lookup"><span data-stu-id="2c4c5-174">yes</span></span>       |
| [<span data-ttu-id="2c4c5-175">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2c4c5-175">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2c4c5-176">no</span><span class="sxs-lookup"><span data-stu-id="2c4c5-176">no</span></span>        |
| [<span data-ttu-id="2c4c5-177">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-177">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2c4c5-178">no</span><span class="sxs-lookup"><span data-stu-id="2c4c5-178">no</span></span>        |
| [<span data-ttu-id="2c4c5-179">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-179">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2c4c5-180">no</span><span class="sxs-lookup"><span data-stu-id="2c4c5-180">no</span></span>        |
| [<span data-ttu-id="2c4c5-181">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-181">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2c4c5-182">no</span><span class="sxs-lookup"><span data-stu-id="2c4c5-182">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2c4c5-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c4c5-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c4c5-184">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2c4c5-184">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





