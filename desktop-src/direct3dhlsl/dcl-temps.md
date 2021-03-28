---
title: dcl_temps (SM4-ASM)
description: DCL \_ Temps (SM4-ASM)
ms.assetid: ecfbdd1e-0f2d-4371-91cc-ebc3e5ee8ee7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5fc3a468575b30836d4574edb13c4fc77a3505fc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996968"
---
# <a name="dcl_temps-sm4---asm"></a><span data-ttu-id="23779-103">DCL \_ Temps (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="23779-103">dcl\_temps (sm4 - asm)</span></span>

<span data-ttu-id="23779-104">Declara los registros temporales.</span><span class="sxs-lookup"><span data-stu-id="23779-104">Declares temporary registers.</span></span>



| <span data-ttu-id="23779-105">DCL \_ Temps N</span><span class="sxs-lookup"><span data-stu-id="23779-105">dcl\_temps N</span></span> |
|--------------|



 



| <span data-ttu-id="23779-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="23779-106">Item</span></span>                                                   | <span data-ttu-id="23779-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="23779-107">Description</span></span>                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23779-108"><span id="N"></span><span id="n"></span>*N*</span><span class="sxs-lookup"><span data-stu-id="23779-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="23779-109">\[en \] el número de registros temporales.</span><span class="sxs-lookup"><span data-stu-id="23779-109">\[in\] The number of temporary registers.</span></span><br/> |



 

<span data-ttu-id="23779-110">Cada registro tiene espacio para un valor de cuatro componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="23779-110">Each register has space for a 32-bit four-component value.</span></span> <span data-ttu-id="23779-111">El número total de registros temporales e [indexables temporales](dcl-indexabletemp.md) debe ser menor o igual que 4096.</span><span class="sxs-lookup"><span data-stu-id="23779-111">The total number of temporary and [indexable-temporary](dcl-indexabletemp.md) registers must be less than or equal to 4096.</span></span>

<span data-ttu-id="23779-112">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="23779-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23779-113">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="23779-113">Vertex Shader</span></span> | <span data-ttu-id="23779-114">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="23779-114">Geometry Shader</span></span> | <span data-ttu-id="23779-115">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="23779-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="23779-116">x</span><span class="sxs-lookup"><span data-stu-id="23779-116">x</span></span>             | <span data-ttu-id="23779-117">x</span><span class="sxs-lookup"><span data-stu-id="23779-117">x</span></span>               | <span data-ttu-id="23779-118">x</span><span class="sxs-lookup"><span data-stu-id="23779-118">x</span></span>            |



 

<span data-ttu-id="23779-119">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="23779-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="23779-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23779-120">Example</span></span>

<span data-ttu-id="23779-121">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="23779-121">Here is an example.</span></span>


```
dcl_temps 10; // Declare r0-r9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="23779-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="23779-122">Minimum Shader Model</span></span>

<span data-ttu-id="23779-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="23779-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23779-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="23779-124">Shader Model</span></span>                                              | <span data-ttu-id="23779-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="23779-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23779-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="23779-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23779-127">sí</span><span class="sxs-lookup"><span data-stu-id="23779-127">yes</span></span>       |
| [<span data-ttu-id="23779-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="23779-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23779-129">sí</span><span class="sxs-lookup"><span data-stu-id="23779-129">yes</span></span>       |
| [<span data-ttu-id="23779-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="23779-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23779-131">sí</span><span class="sxs-lookup"><span data-stu-id="23779-131">yes</span></span>       |
| [<span data-ttu-id="23779-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23779-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23779-133">no</span><span class="sxs-lookup"><span data-stu-id="23779-133">no</span></span>        |
| [<span data-ttu-id="23779-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23779-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23779-135">no</span><span class="sxs-lookup"><span data-stu-id="23779-135">no</span></span>        |
| [<span data-ttu-id="23779-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23779-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23779-137">no</span><span class="sxs-lookup"><span data-stu-id="23779-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23779-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23779-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23779-139">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23779-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





