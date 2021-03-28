---
title: dcl_output_sgv (SM4-ASM)
description: '\_ \_ SGV de salida de DCL (SM4-ASM)'
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419989"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="af951-103">\_ \_ SGV de salida de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="af951-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="af951-104">Declara un registro de salida que contiene un parámetro [de valor del sistema](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="af951-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="af951-105">\_ \_ SGV de salida de DCL en *\[ \] . Mask*, *systemValue*</span><span class="sxs-lookup"><span data-stu-id="af951-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="af951-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="af951-106">Item</span></span>                                                                                                                               | <span data-ttu-id="af951-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="af951-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af951-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="af951-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="af951-109">\[en \] un registro de datos de salida; *N* es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="af951-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="af951-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="af951-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="af951-111">\[en \] opcional.</span><span class="sxs-lookup"><span data-stu-id="af951-111">\[in\] Optional.</span></span> <span data-ttu-id="af951-112">Máscara de componente (. xyzw) que especifica cuál de los componentes de registro se va a usar.</span><span class="sxs-lookup"><span data-stu-id="af951-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="af951-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span><span class="sxs-lookup"><span data-stu-id="af951-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="af951-114">\[en \] el nombre del valor del sistema, que es una cadena (vea [semántica de valor del sistema](dx-graphics-hlsl-semantics.md)) sin el \_ prefijo "VP".</span><span class="sxs-lookup"><span data-stu-id="af951-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="af951-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="af951-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="af951-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="af951-116">Vertex Shader</span></span> | <span data-ttu-id="af951-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="af951-117">Geometry Shader</span></span> | <span data-ttu-id="af951-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="af951-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="af951-119">x</span><span class="sxs-lookup"><span data-stu-id="af951-119">x</span></span>               |              |



 

<span data-ttu-id="af951-120">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="af951-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="af951-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af951-121">Example</span></span>

<span data-ttu-id="af951-122">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="af951-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="af951-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="af951-123">Minimum Shader Model</span></span>

<span data-ttu-id="af951-124">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="af951-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="af951-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="af951-125">Shader Model</span></span>                                              | <span data-ttu-id="af951-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="af951-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="af951-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="af951-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="af951-128">sí</span><span class="sxs-lookup"><span data-stu-id="af951-128">yes</span></span>       |
| [<span data-ttu-id="af951-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="af951-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="af951-130">sí</span><span class="sxs-lookup"><span data-stu-id="af951-130">yes</span></span>       |
| [<span data-ttu-id="af951-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="af951-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="af951-132">sí</span><span class="sxs-lookup"><span data-stu-id="af951-132">yes</span></span>       |
| [<span data-ttu-id="af951-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af951-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="af951-134">no</span><span class="sxs-lookup"><span data-stu-id="af951-134">no</span></span>        |
| [<span data-ttu-id="af951-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af951-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="af951-136">no</span><span class="sxs-lookup"><span data-stu-id="af951-136">no</span></span>        |
| [<span data-ttu-id="af951-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af951-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="af951-138">no</span><span class="sxs-lookup"><span data-stu-id="af951-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="af951-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af951-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af951-140">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="af951-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





