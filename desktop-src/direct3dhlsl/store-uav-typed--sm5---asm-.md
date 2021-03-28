---
title: store_uav_typed (SM5-ASM)
description: Escritura de acceso aleatorio de un elemento en una vista de acceso desordenado con tipo (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077082"
---
# <a name="store_uav_typed-sm5---asm"></a><span data-ttu-id="39431-103">almacenar \_ UAV \_ con tipo (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="39431-103">store\_uav\_typed (sm5 - asm)</span></span>

<span data-ttu-id="39431-104">Escritura de acceso aleatorio de un elemento en una vista de acceso desordenado con tipo (UAV).</span><span class="sxs-lookup"><span data-stu-id="39431-104">Random-access write of an element into a typed unordered access view (UAV).</span></span>



| <span data-ttu-id="39431-105">almacenar \_ UAV \_ con tipo dstUAV. Xyzw, dstAddress \[ . swizzle \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="39431-105">store\_uav\_typed dstUAV.xyzw, dstAddress\[.swizzle\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="39431-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="39431-106">Item</span></span>                                                                                                           | <span data-ttu-id="39431-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="39431-107">Description</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="39431-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span><span class="sxs-lookup"><span data-stu-id="39431-108"><span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*</span></span><br/>                 | <span data-ttu-id="39431-109">\[en \] contiene el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="39431-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="39431-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span><span class="sxs-lookup"><span data-stu-id="39431-110"><span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*</span></span><br/> | <span data-ttu-id="39431-111">\[en \] la dirección en la que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="39431-111">\[in\] The address at which to write.</span></span><br/>        |
| <span data-ttu-id="39431-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="39431-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                                | <span data-ttu-id="39431-113">\[en \] los componentes que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="39431-113">\[in\] The components to write.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="39431-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39431-114">Remarks</span></span>

<span data-ttu-id="39431-115">Esta instrucción realiza un \* elemento de 32 bits de 4 componentes escrito de *Src0* en *dstUAV* en la dirección de *dstAddress*.</span><span class="sxs-lookup"><span data-stu-id="39431-115">This instruction performs a 4 component \*32-bit element written from *src0* to *dstUAV* at the address in *dstAddress*.</span></span> <span data-ttu-id="39431-116">*dstUAV* es un UAV (u) con tipo \# .</span><span class="sxs-lookup"><span data-stu-id="39431-116">*dstUAV* is a typed UAV (u\#).</span></span>

<span data-ttu-id="39431-117">El formato de UAV determina la conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="39431-117">The format of the UAV determines format conversion.</span></span>

<span data-ttu-id="39431-118">El número de componentes enteros sin signo de 32 bits tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *dstUAV*.</span><span class="sxs-lookup"><span data-stu-id="39431-118">The number of 32-bit unsigned integer components taken from the address are determined by the dimensionality of the resource declared at *dstUAV*.</span></span> <span data-ttu-id="39431-119">Esta dirección está en elementos.</span><span class="sxs-lookup"><span data-stu-id="39431-119">This address is in elements.</span></span>

<span data-ttu-id="39431-120">El direccionamiento fuera del límite significa que no se escribe nada en la memoria.</span><span class="sxs-lookup"><span data-stu-id="39431-120">Out of bounds addressing means nothing gets written to memory.</span></span>

<span data-ttu-id="39431-121">*dstUAV* siempre tiene una máscara de escritura. xyzw.</span><span class="sxs-lookup"><span data-stu-id="39431-121">*dstUAV* always has a .xyzw write mask.</span></span> <span data-ttu-id="39431-122">Se deben escribir todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="39431-122">All components must be written.</span></span>

<span data-ttu-id="39431-123">No es válido y no está definido para usar esta instrucción en un UAV que no se declara como con tipo.</span><span class="sxs-lookup"><span data-stu-id="39431-123">It is invalid and undefined to use this instruction on a UAV that is not declared as typed.</span></span> <span data-ttu-id="39431-124">Es decir, hacer esto en un UAV estructurado o sin tipo no es válido.</span><span class="sxs-lookup"><span data-stu-id="39431-124">That is, doing this on a structured or typeless UAV is invalid.</span></span>

<span data-ttu-id="39431-125">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="39431-125">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="39431-126">Vértice</span><span class="sxs-lookup"><span data-stu-id="39431-126">Vertex</span></span> | <span data-ttu-id="39431-127">Casco</span><span class="sxs-lookup"><span data-stu-id="39431-127">Hull</span></span> | <span data-ttu-id="39431-128">Dominio</span><span class="sxs-lookup"><span data-stu-id="39431-128">Domain</span></span> | <span data-ttu-id="39431-129">Geometría</span><span class="sxs-lookup"><span data-stu-id="39431-129">Geometry</span></span> | <span data-ttu-id="39431-130">Píxel</span><span class="sxs-lookup"><span data-stu-id="39431-130">Pixel</span></span> | <span data-ttu-id="39431-131">Compute</span><span class="sxs-lookup"><span data-stu-id="39431-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="39431-132">X</span><span class="sxs-lookup"><span data-stu-id="39431-132">X</span></span>     | <span data-ttu-id="39431-133">X</span><span class="sxs-lookup"><span data-stu-id="39431-133">X</span></span>       |



 

<span data-ttu-id="39431-134">Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39431-134">Because UAVs are available at all shader stages for Direct3D 11.1, this instruction applies to all shader stages for the Direct3D 11.1 runtime, which is available starting with Windows 8.</span></span>



| <span data-ttu-id="39431-135">Vértice</span><span class="sxs-lookup"><span data-stu-id="39431-135">Vertex</span></span> | <span data-ttu-id="39431-136">Casco</span><span class="sxs-lookup"><span data-stu-id="39431-136">Hull</span></span> | <span data-ttu-id="39431-137">Dominio</span><span class="sxs-lookup"><span data-stu-id="39431-137">Domain</span></span> | <span data-ttu-id="39431-138">Geometría</span><span class="sxs-lookup"><span data-stu-id="39431-138">Geometry</span></span> | <span data-ttu-id="39431-139">Píxel</span><span class="sxs-lookup"><span data-stu-id="39431-139">Pixel</span></span> | <span data-ttu-id="39431-140">Compute</span><span class="sxs-lookup"><span data-stu-id="39431-140">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="39431-141">X</span><span class="sxs-lookup"><span data-stu-id="39431-141">X</span></span>      | <span data-ttu-id="39431-142">X</span><span class="sxs-lookup"><span data-stu-id="39431-142">X</span></span>    | <span data-ttu-id="39431-143">X</span><span class="sxs-lookup"><span data-stu-id="39431-143">X</span></span>      | <span data-ttu-id="39431-144">X</span><span class="sxs-lookup"><span data-stu-id="39431-144">X</span></span>        | <span data-ttu-id="39431-145">X</span><span class="sxs-lookup"><span data-stu-id="39431-145">X</span></span>     | <span data-ttu-id="39431-146">X</span><span class="sxs-lookup"><span data-stu-id="39431-146">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="39431-147">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="39431-147">Minimum Shader Model</span></span>

<span data-ttu-id="39431-148">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="39431-148">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="39431-149">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="39431-149">Shader Model</span></span>                                              | <span data-ttu-id="39431-150">Compatible</span><span class="sxs-lookup"><span data-stu-id="39431-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="39431-151">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="39431-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="39431-152">sí</span><span class="sxs-lookup"><span data-stu-id="39431-152">yes</span></span>       |
| [<span data-ttu-id="39431-153">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="39431-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="39431-154">no</span><span class="sxs-lookup"><span data-stu-id="39431-154">no</span></span>        |
| [<span data-ttu-id="39431-155">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="39431-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="39431-156">no</span><span class="sxs-lookup"><span data-stu-id="39431-156">no</span></span>        |
| [<span data-ttu-id="39431-157">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39431-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="39431-158">no</span><span class="sxs-lookup"><span data-stu-id="39431-158">no</span></span>        |
| [<span data-ttu-id="39431-159">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39431-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="39431-160">no</span><span class="sxs-lookup"><span data-stu-id="39431-160">no</span></span>        |
| [<span data-ttu-id="39431-161">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39431-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="39431-162">no</span><span class="sxs-lookup"><span data-stu-id="39431-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="39431-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39431-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39431-164">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39431-164">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





