---
title: f16tof32 (SM5-ASM)
description: Conversión de componentes float16 a float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986427"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="bce50-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bce50-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="bce50-105">Conversión de componentes float16 a float32.</span><span class="sxs-lookup"><span data-stu-id="bce50-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="bce50-106">f16tof32 dest \[ . Mask \] , \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="bce50-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="bce50-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bce50-107">Item</span></span>                                                            | <span data-ttu-id="bce50-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bce50-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bce50-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bce50-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bce50-110">\[en \] la dirección del resultado float32.</span><span class="sxs-lookup"><span data-stu-id="bce50-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="bce50-111"><span id="src"></span><span id="SRC"></span>*diez*</span><span class="sxs-lookup"><span data-stu-id="bce50-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="bce50-112">\[en \] el valor de float16 que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="bce50-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="bce50-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce50-113">Remarks</span></span>

<span data-ttu-id="bce50-114">Esta operación realiza una conversión de forma de componente de un valor float16 de LSB bits a un resultado float32.</span><span class="sxs-lookup"><span data-stu-id="bce50-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="bce50-115">Esta operación sigue las reglas D3D para la conversión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="bce50-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="bce50-116">Use esta instrucción para la descompresión de datos controlada por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="bce50-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="bce50-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="bce50-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bce50-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="bce50-118">Vertex</span></span> | <span data-ttu-id="bce50-119">Casco</span><span class="sxs-lookup"><span data-stu-id="bce50-119">Hull</span></span> | <span data-ttu-id="bce50-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="bce50-120">Domain</span></span> | <span data-ttu-id="bce50-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="bce50-121">Geometry</span></span> | <span data-ttu-id="bce50-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="bce50-122">Pixel</span></span> | <span data-ttu-id="bce50-123">Compute</span><span class="sxs-lookup"><span data-stu-id="bce50-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bce50-124">X</span><span class="sxs-lookup"><span data-stu-id="bce50-124">X</span></span>      | <span data-ttu-id="bce50-125">X</span><span class="sxs-lookup"><span data-stu-id="bce50-125">X</span></span>    | <span data-ttu-id="bce50-126">X</span><span class="sxs-lookup"><span data-stu-id="bce50-126">X</span></span>      | <span data-ttu-id="bce50-127">X</span><span class="sxs-lookup"><span data-stu-id="bce50-127">X</span></span>        | <span data-ttu-id="bce50-128">X</span><span class="sxs-lookup"><span data-stu-id="bce50-128">X</span></span>     | <span data-ttu-id="bce50-129">X</span><span class="sxs-lookup"><span data-stu-id="bce50-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bce50-130">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="bce50-130">Minimum Shader Model</span></span>

<span data-ttu-id="bce50-131">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="bce50-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bce50-132">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="bce50-132">Shader Model</span></span>                                              | <span data-ttu-id="bce50-133">Compatible</span><span class="sxs-lookup"><span data-stu-id="bce50-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bce50-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bce50-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bce50-135">sí</span><span class="sxs-lookup"><span data-stu-id="bce50-135">yes</span></span>       |
| [<span data-ttu-id="bce50-136">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bce50-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bce50-137">no</span><span class="sxs-lookup"><span data-stu-id="bce50-137">no</span></span>        |
| [<span data-ttu-id="bce50-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bce50-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bce50-139">no</span><span class="sxs-lookup"><span data-stu-id="bce50-139">no</span></span>        |
| [<span data-ttu-id="bce50-140">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce50-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bce50-141">no</span><span class="sxs-lookup"><span data-stu-id="bce50-141">no</span></span>        |
| [<span data-ttu-id="bce50-142">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce50-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bce50-143">no</span><span class="sxs-lookup"><span data-stu-id="bce50-143">no</span></span>        |
| [<span data-ttu-id="bce50-144">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce50-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bce50-145">no</span><span class="sxs-lookup"><span data-stu-id="bce50-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bce50-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bce50-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce50-147">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce50-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





