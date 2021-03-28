---
title: store_raw (SM5-ASM)
description: Escritura de acceso aleatorio de componentes de 32 bits de 1-4 en memoria sin tipo.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419975"
---
# <a name="store_raw-sm5---asm"></a><span data-ttu-id="712a6-103">almacén \_ sin procesar (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="712a6-103">store\_raw (sm5 - asm)</span></span>

<span data-ttu-id="712a6-104">Escritura de acceso aleatorio de componentes de 32 bits de 1-4 en memoria sin tipo.</span><span class="sxs-lookup"><span data-stu-id="712a6-104">Random-access write of 1-4 32bit components into typeless memory.</span></span>



| <span data-ttu-id="712a6-105">Almacene la \_ \[ máscara dst0. Write sin formato, el \_ \] \[ componente dstByteOffset. Select \_ \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="712a6-105">store\_raw dst0\[.write\_mask\], dstByteOffset\[.select\_component\], src0\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------|



 



| <span data-ttu-id="712a6-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="712a6-106">Item</span></span>                                                                                                                       | <span data-ttu-id="712a6-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="712a6-107">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span data-ttu-id="712a6-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="712a6-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                            | <span data-ttu-id="712a6-109">\[en \] la dirección de memoria.</span><span class="sxs-lookup"><span data-stu-id="712a6-109">\[in\] The memory address.</span></span><br/>      |
| <span data-ttu-id="712a6-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span><span class="sxs-lookup"><span data-stu-id="712a6-110"><span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*</span></span><br/> | <span data-ttu-id="712a6-111">\[en \] el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="712a6-111">\[in\] The offset.</span></span><br/>              |
| <span data-ttu-id="712a6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="712a6-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                            | <span data-ttu-id="712a6-113">\[en \] los componentes que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="712a6-113">\[in\] The components to write.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="712a6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="712a6-114">Remarks</span></span>

<span data-ttu-id="712a6-115">Esta instrucción realiza componentes de 1-4 de componentes de 32 de componente \* escritos desde *src0* en *dst0* en el desplazamiento en *dstByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="712a6-115">This instruction performs 1-4 component \*32-bit components written from *src0* to *dst0* at the offset in *dstByteOffset*.</span></span> <span data-ttu-id="712a6-116">No hay ninguna conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="712a6-116">There is no format conversion.</span></span>

<span data-ttu-id="712a6-117">*dst0* debe ser un UAV (u \# ) o, en el sombreador de cálculo, también puede ser la memoria compartida del grupo de subprocesos (g \# ).</span><span class="sxs-lookup"><span data-stu-id="712a6-117">*dst0* must be a UAV (u\#), or in the compute shader it can also be thread group shared memory (g\#).</span></span>

<span data-ttu-id="712a6-118">*dstByteOffset* especifica el valor de base 32 bits en memoria para una ventana de 4 valores de 32 bits secuenciales en los que se pueden escribir datos, en función de la swizzle y de la máscara de otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="712a6-118">*dstByteOffset* specifies the base 32-bit value in memory for a window of 4 sequential 32-bit values in which data may be written, depending on the swizzle and mask on other parameters.</span></span>

<span data-ttu-id="712a6-119">La ubicación de los datos escritos es equivalente al siguiente pseudocódigo que muestra la dirección, el puntero al contenido del búfer y los datos almacenados de forma lineal.</span><span class="sxs-lookup"><span data-stu-id="712a6-119">The location of the data written is equivalent to the following pseudocode which show the address, pointer to the buffer contents, and the data stored linearly.</span></span>

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

<span data-ttu-id="712a6-120">En este pseudocódigo se muestra cómo funciona la operación, pero no es necesario que los datos reales se almacenen de forma lineal.</span><span class="sxs-lookup"><span data-stu-id="712a6-120">This pseudocode shows how the operation functions, but the actual data does not have to be stored linearly.</span></span> <span data-ttu-id="712a6-121">*dst0* solo puede tener una máscara de escritura que sea uno de los siguientes:. x,. XY,. XYZ,. xyzw.</span><span class="sxs-lookup"><span data-stu-id="712a6-121">*dst0* can only have a write mask that is one of the following: .x, .xy, .xyz, .xyzw.</span></span> <span data-ttu-id="712a6-122">La máscara de escritura determina el número de componentes de 32 bits que se van a escribir sin huecos.</span><span class="sxs-lookup"><span data-stu-id="712a6-122">The write mask determines the number of 32bit components to write without gaps.</span></span>

<span data-ttu-id="712a6-123">Fuera del límite, el direccionamiento en u \# significa que no se escribe nada en la memoria fuera de los límites; cualquier parte que esté en los límites se escribe correctamente.</span><span class="sxs-lookup"><span data-stu-id="712a6-123">Out of bounds addressing on u\# means nothing is written to the out of bounds memory; any part that is in bounds is written correctly.</span></span>

<span data-ttu-id="712a6-124">Fuera de los límites que se dirigen a g \# (los límites de esa g concreta \# , en contraposición a toda la memoria compartida) de cualquier componente de 32 bits dado, hace que todo el contenido de toda la memoria compartida quede sin definir.</span><span class="sxs-lookup"><span data-stu-id="712a6-124">Out of bounds addressing on g\# (the bounds of that particular g\#, as opposed to all shared memory) for any given 32-bit component causes the entire contents of all shared memory to become undefined.</span></span>

<span data-ttu-id="712a6-125">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV.</span><span class="sxs-lookup"><span data-stu-id="712a6-125">cs\_4\_0 and cs\_4\_1 support this instruction for UAV.</span></span>

<span data-ttu-id="712a6-126">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="712a6-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="712a6-127">Vértice</span><span class="sxs-lookup"><span data-stu-id="712a6-127">Vertex</span></span> | <span data-ttu-id="712a6-128">Casco</span><span class="sxs-lookup"><span data-stu-id="712a6-128">Hull</span></span> | <span data-ttu-id="712a6-129">Dominio</span><span class="sxs-lookup"><span data-stu-id="712a6-129">Domain</span></span> | <span data-ttu-id="712a6-130">Geometría</span><span class="sxs-lookup"><span data-stu-id="712a6-130">Geometry</span></span> | <span data-ttu-id="712a6-131">Píxel</span><span class="sxs-lookup"><span data-stu-id="712a6-131">Pixel</span></span> | <span data-ttu-id="712a6-132">Compute</span><span class="sxs-lookup"><span data-stu-id="712a6-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="712a6-133">X</span><span class="sxs-lookup"><span data-stu-id="712a6-133">X</span></span>     | <span data-ttu-id="712a6-134">X</span><span class="sxs-lookup"><span data-stu-id="712a6-134">X</span></span>       |



 

<span data-ttu-id="712a6-135">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="712a6-135">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="712a6-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="712a6-136">Vertex</span></span> | <span data-ttu-id="712a6-137">Casco</span><span class="sxs-lookup"><span data-stu-id="712a6-137">Hull</span></span> | <span data-ttu-id="712a6-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="712a6-138">Domain</span></span> | <span data-ttu-id="712a6-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="712a6-139">Geometry</span></span> | <span data-ttu-id="712a6-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="712a6-140">Pixel</span></span> | <span data-ttu-id="712a6-141">Compute</span><span class="sxs-lookup"><span data-stu-id="712a6-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="712a6-142">X</span><span class="sxs-lookup"><span data-stu-id="712a6-142">X</span></span>      | <span data-ttu-id="712a6-143">X</span><span class="sxs-lookup"><span data-stu-id="712a6-143">X</span></span>    | <span data-ttu-id="712a6-144">X</span><span class="sxs-lookup"><span data-stu-id="712a6-144">X</span></span>      | <span data-ttu-id="712a6-145">X</span><span class="sxs-lookup"><span data-stu-id="712a6-145">X</span></span>        | <span data-ttu-id="712a6-146">X</span><span class="sxs-lookup"><span data-stu-id="712a6-146">X</span></span>     | <span data-ttu-id="712a6-147">X</span><span class="sxs-lookup"><span data-stu-id="712a6-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="712a6-148">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="712a6-148">Minimum Shader Model</span></span>

<span data-ttu-id="712a6-149">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="712a6-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="712a6-150">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="712a6-150">Shader Model</span></span>                                              | <span data-ttu-id="712a6-151">Compatible</span><span class="sxs-lookup"><span data-stu-id="712a6-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="712a6-152">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="712a6-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="712a6-153">sí</span><span class="sxs-lookup"><span data-stu-id="712a6-153">yes</span></span>       |
| [<span data-ttu-id="712a6-154">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="712a6-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="712a6-155">no</span><span class="sxs-lookup"><span data-stu-id="712a6-155">no</span></span>        |
| [<span data-ttu-id="712a6-156">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="712a6-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="712a6-157">no</span><span class="sxs-lookup"><span data-stu-id="712a6-157">no</span></span>        |
| [<span data-ttu-id="712a6-158">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712a6-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="712a6-159">no</span><span class="sxs-lookup"><span data-stu-id="712a6-159">no</span></span>        |
| [<span data-ttu-id="712a6-160">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712a6-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="712a6-161">no</span><span class="sxs-lookup"><span data-stu-id="712a6-161">no</span></span>        |
| [<span data-ttu-id="712a6-162">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712a6-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="712a6-163">no</span><span class="sxs-lookup"><span data-stu-id="712a6-163">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="712a6-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="712a6-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="712a6-165">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="712a6-165">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





