---
title: store_structured (SM5-ASM)
description: Escritura de acceso aleatorio de componentes de 1-4 32 bits en una vista de acceso desordenado de búfer estructurado (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077086"
---
# <a name="store_structured-sm5---asm"></a><span data-ttu-id="f8378-103">almacenamiento \_ estructurado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f8378-103">store\_structured (sm5 - asm)</span></span>

<span data-ttu-id="f8378-104">Escritura de acceso aleatorio de componentes de 1-4 32 bits en una vista de acceso desordenado de búfer estructurado (UAV).</span><span class="sxs-lookup"><span data-stu-id="f8378-104">Random-access write of 1-4 32-bit components into a structured buffer unordered access view (UAV).</span></span>



| <span data-ttu-id="f8378-105">Almacene la \_ \[ máscara dst0. Write estructurada, el \_ \] \[ componente dstAddress. Select, el componente \_ \] dstByteOffset \[ . Select \_ \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f8378-105">store\_structured dst0\[.write\_mask\], dstAddress\[.select\_component\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f8378-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f8378-106">Item</span></span>                                                                                                                       | <span data-ttu-id="f8378-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8378-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f8378-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="f8378-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="f8378-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="f8378-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f8378-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="f8378-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/>             | <span data-ttu-id="f8378-111">\[en \] la dirección en la que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="f8378-111">\[in\] The address at which to write.</span></span><br/>               |
| <span data-ttu-id="f8378-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="f8378-112"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="f8378-113">\[en \] el índice de la estructura que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="f8378-113">\[in\] The index of the structure to write.</span></span><br/>         |
| <span data-ttu-id="f8378-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f8378-114"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="f8378-115">\[en \] los componentes que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="f8378-115">\[in\] The components to write.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="f8378-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8378-116">Remarks</span></span>

<span data-ttu-id="f8378-117">Esta instrucción realiza \* los componentes de 32 bits del componente de 1-4 escritos desde *src0* en *dst0* en la dirección de *dstAddress* y *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="f8378-117">This instruction performs 1-4 component \*32bit components written from *src0* to *dst0* at the address in *dstAddress* and *dstByteOffset*.</span></span> <span data-ttu-id="f8378-118">Sin conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="f8378-118">No format conversion.</span></span>

<span data-ttu-id="f8378-119">*dst0* debe ser UAV (u \# ).</span><span class="sxs-lookup"><span data-stu-id="f8378-119">*dst0* must be a UAV (u\#).</span></span> <span data-ttu-id="f8378-120">En el sombreador de cálculo, también puede ser memoria compartida de grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="f8378-120">In the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="f8378-121">*dstAddress* especifica el índice de la estructura que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="f8378-121">*dstAddress* specifies the index of the structure to write.</span></span>

<span data-ttu-id="f8378-122">La ubicación de los datos escritos es equivalente a la del pseudocódigo siguiente, que muestra el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.</span><span class="sxs-lookup"><span data-stu-id="f8378-122">The location of the data written is equivalent to the following pseudocode which shows the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

<span data-ttu-id="f8378-123">En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal.</span><span class="sxs-lookup"><span data-stu-id="f8378-123">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="f8378-124">Si los datos no se almacenan de forma lineal, la operación real de la instrucción debe coincidir con el comportamiento de la operación anterior.</span><span class="sxs-lookup"><span data-stu-id="f8378-124">If the data is not stored linearly, the actual operation of the instruction needs to match the behavior of the above operation.</span></span>

<span data-ttu-id="f8378-125">*dst0* solo puede tener una máscara de escritura que sea uno de los siguientes:. x,. XY,. XYZ,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="f8378-125">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="f8378-126">La máscara de escritura determina el número de componentes de 32 bits que se van a escribir sin huecos.</span><span class="sxs-lookup"><span data-stu-id="f8378-126">The write mask determines the number of 32-bit components to write without gaps.</span></span>

<span data-ttu-id="f8378-127">Fuera de los límites que se direccionan en u \# casued por *dstAddress* significa que no se escribe nada en la memoria fuera de los límites.</span><span class="sxs-lookup"><span data-stu-id="f8378-127">Out of bounds addressing on u\# casued by *dstAddress* means nothing is written to the out of bounds memory.</span></span>

<span data-ttu-id="f8378-128">Si el *dstByteOffset*, incluido *dstWriteMask*, es lo que hace que los límites tengan acceso a usted \# , todo el contenido de la UAV se vuelve sin definir.</span><span class="sxs-lookup"><span data-stu-id="f8378-128">If the *dstByteOffset*, including *dstWriteMask*, is what causes out of bounds access to u\#, the entire contents of the UAV become undefined.</span></span>

<span data-ttu-id="f8378-129">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, hace que todo el contenido de toda la memoria compartida quede sin definir.</span><span class="sxs-lookup"><span data-stu-id="f8378-129">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="f8378-130">*dstByteOffset* es un argumento independiente de *dstAddress* porque suele ser un literal.</span><span class="sxs-lookup"><span data-stu-id="f8378-130">*dstByteOffset* is a separate argument from *dstAddress* because it is commonly a literal.</span></span> <span data-ttu-id="f8378-131">Esta separación de parámetros no se ha realizado para Atomics en la memoria estructurada.</span><span class="sxs-lookup"><span data-stu-id="f8378-131">This parameter separation has not been done for atomics on structured memory.</span></span>

<span data-ttu-id="f8378-132">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y TGSM.</span><span class="sxs-lookup"><span data-stu-id="f8378-132">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and TGSM.</span></span>

<span data-ttu-id="f8378-133">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f8378-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8378-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="f8378-134">Vertex</span></span> | <span data-ttu-id="f8378-135">Casco</span><span class="sxs-lookup"><span data-stu-id="f8378-135">Hull</span></span> | <span data-ttu-id="f8378-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="f8378-136">Domain</span></span> | <span data-ttu-id="f8378-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="f8378-137">Geometry</span></span> | <span data-ttu-id="f8378-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="f8378-138">Pixel</span></span> | <span data-ttu-id="f8378-139">Compute</span><span class="sxs-lookup"><span data-stu-id="f8378-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f8378-140">X</span><span class="sxs-lookup"><span data-stu-id="f8378-140">X</span></span>     | <span data-ttu-id="f8378-141">X</span><span class="sxs-lookup"><span data-stu-id="f8378-141">X</span></span>       |



 

<span data-ttu-id="f8378-142">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f8378-142">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="f8378-143">Vértice</span><span class="sxs-lookup"><span data-stu-id="f8378-143">Vertex</span></span> | <span data-ttu-id="f8378-144">Casco</span><span class="sxs-lookup"><span data-stu-id="f8378-144">Hull</span></span> | <span data-ttu-id="f8378-145">Dominio</span><span class="sxs-lookup"><span data-stu-id="f8378-145">Domain</span></span> | <span data-ttu-id="f8378-146">Geometría</span><span class="sxs-lookup"><span data-stu-id="f8378-146">Geometry</span></span> | <span data-ttu-id="f8378-147">Píxel</span><span class="sxs-lookup"><span data-stu-id="f8378-147">Pixel</span></span> | <span data-ttu-id="f8378-148">Compute</span><span class="sxs-lookup"><span data-stu-id="f8378-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f8378-149">X</span><span class="sxs-lookup"><span data-stu-id="f8378-149">X</span></span>      | <span data-ttu-id="f8378-150">X</span><span class="sxs-lookup"><span data-stu-id="f8378-150">X</span></span>    | <span data-ttu-id="f8378-151">X</span><span class="sxs-lookup"><span data-stu-id="f8378-151">X</span></span>      | <span data-ttu-id="f8378-152">X</span><span class="sxs-lookup"><span data-stu-id="f8378-152">X</span></span>        | <span data-ttu-id="f8378-153">X</span><span class="sxs-lookup"><span data-stu-id="f8378-153">X</span></span>     | <span data-ttu-id="f8378-154">X</span><span class="sxs-lookup"><span data-stu-id="f8378-154">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8378-155">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f8378-155">Minimum Shader Model</span></span>

<span data-ttu-id="f8378-156">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f8378-156">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f8378-157">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f8378-157">Shader Model</span></span>                                              | <span data-ttu-id="f8378-158">Compatible</span><span class="sxs-lookup"><span data-stu-id="f8378-158">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8378-159">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f8378-159">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8378-160">sí</span><span class="sxs-lookup"><span data-stu-id="f8378-160">yes</span></span>       |
| [<span data-ttu-id="f8378-161">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f8378-161">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8378-162">no</span><span class="sxs-lookup"><span data-stu-id="f8378-162">no</span></span>        |
| [<span data-ttu-id="f8378-163">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f8378-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8378-164">no</span><span class="sxs-lookup"><span data-stu-id="f8378-164">no</span></span>        |
| [<span data-ttu-id="f8378-165">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8378-165">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8378-166">no</span><span class="sxs-lookup"><span data-stu-id="f8378-166">no</span></span>        |
| [<span data-ttu-id="f8378-167">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8378-167">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8378-168">no</span><span class="sxs-lookup"><span data-stu-id="f8378-168">no</span></span>        |
| [<span data-ttu-id="f8378-169">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8378-169">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8378-170">no</span><span class="sxs-lookup"><span data-stu-id="f8378-170">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8378-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8378-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8378-172">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8378-172">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





