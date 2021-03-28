---
title: dcl_output_control_point_count (SM5-ASM)
description: Declara el recuento de puntos de control de salida del sombreador de casco.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077132"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="c8a8d-103">\_recuento \_ \_ de puntos \_ de control de salida de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c8a8d-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="c8a8d-104">Declara el recuento de puntos de control de salida del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="c8a8d-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="c8a8d-105">número de puntos de control de salida de DCL \_ \_ \_ \_ N</span><span class="sxs-lookup"><span data-stu-id="c8a8d-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="c8a8d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c8a8d-106">Item</span></span>                                                   | <span data-ttu-id="c8a8d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8a8d-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a8d-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="c8a8d-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="c8a8d-109">\[en \] un valor entero comprendido entre 0 y 32 que especifica el recuento de puntos de control de salida.</span><span class="sxs-lookup"><span data-stu-id="c8a8d-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8a8d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8a8d-110">Remarks</span></span>

<span data-ttu-id="c8a8d-111">El sombreador de casco puede producir 0 puntos de control si no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="c8a8d-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="c8a8d-112">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c8a8d-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c8a8d-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="c8a8d-113">Vertex</span></span> | <span data-ttu-id="c8a8d-114">Casco</span><span class="sxs-lookup"><span data-stu-id="c8a8d-114">Hull</span></span>                 | <span data-ttu-id="c8a8d-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="c8a8d-115">Domain</span></span> | <span data-ttu-id="c8a8d-116">Geometría</span><span class="sxs-lookup"><span data-stu-id="c8a8d-116">Geometry</span></span> | <span data-ttu-id="c8a8d-117">Píxel</span><span class="sxs-lookup"><span data-stu-id="c8a8d-117">Pixel</span></span> | <span data-ttu-id="c8a8d-118">Compute</span><span class="sxs-lookup"><span data-stu-id="c8a8d-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="c8a8d-119">Sección declaraciones</span><span class="sxs-lookup"><span data-stu-id="c8a8d-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c8a8d-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c8a8d-120">Minimum Shader Model</span></span>

<span data-ttu-id="c8a8d-121">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c8a8d-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c8a8d-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c8a8d-122">Shader Model</span></span>                                              | <span data-ttu-id="c8a8d-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="c8a8d-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c8a8d-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c8a8d-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c8a8d-125">sí</span><span class="sxs-lookup"><span data-stu-id="c8a8d-125">yes</span></span>       |
| [<span data-ttu-id="c8a8d-126">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c8a8d-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c8a8d-127">no</span><span class="sxs-lookup"><span data-stu-id="c8a8d-127">no</span></span>        |
| [<span data-ttu-id="c8a8d-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c8a8d-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c8a8d-129">no</span><span class="sxs-lookup"><span data-stu-id="c8a8d-129">no</span></span>        |
| [<span data-ttu-id="c8a8d-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c8a8d-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c8a8d-131">no</span><span class="sxs-lookup"><span data-stu-id="c8a8d-131">no</span></span>        |
| [<span data-ttu-id="c8a8d-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c8a8d-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c8a8d-133">no</span><span class="sxs-lookup"><span data-stu-id="c8a8d-133">no</span></span>        |
| [<span data-ttu-id="c8a8d-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c8a8d-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c8a8d-135">no</span><span class="sxs-lookup"><span data-stu-id="c8a8d-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c8a8d-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8a8d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a8d-137">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c8a8d-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





