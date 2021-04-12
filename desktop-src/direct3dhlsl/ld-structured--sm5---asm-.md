---
title: ld_structured (SM5-ASM)
description: Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer estructurado.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419949"
---
# <a name="ld_structured-sm5---asm"></a><span data-ttu-id="db6a1-103">LD \_ estructurado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="db6a1-103">ld\_structured (sm5 - asm)</span></span>

<span data-ttu-id="db6a1-104">Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer estructurado.</span><span class="sxs-lookup"><span data-stu-id="db6a1-104">Random-access read of 1-4 32bit components from a structured buffer.</span></span>



| <span data-ttu-id="db6a1-105">: LD \_ estructurado dst0 \[ . Mask \] , srcAddress \[ . Select \_ Component \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="db6a1-105">: ld\_structured dst0\[.mask\], srcAddress\[.select\_component\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="db6a1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="db6a1-106">Item</span></span>                                                                                                                       | <span data-ttu-id="db6a1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="db6a1-107">Description</span></span>                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6a1-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="db6a1-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="db6a1-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="db6a1-109">\[in\] The address of the results of the operation.</span></span><br/>                                                                                             |
| <span data-ttu-id="db6a1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="db6a1-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>             | <span data-ttu-id="db6a1-111">\[en \] especifica el índice de la estructura que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="db6a1-111">\[in\] Specifies the index of the structure to read.</span></span><br/>                                                                                            |
| <span data-ttu-id="db6a1-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="db6a1-112"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="db6a1-113">\[en \] especifica el desplazamiento de bytes de la estructura en la que se va a empezar a leer.</span><span class="sxs-lookup"><span data-stu-id="db6a1-113">\[in\] Specifies the byte offset in the structure to start reading from.</span></span> <br/>                                                                       |
| <span data-ttu-id="db6a1-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="db6a1-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="db6a1-115">Búfer del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="db6a1-115">The buffer to read from.</span></span> <span data-ttu-id="db6a1-116">Este parámetro debe ser SRV (t \# ), UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="db6a1-116">This parameter must be a SRV (t\#), UAV (u\#).</span></span> <span data-ttu-id="db6a1-117">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="db6a1-117">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="db6a1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db6a1-118">Remarks</span></span>

<span data-ttu-id="db6a1-119">Los datos leídos de la estructura son equivalentes a los siguientes pseudocódigo: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.</span><span class="sxs-lookup"><span data-stu-id="db6a1-119">The data read from the structure is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="db6a1-120">En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal.</span><span class="sxs-lookup"><span data-stu-id="db6a1-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="db6a1-121">Si los datos no se almacenan de forma lineal, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.</span><span class="sxs-lookup"><span data-stu-id="db6a1-121">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="db6a1-122">Fuera de los límites que se direccionan en u \# /t \# de cualquier componente de 32 bits dado devuelve 0 para ese componente, excepto si *srcByteOffset*, más swizzle es lo que hace que los límites de los límites tengan acceso a \# la dirección/t \# , el valor devuelto para todos los componentes es indefinido.</span><span class="sxs-lookup"><span data-stu-id="db6a1-122">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component, except if *srcByteOffset*, plus swizzle is what causes out of bounds access to u\#/t\#, the returned value for all component(s) is undefined.</span></span>

<span data-ttu-id="db6a1-123">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, devuelve un resultado no definido.</span><span class="sxs-lookup"><span data-stu-id="db6a1-123">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="db6a1-124">*srcByteOffset* es un argumento independiente de *srcAddress* porque suele ser un literal.</span><span class="sxs-lookup"><span data-stu-id="db6a1-124">*srcByteOffset* is a separate argument from *srcAddress* because it is commonly a literal.</span></span> <span data-ttu-id="db6a1-125">Esta separación de parámetros no se ha realizado para Atomics en la memoria estructurada.</span><span class="sxs-lookup"><span data-stu-id="db6a1-125">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="db6a1-126">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.</span><span class="sxs-lookup"><span data-stu-id="db6a1-126">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV, and TGSM.</span></span>

<span data-ttu-id="db6a1-127">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="db6a1-127">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db6a1-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="db6a1-128">Vertex</span></span> | <span data-ttu-id="db6a1-129">Casco</span><span class="sxs-lookup"><span data-stu-id="db6a1-129">Hull</span></span> | <span data-ttu-id="db6a1-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="db6a1-130">Domain</span></span> | <span data-ttu-id="db6a1-131">Geometría</span><span class="sxs-lookup"><span data-stu-id="db6a1-131">Geometry</span></span> | <span data-ttu-id="db6a1-132">Píxel</span><span class="sxs-lookup"><span data-stu-id="db6a1-132">Pixel</span></span> | <span data-ttu-id="db6a1-133">Compute</span><span class="sxs-lookup"><span data-stu-id="db6a1-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db6a1-134">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-134">X</span></span>      | <span data-ttu-id="db6a1-135">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-135">X</span></span>    | <span data-ttu-id="db6a1-136">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-136">X</span></span>      | <span data-ttu-id="db6a1-137">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-137">X</span></span>        | <span data-ttu-id="db6a1-138">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-138">X</span></span>     | <span data-ttu-id="db6a1-139">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-139">X</span></span>       |



 

<span data-ttu-id="db6a1-140">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para UAVs para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="db6a1-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="db6a1-141">Vértice</span><span class="sxs-lookup"><span data-stu-id="db6a1-141">Vertex</span></span> | <span data-ttu-id="db6a1-142">Casco</span><span class="sxs-lookup"><span data-stu-id="db6a1-142">Hull</span></span> | <span data-ttu-id="db6a1-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="db6a1-143">Domain</span></span> | <span data-ttu-id="db6a1-144">Geometría</span><span class="sxs-lookup"><span data-stu-id="db6a1-144">Geometry</span></span> | <span data-ttu-id="db6a1-145">Píxel</span><span class="sxs-lookup"><span data-stu-id="db6a1-145">Pixel</span></span> | <span data-ttu-id="db6a1-146">Compute</span><span class="sxs-lookup"><span data-stu-id="db6a1-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db6a1-147">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-147">X</span></span>      | <span data-ttu-id="db6a1-148">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-148">X</span></span>    | <span data-ttu-id="db6a1-149">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-149">X</span></span>      | <span data-ttu-id="db6a1-150">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-150">X</span></span>        | <span data-ttu-id="db6a1-151">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-151">X</span></span>     | <span data-ttu-id="db6a1-152">X</span><span class="sxs-lookup"><span data-stu-id="db6a1-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db6a1-153">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="db6a1-153">Minimum Shader Model</span></span>

<span data-ttu-id="db6a1-154">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="db6a1-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="db6a1-155">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="db6a1-155">Shader Model</span></span>                                              | <span data-ttu-id="db6a1-156">Compatible</span><span class="sxs-lookup"><span data-stu-id="db6a1-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db6a1-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="db6a1-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db6a1-158">sí</span><span class="sxs-lookup"><span data-stu-id="db6a1-158">yes</span></span>       |
| [<span data-ttu-id="db6a1-159">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="db6a1-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db6a1-160">no</span><span class="sxs-lookup"><span data-stu-id="db6a1-160">no</span></span>        |
| [<span data-ttu-id="db6a1-161">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="db6a1-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db6a1-162">no</span><span class="sxs-lookup"><span data-stu-id="db6a1-162">no</span></span>        |
| [<span data-ttu-id="db6a1-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db6a1-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db6a1-164">no</span><span class="sxs-lookup"><span data-stu-id="db6a1-164">no</span></span>        |
| [<span data-ttu-id="db6a1-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db6a1-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db6a1-166">no</span><span class="sxs-lookup"><span data-stu-id="db6a1-166">no</span></span>        |
| [<span data-ttu-id="db6a1-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db6a1-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db6a1-168">no</span><span class="sxs-lookup"><span data-stu-id="db6a1-168">no</span></span>        |



 

<span data-ttu-id="db6a1-169">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.</span><span class="sxs-lookup"><span data-stu-id="db6a1-169">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db6a1-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db6a1-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db6a1-171">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db6a1-171">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





