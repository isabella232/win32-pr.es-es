---
title: dcl_output_siv (SM4-ASM)
description: '\_ \_ SIV de salida de DCL (SM4-ASM)'
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996976"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="35de1-103">\_ \_ SIV de salida de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="35de1-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="35de1-104">Declara un registro de salida que contiene un parámetro [de valor del sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="35de1-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="35de1-105">\_ \_ SIV de salida de DCL en \[ *. masks* \] , *systemValue*</span><span class="sxs-lookup"><span data-stu-id="35de1-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="35de1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="35de1-106">Item</span></span>                                                                                                                               | <span data-ttu-id="35de1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="35de1-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35de1-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="35de1-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="35de1-109">\[en \] un registro de datos de salida; *N* es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="35de1-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="35de1-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="35de1-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="35de1-111">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="35de1-111">\[in\] Optional.</span></span> <span data-ttu-id="35de1-112">Máscara de componente (. xyzw) que especifica cuál de los componentes de registro se va a usar.</span><span class="sxs-lookup"><span data-stu-id="35de1-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="35de1-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="35de1-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="35de1-114">\[en \] el nombre del valor del sistema, que es una cadena (vea [semántica de valor del sistema](dx-graphics-hlsl-semantics.md)) sin el \_ prefijo "VP".</span><span class="sxs-lookup"><span data-stu-id="35de1-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="35de1-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="35de1-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="35de1-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="35de1-116">Vertex Shader</span></span> | <span data-ttu-id="35de1-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="35de1-117">Geometry Shader</span></span> | <span data-ttu-id="35de1-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="35de1-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="35de1-119">x</span><span class="sxs-lookup"><span data-stu-id="35de1-119">x</span></span>             | <span data-ttu-id="35de1-120">x</span><span class="sxs-lookup"><span data-stu-id="35de1-120">x</span></span>               |              |



 

<span data-ttu-id="35de1-121">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="35de1-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="35de1-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35de1-122">Example</span></span>

<span data-ttu-id="35de1-123">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="35de1-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="35de1-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="35de1-124">Minimum Shader Model</span></span>

<span data-ttu-id="35de1-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="35de1-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35de1-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="35de1-126">Shader Model</span></span>                                              | <span data-ttu-id="35de1-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="35de1-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="35de1-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="35de1-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="35de1-129">sí</span><span class="sxs-lookup"><span data-stu-id="35de1-129">yes</span></span>       |
| [<span data-ttu-id="35de1-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="35de1-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="35de1-131">sí</span><span class="sxs-lookup"><span data-stu-id="35de1-131">yes</span></span>       |
| [<span data-ttu-id="35de1-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="35de1-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="35de1-133">sí</span><span class="sxs-lookup"><span data-stu-id="35de1-133">yes</span></span>       |
| [<span data-ttu-id="35de1-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35de1-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="35de1-135">no</span><span class="sxs-lookup"><span data-stu-id="35de1-135">no</span></span>        |
| [<span data-ttu-id="35de1-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35de1-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="35de1-137">no</span><span class="sxs-lookup"><span data-stu-id="35de1-137">no</span></span>        |
| [<span data-ttu-id="35de1-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35de1-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="35de1-139">no</span><span class="sxs-lookup"><span data-stu-id="35de1-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="35de1-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35de1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35de1-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35de1-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





