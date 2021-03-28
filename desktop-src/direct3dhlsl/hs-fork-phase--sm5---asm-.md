---
title: hs_fork_phase (SM5-ASM)
description: Inicie la fase de bifurcación en un sombreador de casco.
ms.assetid: 13D6A06C-F001-45BE-8AB4-D7ACA73BF535
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9316cc92c1bf5683afa620927b3c6f38432c3c4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419969"
---
# <a name="hs_fork_phase-sm5---asm"></a><span data-ttu-id="12341-103">\_fase HS \_ de la bifurcación (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="12341-103">hs\_fork\_phase (sm5 - asm)</span></span>

<span data-ttu-id="12341-104">Inicie la fase de bifurcación en un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="12341-104">Start the fork phase in a hull shader.</span></span>



| <span data-ttu-id="12341-105">\_fase de bifurcación HS \_</span><span class="sxs-lookup"><span data-stu-id="12341-105">hs\_fork\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="12341-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12341-106">Remarks</span></span>

<span data-ttu-id="12341-107">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="12341-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="12341-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="12341-108">Vertex</span></span> | <span data-ttu-id="12341-109">Casco</span><span class="sxs-lookup"><span data-stu-id="12341-109">Hull</span></span> | <span data-ttu-id="12341-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="12341-110">Domain</span></span> | <span data-ttu-id="12341-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="12341-111">Geometry</span></span> | <span data-ttu-id="12341-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="12341-112">Pixel</span></span> | <span data-ttu-id="12341-113">Compute</span><span class="sxs-lookup"><span data-stu-id="12341-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="12341-114">X</span><span class="sxs-lookup"><span data-stu-id="12341-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12341-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="12341-115">Minimum Shader Model</span></span>

<span data-ttu-id="12341-116">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="12341-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="12341-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="12341-117">Shader Model</span></span>                                              | <span data-ttu-id="12341-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="12341-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="12341-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="12341-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="12341-120">sí</span><span class="sxs-lookup"><span data-stu-id="12341-120">yes</span></span>       |
| [<span data-ttu-id="12341-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="12341-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="12341-122">no</span><span class="sxs-lookup"><span data-stu-id="12341-122">no</span></span>        |
| [<span data-ttu-id="12341-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="12341-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="12341-124">no</span><span class="sxs-lookup"><span data-stu-id="12341-124">no</span></span>        |
| [<span data-ttu-id="12341-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12341-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="12341-126">no</span><span class="sxs-lookup"><span data-stu-id="12341-126">no</span></span>        |
| [<span data-ttu-id="12341-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12341-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="12341-128">no</span><span class="sxs-lookup"><span data-stu-id="12341-128">no</span></span>        |
| [<span data-ttu-id="12341-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12341-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="12341-130">no</span><span class="sxs-lookup"><span data-stu-id="12341-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="12341-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12341-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12341-132">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12341-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




