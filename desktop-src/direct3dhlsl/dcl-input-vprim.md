---
title: dcl_input vPrim (SM4-ASM)
description: '\_vPrim de entrada de DCL (SM4-ASM)'
ms.assetid: 75287673-21d6-4eb7-829f-7f2f340aec54
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9742c6066d66d7aa4121c1d1d1df98a37cb0147e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419993"
---
# <a name="dcl_input-vprim-sm4---asm"></a><span data-ttu-id="b6657-103">\_vPrim de entrada de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b6657-103">dcl\_input vPrim (sm4 - asm)</span></span>

<span data-ttu-id="b6657-104">Declara que un sombreador de geometría utiliza su vPrim de registro de entrada escalar.</span><span class="sxs-lookup"><span data-stu-id="b6657-104">Declares that a geometry shader uses its scalar input-register vPrim.</span></span>



| <span data-ttu-id="b6657-105">\_ *vPrim* de entrada de DCL</span><span class="sxs-lookup"><span data-stu-id="b6657-105">dcl\_input *vPrim*</span></span> |
|--------------------|



 



| <span data-ttu-id="b6657-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b6657-106">Item</span></span>                                                                                       | <span data-ttu-id="b6657-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6657-107">Description</span></span>                                                                                              |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6657-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span><span class="sxs-lookup"><span data-stu-id="b6657-108"><span id="vPrim"></span><span id="vprim"></span><span id="VPRIM"></span>*vPrim*</span></span><br/> | <span data-ttu-id="b6657-109">\[en \] un escalar de 32 bits, que se puede aplicar a cada primitiva interior de un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="b6657-109">\[in\] A 32-bit scalar, which can be applied to each interior primitive in a geometry shader.</span></span><br/> |



 

<span data-ttu-id="b6657-110">No se puede aplicar el escalar a ningún primitivo adyacente.</span><span class="sxs-lookup"><span data-stu-id="b6657-110">The scalar cannot be applied to any adjacent primitives.</span></span>

<span data-ttu-id="b6657-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="b6657-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b6657-112">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b6657-112">Vertex Shader</span></span> | <span data-ttu-id="b6657-113">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="b6657-113">Geometry Shader</span></span> | <span data-ttu-id="b6657-114">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b6657-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="b6657-115">x</span><span class="sxs-lookup"><span data-stu-id="b6657-115">x</span></span>               |              |



 

<span data-ttu-id="b6657-116">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="b6657-116">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b6657-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b6657-117">Minimum Shader Model</span></span>

<span data-ttu-id="b6657-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b6657-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b6657-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b6657-119">Shader Model</span></span>                                              | <span data-ttu-id="b6657-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="b6657-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b6657-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b6657-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b6657-122">sí</span><span class="sxs-lookup"><span data-stu-id="b6657-122">yes</span></span>       |
| [<span data-ttu-id="b6657-123">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b6657-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b6657-124">sí</span><span class="sxs-lookup"><span data-stu-id="b6657-124">yes</span></span>       |
| [<span data-ttu-id="b6657-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b6657-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b6657-126">sí</span><span class="sxs-lookup"><span data-stu-id="b6657-126">yes</span></span>       |
| [<span data-ttu-id="b6657-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6657-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b6657-128">no</span><span class="sxs-lookup"><span data-stu-id="b6657-128">no</span></span>        |
| [<span data-ttu-id="b6657-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6657-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b6657-130">no</span><span class="sxs-lookup"><span data-stu-id="b6657-130">no</span></span>        |
| [<span data-ttu-id="b6657-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6657-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b6657-132">no</span><span class="sxs-lookup"><span data-stu-id="b6657-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b6657-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6657-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6657-134">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b6657-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





