---
title: hs_join_phase (SM5-ASM)
description: Iniciar la fase de combinación en un sombreador de casco.
ms.assetid: C53889BE-B65F-4F5F-8B87-7C5263FAC800
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c45011209124d73fe866872772a3a787c538d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358497"
---
# <a name="hs_join_phase-sm5---asm"></a><span data-ttu-id="992c5-103">\_ \_ fase de combinación HS (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="992c5-103">hs\_join\_phase (sm5 - asm)</span></span>

<span data-ttu-id="992c5-104">Iniciar la fase de combinación en un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="992c5-104">Start the join phase in a hull shader.</span></span>



| <span data-ttu-id="992c5-105">\_fase de combinación HS \_</span><span class="sxs-lookup"><span data-stu-id="992c5-105">hs\_join\_phase</span></span> |
|-----------------|



 

## <a name="remarks"></a><span data-ttu-id="992c5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="992c5-106">Remarks</span></span>

<span data-ttu-id="992c5-107">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="992c5-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="992c5-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="992c5-108">Vertex</span></span> | <span data-ttu-id="992c5-109">Casco</span><span class="sxs-lookup"><span data-stu-id="992c5-109">Hull</span></span> | <span data-ttu-id="992c5-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="992c5-110">Domain</span></span> | <span data-ttu-id="992c5-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="992c5-111">Geometry</span></span> | <span data-ttu-id="992c5-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="992c5-112">Pixel</span></span> | <span data-ttu-id="992c5-113">Compute</span><span class="sxs-lookup"><span data-stu-id="992c5-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="992c5-114">X</span><span class="sxs-lookup"><span data-stu-id="992c5-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="992c5-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="992c5-115">Minimum Shader Model</span></span>

<span data-ttu-id="992c5-116">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="992c5-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="992c5-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="992c5-117">Shader Model</span></span>                                              | <span data-ttu-id="992c5-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="992c5-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="992c5-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="992c5-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="992c5-120">sí</span><span class="sxs-lookup"><span data-stu-id="992c5-120">yes</span></span>       |
| [<span data-ttu-id="992c5-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="992c5-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="992c5-122">no</span><span class="sxs-lookup"><span data-stu-id="992c5-122">no</span></span>        |
| [<span data-ttu-id="992c5-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="992c5-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="992c5-124">no</span><span class="sxs-lookup"><span data-stu-id="992c5-124">no</span></span>        |
| [<span data-ttu-id="992c5-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="992c5-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="992c5-126">no</span><span class="sxs-lookup"><span data-stu-id="992c5-126">no</span></span>        |
| [<span data-ttu-id="992c5-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="992c5-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="992c5-128">no</span><span class="sxs-lookup"><span data-stu-id="992c5-128">no</span></span>        |
| [<span data-ttu-id="992c5-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="992c5-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="992c5-130">no</span><span class="sxs-lookup"><span data-stu-id="992c5-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="992c5-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="992c5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="992c5-132">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="992c5-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




