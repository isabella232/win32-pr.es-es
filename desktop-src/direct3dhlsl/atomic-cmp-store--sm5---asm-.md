---
title: atomic_cmp_store (SM5-ASM)
description: Comparación atómica y escritura en la memoria.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a5292d65b32988017044a2ec52680848dffbef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784978"
---
# <a name="atomic_cmp_store-sm5---asm"></a><span data-ttu-id="e8bb7-103">\_almacén atómico \_ de CMP (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e8bb7-103">atomic\_cmp\_store (sm5 - asm)</span></span>

<span data-ttu-id="e8bb7-104">Comparación atómica y escritura en la memoria.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-104">Atomic compare and write to memory.</span></span>



| <span data-ttu-id="e8bb7-105">almacén atómico de \_ CMP \_ , DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_ \] , componente SRC1 \[ . Select. \_\]</span><span class="sxs-lookup"><span data-stu-id="e8bb7-105">atomic\_cmp\_store dst, dstAddress\[.swizzle\], src0\[.select\_component\], src1\[.select\_component\]</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e8bb7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8bb7-106">Item</span></span>                                                                                                           | <span data-ttu-id="e8bb7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8bb7-107">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bb7-108"><span id="dst"></span><span id="DST"></span>*DST*</span><span class="sxs-lookup"><span data-stu-id="e8bb7-108"><span id="dst"></span><span id="DST"></span>*dst*</span></span><br/>                                                   | <span data-ttu-id="e8bb7-109">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-109">\[in\] The components to compare with *src0*.</span></span> <span data-ttu-id="e8bb7-110">Este valor debe ser una vista de acceso desordenado (UAV) (u \# ).</span><span class="sxs-lookup"><span data-stu-id="e8bb7-110">This value must be an unordered access view (UAV) (u\#).</span></span> <span data-ttu-id="e8bb7-111">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="e8bb7-111">In the compute shader it can also be thread group shared memory (g\#).</span></span> <br/> |
| <span data-ttu-id="e8bb7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="e8bb7-112"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="e8bb7-113">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-113">\[in\] The memory address.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="e8bb7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e8bb7-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="e8bb7-115">\[en \] el valor de 32 bits para comparar con el *DST*.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-115">\[in\] The 32-bit value to compare with *dst*.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="e8bb7-116"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="e8bb7-116"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                                | <span data-ttu-id="e8bb7-117">\[en \] el valor que se va a escribir en la memoria si los valores comparados son idénticos.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-117">\[in\] The value to write to memory if the compared values are identical.</span></span> <br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="e8bb7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8bb7-118">Remarks</span></span>

<span data-ttu-id="e8bb7-119">Esta instrucción realiza una comparación de valores de 32 bits de un solo componente de operando *src0* con *DST* en 32 bits por dirección de componente *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-119">This instruction performs a single component 32-bit value compare of operand *src0* with *dst* at 32-bit per component address *dstAddress*.</span></span>

<span data-ttu-id="e8bb7-120">Si los valores comparados son idénticos, el valor de 32 bits de un solo componente de *SRC1* se escribe en la memoria de destino.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-120">If the compared values are identical, the single-component 32-bit value in *src1* is written to destination memory.</span></span> <span data-ttu-id="e8bb7-121">De lo contrario, no se cambia el destino.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-121">Otherwise, the destination is not changed.</span></span>

<span data-ttu-id="e8bb7-122">Toda la operación de comparación y escritura se realiza de forma atómica.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-122">The entire compare and write operation is performed atomically.</span></span>

<span data-ttu-id="e8bb7-123">Si el *DST* es una u \# , se puede declarar como sin formato, con tipo o estructurada.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-123">If *dst* is a u\#, it can be declared as raw, typed or structured.</span></span> <span data-ttu-id="e8bb7-124">Si tiene un tipo, debe declararse como UINT/SINT con el formato de recurso enlazado R32 \_ uint/ \_ Sint.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-124">If typed, it must be declared as UINT/SINT with the bound resource format being R32\_UINT/\_SINT.</span></span>

<span data-ttu-id="e8bb7-125">Si *DST* es g \# , debe declararse como RAW o Structured.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-125">If *dst* is g\#, it must be declared as raw or structured.</span></span>

<span data-ttu-id="e8bb7-126">El número de componentes tomado de la dirección viene determinado por la dimensionalidad del DST u \# o g \# .</span><span class="sxs-lookup"><span data-stu-id="e8bb7-126">The number of components taken from the address is determined by the dimensionality of dst u\# or g\#.</span></span>

<span data-ttu-id="e8bb7-127">No se devuelve nada al sombreador.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-127">Nothing is returned to the shader.</span></span>

