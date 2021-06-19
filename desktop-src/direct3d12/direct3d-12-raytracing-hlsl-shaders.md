---
title: Sombreadores de HLSL de Direct3D 12 Raytracing
description: Vea vínculos a artículos que describen sombreadores de lenguaje de sombreador de alto nivel (HLSL) que admiten la canalización de trazado de rayos de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394840"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="27ff4-103">Sombreadores de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="27ff4-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="27ff4-104">Los siguientes sombreadores HLSL admiten la canalización de trazado de rayos de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="27ff4-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="27ff4-105">Estos sombreadores son funciones compiladas en una biblioteca, con el modelo de destino lib_6_3 y identificadas por un atributo *[shader("shadertype")]* en la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="27ff4-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="27ff4-106">Vea **Intrínsecos** **y valores del sistema** para ver lo que se permite para cada tipo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="27ff4-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="27ff4-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="27ff4-107">In this section</span></span>



| <span data-ttu-id="27ff4-108">Tema</span><span class="sxs-lookup"><span data-stu-id="27ff4-108">Topic</span></span>                                                                                                       | <span data-ttu-id="27ff4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="27ff4-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27ff4-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="27ff4-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="27ff4-111">Sombreador que se invoca cuando las intersecciones de rayos no son opacas.</span><span class="sxs-lookup"><span data-stu-id="27ff4-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="27ff4-112">**Sombreador al que se puede llamar**</span><span class="sxs-lookup"><span data-stu-id="27ff4-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="27ff4-113">Sombreador que se invoca desde otro sombreador con **el intrínseco CallShader.**</span><span class="sxs-lookup"><span data-stu-id="27ff4-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="27ff4-114">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="27ff4-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="27ff4-115">Sombreador que se invoca cuando está habilitado y se ha determinado el impacto más cercano o se ha finalizado la búsqueda de intersección de rayos.</span><span class="sxs-lookup"><span data-stu-id="27ff4-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="27ff4-116">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="27ff4-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="27ff4-117">Sombreador que se usa para implementar primitivas de intersección personalizadas para los rayos que intersecan con un volumen de límite asociado (rectángulo de selección).</span><span class="sxs-lookup"><span data-stu-id="27ff4-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="27ff4-118">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="27ff4-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="27ff4-119">Sombreador que se invoca cuando no se encuentra ni se acepta ninguna intersección de rayos.</span><span class="sxs-lookup"><span data-stu-id="27ff4-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="27ff4-120">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="27ff4-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="27ff4-121">Sombreador que llama [**a TraceRay**](traceray-function.md) para generar rayos.</span><span class="sxs-lookup"><span data-stu-id="27ff4-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="27ff4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27ff4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ff4-123">Referencia principal</span><span class="sxs-lookup"><span data-stu-id="27ff4-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="27ff4-124">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="27ff4-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





