---
title: dcl_outputTopology (SM4-ASM)
description: DCL \_ outputTopology (SM4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785009"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="37d51-103">DCL \_ outputTopology (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="37d51-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="37d51-104">Declara los datos de salida del sombreador de tipo primitivo.</span><span class="sxs-lookup"><span data-stu-id="37d51-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="37d51-105">\_ *tipo* de outputTopology de DCL</span><span class="sxs-lookup"><span data-stu-id="37d51-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37d51-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="37d51-106">Item</span></span></th>
<th><span data-ttu-id="37d51-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="37d51-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37d51-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Automáticamente</em></span><span class="sxs-lookup"><span data-stu-id="37d51-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="37d51-109">de Una topología primitiva de salida, que es uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="37d51-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="37d51-110"><em>pointlist</em></span><span class="sxs-lookup"><span data-stu-id="37d51-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="37d51-111"><em>linestrip</em></span><span class="sxs-lookup"><span data-stu-id="37d51-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="37d51-112"><em>trianglestrip</em></span><span class="sxs-lookup"><span data-stu-id="37d51-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="37d51-113">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="37d51-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="37d51-114">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="37d51-114">Vertex Shader</span></span> | <span data-ttu-id="37d51-115">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="37d51-115">Geometry Shader</span></span> | <span data-ttu-id="37d51-116">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="37d51-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="37d51-117">x</span><span class="sxs-lookup"><span data-stu-id="37d51-117">x</span></span>               |              |



 

<span data-ttu-id="37d51-118">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="37d51-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="37d51-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37d51-119">Example</span></span>

<span data-ttu-id="37d51-120">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="37d51-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="37d51-121">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="37d51-121">Minimum Shader Model</span></span>

<span data-ttu-id="37d51-122">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="37d51-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="37d51-123">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="37d51-123">Shader Model</span></span>                                              | <span data-ttu-id="37d51-124">Compatible</span><span class="sxs-lookup"><span data-stu-id="37d51-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="37d51-125">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="37d51-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="37d51-126">sí</span><span class="sxs-lookup"><span data-stu-id="37d51-126">yes</span></span>       |
| [<span data-ttu-id="37d51-127">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="37d51-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="37d51-128">sí</span><span class="sxs-lookup"><span data-stu-id="37d51-128">yes</span></span>       |
| [<span data-ttu-id="37d51-129">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="37d51-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="37d51-130">sí</span><span class="sxs-lookup"><span data-stu-id="37d51-130">yes</span></span>       |
| [<span data-ttu-id="37d51-131">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37d51-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="37d51-132">no</span><span class="sxs-lookup"><span data-stu-id="37d51-132">no</span></span>        |
| [<span data-ttu-id="37d51-133">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37d51-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="37d51-134">no</span><span class="sxs-lookup"><span data-stu-id="37d51-134">no</span></span>        |
| [<span data-ttu-id="37d51-135">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37d51-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="37d51-136">no</span><span class="sxs-lookup"><span data-stu-id="37d51-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="37d51-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37d51-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37d51-138">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="37d51-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





