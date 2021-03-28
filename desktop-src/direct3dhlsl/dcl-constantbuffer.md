---
title: dcl_constantBuffer (SM4-ASM)
description: DCL \_ constantBuffer (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148999"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="190d4-103">DCL \_ constantBuffer (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="190d4-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="190d4-104">Declara un búfer de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="190d4-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="190d4-105">DCL \_ constantBuffer *cbN \[ tamaño \]*, *AccessPattern*</span><span class="sxs-lookup"><span data-stu-id="190d4-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="190d4-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="190d4-106">Item</span></span></th>
<th><span data-ttu-id="190d4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="190d4-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="190d4-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [tamaño]</em></span><span class="sxs-lookup"><span data-stu-id="190d4-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="190d4-109">de Un búfer de constantes de sombreador, donde N es un entero que denota el número de registro de constantes y el tamaño es un entero que denota el número de elementos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="190d4-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="190d4-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span><span class="sxs-lookup"><span data-stu-id="190d4-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="190d4-111">de La forma en que el código del sombreador tendrá acceso al búfer, que es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="190d4-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="190d4-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="190d4-112">Name</span></span></th>
<th><span data-ttu-id="190d4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="190d4-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="190d4-114">immediateIndexed</span><span class="sxs-lookup"><span data-stu-id="190d4-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="190d4-115">Indizar el búfer con un valor literal.</span><span class="sxs-lookup"><span data-stu-id="190d4-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="190d4-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="190d4-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="190d4-117">Indexa el búfer con el resultado de una expresión evaluada.</span><span class="sxs-lookup"><span data-stu-id="190d4-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="190d4-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="190d4-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="190d4-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="190d4-119">Vertex Shader</span></span> | <span data-ttu-id="190d4-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="190d4-120">Geometry Shader</span></span> | <span data-ttu-id="190d4-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="190d4-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="190d4-122">x</span><span class="sxs-lookup"><span data-stu-id="190d4-122">x</span></span>             | <span data-ttu-id="190d4-123">x</span><span class="sxs-lookup"><span data-stu-id="190d4-123">x</span></span>               | <span data-ttu-id="190d4-124">x</span><span class="sxs-lookup"><span data-stu-id="190d4-124">x</span></span>            |



 

<span data-ttu-id="190d4-125">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="190d4-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="190d4-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="190d4-126">Example</span></span>

<span data-ttu-id="190d4-127">En este ejemplo se declara un búfer de constantes para Register cB0, que tiene 19 elementos.</span><span class="sxs-lookup"><span data-stu-id="190d4-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="190d4-128">Se tiene acceso a estos elementos con un índice literal.</span><span class="sxs-lookup"><span data-stu-id="190d4-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="190d4-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="190d4-129">Minimum Shader Model</span></span>

<span data-ttu-id="190d4-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="190d4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="190d4-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="190d4-131">Shader Model</span></span>                                              | <span data-ttu-id="190d4-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="190d4-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="190d4-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="190d4-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="190d4-134">sí</span><span class="sxs-lookup"><span data-stu-id="190d4-134">yes</span></span>       |
| [<span data-ttu-id="190d4-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="190d4-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="190d4-136">sí</span><span class="sxs-lookup"><span data-stu-id="190d4-136">yes</span></span>       |
| [<span data-ttu-id="190d4-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="190d4-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="190d4-138">sí</span><span class="sxs-lookup"><span data-stu-id="190d4-138">yes</span></span>       |
| [<span data-ttu-id="190d4-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="190d4-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="190d4-140">no</span><span class="sxs-lookup"><span data-stu-id="190d4-140">no</span></span>        |
| [<span data-ttu-id="190d4-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="190d4-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="190d4-142">no</span><span class="sxs-lookup"><span data-stu-id="190d4-142">no</span></span>        |
| [<span data-ttu-id="190d4-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="190d4-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="190d4-144">no</span><span class="sxs-lookup"><span data-stu-id="190d4-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="190d4-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="190d4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190d4-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="190d4-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





