---
title: dcl_function_table (SM5-ASM)
description: Declare una tabla de función.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996993"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="c5ec1-103">\_ \_ tabla de funciones DCL (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c5ec1-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="c5ec1-104">Declare una tabla de función.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-104">Declare a function table.</span></span>



| <span data-ttu-id="c5ec1-105">\_ \_ tabla ft de la función DCL \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="c5ec1-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="c5ec1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="c5ec1-106">Item</span></span>                                                      | <span data-ttu-id="c5ec1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5ec1-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c5ec1-108"><span id="ft"></span><span id="FT"></span>*tolerancia*</span><span class="sxs-lookup"><span data-stu-id="c5ec1-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="c5ec1-109">\[en \] las entradas de la tabla de funciones.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5ec1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5ec1-110">Remarks</span></span>

<span data-ttu-id="c5ec1-111">Esta función declara una tabla de funciones como un conjunto de cuerpos de función que se han declarado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="c5ec1-112">Esto es como una vtable de C++, salvo que hay una entrada por cada sitio de llamada para una interfaz en lugar de por método.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="c5ec1-113">No hay ningún límite en el número de cuerpos de función que se pueden enumerar en una tabla de función.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="c5ec1-114">Es válido para que \# se haga referencia varias veces a un cuerpo de función FB en una o varias tablas de funciones, como una manera de compartir código común.</span><span class="sxs-lookup"><span data-stu-id="c5ec1-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="c5ec1-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="c5ec1-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c5ec1-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="c5ec1-116">Vertex</span></span> | <span data-ttu-id="c5ec1-117">Casco</span><span class="sxs-lookup"><span data-stu-id="c5ec1-117">Hull</span></span> | <span data-ttu-id="c5ec1-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="c5ec1-118">Domain</span></span> | <span data-ttu-id="c5ec1-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="c5ec1-119">Geometry</span></span> | <span data-ttu-id="c5ec1-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="c5ec1-120">Pixel</span></span> | <span data-ttu-id="c5ec1-121">Compute</span><span class="sxs-lookup"><span data-stu-id="c5ec1-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c5ec1-122">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-122">X</span></span>      | <span data-ttu-id="c5ec1-123">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-123">X</span></span>    | <span data-ttu-id="c5ec1-124">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-124">X</span></span>      | <span data-ttu-id="c5ec1-125">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-125">X</span></span>        | <span data-ttu-id="c5ec1-126">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-126">X</span></span>     | <span data-ttu-id="c5ec1-127">X</span><span class="sxs-lookup"><span data-stu-id="c5ec1-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c5ec1-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c5ec1-128">Minimum Shader Model</span></span>

<span data-ttu-id="c5ec1-129">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="c5ec1-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c5ec1-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c5ec1-130">Shader Model</span></span>                                              | <span data-ttu-id="c5ec1-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="c5ec1-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c5ec1-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c5ec1-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c5ec1-133">sí</span><span class="sxs-lookup"><span data-stu-id="c5ec1-133">yes</span></span>       |
| [<span data-ttu-id="c5ec1-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c5ec1-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c5ec1-135">no</span><span class="sxs-lookup"><span data-stu-id="c5ec1-135">no</span></span>        |
| [<span data-ttu-id="c5ec1-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c5ec1-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c5ec1-137">no</span><span class="sxs-lookup"><span data-stu-id="c5ec1-137">no</span></span>        |
| [<span data-ttu-id="c5ec1-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5ec1-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c5ec1-139">no</span><span class="sxs-lookup"><span data-stu-id="c5ec1-139">no</span></span>        |
| [<span data-ttu-id="c5ec1-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5ec1-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c5ec1-141">no</span><span class="sxs-lookup"><span data-stu-id="c5ec1-141">no</span></span>        |
| [<span data-ttu-id="c5ec1-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5ec1-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c5ec1-143">no</span><span class="sxs-lookup"><span data-stu-id="c5ec1-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c5ec1-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5ec1-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5ec1-145">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5ec1-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





