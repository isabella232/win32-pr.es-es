---
title: Modelo de sombreador 5
description: Esta sección contiene las páginas de referencia para el modelo 5 del sombreador HLSL.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420910"
---
# <a name="shader-model-5"></a><span data-ttu-id="80afb-103">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="80afb-103">Shader Model 5</span></span>

<span data-ttu-id="80afb-104">Esta sección contiene las páginas de referencia para el modelo 5 del sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="80afb-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="80afb-105">El modelo de sombreador 5 es un supraconjunto de las capacidades del [modelo de sombreador 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="80afb-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="80afb-106">Se ha diseñado con un núcleo de sombreador común que proporciona un conjunto común de características para todos los sombreadores programables, que solo se pueden programar mediante HLSL.</span><span class="sxs-lookup"><span data-stu-id="80afb-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="80afb-107">Característica</span><span class="sxs-lookup"><span data-stu-id="80afb-107">Feature</span></span>                   | <span data-ttu-id="80afb-108">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="80afb-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80afb-109">Conjunto de instrucciones</span><span class="sxs-lookup"><span data-stu-id="80afb-109">Instruction Set</span></span>           | [<span data-ttu-id="80afb-110">**Funciones intrínsecas de HLSL**</span><span class="sxs-lookup"><span data-stu-id="80afb-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="80afb-111">Sombreador de vértices máximo</span><span class="sxs-lookup"><span data-stu-id="80afb-111">Vertex Shader Max</span></span>         | <span data-ttu-id="80afb-112">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="80afb-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="80afb-113">Sombreador de píxeles máximo</span><span class="sxs-lookup"><span data-stu-id="80afb-113">Pixel Shader Max</span></span>          | <span data-ttu-id="80afb-114">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="80afb-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="80afb-115">Nuevos perfiles de sombreador agregados</span><span class="sxs-lookup"><span data-stu-id="80afb-115">New Shader Profiles Added</span></span> | <span data-ttu-id="80afb-116">CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS 4 1 \_ \_ \* , vs \_ 4 \_ 1, \* CS \_ 5 \_ 0, DS \_ 5 0, GS 5 \_ \_ \_ 0, HS \_ 5 0 \_ , PS \_ 5 \_ 0, vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80afb-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="80afb-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 y vs \_ 4 \_ 1 se introdujeron en el modelo de sombreador 4,0. sin embargo, DirectX 11 agrega compatibilidad con [búferes estructurados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) y búferes de direcciones de bytes al modelo de sombreador 4 que se ejecuta en hardware de DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="80afb-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="80afb-118">El modelo de sombreador 5 presenta el [sombreador de cálculo](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) que proporciona informática de uso general de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="80afb-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="80afb-119">En una lista de las [características de Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features)se incluye una lista más completa de las características del modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="80afb-120">En la sección de [ensamblado modelo de sombreador 5](shader-model-5-assembly--directx-hlsl-.md) se describen las instrucciones de ensamblado que admite el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80afb-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="80afb-121">In This Section</span></span>



| <span data-ttu-id="80afb-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="80afb-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="80afb-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="80afb-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="80afb-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Atributos del modelo de sombreador 5](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="80afb-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="80afb-125">Páginas de referencia para los atributos del modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="80afb-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funciones intrínsecas del modelo de sombreador 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="80afb-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="80afb-127">Páginas de referencia de las funciones intrínsecas del modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="80afb-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objetos del modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="80afb-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="80afb-129">Páginas de referencia para objetos y métodos del modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="80afb-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valores del sistema del modelo de sombreador 5](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="80afb-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="80afb-131">Páginas de referencia para los valores del sistema del modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="80afb-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="80afb-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80afb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80afb-133">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="80afb-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

