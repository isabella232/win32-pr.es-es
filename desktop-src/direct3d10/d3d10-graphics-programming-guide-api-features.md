---
description: La canalización de gráficos de Direct3D 10 representa un cambio fundamental en la arquitectura, que se vuelve a crear desde el principio del hardware y el software para potenciar la próxima generación de juegos y aplicaciones multimedia 3D.
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: Características de la API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274892"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="4492f-103">Características de la API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4492f-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="4492f-104">La canalización de gráficos de Direct3D 10 representa un cambio fundamental en la arquitectura, que se vuelve a crear desde el principio del hardware y el software para potenciar la próxima generación de juegos y aplicaciones multimedia 3D.</span><span class="sxs-lookup"><span data-stu-id="4492f-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="4492f-105">Usa Windows Display Driver Model (WDDM), que permite mejorar el rendimiento y el comportamiento, como la memoria virtual de la GPU.</span><span class="sxs-lookup"><span data-stu-id="4492f-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="4492f-106">Los desarrolladores familiarizados con Direct3D 9 detectarán una serie de mejoras funcionales y mejoras de rendimiento en Direct3D 10, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="4492f-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="4492f-107">La capacidad de procesar primitivas enteras en la nueva [fase de sombreador de geometría](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4492f-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="4492f-108">La capacidad de generar datos de vértices generados por la canalización en la memoria mediante la [fase de flujo de salida](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span><span class="sxs-lookup"><span data-stu-id="4492f-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="4492f-109">Organización del estado de la canalización en cinco [objetos de estado](d3d10-graphics-programming-guide-api-features-state-objects.md)inmutables, lo que permite una configuración rápida de la canalización.</span><span class="sxs-lookup"><span data-stu-id="4492f-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="4492f-110">Organización de constantes de sombreador en [búferes de constantes](d3d10-graphics-programming-guide-resources-types.md), lo que minimiza la sobrecarga de ancho de banda para proporcionar datos de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4492f-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="4492f-111">La capacidad de realizar el intercambio y la configuración de materiales por primitivo mediante un sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="4492f-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="4492f-112">Nuevos [tipos de recursos](d3d10-graphics-programming-guide-resources-types.md) (incluidas las matrices de texturas que se pueden indizar a partir de sombreadores) y formatos de recursos.</span><span class="sxs-lookup"><span data-stu-id="4492f-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="4492f-113">Mayor generalización del acceso a los recursos mediante una [vista](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="4492f-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="4492f-114">Los bits de capacidad de hardware heredado (Cap) se han quitado en favor de un amplio conjunto de funcionalidades garantizadas, cuyo destino es hardware de clase de Direct3D 10 (mínimo).</span><span class="sxs-lookup"><span data-stu-id="4492f-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="4492f-115">[Runtime en capas](d3d10-graphics-programming-guide-api-features-layers.md) : la API de Direct3D 10 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores (depuración, etc.) en capas externas.</span><span class="sxs-lookup"><span data-stu-id="4492f-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="4492f-116">Integración de HLSL completa: todos los sombreadores de Direct3D 10 están escritos en HLSL e implementados con [Common-Shader Core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span><span class="sxs-lookup"><span data-stu-id="4492f-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="4492f-117">Aumento en el número de destinos de representación, texturas y muestreadores.</span><span class="sxs-lookup"><span data-stu-id="4492f-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="4492f-118">Tampoco hay ningún límite de longitud de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4492f-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="4492f-119">Operaciones de sombreador Integer y bit a bit.</span><span class="sxs-lookup"><span data-stu-id="4492f-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="4492f-120">Readback de una superficie de estarcido o profundidad o un recurso de muestreo multimuestreado, una vez que ya no está enlazado como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4492f-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="4492f-121">Compatibilidad con Alpha-to-Coverage multimuestreado.</span><span class="sxs-lookup"><span data-stu-id="4492f-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="4492f-122">Existen diferencias de comportamiento adicionales que los desarrolladores de Direct3D 9 también deben tener en cuenta (consulte [consideraciones de Direct3D 9 a Direct3D 10](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span><span class="sxs-lookup"><span data-stu-id="4492f-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="4492f-123">Esta es una lista de características de Direct3D 9 que ya no se admiten o que se han revisado en Direct3D 10 (consulte [características desusadas](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span><span class="sxs-lookup"><span data-stu-id="4492f-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4492f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4492f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4492f-125">Guía de programación para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="4492f-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
