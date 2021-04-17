---
title: Sombreadores de HLSL de Direct3D 12 Raytracing
description: Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105648155"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="9427b-103">Sombreadores de HLSL de Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="9427b-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="9427b-104">Los siguientes sombreadores HLSL admiten la canalización raytracing de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9427b-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="9427b-105">Estos sombreadores son funciones compiladas en una biblioteca, con el modelo de destino lib_6_3 y que se identifican mediante un atributo *[Shader ("shadertype")]* en la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9427b-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="9427b-106">Vea **intrínsecos** y **valores del sistema** para ver lo que se permite para cada tipo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9427b-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9427b-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9427b-107">In this section</span></span>



| <span data-ttu-id="9427b-108">Tema</span><span class="sxs-lookup"><span data-stu-id="9427b-108">Topic</span></span>                                                                                                       | <span data-ttu-id="9427b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9427b-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9427b-110">**Sombreador de cualquier acierto**</span><span class="sxs-lookup"><span data-stu-id="9427b-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="9427b-111">Sombreador que se invoca cuando las intersecciones de rayo no son opacas.</span><span class="sxs-lookup"><span data-stu-id="9427b-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9427b-112">**Sombreador al que se puede llamar**</span><span class="sxs-lookup"><span data-stu-id="9427b-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="9427b-113">Sombreador que se invoca desde otro sombreador con la función intrínseca **CallShader** .</span><span class="sxs-lookup"><span data-stu-id="9427b-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9427b-114">**Sombreador del acierto más cercano**</span><span class="sxs-lookup"><span data-stu-id="9427b-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="9427b-115">Sombreador que se invoca cuando está habilitado y se ha determinado el acierto más cercano o ha finalizado la búsqueda de interseccións de Ray.</span><span class="sxs-lookup"><span data-stu-id="9427b-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9427b-116">**Sombreador de intersección**</span><span class="sxs-lookup"><span data-stu-id="9427b-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="9427b-117">Sombreador que se utiliza para implementar primitivas de intersección personalizadas para los rayos que intersectan con un volumen de límite asociado (rectángulo de selección).</span><span class="sxs-lookup"><span data-stu-id="9427b-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9427b-118">**Sombreador de errores**</span><span class="sxs-lookup"><span data-stu-id="9427b-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="9427b-119">Sombreador que se invoca cuando no se encuentran ni se aceptan intersecciones de rayo.</span><span class="sxs-lookup"><span data-stu-id="9427b-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9427b-120">**Sombreador de generación de rayos**</span><span class="sxs-lookup"><span data-stu-id="9427b-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="9427b-121">Sombreador que llama a [**TraceRay**](traceray-function.md) para generar rayos.</span><span class="sxs-lookup"><span data-stu-id="9427b-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="9427b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9427b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9427b-123">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="9427b-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="9427b-124">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9427b-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





