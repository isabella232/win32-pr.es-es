---
title: dcl_stream (SM5-ASM)
description: Declare un flujo de salida del sombreador de geometría.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419986"
---
# <a name="dcl_stream-sm5---asm"></a><span data-ttu-id="7e6c7-103">\_secuencia de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-103">dcl\_stream (sm5 - asm)</span></span>

<span data-ttu-id="7e6c7-104">Declare un flujo de salida del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-104">Declare a geometry shader output stream.</span></span>



| <span data-ttu-id="7e6c7-105">secuencia de DCL \_ m\#</span><span class="sxs-lookup"><span data-stu-id="7e6c7-105">dcl\_stream m\#</span></span> |
|-----------------|



 



| <span data-ttu-id="7e6c7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7e6c7-106">Item</span></span>                                                       | <span data-ttu-id="7e6c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e6c7-107">Description</span></span>                             |
|------------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="7e6c7-108"><span id="m_"></span><span id="M_"></span>*f\#*</span><span class="sxs-lookup"><span data-stu-id="7e6c7-108"><span id="m_"></span><span id="M_"></span>*m\#*</span></span><br/> | <span data-ttu-id="7e6c7-109">\[en el \] flujo 0.. 3 (M0.. m3).</span><span class="sxs-lookup"><span data-stu-id="7e6c7-109">\[in\] Stream 0..3 (m0..m3).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e6c7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e6c7-110">Remarks</span></span>

<span data-ttu-id="7e6c7-111">Un flujo determinado solo puede declararse una vez.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-111">A given stream can only be declared once.</span></span>

<span data-ttu-id="7e6c7-112">Si no se declara ningún flujo, se supone que las declaraciones de topología de salida y salida son para el flujo 0.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-112">If no streams are declared, output and output topology declarations are assumed to be for stream 0.</span></span>

<span data-ttu-id="7e6c7-113">La primera **\_ secuencia DCL** no puede aparecer después de las instrucciones **\_ Output** o **DCL \_ outputTopology** de DCL.</span><span class="sxs-lookup"><span data-stu-id="7e6c7-113">The first **dcl\_stream** cannot appear after any **dcl\_output** or **dcl\_outputTopology** statements.</span></span>

<span data-ttu-id="7e6c7-114">Las **instrucciones \_ Output** o **DCL \_ outputToplogy** de DCL después de cualquier instrucción **DCL \_ Stream** m \# definen las salidas de Stream m \# .</span><span class="sxs-lookup"><span data-stu-id="7e6c7-114">Any **dcl\_output** or **dcl\_outputToplogy** statements after any **dcl\_stream** m\# statement define the outputs for stream m\#.</span></span>

<span data-ttu-id="7e6c7-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="7e6c7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7e6c7-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="7e6c7-116">Vertex</span></span> | <span data-ttu-id="7e6c7-117">Casco</span><span class="sxs-lookup"><span data-stu-id="7e6c7-117">Hull</span></span> | <span data-ttu-id="7e6c7-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="7e6c7-118">Domain</span></span> | <span data-ttu-id="7e6c7-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="7e6c7-119">Geometry</span></span> | <span data-ttu-id="7e6c7-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="7e6c7-120">Pixel</span></span> | <span data-ttu-id="7e6c7-121">Compute</span><span class="sxs-lookup"><span data-stu-id="7e6c7-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="7e6c7-122">X</span><span class="sxs-lookup"><span data-stu-id="7e6c7-122">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7e6c7-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="7e6c7-123">Minimum Shader Model</span></span>

<span data-ttu-id="7e6c7-124">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="7e6c7-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7e6c7-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="7e6c7-125">Shader Model</span></span>                                              | <span data-ttu-id="7e6c7-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="7e6c7-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7e6c7-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="7e6c7-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7e6c7-128">sí</span><span class="sxs-lookup"><span data-stu-id="7e6c7-128">yes</span></span>       |
| [<span data-ttu-id="7e6c7-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="7e6c7-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7e6c7-130">no</span><span class="sxs-lookup"><span data-stu-id="7e6c7-130">no</span></span>        |
| [<span data-ttu-id="7e6c7-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="7e6c7-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7e6c7-132">no</span><span class="sxs-lookup"><span data-stu-id="7e6c7-132">no</span></span>        |
| [<span data-ttu-id="7e6c7-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7e6c7-134">no</span><span class="sxs-lookup"><span data-stu-id="7e6c7-134">no</span></span>        |
| [<span data-ttu-id="7e6c7-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7e6c7-136">no</span><span class="sxs-lookup"><span data-stu-id="7e6c7-136">no</span></span>        |
| [<span data-ttu-id="7e6c7-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7e6c7-138">no</span><span class="sxs-lookup"><span data-stu-id="7e6c7-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7e6c7-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e6c7-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e6c7-140">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7e6c7-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





