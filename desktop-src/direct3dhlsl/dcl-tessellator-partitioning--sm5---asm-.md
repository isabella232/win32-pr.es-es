---
title: dcl_tessellator_partitioning (SM5-ASM)
description: Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.
ms.assetid: 6EA00C6B-A0DE-4CE4-8B52-1337CA92CA5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6f6091301f95dd2364debec2bf54c0966c0e64
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419983"
---
# <a name="dcl_tessellator_partitioning-sm5---asm"></a><span data-ttu-id="57e56-103">creación \_ \_ de particiones de DCL del teselador (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="57e56-103">dcl\_tessellator\_partitioning (sm5 - asm)</span></span>

<span data-ttu-id="57e56-104">Declare la creación de particiones del teselador en una sección de declaración del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="57e56-104">Declare the tessellator partitioning in a hull shader declaration section.</span></span>



| <span data-ttu-id="57e56-105">DCL \_ del teselador creación de \_ particiones {entero de particionamiento \_ </span><span class="sxs-lookup"><span data-stu-id="57e56-105">dcl\_tessellator\_partitioning {partitioning\_integer</span></span>\| <span data-ttu-id="57e56-106">creación de particiones \_ pow2 </span><span class="sxs-lookup"><span data-stu-id="57e56-106">partitioning\_pow2</span></span>\|<span data-ttu-id="57e56-107">crear particiones de las \_ fracciones \_ impares</span><span class="sxs-lookup"><span data-stu-id="57e56-107">partitioning\_fractional\_odd\</span></span>| <span data-ttu-id="57e56-108">dividir las particiones \_ \_ pares}</span><span class="sxs-lookup"><span data-stu-id="57e56-108">partitioning\_fractional\_even}</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="57e56-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="57e56-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="57e56-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="57e56-110">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="57e56-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*creación de particiones de entero de particionamiento \_ \| \_ pow2 \| particionamiento \_ fraccionario \_ \| \_ \_*</span><span class="sxs-lookup"><span data-stu-id="57e56-111"><span id="partitioning_integer__________________________________partitioning_pow2_partitioning_fractional_odd__________________________________partitioning_fractional_even"></span><span id="PARTITIONING_INTEGER__________________________________PARTITIONING_POW2_PARTITIONING_FRACTIONAL_ODD__________________________________PARTITIONING_FRACTIONAL_EVEN"></span>*partitioning\_integer\| partitioning\_pow2\|partitioning\_fractional\_odd\| partitioning\_fractional\_even*</span></span><br/> | <span data-ttu-id="57e56-112">\[en \] la partición del teselador.</span><span class="sxs-lookup"><span data-stu-id="57e56-112">\[in\] The tessellator partitioning.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57e56-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57e56-113">Remarks</span></span>

<span data-ttu-id="57e56-114">Desde el punto de vista del hardware, \_ pow2 se comporta como un \_ entero.</span><span class="sxs-lookup"><span data-stu-id="57e56-114">From the hardware point of view, \_pow2 behaves just like \_integer.</span></span> <span data-ttu-id="57e56-115">Es el autor del sombreador de HLSL y/o compilercode para redondear TessFactors a potencias de 2.</span><span class="sxs-lookup"><span data-stu-id="57e56-115">It is up to the HLSL shader author and/or compilercode to round TessFactors to powers of 2.</span></span>

<span data-ttu-id="57e56-116">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="57e56-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="57e56-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="57e56-117">Vertex</span></span> | <span data-ttu-id="57e56-118">Casco</span><span class="sxs-lookup"><span data-stu-id="57e56-118">Hull</span></span>                 | <span data-ttu-id="57e56-119">Dominio</span><span class="sxs-lookup"><span data-stu-id="57e56-119">Domain</span></span> | <span data-ttu-id="57e56-120">Geometría</span><span class="sxs-lookup"><span data-stu-id="57e56-120">Geometry</span></span> | <span data-ttu-id="57e56-121">Píxel</span><span class="sxs-lookup"><span data-stu-id="57e56-121">Pixel</span></span> | <span data-ttu-id="57e56-122">Compute</span><span class="sxs-lookup"><span data-stu-id="57e56-122">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="57e56-123">Sección declaraciones</span><span class="sxs-lookup"><span data-stu-id="57e56-123">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="57e56-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="57e56-124">Minimum Shader Model</span></span>

<span data-ttu-id="57e56-125">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="57e56-125">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="57e56-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="57e56-126">Shader Model</span></span>                                              | <span data-ttu-id="57e56-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="57e56-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="57e56-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="57e56-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="57e56-129">sí</span><span class="sxs-lookup"><span data-stu-id="57e56-129">yes</span></span>       |
| [<span data-ttu-id="57e56-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="57e56-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="57e56-131">no</span><span class="sxs-lookup"><span data-stu-id="57e56-131">no</span></span>        |
| [<span data-ttu-id="57e56-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="57e56-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="57e56-133">no</span><span class="sxs-lookup"><span data-stu-id="57e56-133">no</span></span>        |
| [<span data-ttu-id="57e56-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e56-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="57e56-135">no</span><span class="sxs-lookup"><span data-stu-id="57e56-135">no</span></span>        |
| [<span data-ttu-id="57e56-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e56-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="57e56-137">no</span><span class="sxs-lookup"><span data-stu-id="57e56-137">no</span></span>        |
| [<span data-ttu-id="57e56-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e56-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="57e56-139">no</span><span class="sxs-lookup"><span data-stu-id="57e56-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="57e56-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57e56-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e56-141">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57e56-141">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





