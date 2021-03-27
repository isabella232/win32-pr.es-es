---
title: firstbit (SM5-ASM)
description: Busca el primer bit establecido en un número, ya sea de LSB o MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358509"
---
# <a name="firstbit-sm5---asm"></a><span data-ttu-id="2488c-103">firstbit (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2488c-103">firstbit (sm5 - asm)</span></span>

<span data-ttu-id="2488c-104">Busca el primer bit establecido en un número, ya sea de LSB o MSB.</span><span class="sxs-lookup"><span data-stu-id="2488c-104">Finds the first bit set in a number, either from LSB or MSB.</span></span>



| <span data-ttu-id="2488c-105">firstbit { \_ HI </span><span class="sxs-lookup"><span data-stu-id="2488c-105">firstbit{\_hi</span></span>\|<span data-ttu-id="2488c-106">\_lo</span><span class="sxs-lookup"><span data-stu-id="2488c-106">\_lo\</span></span>|<span data-ttu-id="2488c-107">\_Shi} dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2488c-107">\_shi} dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="2488c-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="2488c-108">Item</span></span>                                                            | <span data-ttu-id="2488c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2488c-109">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2488c-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2488c-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2488c-111">\[en \] la posición entera del primer bit establecido en *src0* a partir de LSB para FIRSTBIT lo \_ o MSB para firstbit \_ HI.</span><span class="sxs-lookup"><span data-stu-id="2488c-111">\[in\] The integer position of the first bit set in *src0* starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span><br/> |
| <span data-ttu-id="2488c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2488c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2488c-113">\[en \] el entero de entrada.</span><span class="sxs-lookup"><span data-stu-id="2488c-113">\[in\] The input integer.</span></span><br/>                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="2488c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2488c-114">Remarks</span></span>

<span data-ttu-id="2488c-115">Esta operación devuelve la posición entera del primer bit establecido en la entrada de 32 bits a partir de LSB para firstbit lo \_ o MSB para firstbit \_ HI.</span><span class="sxs-lookup"><span data-stu-id="2488c-115">This operation returns the integer position of the first bit set in the 32-bit input starting from the LSB for firstbit\_lo or MSB for firstbit\_hi.</span></span> <span data-ttu-id="2488c-116">Por ejemplo, firstbit \_ en 0x00000001 devuelve 0.</span><span class="sxs-lookup"><span data-stu-id="2488c-116">For example firstbit\_lo on 0x00000001 returns 0.</span></span> <span data-ttu-id="2488c-117">firstbit \_ HI on 0x10000000 devuelve 3.</span><span class="sxs-lookup"><span data-stu-id="2488c-117">firstbit\_hi on 0x10000000 returns 3.</span></span>

<span data-ttu-id="2488c-118">firstbit \_ Shi (s para signed) devuelve el primer 0 del MSB si el número es negativo; de lo contrario, devuelve el primer 1 del MSB.</span><span class="sxs-lookup"><span data-stu-id="2488c-118">firstbit\_shi (s for signed) returns the first 0 from the MSB if the number is negative; otherwise it returns the first 1 from the MSB.</span></span>

<span data-ttu-id="2488c-119">Todas las variantes de la instrucción devuelven ~ 0 (0xFFFFFFFF en el registro de 32 bits) si no se encuentra ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="2488c-119">All variants of the instruction return ~0 (0xffffffff in 32-bit register) if no match is found.</span></span>

<span data-ttu-id="2488c-120">Use esta instrucción para enumerar rápidamente los bits establecidos en un campo de bits o buscar la potencia más grande de 2 en un número.</span><span class="sxs-lookup"><span data-stu-id="2488c-120">Use this instruction to quickly enumerate set bits in a bitfield, or find the largest power of 2 in a number.</span></span>

<span data-ttu-id="2488c-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2488c-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2488c-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="2488c-122">Vertex</span></span> | <span data-ttu-id="2488c-123">Casco</span><span class="sxs-lookup"><span data-stu-id="2488c-123">Hull</span></span> | <span data-ttu-id="2488c-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="2488c-124">Domain</span></span> | <span data-ttu-id="2488c-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="2488c-125">Geometry</span></span> | <span data-ttu-id="2488c-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="2488c-126">Pixel</span></span> | <span data-ttu-id="2488c-127">Compute</span><span class="sxs-lookup"><span data-stu-id="2488c-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2488c-128">X</span><span class="sxs-lookup"><span data-stu-id="2488c-128">X</span></span>      | <span data-ttu-id="2488c-129">X</span><span class="sxs-lookup"><span data-stu-id="2488c-129">X</span></span>    | <span data-ttu-id="2488c-130">X</span><span class="sxs-lookup"><span data-stu-id="2488c-130">X</span></span>      | <span data-ttu-id="2488c-131">X</span><span class="sxs-lookup"><span data-stu-id="2488c-131">X</span></span>        | <span data-ttu-id="2488c-132">X</span><span class="sxs-lookup"><span data-stu-id="2488c-132">X</span></span>     | <span data-ttu-id="2488c-133">X</span><span class="sxs-lookup"><span data-stu-id="2488c-133">X</span></span>       |



 

## <a name="mimimum-shader-model"></a><span data-ttu-id="2488c-134">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2488c-134">Mimimum Shader Model</span></span>

<span data-ttu-id="2488c-135">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="2488c-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2488c-136">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2488c-136">Shader Model</span></span>                                              | <span data-ttu-id="2488c-137">Compatible</span><span class="sxs-lookup"><span data-stu-id="2488c-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2488c-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2488c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2488c-139">sí</span><span class="sxs-lookup"><span data-stu-id="2488c-139">yes</span></span>       |
| [<span data-ttu-id="2488c-140">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2488c-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2488c-141">no</span><span class="sxs-lookup"><span data-stu-id="2488c-141">no</span></span>        |
| [<span data-ttu-id="2488c-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2488c-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2488c-143">no</span><span class="sxs-lookup"><span data-stu-id="2488c-143">no</span></span>        |
| [<span data-ttu-id="2488c-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2488c-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2488c-145">no</span><span class="sxs-lookup"><span data-stu-id="2488c-145">no</span></span>        |
| [<span data-ttu-id="2488c-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2488c-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2488c-147">no</span><span class="sxs-lookup"><span data-stu-id="2488c-147">no</span></span>        |
| [<span data-ttu-id="2488c-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2488c-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2488c-149">no</span><span class="sxs-lookup"><span data-stu-id="2488c-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2488c-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2488c-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2488c-151">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2488c-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





