---
title: dcl_tessellator_output_primitive (SM5-ASM)
description: Declare el tipo primitivo de salida del teselador en una sección de declaración del sombreador de casco.
ms.assetid: 95F074C5-6012-4160-B78E-440C33C1ECC3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 390f22cdafe3b0d078bf8a502623a1c741e34e34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077128"
---
# <a name="dcl_tessellator_output_primitive-sm5---asm"></a><span data-ttu-id="1b22a-103">\_del teselador \_ de salida \_ de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b22a-103">dcl\_tessellator\_output\_primitive (sm5 - asm)</span></span>

<span data-ttu-id="1b22a-104">Declare el tipo primitivo de salida del teselador en una sección de declaración del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="1b22a-104">Declare the tessellator output primitive type in a hull shader declaration section.</span></span>



| <span data-ttu-id="1b22a-105">del teselador de salida de DCL de DCL \_ \_ \_ {punto de salida \_ </span><span class="sxs-lookup"><span data-stu-id="1b22a-105">dcl\_tessellator\_output\_primitive {output\_point </span></span>\| <span data-ttu-id="1b22a-106">línea de salida \_ </span><span class="sxs-lookup"><span data-stu-id="1b22a-106">output\_line </span></span>\| <span data-ttu-id="1b22a-107">triangloutput \_ e \_ CW </span><span class="sxs-lookup"><span data-stu-id="1b22a-107">triangloutput\_e\_cw </span></span>\| <span data-ttu-id="1b22a-108">triángulo de salida \_ \_ CCW}</span><span class="sxs-lookup"><span data-stu-id="1b22a-108">output\_triangle\_ccw}</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1b22a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b22a-109">Item</span></span>                                                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="1b22a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b22a-110">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="1b22a-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*línea de salida de punto de salida \_ \| \_ \| triangloutput \_ e \_ CW \| triángulo de salida \_ \_ CCW*</span><span class="sxs-lookup"><span data-stu-id="1b22a-111"><span id="output_point___output_line_____________________________________triangloutput_e_cw___output_triangle_ccw"></span><span id="OUTPUT_POINT___OUTPUT_LINE_____________________________________TRIANGLOUTPUT_E_CW___OUTPUT_TRIANGLE_CCW"></span>*output\_point \| output\_line \| triangloutput\_e\_cw \| output\_triangle\_ccw*</span></span><br/> | <span data-ttu-id="1b22a-112">\[en \] el tipo primitivo de salida.</span><span class="sxs-lookup"><span data-stu-id="1b22a-112">\[in\] The output primitive type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b22a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b22a-113">Remarks</span></span>

<span data-ttu-id="1b22a-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="1b22a-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b22a-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="1b22a-115">Vertex</span></span> | <span data-ttu-id="1b22a-116">Casco</span><span class="sxs-lookup"><span data-stu-id="1b22a-116">Hull</span></span>                 | <span data-ttu-id="1b22a-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="1b22a-117">Domain</span></span> | <span data-ttu-id="1b22a-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="1b22a-118">Geometry</span></span> | <span data-ttu-id="1b22a-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="1b22a-119">Pixel</span></span> | <span data-ttu-id="1b22a-120">Compute</span><span class="sxs-lookup"><span data-stu-id="1b22a-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="1b22a-121">Sección declaraciones</span><span class="sxs-lookup"><span data-stu-id="1b22a-121">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b22a-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="1b22a-122">Minimum Shader Model</span></span>

<span data-ttu-id="1b22a-123">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1b22a-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1b22a-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="1b22a-124">Shader Model</span></span>                                              | <span data-ttu-id="1b22a-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="1b22a-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b22a-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1b22a-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b22a-127">sí</span><span class="sxs-lookup"><span data-stu-id="1b22a-127">yes</span></span>       |
| [<span data-ttu-id="1b22a-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1b22a-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b22a-129">no</span><span class="sxs-lookup"><span data-stu-id="1b22a-129">no</span></span>        |
| [<span data-ttu-id="1b22a-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1b22a-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b22a-131">no</span><span class="sxs-lookup"><span data-stu-id="1b22a-131">no</span></span>        |
| [<span data-ttu-id="1b22a-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b22a-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b22a-133">no</span><span class="sxs-lookup"><span data-stu-id="1b22a-133">no</span></span>        |
| [<span data-ttu-id="1b22a-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b22a-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b22a-135">no</span><span class="sxs-lookup"><span data-stu-id="1b22a-135">no</span></span>        |
| [<span data-ttu-id="1b22a-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b22a-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b22a-137">no</span><span class="sxs-lookup"><span data-stu-id="1b22a-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b22a-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b22a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b22a-139">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b22a-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





