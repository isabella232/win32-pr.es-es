---
title: f32tof16 (SM5-ASM)
description: Conversión de componentes float16 a float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986706"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="c717c-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c717c-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="c717c-105">Conversión de componentes float16 a float32.</span><span class="sxs-lookup"><span data-stu-id="c717c-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="c717c-106">f32tof16 dest \[ . Mask \] , \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="c717c-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="c717c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c717c-107">Item</span></span>                                                            | <span data-ttu-id="c717c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c717c-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="c717c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c717c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c717c-110">\[en \] la dirección del resultado de float16.</span><span class="sxs-lookup"><span data-stu-id="c717c-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="c717c-111"><span id="src"></span><span id="SRC"></span>*diez*</span><span class="sxs-lookup"><span data-stu-id="c717c-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="c717c-112">\[en \] el valor float32 que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="c717c-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="c717c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c717c-113">Remarks</span></span>

<span data-ttu-id="c717c-114">Esta instrucción realiza una conversión de componentes de un valor float32 en un resultado de valor float16 colocado en LSB 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c717c-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="c717c-115">Esta instrucción sigue las reglas D3D para la conversión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="c717c-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="c717c-116">Use esta instrucción para la compresión de datos controlada por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="c717c-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="c717c-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c717c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c717c-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="c717c-118">Vertex</span></span> | <span data-ttu-id="c717c-119">Casco</span><span class="sxs-lookup"><span data-stu-id="c717c-119">Hull</span></span> | <span data-ttu-id="c717c-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="c717c-120">Domain</span></span> | <span data-ttu-id="c717c-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="c717c-121">Geometry</span></span> | <span data-ttu-id="c717c-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="c717c-122">Pixel</span></span> | <span data-ttu-id="c717c-123">Compute</span><span class="sxs-lookup"><span data-stu-id="c717c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c717c-124">X</span><span class="sxs-lookup"><span data-stu-id="c717c-124">X</span></span>      | <span data-ttu-id="c717c-125">X</span><span class="sxs-lookup"><span data-stu-id="c717c-125">X</span></span>    | <span data-ttu-id="c717c-126">X</span><span class="sxs-lookup"><span data-stu-id="c717c-126">X</span></span>      | <span data-ttu-id="c717c-127">X</span><span class="sxs-lookup"><span data-stu-id="c717c-127">X</span></span>        | <span data-ttu-id="c717c-128">X</span><span class="sxs-lookup"><span data-stu-id="c717c-128">X</span></span>     | <span data-ttu-id="c717c-129">X</span><span class="sxs-lookup"><span data-stu-id="c717c-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c717c-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c717c-130">Minimum Shader Model</span></span>

<span data-ttu-id="c717c-131">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c717c-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c717c-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c717c-132">Shader Model</span></span>                                              | <span data-ttu-id="c717c-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="c717c-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c717c-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c717c-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c717c-135">sí</span><span class="sxs-lookup"><span data-stu-id="c717c-135">yes</span></span>       |
| [<span data-ttu-id="c717c-136">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c717c-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c717c-137">no</span><span class="sxs-lookup"><span data-stu-id="c717c-137">no</span></span>        |
| [<span data-ttu-id="c717c-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c717c-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c717c-139">no</span><span class="sxs-lookup"><span data-stu-id="c717c-139">no</span></span>        |
| [<span data-ttu-id="c717c-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c717c-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c717c-141">no</span><span class="sxs-lookup"><span data-stu-id="c717c-141">no</span></span>        |
| [<span data-ttu-id="c717c-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c717c-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c717c-143">no</span><span class="sxs-lookup"><span data-stu-id="c717c-143">no</span></span>        |
| [<span data-ttu-id="c717c-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c717c-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c717c-145">no</span><span class="sxs-lookup"><span data-stu-id="c717c-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c717c-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c717c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c717c-147">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c717c-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





