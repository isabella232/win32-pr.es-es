---
title: dcl_input_control_point_count (SM5-ASM)
description: Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419995"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="9dcfd-103">\_recuento \_ \_ de puntos \_ de control de entrada de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9dcfd-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="9dcfd-104">Declare el recuento de puntos de control de entrada del sombreador de casco en la sección declaración del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="9dcfd-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="9dcfd-105">recuento de puntos de control de entrada de DCL \_ \_ \_ \_ {1.. 32}</span><span class="sxs-lookup"><span data-stu-id="9dcfd-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="9dcfd-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="9dcfd-106">Item</span></span>                                                   | <span data-ttu-id="9dcfd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dcfd-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="9dcfd-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="9dcfd-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="9dcfd-109">\[en \] el recuento de puntos de control de entrada.</span><span class="sxs-lookup"><span data-stu-id="9dcfd-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9dcfd-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dcfd-110">Remarks</span></span>

<span data-ttu-id="9dcfd-111">Se requiere al menos un punto de control de entrada; puede estar vacío si no es necesario.</span><span class="sxs-lookup"><span data-stu-id="9dcfd-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="9dcfd-112">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9dcfd-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9dcfd-113">Vértice</span><span class="sxs-lookup"><span data-stu-id="9dcfd-113">Vertex</span></span> | <span data-ttu-id="9dcfd-114">Casco</span><span class="sxs-lookup"><span data-stu-id="9dcfd-114">Hull</span></span> | <span data-ttu-id="9dcfd-115">Dominio</span><span class="sxs-lookup"><span data-stu-id="9dcfd-115">Domain</span></span> | <span data-ttu-id="9dcfd-116">Geometría</span><span class="sxs-lookup"><span data-stu-id="9dcfd-116">Geometry</span></span> | <span data-ttu-id="9dcfd-117">Píxel</span><span class="sxs-lookup"><span data-stu-id="9dcfd-117">Pixel</span></span> | <span data-ttu-id="9dcfd-118">Compute</span><span class="sxs-lookup"><span data-stu-id="9dcfd-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9dcfd-119">X</span><span class="sxs-lookup"><span data-stu-id="9dcfd-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9dcfd-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9dcfd-120">Minimum Shader Model</span></span>

<span data-ttu-id="9dcfd-121">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9dcfd-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9dcfd-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9dcfd-122">Shader Model</span></span>                                              | <span data-ttu-id="9dcfd-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="9dcfd-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9dcfd-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9dcfd-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9dcfd-125">sí</span><span class="sxs-lookup"><span data-stu-id="9dcfd-125">yes</span></span>       |
| [<span data-ttu-id="9dcfd-126">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9dcfd-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9dcfd-127">no</span><span class="sxs-lookup"><span data-stu-id="9dcfd-127">no</span></span>        |
| [<span data-ttu-id="9dcfd-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9dcfd-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9dcfd-129">no</span><span class="sxs-lookup"><span data-stu-id="9dcfd-129">no</span></span>        |
| [<span data-ttu-id="9dcfd-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dcfd-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9dcfd-131">no</span><span class="sxs-lookup"><span data-stu-id="9dcfd-131">no</span></span>        |
| [<span data-ttu-id="9dcfd-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dcfd-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9dcfd-133">no</span><span class="sxs-lookup"><span data-stu-id="9dcfd-133">no</span></span>        |
| [<span data-ttu-id="9dcfd-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dcfd-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9dcfd-135">no</span><span class="sxs-lookup"><span data-stu-id="9dcfd-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9dcfd-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9dcfd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcfd-137">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dcfd-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





