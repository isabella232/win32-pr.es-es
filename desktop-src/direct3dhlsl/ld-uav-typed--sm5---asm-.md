---
title: ld_uav_typed (SM5-ASM)
description: Lectura de acceso aleatorio de un elemento a partir de una vista de acceso desordenado con tipo (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358487"
---
# <a name="ld_uav_typed-sm5---asm"></a><span data-ttu-id="e56f7-103">LD \_ UAV \_ con tipo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e56f7-103">ld\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="e56f7-104">Lectura de acceso aleatorio de un elemento a partir de una vista de acceso desordenado con tipo (UAV).</span><span class="sxs-lookup"><span data-stu-id="e56f7-104">Random-access read of an element from a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="e56f7-105">LD \_ UAV \_ con tipo dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e56f7-105">ld\_uav\_typed dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="e56f7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e56f7-106">Item</span></span>                                                                                                           | <span data-ttu-id="e56f7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e56f7-107">Description</span></span>                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="e56f7-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span><span class="sxs-lookup"><span data-stu-id="e56f7-108"><span id="dst0"></span><span id="DST0"></span>*dst0*</span></span><br/>                                                | <span data-ttu-id="e56f7-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="e56f7-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="e56f7-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span><span class="sxs-lookup"><span data-stu-id="e56f7-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/> | <span data-ttu-id="e56f7-111">\[en \] especifica la dirección de la que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="e56f7-111">\[in\] Specifies the address to read from.</span></span><br/>          |
| <span data-ttu-id="e56f7-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span><span class="sxs-lookup"><span data-stu-id="e56f7-112"><span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*</span></span><br/>                 | <span data-ttu-id="e56f7-113">\[en \] el origen del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="e56f7-113">\[in\] The source to read from.</span></span> <br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e56f7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e56f7-114">Remarks</span></span>

<span data-ttu-id="e56f7-115">Esta instrucción realiza una lectura de un elemento de 4 componentes de *srcUAV* en la dirección de entero sin signo de *srcAddress*, convertido a 32 bits por componente basado en el formato y, a continuación, se escribe en *dst0* en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="e56f7-115">This instruction performs a 4-component element read from *srcUAV* at the unsigned integer address in *srcAddress*, converted to 32bit per component based on the format, then written to *dst0* in the shader.</span></span>

<span data-ttu-id="e56f7-116">*srcUAV* es un UAV (u \# ) declarado como con tipo.</span><span class="sxs-lookup"><span data-stu-id="e56f7-116">*srcUAV* is a UAV (u\#) declared as typed.</span></span> <span data-ttu-id="e56f7-117">Sin embargo, el tipo de recurso enlazado debe ser R32 \_ uint/Sint/float.</span><span class="sxs-lookup"><span data-stu-id="e56f7-117">However, the type of the bound resource must be R32\_UINT/SINT/FLOAT.</span></span>

<span data-ttu-id="e56f7-118">El número de componentes enteros sin signo de 32 bits tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *srcUAV*.</span><span class="sxs-lookup"><span data-stu-id="e56f7-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *srcUAV*.</span></span> <span data-ttu-id="e56f7-119">El direccionamiento es el mismo que el de la instrucción [LD](ld--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="e56f7-119">Addressing is the same as the [ld](ld--sm4---asm-.md) instruction.</span></span>

<span data-ttu-id="e56f7-120">El direccionamiento fuera de los límites es igual que la instrucción **LD** .</span><span class="sxs-lookup"><span data-stu-id="e56f7-120">Out of bounds addressing is the same as the **ld** instruction.</span></span>

<span data-ttu-id="e56f7-121">El comportamiento de esta instrucción es idéntico a la instrucción **LD** si se llama como **LD dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . \] swizzle**</span><span class="sxs-lookup"><span data-stu-id="e56f7-121">The behavior of this instruction is identical to the **ld** instruction if called as **ld dst0\[.mask\], srcAddress\[.swizzle\], srcUAV\[.swizzle\]**</span></span>

<span data-ttu-id="e56f7-122">No es válido y no está definido para usar esta instrucción en un UAV que no se declara como con tipo.</span><span class="sxs-lookup"><span data-stu-id="e56f7-122">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="e56f7-123">Hacer esto en un UAV estructurado o sin tipo no es válido.</span><span class="sxs-lookup"><span data-stu-id="e56f7-123">Doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="e56f7-124">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e56f7-124">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e56f7-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="e56f7-125">Vertex</span></span> | <span data-ttu-id="e56f7-126">Casco</span><span class="sxs-lookup"><span data-stu-id="e56f7-126">Hull</span></span> | <span data-ttu-id="e56f7-127">Dominio</span><span class="sxs-lookup"><span data-stu-id="e56f7-127">Domain</span></span> | <span data-ttu-id="e56f7-128">Geometría</span><span class="sxs-lookup"><span data-stu-id="e56f7-128">Geometry</span></span> | <span data-ttu-id="e56f7-129">Píxel</span><span class="sxs-lookup"><span data-stu-id="e56f7-129">Pixel</span></span> | <span data-ttu-id="e56f7-130">Compute</span><span class="sxs-lookup"><span data-stu-id="e56f7-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e56f7-131">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-131">X</span></span>     | <span data-ttu-id="e56f7-132">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-132">X</span></span>       |



 

<span data-ttu-id="e56f7-133">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e56f7-133">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="e56f7-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="e56f7-134">Vertex</span></span> | <span data-ttu-id="e56f7-135">Casco</span><span class="sxs-lookup"><span data-stu-id="e56f7-135">Hull</span></span> | <span data-ttu-id="e56f7-136">Dominio</span><span class="sxs-lookup"><span data-stu-id="e56f7-136">Domain</span></span> | <span data-ttu-id="e56f7-137">Geometría</span><span class="sxs-lookup"><span data-stu-id="e56f7-137">Geometry</span></span> | <span data-ttu-id="e56f7-138">Píxel</span><span class="sxs-lookup"><span data-stu-id="e56f7-138">Pixel</span></span> | <span data-ttu-id="e56f7-139">Compute</span><span class="sxs-lookup"><span data-stu-id="e56f7-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e56f7-140">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-140">X</span></span>      | <span data-ttu-id="e56f7-141">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-141">X</span></span>    | <span data-ttu-id="e56f7-142">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-142">X</span></span>      | <span data-ttu-id="e56f7-143">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-143">X</span></span>        | <span data-ttu-id="e56f7-144">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-144">X</span></span>     | <span data-ttu-id="e56f7-145">X</span><span class="sxs-lookup"><span data-stu-id="e56f7-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e56f7-146">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e56f7-146">Minimum Shader Model</span></span>

<span data-ttu-id="e56f7-147">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e56f7-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e56f7-148">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e56f7-148">Shader Model</span></span>                                              | <span data-ttu-id="e56f7-149">Compatible</span><span class="sxs-lookup"><span data-stu-id="e56f7-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e56f7-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e56f7-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e56f7-151">sí</span><span class="sxs-lookup"><span data-stu-id="e56f7-151">yes</span></span>       |
| [<span data-ttu-id="e56f7-152">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e56f7-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e56f7-153">no</span><span class="sxs-lookup"><span data-stu-id="e56f7-153">no</span></span>        |
| [<span data-ttu-id="e56f7-154">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e56f7-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e56f7-155">no</span><span class="sxs-lookup"><span data-stu-id="e56f7-155">no</span></span>        |
| [<span data-ttu-id="e56f7-156">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e56f7-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e56f7-157">no</span><span class="sxs-lookup"><span data-stu-id="e56f7-157">no</span></span>        |
| [<span data-ttu-id="e56f7-158">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e56f7-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e56f7-159">no</span><span class="sxs-lookup"><span data-stu-id="e56f7-159">no</span></span>        |
| [<span data-ttu-id="e56f7-160">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e56f7-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e56f7-161">no</span><span class="sxs-lookup"><span data-stu-id="e56f7-161">no</span></span>        |



 

<span data-ttu-id="e56f7-162">CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.</span><span class="sxs-lookup"><span data-stu-id="e56f7-162">cs\_4\_0 and cs\_4\_1 support this instruction for UAV, SRV and TGSM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e56f7-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e56f7-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e56f7-164">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e56f7-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





