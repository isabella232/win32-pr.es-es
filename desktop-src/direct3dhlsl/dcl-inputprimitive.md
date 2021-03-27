---
title: dcl_inputPrimitive (SM4-ASM)
description: DCL \_ inputPrimitive (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103994843"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="55a27-103">DCL \_ inputPrimitive (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="55a27-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="55a27-104">Declara el tipo primitivo para las entradas del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="55a27-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="55a27-105">\_ *tipo* de inputPrimitive de DCL</span><span class="sxs-lookup"><span data-stu-id="55a27-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55a27-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="55a27-106">Item</span></span></th>
<th><span data-ttu-id="55a27-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="55a27-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="55a27-108"><span id="type"></span><span id="TYPE"></span><em>automáticamente</em></span><span class="sxs-lookup"><span data-stu-id="55a27-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="55a27-109">de Tipo primitivo de datos de entrada, que es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="55a27-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="55a27-110"><em>punto</em> - de lista de puntos</span><span class="sxs-lookup"><span data-stu-id="55a27-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="55a27-111"><em>línea</em> - de lista de líneas</span><span class="sxs-lookup"><span data-stu-id="55a27-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="55a27-112"><em>triángulo</em> - lista de triángulos</span><span class="sxs-lookup"><span data-stu-id="55a27-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="55a27-113"><em>line_adj</em> - lista de líneas con datos de adyacencia</span><span class="sxs-lookup"><span data-stu-id="55a27-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="55a27-114"><em>triangle_adj</em> - lista de triángulos con datos de adyacencia</span><span class="sxs-lookup"><span data-stu-id="55a27-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55a27-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="55a27-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="55a27-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="55a27-116">Vertex Shader</span></span> | <span data-ttu-id="55a27-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="55a27-117">Geometry Shader</span></span> | <span data-ttu-id="55a27-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="55a27-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="55a27-119">x</span><span class="sxs-lookup"><span data-stu-id="55a27-119">x</span></span>               |              |



 

<span data-ttu-id="55a27-120">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="55a27-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="55a27-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55a27-121">Example</span></span>

<span data-ttu-id="55a27-122">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="55a27-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="55a27-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="55a27-123">Minimum Shader Model</span></span>

<span data-ttu-id="55a27-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="55a27-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="55a27-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="55a27-125">Shader Model</span></span>                                              | <span data-ttu-id="55a27-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="55a27-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="55a27-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="55a27-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="55a27-128">sí</span><span class="sxs-lookup"><span data-stu-id="55a27-128">yes</span></span>       |
| [<span data-ttu-id="55a27-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="55a27-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="55a27-130">sí</span><span class="sxs-lookup"><span data-stu-id="55a27-130">yes</span></span>       |
| [<span data-ttu-id="55a27-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="55a27-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="55a27-132">sí</span><span class="sxs-lookup"><span data-stu-id="55a27-132">yes</span></span>       |
| [<span data-ttu-id="55a27-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55a27-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="55a27-134">no</span><span class="sxs-lookup"><span data-stu-id="55a27-134">no</span></span>        |
| [<span data-ttu-id="55a27-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55a27-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="55a27-136">no</span><span class="sxs-lookup"><span data-stu-id="55a27-136">no</span></span>        |
| [<span data-ttu-id="55a27-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55a27-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="55a27-138">no</span><span class="sxs-lookup"><span data-stu-id="55a27-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="55a27-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55a27-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a27-140">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55a27-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





