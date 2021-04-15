---
title: dcl_output (SM4-ASM)
description: '\_salida de DCL (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983906"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="aa664-103">\_salida de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa664-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="aa664-104">Declara un registro de salida de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aa664-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="aa664-105">salida de DCL \_ o *N \[ . \] Mask*</span><span class="sxs-lookup"><span data-stu-id="aa664-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="aa664-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa664-106">Item</span></span>                                                                           | <span data-ttu-id="aa664-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa664-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa664-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="aa664-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="aa664-109">\[en \] un registro de datos de salida; *N* es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="aa664-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="aa664-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="aa664-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="aa664-111">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="aa664-111">\[in\] Optional.</span></span> <span data-ttu-id="aa664-112">Máscara de componente (. xyzw) que especifica cuál de los componentes de registro se va a usar.</span><span class="sxs-lookup"><span data-stu-id="aa664-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="aa664-113">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="aa664-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa664-114">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="aa664-114">Vertex Shader</span></span> | <span data-ttu-id="aa664-115">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="aa664-115">Geometry Shader</span></span> | <span data-ttu-id="aa664-116">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="aa664-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa664-117">x</span><span class="sxs-lookup"><span data-stu-id="aa664-117">x</span></span>             | <span data-ttu-id="aa664-118">x</span><span class="sxs-lookup"><span data-stu-id="aa664-118">x</span></span>               | <span data-ttu-id="aa664-119">x</span><span class="sxs-lookup"><span data-stu-id="aa664-119">x</span></span>            |



 

<span data-ttu-id="aa664-120">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="aa664-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="aa664-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa664-121">Example</span></span>

<span data-ttu-id="aa664-122">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="aa664-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="aa664-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="aa664-123">Minimum Shader Model</span></span>

<span data-ttu-id="aa664-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aa664-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa664-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="aa664-125">Shader Model</span></span>                                              | <span data-ttu-id="aa664-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="aa664-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa664-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aa664-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa664-128">sí</span><span class="sxs-lookup"><span data-stu-id="aa664-128">yes</span></span>       |
| [<span data-ttu-id="aa664-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="aa664-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa664-130">sí</span><span class="sxs-lookup"><span data-stu-id="aa664-130">yes</span></span>       |
| [<span data-ttu-id="aa664-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="aa664-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa664-132">sí</span><span class="sxs-lookup"><span data-stu-id="aa664-132">yes</span></span>       |
| [<span data-ttu-id="aa664-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa664-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa664-134">no</span><span class="sxs-lookup"><span data-stu-id="aa664-134">no</span></span>        |
| [<span data-ttu-id="aa664-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa664-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa664-136">no</span><span class="sxs-lookup"><span data-stu-id="aa664-136">no</span></span>        |
| [<span data-ttu-id="aa664-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa664-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa664-138">no</span><span class="sxs-lookup"><span data-stu-id="aa664-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa664-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa664-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa664-140">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa664-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





