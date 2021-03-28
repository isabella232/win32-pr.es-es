---
title: dcl_hs_fork_phase_instance_count (SM5-ASM)
description: Declare el recuento de instancias de fase de bifurcación en una fase de bifurcación de sombreador de casco.
ms.assetid: E38C48BB-3439-4F63-8DF8-21CF562CF5E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3459b43c22f60699445f3ef05e5323e268eeb71
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419998"
---
# <a name="dcl_hs_fork_phase_instance_count-sm5---asm"></a><span data-ttu-id="ca300-103">\_recuento \_ \_ \_ de instancias de fase de la bifurcación de DCL HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ca300-103">dcl\_hs\_fork\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="ca300-104">Declare el recuento de instancias de fase de bifurcación en una fase de bifurcación de sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="ca300-104">Declare the fork phase instance count in a hull shader fork phase.</span></span>



| <span data-ttu-id="ca300-105">\_número de \_ instancias de fase de bifurcación de DCL% \_ \_ \_ 1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="ca300-105">dcl\_hs\_fork\_phase\_instance\_count {1...max 32-bit UINT}</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="ca300-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ca300-106">Item</span></span>                                                   | <span data-ttu-id="ca300-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca300-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="ca300-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="ca300-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="ca300-109">\[en \] el recuento de instancias.</span><span class="sxs-lookup"><span data-stu-id="ca300-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca300-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca300-110">Remarks</span></span>

<span data-ttu-id="ca300-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ca300-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ca300-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="ca300-112">Vertex</span></span> | <span data-ttu-id="ca300-113">Casco</span><span class="sxs-lookup"><span data-stu-id="ca300-113">Hull</span></span> | <span data-ttu-id="ca300-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="ca300-114">Domain</span></span> | <span data-ttu-id="ca300-115">Geometría</span><span class="sxs-lookup"><span data-stu-id="ca300-115">Geometry</span></span> | <span data-ttu-id="ca300-116">Píxel</span><span class="sxs-lookup"><span data-stu-id="ca300-116">Pixel</span></span> | <span data-ttu-id="ca300-117">Compute</span><span class="sxs-lookup"><span data-stu-id="ca300-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="ca300-118">X</span><span class="sxs-lookup"><span data-stu-id="ca300-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ca300-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ca300-119">Minimum Shader Model</span></span>

<span data-ttu-id="ca300-120">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ca300-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ca300-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ca300-121">Shader Model</span></span>                                              | <span data-ttu-id="ca300-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="ca300-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ca300-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ca300-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ca300-124">sí</span><span class="sxs-lookup"><span data-stu-id="ca300-124">yes</span></span>       |
| [<span data-ttu-id="ca300-125">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ca300-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ca300-126">no</span><span class="sxs-lookup"><span data-stu-id="ca300-126">no</span></span>        |
| [<span data-ttu-id="ca300-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ca300-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ca300-128">no</span><span class="sxs-lookup"><span data-stu-id="ca300-128">no</span></span>        |
| [<span data-ttu-id="ca300-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca300-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ca300-130">no</span><span class="sxs-lookup"><span data-stu-id="ca300-130">no</span></span>        |
| [<span data-ttu-id="ca300-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca300-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ca300-132">no</span><span class="sxs-lookup"><span data-stu-id="ca300-132">no</span></span>        |
| [<span data-ttu-id="ca300-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca300-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ca300-134">no</span><span class="sxs-lookup"><span data-stu-id="ca300-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ca300-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca300-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca300-136">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ca300-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





