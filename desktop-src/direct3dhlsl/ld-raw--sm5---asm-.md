---
title: ld_raw (SM5-ASM)
description: Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer sin formato.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983859"
---
# <a name="ld_raw-sm5---asm"></a><span data-ttu-id="8af5d-103">LD \_ sin formato (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8af5d-103">ld\_raw (sm5 - asm)</span></span>

<span data-ttu-id="8af5d-104">Lectura de acceso aleatorio de componentes de 32 bits de 1-4 desde un búfer sin formato.</span><span class="sxs-lookup"><span data-stu-id="8af5d-104">Random-access read of 1-4 32bit components from a raw buffer.</span></span>



| <span data-ttu-id="8af5d-105">LD \_ raw dst0 \[ . Mask \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8af5d-105">ld\_raw dst0\[.mask\], srcByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------|



 



| <span data-ttu-id="8af5d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="8af5d-106">Item</span></span>                                                                                                                       | <span data-ttu-id="8af5d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8af5d-107">Description</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8af5d-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="8af5d-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="8af5d-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="8af5d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="8af5d-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span><span class="sxs-lookup"><span data-stu-id="8af5d-110"><span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*</span></span><br/> | <span data-ttu-id="8af5d-111">\[en \] especifica el desplazamiento del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="8af5d-111">\[in\] Specifies the offset to read from.</span></span><br/>          |
| <span data-ttu-id="8af5d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8af5d-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="8af5d-113">\[en \] el componente que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="8af5d-113">\[in\] The component to read.</span></span> <br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="8af5d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8af5d-114">Remarks</span></span>

<span data-ttu-id="8af5d-115">*src0* debe ser:</span><span class="sxs-lookup"><span data-stu-id="8af5d-115">*src0* must be:</span></span>

-   <span data-ttu-id="8af5d-116">Cualquier fase del sombreador: SRV (t \# ) LD St</span><span class="sxs-lookup"><span data-stu-id="8af5d-116">Any shader stage: SRV (t\#)ld st</span></span>
-   <span data-ttu-id="8af5d-117">Sombreador de cálculo o sombreador de píxeles: UAV (u \# )</span><span class="sxs-lookup"><span data-stu-id="8af5d-117">Compute shader or pixel shader: UAV (u\#)</span></span>
-   <span data-ttu-id="8af5d-118">Sombreador de cálculo: memoria compartida de grupo de subprocesos (g \# )</span><span class="sxs-lookup"><span data-stu-id="8af5d-118">Compute shader: thread group shared memory (g\#)</span></span>

<span data-ttu-id="8af5d-119">*srcByteOffset* especifica el valor de base 32 bits en memoria para una ventana de 4 valores de 32 bits secuenciales en los que se pueden leer los datos, en función de la swizzle y de la máscara de otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="8af5d-119">*srcByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be read, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="8af5d-120">Los datos leídos del búfer sin formato son equivalentes a los siguientes pseudocódigo: donde tenemos el desplazamiento, la dirección, el puntero al contenido del búfer, el paso del origen y los datos almacenados linealmente.</span><span class="sxs-lookup"><span data-stu-id="8af5d-120">The data read from the raw buffer is equivalent to the following pseudocode: where we have the offset, address, pointer to the buffer contents, stride of the source, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

<span data-ttu-id="8af5d-121">Fuera de los límites que se direccionan en u \# /t \# de cualquier componente de 32 bits determinado devuelve 0 para ese componente.</span><span class="sxs-lookup"><span data-stu-id="8af5d-121">Out of bounds addressing on u\#/t\# of any given 32-bit component returns 0 for that component.</span></span>

<span data-ttu-id="8af5d-122">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, devuelve un resultado no definido.</span><span class="sxs-lookup"><span data-stu-id="8af5d-122">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component returns an undefined result.</span></span>

<span data-ttu-id="8af5d-123">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.</span><span class="sxs-lookup"><span data-stu-id="8af5d-123">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

<span data-ttu-id="8af5d-124">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8af5d-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8af5d-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="8af5d-125">Vertex</span></span> | <span data-ttu-id="8af5d-126">Casco</span><span class="sxs-lookup"><span data-stu-id="8af5d-126">Hull</span></span> | <span data-ttu-id="8af5d-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="8af5d-127">Domain</span></span> | <span data-ttu-id="8af5d-128">Geometría</span><span class="sxs-lookup"><span data-stu-id="8af5d-128">Geometry</span></span> | <span data-ttu-id="8af5d-129">Píxel</span><span class="sxs-lookup"><span data-stu-id="8af5d-129">Pixel</span></span> | <span data-ttu-id="8af5d-130">Compute</span><span class="sxs-lookup"><span data-stu-id="8af5d-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8af5d-131">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-131">X</span></span>      | <span data-ttu-id="8af5d-132">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-132">X</span></span>    | <span data-ttu-id="8af5d-133">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-133">X</span></span>      | <span data-ttu-id="8af5d-134">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-134">X</span></span>        | <span data-ttu-id="8af5d-135">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-135">X</span></span>     | <span data-ttu-id="8af5d-136">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-136">X</span></span>       |



 

<span data-ttu-id="8af5d-137">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para UAVs para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8af5d-137">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for UAVs for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="8af5d-138">Vértice</span><span class="sxs-lookup"><span data-stu-id="8af5d-138">Vertex</span></span> | <span data-ttu-id="8af5d-139">Casco</span><span class="sxs-lookup"><span data-stu-id="8af5d-139">Hull</span></span> | <span data-ttu-id="8af5d-140">Dominio</span><span class="sxs-lookup"><span data-stu-id="8af5d-140">Domain</span></span> | <span data-ttu-id="8af5d-141">Geometría</span><span class="sxs-lookup"><span data-stu-id="8af5d-141">Geometry</span></span> | <span data-ttu-id="8af5d-142">Píxel</span><span class="sxs-lookup"><span data-stu-id="8af5d-142">Pixel</span></span> | <span data-ttu-id="8af5d-143">Compute</span><span class="sxs-lookup"><span data-stu-id="8af5d-143">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8af5d-144">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-144">X</span></span>      | <span data-ttu-id="8af5d-145">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-145">X</span></span>    | <span data-ttu-id="8af5d-146">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-146">X</span></span>      | <span data-ttu-id="8af5d-147">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-147">X</span></span>        | <span data-ttu-id="8af5d-148">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-148">X</span></span>     | <span data-ttu-id="8af5d-149">X</span><span class="sxs-lookup"><span data-stu-id="8af5d-149">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8af5d-150">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8af5d-150">Minimum Shader Model</span></span>

<span data-ttu-id="8af5d-151">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8af5d-151">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8af5d-152">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8af5d-152">Shader Model</span></span>                                              | <span data-ttu-id="8af5d-153">Compatible</span><span class="sxs-lookup"><span data-stu-id="8af5d-153">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8af5d-154">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8af5d-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8af5d-155">sí</span><span class="sxs-lookup"><span data-stu-id="8af5d-155">yes</span></span>       |
| [<span data-ttu-id="8af5d-156">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8af5d-156">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8af5d-157">no</span><span class="sxs-lookup"><span data-stu-id="8af5d-157">no</span></span>        |
| [<span data-ttu-id="8af5d-158">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8af5d-158">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8af5d-159">no</span><span class="sxs-lookup"><span data-stu-id="8af5d-159">no</span></span>        |
| [<span data-ttu-id="8af5d-160">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8af5d-160">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8af5d-161">no</span><span class="sxs-lookup"><span data-stu-id="8af5d-161">no</span></span>        |
| [<span data-ttu-id="8af5d-162">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8af5d-162">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8af5d-163">no</span><span class="sxs-lookup"><span data-stu-id="8af5d-163">no</span></span>        |
| [<span data-ttu-id="8af5d-164">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8af5d-164">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8af5d-165">no</span><span class="sxs-lookup"><span data-stu-id="8af5d-165">no</span></span>        |



 

<span data-ttu-id="8af5d-166">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.</span><span class="sxs-lookup"><span data-stu-id="8af5d-166">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8af5d-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8af5d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af5d-168">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8af5d-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





