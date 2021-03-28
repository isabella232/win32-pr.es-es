---
title: dcl_output oMask (SM5-ASM)
description: Declare un registro de salida para que lo escriba el sombreador.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1831a47680a06eba085f61badfe56529eed4ba32
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419990"
---
# <a name="dcl_output-omask-sm5---asm"></a><span data-ttu-id="a588e-103">\_oMask de salida de DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="a588e-103">dcl\_output oMask (sm5 - asm)</span></span>

<span data-ttu-id="a588e-104">Declare un registro de salida para que lo escriba el sombreador.</span><span class="sxs-lookup"><span data-stu-id="a588e-104">Declare an output register to be written by the shader.</span></span>



| <span data-ttu-id="a588e-105">salida de DCL \_ o \# \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="a588e-105">dcl\_output o\#\[.mask\]</span></span> |
|--------------------------|



 



| <span data-ttu-id="a588e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a588e-106">Item</span></span>                                                   | <span data-ttu-id="a588e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a588e-107">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="a588e-108"><span id="o"></span><span id="O"></span>*aceptar*</span><span class="sxs-lookup"><span data-stu-id="a588e-108"><span id="o"></span><span id="O"></span>*o*</span></span><br/> | <span data-ttu-id="a588e-109">\[en \] el registro de salida.</span><span class="sxs-lookup"><span data-stu-id="a588e-109">\[in\] The output register.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a588e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a588e-110">Remarks</span></span>


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a><span data-ttu-id="a588e-111">Restricciones</span><span class="sxs-lookup"><span data-stu-id="a588e-111">Restrictions</span></span>

-   <span data-ttu-id="a588e-112">La máscara de componentes puede ser cualquier subconjunto de \[ xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="a588e-112">The component mask can be any subset of \[xyzw\].</span></span> <span data-ttu-id="a588e-113">Sin embargo, dejar huecos entre componentes desperdicia espacio.</span><span class="sxs-lookup"><span data-stu-id="a588e-113">However, leaving gaps between components wastes space.</span></span>
-   <span data-ttu-id="a588e-114">Es legal declarar un supraconjunto de la máscara de componente declarada para la entrada en la siguiente fase.</span><span class="sxs-lookup"><span data-stu-id="a588e-114">It is legal to declare a superset of the component mask declared for input by the next stage.</span></span> <span data-ttu-id="a588e-115">Sin embargo, no se permiten las máscaras mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="a588e-115">However mutually exclusive masks are not allowed.</span></span> <span data-ttu-id="a588e-116">El sombreador de vértices que genera O3. XY significa que el sombreador de píxeles que inserta V3. z no es válido, pero la entrada V3. x o V3. y o V3. XY es válida.</span><span class="sxs-lookup"><span data-stu-id="a588e-116">The vertex shader outputting o3.xy, means the pixel shader inputting v3.z is invalid, but inputting v3.x or v3.y or v3.xy is valid.</span></span>

<span data-ttu-id="a588e-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="a588e-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a588e-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="a588e-118">Vertex</span></span> | <span data-ttu-id="a588e-119">Casco</span><span class="sxs-lookup"><span data-stu-id="a588e-119">Hull</span></span> | <span data-ttu-id="a588e-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="a588e-120">Domain</span></span> | <span data-ttu-id="a588e-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="a588e-121">Geometry</span></span> | <span data-ttu-id="a588e-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="a588e-122">Pixel</span></span> | <span data-ttu-id="a588e-123">Compute</span><span class="sxs-lookup"><span data-stu-id="a588e-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a588e-124">X</span><span class="sxs-lookup"><span data-stu-id="a588e-124">X</span></span>      | <span data-ttu-id="a588e-125">X</span><span class="sxs-lookup"><span data-stu-id="a588e-125">X</span></span>    | <span data-ttu-id="a588e-126">X</span><span class="sxs-lookup"><span data-stu-id="a588e-126">X</span></span>      | <span data-ttu-id="a588e-127">X</span><span class="sxs-lookup"><span data-stu-id="a588e-127">X</span></span>        | <span data-ttu-id="a588e-128">X</span><span class="sxs-lookup"><span data-stu-id="a588e-128">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a588e-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a588e-129">Minimum Shader Model</span></span>

<span data-ttu-id="a588e-130">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="a588e-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="a588e-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a588e-131">Shader Model</span></span>                                              | <span data-ttu-id="a588e-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="a588e-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a588e-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a588e-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a588e-134">sí</span><span class="sxs-lookup"><span data-stu-id="a588e-134">yes</span></span>       |
| [<span data-ttu-id="a588e-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a588e-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a588e-136">no</span><span class="sxs-lookup"><span data-stu-id="a588e-136">no</span></span>        |
| [<span data-ttu-id="a588e-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a588e-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a588e-138">no</span><span class="sxs-lookup"><span data-stu-id="a588e-138">no</span></span>        |
| [<span data-ttu-id="a588e-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a588e-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a588e-140">no</span><span class="sxs-lookup"><span data-stu-id="a588e-140">no</span></span>        |
| [<span data-ttu-id="a588e-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a588e-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a588e-142">no</span><span class="sxs-lookup"><span data-stu-id="a588e-142">no</span></span>        |
| [<span data-ttu-id="a588e-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a588e-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a588e-144">no</span><span class="sxs-lookup"><span data-stu-id="a588e-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a588e-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a588e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a588e-146">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a588e-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





