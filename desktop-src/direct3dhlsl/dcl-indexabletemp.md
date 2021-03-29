---
title: dcl_indexableTemp (SM4-ASM)
description: DCL \_ indexableTemp (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996988"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="62d7b-103">DCL \_ indexableTemp (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="62d7b-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="62d7b-104">Declara un registro temporal indexable.</span><span class="sxs-lookup"><span data-stu-id="62d7b-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="62d7b-105">DCL \_ indexableTemp x *N \[ tamaño \] , ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="62d7b-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="62d7b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="62d7b-106">Item</span></span>                                                                                                                           | <span data-ttu-id="62d7b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="62d7b-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="62d7b-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="62d7b-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="62d7b-109">\[en \] un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="62d7b-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="62d7b-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[ajusta\]*</span><span class="sxs-lookup"><span data-stu-id="62d7b-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="62d7b-111">\[en \] un valor entero opcional.</span><span class="sxs-lookup"><span data-stu-id="62d7b-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="62d7b-112">El número de elementos de la matriz de registro.</span><span class="sxs-lookup"><span data-stu-id="62d7b-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="62d7b-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span><span class="sxs-lookup"><span data-stu-id="62d7b-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="62d7b-114">\[en \] un valor entero opcional. El número de componentes de la matriz de registro.</span><span class="sxs-lookup"><span data-stu-id="62d7b-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="62d7b-115">Un registro contiene suficiente espacio para un valor de cuatro componentes de 32 bits; el número de elementos de la matriz de registros temporales (indexables y [no indexables](dcl-temps.md)) no puede superar 4096.</span><span class="sxs-lookup"><span data-stu-id="62d7b-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="62d7b-116">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="62d7b-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="62d7b-117">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="62d7b-117">Vertex Shader</span></span> | <span data-ttu-id="62d7b-118">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="62d7b-118">Geometry Shader</span></span> | <span data-ttu-id="62d7b-119">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="62d7b-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="62d7b-120">x</span><span class="sxs-lookup"><span data-stu-id="62d7b-120">x</span></span>             | <span data-ttu-id="62d7b-121">x</span><span class="sxs-lookup"><span data-stu-id="62d7b-121">x</span></span>               | <span data-ttu-id="62d7b-122">x</span><span class="sxs-lookup"><span data-stu-id="62d7b-122">x</span></span>            |



 

<span data-ttu-id="62d7b-123">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="62d7b-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="62d7b-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62d7b-124">Example</span></span>

<span data-ttu-id="62d7b-125">Estos son algunos ejemplos del código generado para los registros indexables.</span><span class="sxs-lookup"><span data-stu-id="62d7b-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="62d7b-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="62d7b-126">Minimum Shader Model</span></span>

<span data-ttu-id="62d7b-127">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="62d7b-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="62d7b-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="62d7b-128">Shader Model</span></span>                                              | <span data-ttu-id="62d7b-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="62d7b-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="62d7b-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="62d7b-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="62d7b-131">sí</span><span class="sxs-lookup"><span data-stu-id="62d7b-131">yes</span></span>       |
| [<span data-ttu-id="62d7b-132">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="62d7b-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="62d7b-133">sí</span><span class="sxs-lookup"><span data-stu-id="62d7b-133">yes</span></span>       |
| [<span data-ttu-id="62d7b-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="62d7b-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="62d7b-135">sí</span><span class="sxs-lookup"><span data-stu-id="62d7b-135">yes</span></span>       |
| [<span data-ttu-id="62d7b-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62d7b-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="62d7b-137">no</span><span class="sxs-lookup"><span data-stu-id="62d7b-137">no</span></span>        |
| [<span data-ttu-id="62d7b-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62d7b-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="62d7b-139">no</span><span class="sxs-lookup"><span data-stu-id="62d7b-139">no</span></span>        |
| [<span data-ttu-id="62d7b-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62d7b-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="62d7b-141">no</span><span class="sxs-lookup"><span data-stu-id="62d7b-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="62d7b-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62d7b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62d7b-143">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="62d7b-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





