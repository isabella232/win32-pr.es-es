---
title: dcl_output oDepth (SM4-ASM)
description: '\_oDepth de salida de DCL (SM4-ASM)'
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358512"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="a40ef-103">\_oDepth de salida de DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a40ef-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="a40ef-104">Declara que un sombreador de píxeles usará el registro de profundidad de salida.</span><span class="sxs-lookup"><span data-stu-id="a40ef-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="a40ef-105">oDepth de salida de DCL \_</span><span class="sxs-lookup"><span data-stu-id="a40ef-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="a40ef-106">El valor del registro de profundidad de salida se usa durante una comparación de profundidad (si está habilitada la comparación de profundidad).</span><span class="sxs-lookup"><span data-stu-id="a40ef-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="a40ef-107">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a40ef-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a40ef-108">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="a40ef-108">Vertex Shader</span></span> | <span data-ttu-id="a40ef-109">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="a40ef-109">Geometry Shader</span></span> | <span data-ttu-id="a40ef-110">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="a40ef-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="a40ef-111">x</span><span class="sxs-lookup"><span data-stu-id="a40ef-111">x</span></span>            |



 

<span data-ttu-id="a40ef-112">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="a40ef-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="a40ef-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a40ef-113">Example</span></span>

<span data-ttu-id="a40ef-114">Estos son algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a40ef-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="a40ef-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a40ef-115">Minimum Shader Model</span></span>

<span data-ttu-id="a40ef-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a40ef-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a40ef-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a40ef-117">Shader Model</span></span>                                              | <span data-ttu-id="a40ef-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="a40ef-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a40ef-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a40ef-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a40ef-120">sí</span><span class="sxs-lookup"><span data-stu-id="a40ef-120">yes</span></span>       |
| [<span data-ttu-id="a40ef-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a40ef-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a40ef-122">sí</span><span class="sxs-lookup"><span data-stu-id="a40ef-122">yes</span></span>       |
| [<span data-ttu-id="a40ef-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a40ef-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a40ef-124">sí</span><span class="sxs-lookup"><span data-stu-id="a40ef-124">yes</span></span>       |
| [<span data-ttu-id="a40ef-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a40ef-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a40ef-126">no</span><span class="sxs-lookup"><span data-stu-id="a40ef-126">no</span></span>        |
| [<span data-ttu-id="a40ef-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a40ef-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a40ef-128">no</span><span class="sxs-lookup"><span data-stu-id="a40ef-128">no</span></span>        |
| [<span data-ttu-id="a40ef-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a40ef-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a40ef-130">no</span><span class="sxs-lookup"><span data-stu-id="a40ef-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a40ef-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a40ef-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40ef-132">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a40ef-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




