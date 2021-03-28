---
title: dcl_hs_max_tessfactor (SM5-ASM)
description: Declare maxTessFactor para la revisión.
ms.assetid: 7EF0FD81-69FE-49F6-95DF-0C452A90A713
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69bd20fc8f4a3687988e8b100975f74016a45ae6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996989"
---
# <a name="dcl_hs_max_tessfactor-sm5---asm"></a><span data-ttu-id="0bb20-103">DCL \_ HS \_ Max \_ tessfactor (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0bb20-103">dcl\_hs\_max\_tessfactor (sm5 - asm)</span></span>

<span data-ttu-id="0bb20-104">Declare maxTessFactor para la revisión.</span><span class="sxs-lookup"><span data-stu-id="0bb20-104">Declare the maxTessFactor for the patch.</span></span>



| <span data-ttu-id="0bb20-105">DCL \_ HS \_ Max \_ tessfactor n</span><span class="sxs-lookup"><span data-stu-id="0bb20-105">dcl\_hs\_max\_tessfactor n</span></span> |
|----------------------------|



 



| <span data-ttu-id="0bb20-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="0bb20-106">Item</span></span>                                                   | <span data-ttu-id="0bb20-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bb20-107">Description</span></span>                          |
|--------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="0bb20-108"><span id="n"></span><span id="N"></span>*n*</span><span class="sxs-lookup"><span data-stu-id="0bb20-108"><span id="n"></span><span id="N"></span>*n*</span></span><br/> | <span data-ttu-id="0bb20-109">\[en \] maxTessFactor.</span><span class="sxs-lookup"><span data-stu-id="0bb20-109">\[in\] The maxTessFactor.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0bb20-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bb20-110">Remarks</span></span>

<span data-ttu-id="0bb20-111">MaxTessFactor es un valor float32 en el intervalo {1,0... 64,0}.</span><span class="sxs-lookup"><span data-stu-id="0bb20-111">The maxTessFactor is a float32 value in the range {1.0 ... 64.0}.</span></span>

<span data-ttu-id="0bb20-112">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0bb20-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0bb20-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="0bb20-113">Vertex</span></span> | <span data-ttu-id="0bb20-114">Casco</span><span class="sxs-lookup"><span data-stu-id="0bb20-114">Hull</span></span> | <span data-ttu-id="0bb20-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="0bb20-115">Domain</span></span> | <span data-ttu-id="0bb20-116">Geometría</span><span class="sxs-lookup"><span data-stu-id="0bb20-116">Geometry</span></span> | <span data-ttu-id="0bb20-117">Píxel</span><span class="sxs-lookup"><span data-stu-id="0bb20-117">Pixel</span></span> | <span data-ttu-id="0bb20-118">Compute</span><span class="sxs-lookup"><span data-stu-id="0bb20-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="0bb20-119">X</span><span class="sxs-lookup"><span data-stu-id="0bb20-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0bb20-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0bb20-120">Minimum Shader Model</span></span>

<span data-ttu-id="0bb20-121">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0bb20-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0bb20-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0bb20-122">Shader Model</span></span>                                              | <span data-ttu-id="0bb20-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="0bb20-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0bb20-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0bb20-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0bb20-125">sí</span><span class="sxs-lookup"><span data-stu-id="0bb20-125">yes</span></span>       |
| [<span data-ttu-id="0bb20-126">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0bb20-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0bb20-127">no</span><span class="sxs-lookup"><span data-stu-id="0bb20-127">no</span></span>        |
| [<span data-ttu-id="0bb20-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0bb20-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0bb20-129">no</span><span class="sxs-lookup"><span data-stu-id="0bb20-129">no</span></span>        |
| [<span data-ttu-id="0bb20-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bb20-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0bb20-131">no</span><span class="sxs-lookup"><span data-stu-id="0bb20-131">no</span></span>        |
| [<span data-ttu-id="0bb20-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bb20-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0bb20-133">no</span><span class="sxs-lookup"><span data-stu-id="0bb20-133">no</span></span>        |
| [<span data-ttu-id="0bb20-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bb20-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0bb20-135">no</span><span class="sxs-lookup"><span data-stu-id="0bb20-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0bb20-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bb20-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bb20-137">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bb20-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





