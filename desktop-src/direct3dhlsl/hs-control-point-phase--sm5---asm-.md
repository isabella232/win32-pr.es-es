---
title: hs_control_point_phase (SM5-ASM)
description: Inicie la fase de punto de control en un sombreador de casco.
ms.assetid: 9CF26691-C04F-4728-8418-40F313ABBE4A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba3f591fcd656e64609513dca7b9126496a86d6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077116"
---
# <a name="hs_control_point_phase-sm5---asm"></a><span data-ttu-id="8c7e6-103">\_ \_ \_ fase de punto de control HS (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8c7e6-103">hs\_control\_point\_phase (sm5 - asm)</span></span>

<span data-ttu-id="8c7e6-104">Inicie la fase de punto de control en un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="8c7e6-104">Start the control point phase in a hull shader.</span></span>



| <span data-ttu-id="8c7e6-105">\_fase de \_ punto de control HS \_</span><span class="sxs-lookup"><span data-stu-id="8c7e6-105">hs\_control\_point\_phase</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="8c7e6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c7e6-106">Remarks</span></span>

<span data-ttu-id="8c7e6-107">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="8c7e6-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8c7e6-108">Vértice</span><span class="sxs-lookup"><span data-stu-id="8c7e6-108">Vertex</span></span> | <span data-ttu-id="8c7e6-109">Casco</span><span class="sxs-lookup"><span data-stu-id="8c7e6-109">Hull</span></span> | <span data-ttu-id="8c7e6-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="8c7e6-110">Domain</span></span> | <span data-ttu-id="8c7e6-111">Geometría</span><span class="sxs-lookup"><span data-stu-id="8c7e6-111">Geometry</span></span> | <span data-ttu-id="8c7e6-112">Píxel</span><span class="sxs-lookup"><span data-stu-id="8c7e6-112">Pixel</span></span> | <span data-ttu-id="8c7e6-113">Compute</span><span class="sxs-lookup"><span data-stu-id="8c7e6-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="8c7e6-114">X</span><span class="sxs-lookup"><span data-stu-id="8c7e6-114">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8c7e6-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8c7e6-115">Minimum Shader Model</span></span>

<span data-ttu-id="8c7e6-116">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8c7e6-116">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8c7e6-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8c7e6-117">Shader Model</span></span>                                              | <span data-ttu-id="8c7e6-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="8c7e6-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8c7e6-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8c7e6-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8c7e6-120">sí</span><span class="sxs-lookup"><span data-stu-id="8c7e6-120">yes</span></span>       |
| [<span data-ttu-id="8c7e6-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8c7e6-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8c7e6-122">no</span><span class="sxs-lookup"><span data-stu-id="8c7e6-122">no</span></span>        |
| [<span data-ttu-id="8c7e6-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8c7e6-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8c7e6-124">no</span><span class="sxs-lookup"><span data-stu-id="8c7e6-124">no</span></span>        |
| [<span data-ttu-id="8c7e6-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c7e6-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8c7e6-126">no</span><span class="sxs-lookup"><span data-stu-id="8c7e6-126">no</span></span>        |
| [<span data-ttu-id="8c7e6-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c7e6-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8c7e6-128">no</span><span class="sxs-lookup"><span data-stu-id="8c7e6-128">no</span></span>        |
| [<span data-ttu-id="8c7e6-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c7e6-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8c7e6-130">no</span><span class="sxs-lookup"><span data-stu-id="8c7e6-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8c7e6-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c7e6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c7e6-132">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c7e6-132">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 




