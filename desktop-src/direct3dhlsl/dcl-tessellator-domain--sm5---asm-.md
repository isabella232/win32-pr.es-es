---
title: dcl_tessellator_domain (SM5-ASM)
description: Declare el dominio del teselador en una sección de declaración del sombreador de casco y en el sombreador de dominios.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419984"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="cef30-103">\_ \_ dominio de del teselador de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="cef30-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="cef30-104">Declare el dominio del teselador en una sección de declaración del sombreador de casco y en el sombreador de dominios.</span><span class="sxs-lookup"><span data-stu-id="cef30-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="cef30-105">\_dominio del teselador de DCL \_ {dominio \_ Isoline </span><span class="sxs-lookup"><span data-stu-id="cef30-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="cef30-106">dominio \_ Tri </span><span class="sxs-lookup"><span data-stu-id="cef30-106">domain\_tri </span></span>\| <span data-ttu-id="cef30-107">dominio \_ cuádruple}</span><span class="sxs-lookup"><span data-stu-id="cef30-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="cef30-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cef30-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="cef30-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cef30-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="cef30-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*dominio \_ Isoline \| dominio \_ Tri \| dominio \_ cuádruple*</span><span class="sxs-lookup"><span data-stu-id="cef30-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="cef30-111">\[en \] el dominio.</span><span class="sxs-lookup"><span data-stu-id="cef30-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cef30-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cef30-112">Remarks</span></span>

<span data-ttu-id="cef30-113">El comportamiento es indefinido si el sombreador de casco y el sombreador de dominios proporcionan dominios que no coinciden o cualquier otro decalarations en conflicto.</span><span class="sxs-lookup"><span data-stu-id="cef30-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="cef30-114">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="cef30-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cef30-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="cef30-115">Vertex</span></span> | <span data-ttu-id="cef30-116">Casco</span><span class="sxs-lookup"><span data-stu-id="cef30-116">Hull</span></span>                 | <span data-ttu-id="cef30-117">Dominio</span><span class="sxs-lookup"><span data-stu-id="cef30-117">Domain</span></span> | <span data-ttu-id="cef30-118">Geometría</span><span class="sxs-lookup"><span data-stu-id="cef30-118">Geometry</span></span> | <span data-ttu-id="cef30-119">Píxel</span><span class="sxs-lookup"><span data-stu-id="cef30-119">Pixel</span></span> | <span data-ttu-id="cef30-120">Compute</span><span class="sxs-lookup"><span data-stu-id="cef30-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="cef30-121">Sección declaraciones</span><span class="sxs-lookup"><span data-stu-id="cef30-121">Declarations Section</span></span> | <span data-ttu-id="cef30-122">X</span><span class="sxs-lookup"><span data-stu-id="cef30-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cef30-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="cef30-123">Minimum Shader Model</span></span>

<span data-ttu-id="cef30-124">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cef30-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cef30-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="cef30-125">Shader Model</span></span>                                              | <span data-ttu-id="cef30-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="cef30-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cef30-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cef30-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cef30-128">sí</span><span class="sxs-lookup"><span data-stu-id="cef30-128">yes</span></span>       |
| [<span data-ttu-id="cef30-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cef30-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cef30-130">no</span><span class="sxs-lookup"><span data-stu-id="cef30-130">no</span></span>        |
| [<span data-ttu-id="cef30-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cef30-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cef30-132">no</span><span class="sxs-lookup"><span data-stu-id="cef30-132">no</span></span>        |
| [<span data-ttu-id="cef30-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cef30-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cef30-134">no</span><span class="sxs-lookup"><span data-stu-id="cef30-134">no</span></span>        |
| [<span data-ttu-id="cef30-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cef30-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cef30-136">no</span><span class="sxs-lookup"><span data-stu-id="cef30-136">no</span></span>        |
| [<span data-ttu-id="cef30-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cef30-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cef30-138">no</span><span class="sxs-lookup"><span data-stu-id="cef30-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cef30-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cef30-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef30-140">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cef30-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