<span data-ttu-id="e8bb7-128">Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o una instrucción de ejemplo o píxel no modifica la memoria de *DST* en absoluto (en modo silencioso).</span><span class="sxs-lookup"><span data-stu-id="e8bb7-128">If the shader invocation is inactive, for example if the pixel has been discarded earlier in its execution, or a pixel/sample instruction does not alter the *dst* memory at all (silently).</span></span>

<span data-ttu-id="e8bb7-129">Fuera del límite el direccionamiento en u \# hace que no se escriba nada en la memoria, excepto si la u \# está estructurada y el desplazamiento de bytes en el struct (componente de segundo de la dirección) está provocando el acceso fuera de los límites, todo el contenido de UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-129">Out of bounds addressing on u\# causes nothing to be written to memory, except if the u\# is structured, and byte offset into the struct (second component of the address) is causing the out of bounds access, then the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="e8bb7-130">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida), hace que todo el contenido de toda la memoria compartida quede sin definir.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-130">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="e8bb7-131">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8bb7-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e8bb7-132">Vértice</span><span class="sxs-lookup"><span data-stu-id="e8bb7-132">Vertex</span></span> | <span data-ttu-id="e8bb7-133">Casco</span><span class="sxs-lookup"><span data-stu-id="e8bb7-133">Hull</span></span> | <span data-ttu-id="e8bb7-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="e8bb7-134">Domain</span></span> | <span data-ttu-id="e8bb7-135">Geometría</span><span class="sxs-lookup"><span data-stu-id="e8bb7-135">Geometry</span></span> | <span data-ttu-id="e8bb7-136">Píxel</span><span class="sxs-lookup"><span data-stu-id="e8bb7-136">Pixel</span></span> | <span data-ttu-id="e8bb7-137">Compute</span><span class="sxs-lookup"><span data-stu-id="e8bb7-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e8bb7-138">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-138">X</span></span>     | <span data-ttu-id="e8bb7-139">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-139">X</span></span>       |



 

<span data-ttu-id="e8bb7-140">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e8bb7-140">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e8bb7-141">Vértice</span><span class="sxs-lookup"><span data-stu-id="e8bb7-141">Vertex</span></span> | <span data-ttu-id="e8bb7-142">Casco</span><span class="sxs-lookup"><span data-stu-id="e8bb7-142">Hull</span></span> | <span data-ttu-id="e8bb7-143">Dominio</span><span class="sxs-lookup"><span data-stu-id="e8bb7-143">Domain</span></span> | <span data-ttu-id="e8bb7-144">Geometría</span><span class="sxs-lookup"><span data-stu-id="e8bb7-144">Geometry</span></span> | <span data-ttu-id="e8bb7-145">Píxel</span><span class="sxs-lookup"><span data-stu-id="e8bb7-145">Pixel</span></span> | <span data-ttu-id="e8bb7-146">Compute</span><span class="sxs-lookup"><span data-stu-id="e8bb7-146">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e8bb7-147">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-147">X</span></span>      | <span data-ttu-id="e8bb7-148">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-148">X</span></span>    | <span data-ttu-id="e8bb7-149">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-149">X</span></span>      | <span data-ttu-id="e8bb7-150">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-150">X</span></span>        | <span data-ttu-id="e8bb7-151">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-151">X</span></span>     | <span data-ttu-id="e8bb7-152">X</span><span class="sxs-lookup"><span data-stu-id="e8bb7-152">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8bb7-153">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e8bb7-153">Minimum Shader Model</span></span>

<span data-ttu-id="e8bb7-154">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e8bb7-154">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e8bb7-155">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e8bb7-155">Shader Model</span></span>                                              | <span data-ttu-id="e8bb7-156">Compatible</span><span class="sxs-lookup"><span data-stu-id="e8bb7-156">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e8bb7-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e8bb7-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e8bb7-158">sí</span><span class="sxs-lookup"><span data-stu-id="e8bb7-158">yes</span></span>       |
| [<span data-ttu-id="e8bb7-159">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e8bb7-159">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e8bb7-160">no</span><span class="sxs-lookup"><span data-stu-id="e8bb7-160">no</span></span>        |
| [<span data-ttu-id="e8bb7-161">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e8bb7-161">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8bb7-162">no</span><span class="sxs-lookup"><span data-stu-id="e8bb7-162">no</span></span>        |
| [<span data-ttu-id="e8bb7-163">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8bb7-163">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8bb7-164">no</span><span class="sxs-lookup"><span data-stu-id="e8bb7-164">no</span></span>        |
| [<span data-ttu-id="e8bb7-165">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8bb7-165">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8bb7-166">no</span><span class="sxs-lookup"><span data-stu-id="e8bb7-166">no</span></span>        |
| [<span data-ttu-id="e8bb7-167">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8bb7-167">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8bb7-168">no</span><span class="sxs-lookup"><span data-stu-id="e8bb7-168">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e8bb7-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8bb7-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8bb7-170">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8bb7-170">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





