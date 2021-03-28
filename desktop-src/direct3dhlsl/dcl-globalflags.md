---
title: dcl_globalFlags (SM4-ASM)
description: DCL \_ indicadores_globales (SM4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419997"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="49935-103">DCL \_ indicadores_globales (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="49935-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="49935-104">Declara las marcas globales del sombreador.</span><span class="sxs-lookup"><span data-stu-id="49935-104">Declares shader global flags.</span></span>



| <span data-ttu-id="49935-105">\_ *marcas* de DCL indicadores_globales</span><span class="sxs-lookup"><span data-stu-id="49935-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="49935-106"><span id="flags"></span><span id="FLAGS"></span>*marcas*</span><span class="sxs-lookup"><span data-stu-id="49935-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="49935-107">\[en \] una marca de sombreador global.</span><span class="sxs-lookup"><span data-stu-id="49935-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="49935-108">Actualmente hay una marca definida.</span><span class="sxs-lookup"><span data-stu-id="49935-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="49935-109">Refactorización \_ permitida: permite que el controlador reordene las operaciones aritméticas para la optimización, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="49935-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="49935-110">La reordenación de operaciones aritméticas puede generar resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="49935-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="49935-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49935-111">Remarks</span></span>

<span data-ttu-id="49935-112">Esta instrucción opcional se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="49935-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="49935-113">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="49935-113">Vertex Shader</span></span> | <span data-ttu-id="49935-114">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="49935-114">Geometry Shader</span></span> | <span data-ttu-id="49935-115">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="49935-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="49935-116">x</span><span class="sxs-lookup"><span data-stu-id="49935-116">x</span></span>             | <span data-ttu-id="49935-117">x</span><span class="sxs-lookup"><span data-stu-id="49935-117">x</span></span>               | <span data-ttu-id="49935-118">x</span><span class="sxs-lookup"><span data-stu-id="49935-118">x</span></span>            |



 

<span data-ttu-id="49935-119">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="49935-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="49935-120">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="49935-120">Minimum Shader Model</span></span>

<span data-ttu-id="49935-121">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="49935-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="49935-122">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="49935-122">Shader Model</span></span>                                              | <span data-ttu-id="49935-123">Compatible</span><span class="sxs-lookup"><span data-stu-id="49935-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="49935-124">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="49935-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="49935-125">sí</span><span class="sxs-lookup"><span data-stu-id="49935-125">yes</span></span>       |
| [<span data-ttu-id="49935-126">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="49935-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="49935-127">sí</span><span class="sxs-lookup"><span data-stu-id="49935-127">yes</span></span>       |
| [<span data-ttu-id="49935-128">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="49935-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="49935-129">sí</span><span class="sxs-lookup"><span data-stu-id="49935-129">yes</span></span>       |
| [<span data-ttu-id="49935-130">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49935-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="49935-131">no</span><span class="sxs-lookup"><span data-stu-id="49935-131">no</span></span>        |
| [<span data-ttu-id="49935-132">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49935-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="49935-133">no</span><span class="sxs-lookup"><span data-stu-id="49935-133">no</span></span>        |
| [<span data-ttu-id="49935-134">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49935-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="49935-135">no</span><span class="sxs-lookup"><span data-stu-id="49935-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="49935-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49935-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49935-137">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="49935-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




