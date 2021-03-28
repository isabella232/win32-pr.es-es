---
title: LD (SM4-ASM)
description: Recupera los datos del búfer o la textura especificados sin ningún filtrado (por ejemplo, el muestreo de puntos) mediante la dirección de entero proporcionada. Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358488"
---
# <a name="ld-sm4---asm"></a><span data-ttu-id="5ba8f-104">LD (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-104">ld (sm4 - asm)</span></span>

<span data-ttu-id="5ba8f-105">Recupera los datos del búfer o la textura especificados sin ningún filtrado (por ejemplo, el muestreo de puntos) mediante la dirección de entero proporcionada.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-105">Fetches data from the specified buffer or texture without any filtering (e.g. point sampling) using the provided integer address.</span></span> <span data-ttu-id="5ba8f-106">Los datos de origen pueden provienen de cualquier tipo de recurso, que no sea TextureCube.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-106">The source data may come from any resource type, other than TextureCube.</span></span>



| <span data-ttu-id="5ba8f-107">LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5ba8f-107">ld\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="5ba8f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ba8f-108">Item</span></span>                                                                                                               | <span data-ttu-id="5ba8f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ba8f-109">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba8f-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5ba8f-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="5ba8f-111">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-111">\[in\] The address of the result of the operation.</span></span><br/>                                                               |
| <span data-ttu-id="5ba8f-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="5ba8f-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="5ba8f-113">\[en \] las coordenadas de textura necesarias para realizar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-113">\[in\] The texture coordinates needed to perform the sample.</span></span><br/>                                                     |
| <span data-ttu-id="5ba8f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span><span class="sxs-lookup"><span data-stu-id="5ba8f-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="5ba8f-115">\[en \] un registro de textura (t \# ), que se debe haber declarado para identificar la textura o el búfer del que se va a capturar.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-115">\[in\] A texture register (t\#) which must have been declared identifying which Texture or Buffer to fetch from.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ba8f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ba8f-116">Remarks</span></span>

<span data-ttu-id="5ba8f-117">Esta instrucción es una alternativa simplificada a la instrucción de [ejemplo](sample--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="5ba8f-117">This instruction is a simplified alternative to the [sample](sample--sm4---asm-.md) instruction.</span></span> <span data-ttu-id="5ba8f-118">A diferencia del **ejemplo**, **LD** también es capaz de capturar datos de búferes.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-118">Unlike **sample**, **ld** is also capable of fetching data from buffers.</span></span> <span data-ttu-id="5ba8f-119">**LD** también se puede recuperar de recursos de varios ejemplos (solo en el sombreador de píxeles).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-119">**ld** is can also fetch from multi-sample resources (on pixel shader only).</span></span>

<span data-ttu-id="5ba8f-120">*srcAddress* proporciona el conjunto de coordenadas de textura necesarias para realizar el ejemplo en forma de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-120">*srcAddress* provides the set of texture coordinates needed to perform the sample in the form of unsigned integers.</span></span> <span data-ttu-id="5ba8f-121">Si *srcAddress* está fuera del intervalo \[ 0... ( \# textura en dimensión-1) \] , se invoca el comportamiento fuera del límite, donde **LD** devuelve 0 en todos los componentes que no faltan del formato de *srcResource* y el valor predeterminado para los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-121">If *srcAddress* is out of the range\[0...(\#texels in dimension -1)\], then out-of-bounds behavior is invoked, where **ld** returns 0 in all non-missing components of the format of the *srcResource*, and the default for missing components.</span></span> <span data-ttu-id="5ba8f-122">Una aplicación que desee tener un control más flexible sobre el comportamiento de la dirección fuera del intervalo debería usar la instrucción de **ejemplo** en su lugar, ya que respeta el comportamiento de la dirección, el reflejo, la abrazadera y el borde definidos como estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-122">An application wishing any more flexible control over out-of-range address behavior should use the **sample** instruction instead, as it honors address wrap/mirror/clamp/border behavior defined as sampler state.</span></span>

<span data-ttu-id="5ba8f-123">*srcAddress. a* (pos-swizzle) siempre proporciona un nivel de mipmap entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-123">*srcAddress.a* (POS-swizzle) always provides an unsigned integer mipmap level.</span></span> <span data-ttu-id="5ba8f-124">Si el valor está fuera del intervalo \[ 0... ( Num miplevels in Resource-1) \] ), se invoca el comportamiento fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-124">If the value is out of the range \[0...(num miplevels in resource-1)\]), then out-of-bounds behavior is invoked.</span></span> <span data-ttu-id="5ba8f-125">Si el recurso es un búfer, que no puede tener ningún MIP, se omite *srcAddress. a*</span><span class="sxs-lookup"><span data-stu-id="5ba8f-125">If the resource is a buffer, which can not have any mipmaps, then *srcAddress.a* is ignored</span></span>

<span data-ttu-id="5ba8f-126">*srcAddress. GB* (pos-swizzle) se omite para los búferes y texture1D (no matrices).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-126">*srcAddress.gb* (POS-swizzle) is ignored for buffers and texture1D (non-Array).</span></span> <span data-ttu-id="5ba8f-127">*srcAddress. b* (pos-swizzle) se omite para las matrices de Texture1D y texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-127">*srcAddress.b* (POS-swizzle) is ignored for texture1D arrays and texture2Ds.</span></span>

<span data-ttu-id="5ba8f-128">En el caso de las matrices texture1D, *srcAddress. g* (pos-swizzle) proporciona el índice de matriz como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-128">For texture1D arrays, *srcAddress.g* (POS-swizzle) provides the array index as an unsigned integer.</span></span> <span data-ttu-id="5ba8f-129">Si el valor está fuera del intervalo de índices de matriz disponibles \[ 0... ( tamaño de matriz: 1) \] , se invoca el comportamiento fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-129">If the value is out of the range of available array indices \[0...(array size-1)\], then out-of-bounds behavior is invoked.</span></span>

<span data-ttu-id="5ba8f-130">En el caso de las matrices texture2D, *srcAddress. b* (pos-swizzle) proporciona el índice de la matriz, de lo contrario con la misma semántica que para texture1D.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-130">For texture2D arrays, *srcAddress.b* (POS-swizzle) provides the array index, otherwise with same semantics as for texture1D.</span></span>

<span data-ttu-id="5ba8f-131">La captura de *t \#* que no tiene nada enlazado devuelve 0 para todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-131">Fetching from *t\#* that has nothing bound to it returns 0 for all components.</span></span>

### <a name="address-offset"></a><span data-ttu-id="5ba8f-132">Desplazamiento de dirección</span><span class="sxs-lookup"><span data-stu-id="5ba8f-132">Address Offset</span></span>

<span data-ttu-id="5ba8f-133">El \[ \_ sufijo aoffimmi (u, v, w) opcional \] (desplazamiento de dirección por entero inmediato) indica que las coordenadas de textura para la **LD** se van a desplazar por un conjunto de valores constantes de tipo entero de espacio de textura proporcionado.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-133">The optional \[\_aoffimmi(u,v,w)\] suffix (address offset by immediate integer) indicates that the texture coordinates for the **ld** are to be offset by a set of provided immediate texel space integer constant values.</span></span> <span data-ttu-id="5ba8f-134">Los valores literales son un conjunto de números complementarios de 4 bits 2 que tienen un intervalo \[ de enteros de 8 a 7 \] .</span><span class="sxs-lookup"><span data-stu-id="5ba8f-134">The literal values are a set of 4 bit 2's complement numbers, having integer range \[-8,7\].</span></span> <span data-ttu-id="5ba8f-135">Este modificador solo se define para texture1D/2D/3D, incluidas las matrices, y no para los búferes.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-135">This modifier is defined only for texture1D/2D/3D, including arrays, and not for buffers.</span></span>

<span data-ttu-id="5ba8f-136">Los desplazamientos se agregan a las coordenadas de textura, en el espacio textura, con respecto a la miplevel a la que obtiene acceso el **LD**.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-136">The offsets are added to the texture coordinates, in texel space, relative to the miplevel being accessed by the **ld**.</span></span>

<span data-ttu-id="5ba8f-137">Los desplazamientos de direcciones no se aplican a lo largo del eje de matriz de matrices texture1D/2D.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-137">Address offsets are not applied along the array axis of texture1D/2D arrays.</span></span>

<span data-ttu-id="5ba8f-138">Los componentes de *\_ aoffimmi v, w* se omiten para texture1Ds.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-138">The *\_aoffimmi v,w* components are ignored for texture1Ds.</span></span>

<span data-ttu-id="5ba8f-139">El componente *\_ aoffimmi w* se omite para texture2Ds.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-139">The *\_aoffimmi w* component is ignored for texture2Ds.</span></span>

<span data-ttu-id="5ba8f-140">Dado que las coordenadas de textura para **LD** son enteros sin signo, si el desplazamiento hace que la dirección pase por debajo de cero, se ajustará a una dirección grande y se producirá un acceso fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-140">Because the texture coordinates for **ld** are unsigned integers, if the offset causes the address to go below zero, it will wrap to a large address, and result in an out of bounds access.</span></span>

### <a name="return-type-control"></a><span data-ttu-id="5ba8f-141">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ba8f-141">Return Type Control</span></span>

<span data-ttu-id="5ba8f-142">El formato de datos que devuelve **LD** al registro de destino se determina de la misma manera que se describe para la instrucción de **ejemplo** . se basa en el formato enlazado al parámetro *srcResource* (*t \#*).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-142">The data format returned by **ld** to the destination register is determined in the same way as described for the **sample** instruction; it is based on the format bound to the *srcResource* parameter (*t\#*).</span></span>

<span data-ttu-id="5ba8f-143">Al igual que con la instrucción de **ejemplo** , los valores devueltos para **LD** son de 4 vectores con valores predeterminados específicos del formato para los componentes que no están presentes en el formato.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-143">As with the **sample** instruction, returned values for **ld** are 4-vectors with format-specific defaults for components not present in the format.</span></span> <span data-ttu-id="5ba8f-144">El swizzle en *srcResource* determina cómo swizzle el resultado de 4 componentes que se devolverá de la carga de textura, después del cual. Mask en *dest* determina qué componentes de *dest* se actualizan.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-144">The swizzle on *srcResource* determines how to swizzle the 4-component result coming back from the texture load, after which .mask on *dest* determines which components in *dest* get updated.</span></span>

<span data-ttu-id="5ba8f-145">Cuando se lee un valor *float de 32 bits en un* registro de 32 bits, los bits no se tocan; es decir, los valores desnormalizados permanecen desnormalizados.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-145">When a 32-bit float value is read by *ld* into a 32-bit register, the bits are untouched; that is, denormal values remain denormal.</span></span> <span data-ttu-id="5ba8f-146">Esto no es lo mismo que la instrucción de **ejemplo** .</span><span class="sxs-lookup"><span data-stu-id="5ba8f-146">This is unlike the **sample** instruction.</span></span>

### <a name="miscellaneous-details"></a><span data-ttu-id="5ba8f-147">Detalles varios</span><span class="sxs-lookup"><span data-stu-id="5ba8f-147">Miscellaneous Details</span></span>

<span data-ttu-id="5ba8f-148">Como no hay ningún filtrado asociado a la instrucción **LD** , los conceptos como la diferencia de LOD no se aplican a **LD**.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-148">As there is no filtering associated with the **ld** instruction, concepts like LOD bias do not apply to **ld**.</span></span> <span data-ttu-id="5ba8f-149">En consecuencia, no hay *ningún \# parámetro* samples.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-149">Accordingly there is no sampler *s\#* parameter.</span></span>

### <a name="restrictions"></a><span data-ttu-id="5ba8f-150">Restricciones</span><span class="sxs-lookup"><span data-stu-id="5ba8f-150">Restrictions</span></span>

-   <span data-ttu-id="5ba8f-151">*srcResource* debe ser un \# registro t y no un TextureCube.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-151">*srcResource* must be a t\# register, and not a TextureCube.</span></span> <span data-ttu-id="5ba8f-152">*srcResource* no puede ser constantbuffer, que no se puede enlazar a \# registros t.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-152">*srcResource* cannot be a constantbuffer either, which cannot be bound to t\# registers.</span></span>
-   <span data-ttu-id="5ba8f-153">No se permite el direccionamiento relativo en *srcResource* .</span><span class="sxs-lookup"><span data-stu-id="5ba8f-153">Relative addressing on *srcResource* is not permitted.</span></span>
-   <span data-ttu-id="5ba8f-154">*srcAddress* debe ser un registro Temp (r \# /x \# ), Constant (CB \# ) o INPUT (v \# ).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-154">*srcAddress* must be a temp (r\#/x\#), constant (cb\#) or input (v\#) register.</span></span>
-   <span data-ttu-id="5ba8f-155">*dest* debe ser un registro Temp (r \# /x \# ) o Output (o \* \# ).</span><span class="sxs-lookup"><span data-stu-id="5ba8f-155">*dest* must be a temp (r\#/x\#) or output (o\*\#) register.</span></span>

<span data-ttu-id="5ba8f-156">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5ba8f-156">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5ba8f-157">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5ba8f-157">Vertex Shader</span></span> | <span data-ttu-id="5ba8f-158">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="5ba8f-158">Geometry Shader</span></span> | <span data-ttu-id="5ba8f-159">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5ba8f-159">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5ba8f-160">x</span><span class="sxs-lookup"><span data-stu-id="5ba8f-160">x</span></span>             | <span data-ttu-id="5ba8f-161">x</span><span class="sxs-lookup"><span data-stu-id="5ba8f-161">x</span></span>               | <span data-ttu-id="5ba8f-162">x</span><span class="sxs-lookup"><span data-stu-id="5ba8f-162">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5ba8f-163">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5ba8f-163">Minimum Shader Model</span></span>

<span data-ttu-id="5ba8f-164">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5ba8f-164">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5ba8f-165">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5ba8f-165">Shader Model</span></span>                                              | <span data-ttu-id="5ba8f-166">Compatible</span><span class="sxs-lookup"><span data-stu-id="5ba8f-166">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5ba8f-167">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5ba8f-167">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5ba8f-168">sí</span><span class="sxs-lookup"><span data-stu-id="5ba8f-168">yes</span></span>       |
| [<span data-ttu-id="5ba8f-169">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5ba8f-169">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5ba8f-170">sí</span><span class="sxs-lookup"><span data-stu-id="5ba8f-170">yes</span></span>       |
| [<span data-ttu-id="5ba8f-171">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5ba8f-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5ba8f-172">sí</span><span class="sxs-lookup"><span data-stu-id="5ba8f-172">yes</span></span>       |
| [<span data-ttu-id="5ba8f-173">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-173">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5ba8f-174">no</span><span class="sxs-lookup"><span data-stu-id="5ba8f-174">no</span></span>        |
| [<span data-ttu-id="5ba8f-175">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-175">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5ba8f-176">no</span><span class="sxs-lookup"><span data-stu-id="5ba8f-176">no</span></span>        |
| [<span data-ttu-id="5ba8f-177">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-177">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5ba8f-178">no</span><span class="sxs-lookup"><span data-stu-id="5ba8f-178">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5ba8f-179">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ba8f-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ba8f-180">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ba8f-180">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





