---
title: dcl_immediateConstantBuffer (SM4-ASM)
description: DCL \_ immediateConstantBuffer (SM4-ASM)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f4b4868f3b07285465abb9080688adf6129e1bf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358516"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a><span data-ttu-id="fd389-103">DCL \_ immediateConstantBuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fd389-103">dcl\_immediateConstantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="fd389-104">Declara un búfer de constantes de sombreador inmediato.</span><span class="sxs-lookup"><span data-stu-id="fd389-104">Declares a shader immediate-constant buffer.</span></span>



| <span data-ttu-id="fd389-105">\_ *valores* de immediateConstantBuffer de DCL</span><span class="sxs-lookup"><span data-stu-id="fd389-105">dcl\_immediateConstantBuffer *value(s)*</span></span> |
|-----------------------------------------|



 

<dl> <dt>

<span data-ttu-id="fd389-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*valores*</span><span class="sxs-lookup"><span data-stu-id="fd389-106"><span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*</span></span>
</dt> <dd>

<span data-ttu-id="fd389-107">\[en \] el búfer debe contener al menos un valor, pero no más de 4096 valores.</span><span class="sxs-lookup"><span data-stu-id="fd389-107">\[in\] The buffer must contain at least one value, but not more than 4096 values.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="fd389-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd389-108">Remarks</span></span>

<span data-ttu-id="fd389-109">Se permite un sombreador en un búfer de constante inmediata.</span><span class="sxs-lookup"><span data-stu-id="fd389-109">A shader is allowed one immediate-constant buffer.</span></span> <span data-ttu-id="fd389-110">Se tiene acceso a un búfer de constantes inmediatas, al igual que un búfer de constantes con indexación dinámica.</span><span class="sxs-lookup"><span data-stu-id="fd389-110">An immediate-constant buffer is accessed just like a constant buffer with dynamic indexing.</span></span>

<span data-ttu-id="fd389-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fd389-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fd389-112">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fd389-112">Vertex Shader</span></span> | <span data-ttu-id="fd389-113">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fd389-113">Geometry Shader</span></span> | <span data-ttu-id="fd389-114">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fd389-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fd389-115">x</span><span class="sxs-lookup"><span data-stu-id="fd389-115">x</span></span>             | <span data-ttu-id="fd389-116">x</span><span class="sxs-lookup"><span data-stu-id="fd389-116">x</span></span>               | <span data-ttu-id="fd389-117">x</span><span class="sxs-lookup"><span data-stu-id="fd389-117">x</span></span>            |



 

<span data-ttu-id="fd389-118">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="fd389-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fd389-119">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fd389-119">Minimum Shader Model</span></span>

<span data-ttu-id="fd389-120">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fd389-120">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fd389-121">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fd389-121">Shader Model</span></span>                                              | <span data-ttu-id="fd389-122">Compatible</span><span class="sxs-lookup"><span data-stu-id="fd389-122">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fd389-123">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fd389-123">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fd389-124">sí</span><span class="sxs-lookup"><span data-stu-id="fd389-124">yes</span></span>       |
| [<span data-ttu-id="fd389-125">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fd389-125">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fd389-126">sí</span><span class="sxs-lookup"><span data-stu-id="fd389-126">yes</span></span>       |
| [<span data-ttu-id="fd389-127">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fd389-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fd389-128">sí</span><span class="sxs-lookup"><span data-stu-id="fd389-128">yes</span></span>       |
| [<span data-ttu-id="fd389-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd389-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fd389-130">no</span><span class="sxs-lookup"><span data-stu-id="fd389-130">no</span></span>        |
| [<span data-ttu-id="fd389-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd389-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fd389-132">no</span><span class="sxs-lookup"><span data-stu-id="fd389-132">no</span></span>        |
| [<span data-ttu-id="fd389-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd389-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fd389-134">no</span><span class="sxs-lookup"><span data-stu-id="fd389-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fd389-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd389-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd389-136">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fd389-136">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




