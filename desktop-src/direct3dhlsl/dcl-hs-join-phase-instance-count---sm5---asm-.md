---
title: dcl_hs_join_phase_instance_count (SM5-ASM)
description: Declare el recuento de instancias de fase de combinación en una fase de combinación del sombreador de casco.
ms.assetid: 9951B849-0537-4D08-9ADE-8CF6FF51A193
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c3acc7074170ab4561a54e67668698d58b7ac1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419999"
---
# <a name="dcl_hs_join_phase_instance_count-sm5---asm"></a><span data-ttu-id="13061-103">\_recuento \_ \_ \_ de instancias de fase de unión de DCL HS \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="13061-103">dcl\_hs\_join\_phase\_instance\_count (sm5 - asm)</span></span>

<span data-ttu-id="13061-104">Declare el recuento de instancias de fase de combinación en una fase de combinación del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="13061-104">Declare the join phase instance count in a hull shader join phase.</span></span>



| <span data-ttu-id="13061-105">recuento de \_ \_ instancias de fase de incorporación de DCL del 1% \_ \_ \_ 1... Max 32-bit uint}</span><span class="sxs-lookup"><span data-stu-id="13061-105">dcl\_hs\_join\_phase\_instance\_count {1... max 32-bit UINT}</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="13061-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="13061-106">Item</span></span>                                                   | <span data-ttu-id="13061-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="13061-107">Description</span></span>                           |
|--------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="13061-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="13061-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="13061-109">\[en \] el recuento de instancias.</span><span class="sxs-lookup"><span data-stu-id="13061-109">\[in\] The instance count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13061-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13061-110">Remarks</span></span>

<span data-ttu-id="13061-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="13061-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="13061-112">Vértice</span><span class="sxs-lookup"><span data-stu-id="13061-112">Vertex</span></span> | <span data-ttu-id="13061-113">Casco</span><span class="sxs-lookup"><span data-stu-id="13061-113">Hull</span></span> | <span data-ttu-id="13061-114">Dominio</span><span class="sxs-lookup"><span data-stu-id="13061-114">Domain</span></span> | <span data-ttu-id="13061-115">Geometría</span><span class="sxs-lookup"><span data-stu-id="13061-115">Geometry</span></span> | <span data-ttu-id="13061-116">Píxel</span><span class="sxs-lookup"><span data-stu-id="13061-116">Pixel</span></span> | <span data-ttu-id="13061-117">Compute</span><span class="sxs-lookup"><span data-stu-id="13061-117">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="13061-118">X</span><span class="sxs-lookup"><span data-stu-id="13061-118">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="13061-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="13061-119">Minimum Shader Model</span></span>

<span data-ttu-id="13061-120">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="13061-120">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="13061-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="13061-121">Shader Model</span></span>                                              | <span data-ttu-id="13061-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="13061-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="13061-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="13061-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="13061-124">sí</span><span class="sxs-lookup"><span data-stu-id="13061-124">yes</span></span>       |
| [<span data-ttu-id="13061-125">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="13061-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="13061-126">no</span><span class="sxs-lookup"><span data-stu-id="13061-126">no</span></span>        |
| [<span data-ttu-id="13061-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="13061-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="13061-128">no</span><span class="sxs-lookup"><span data-stu-id="13061-128">no</span></span>        |
| [<span data-ttu-id="13061-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13061-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="13061-130">no</span><span class="sxs-lookup"><span data-stu-id="13061-130">no</span></span>        |
| [<span data-ttu-id="13061-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13061-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="13061-132">no</span><span class="sxs-lookup"><span data-stu-id="13061-132">no</span></span>        |
| [<span data-ttu-id="13061-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13061-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="13061-134">no</span><span class="sxs-lookup"><span data-stu-id="13061-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="13061-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13061-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13061-136">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13061-136">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





