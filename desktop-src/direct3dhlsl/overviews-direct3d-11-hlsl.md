---
title: Modelo 5 del sombreador HLSL
description: Modelo 5 del sombreador HLSL
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904672"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="32c1a-103">Modelo 5 del sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="32c1a-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="32c1a-104">Esta sección contiene material de información general para el lenguaje de sombreador de High-Level, concretamente las nuevas características del modelo de sombreador 5 que se introdujeron en Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="32c1a-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="32c1a-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="32c1a-105">In This Section</span></span>



| <span data-ttu-id="32c1a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="32c1a-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="32c1a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c1a-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c1a-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculación dinámica](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="32c1a-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="32c1a-109">La vinculación dinámica permite que el tiempo de ejecución tome una decisión en tiempo de dibujo (en lugar de tiempo de compilación) sobre qué ruta de acceso del código se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="32c1a-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="32c1a-110">Esto reduce el problema de proliferación del sombreador causado por los sombreadores con firmas de entrada casi idénticas.</span><span class="sxs-lookup"><span data-stu-id="32c1a-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="32c1a-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="32c1a-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="32c1a-112">Nuevas características del sombreador de geometría, entre las que se incluyen: creación de instancias, que proporciona un aumento del rendimiento cuando el orden de los primitivos en la secuencia no es importante, y flujos de salida de varios puntos para que un sombreador pueda generar vértices en más de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="32c1a-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="32c1a-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tesela](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="32c1a-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="32c1a-114">El tiempo de ejecución de Direct3D 11 admite tres nuevas fases que implementan Teselación, que convierte las superficies de subdivisiones de bajo detalle en primitivas más detalladas en la GPU.</span><span class="sxs-lookup"><span data-stu-id="32c1a-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="32c1a-115">Mosaicos de teselación (o rotura) de superficies de orden superior en estructuras adecuadas para la representación.</span><span class="sxs-lookup"><span data-stu-id="32c1a-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="32c1a-116">Las tres fases de teselación son las fases del sombreador de casco, del teselador y del sombreador de dominio.</span><span class="sxs-lookup"><span data-stu-id="32c1a-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="32c1a-117">Además, la sección de referencia abarca muchos elementos de API nuevos para el modelo de sombreador 5: [atributos](d3d11-graphics-reference-sm5-attributes.md), [funciones intrínsecas](d3d11-graphics-reference-sm5-intrinsics.md), [objetos y métodos de modelo de sombreador 5](d3d11-graphics-reference-sm5-objects.md)y [valores del sistema](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="32c1a-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c1a-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32c1a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c1a-119">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="32c1a-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

