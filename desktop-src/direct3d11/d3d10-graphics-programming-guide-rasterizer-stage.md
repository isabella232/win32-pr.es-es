---
title: Etapa del rasterizador
description: La fase de rasterización convierte información de vectores (formada por formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995762"
---
# <a name="rasterizer-stage"></a><span data-ttu-id="2b84d-103">Etapa del rasterizador</span><span class="sxs-lookup"><span data-stu-id="2b84d-103">Rasterizer Stage</span></span>

<span data-ttu-id="2b84d-104">La fase de rasterización convierte información de vectores (formada por formas o primitivas) en una imagen de trama (compuesta de píxeles) con el fin de mostrar gráficos 3D en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="2b84d-104">The rasterization stage converts vector information (composed of shapes or primitives) into a raster image (composed of pixels) for the purpose of displaying real-time 3D graphics.</span></span>

<span data-ttu-id="2b84d-105">Durante la rasterización, cada primitiva se convierte en píxeles, mientras que los valores de cada vértice se interpolan en cada primitiva.</span><span class="sxs-lookup"><span data-stu-id="2b84d-105">During rasterization, each primitive is converted into pixels, while interpolating per-vertex values across each primitive.</span></span> <span data-ttu-id="2b84d-106">La rasterización incluye vértices de recorte para el frustum de la vista, que realiza una división por z para proporcionar perspectiva, asignar primitivos a una ventanilla 2D y determinar cómo invocar el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2b84d-106">Rasterization includes clipping vertices to the view frustum, performing a divide by z to provide perspective, mapping primitives to a 2D viewport, and determining how to invoke the pixel shader.</span></span> <span data-ttu-id="2b84d-107">Aunque el uso de un sombreador de píxeles es opcional, la fase de rasterizador siempre realiza el recorte, una división de perspectiva para transformar los puntos en un espacio homogéneo y asigna los vértices a la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="2b84d-107">While using a pixel shader is optional, the rasterizer stage always performs clipping, a perspective divide to transform the points into homogeneous space, and maps the vertices to the viewport.</span></span>

<span data-ttu-id="2b84d-108">Se supone que los vértices (x, y, z, w) que entran en la fase de rasterizador están en el espacio de recorte homogéneo.</span><span class="sxs-lookup"><span data-stu-id="2b84d-108">Vertices (x,y,z,w), coming into the rasterizer stage are assumed to be in homogeneous clip-space.</span></span> <span data-ttu-id="2b84d-109">En este espacio de coordenadas, el eje X apunta hacia la derecha, y apunta hacia arriba y a la Z.</span><span class="sxs-lookup"><span data-stu-id="2b84d-109">In this coordinate space the X axis points right, Y points up and Z points away from camera.</span></span>

<span data-ttu-id="2b84d-110">Puede deshabilitar la rasterización indicando a la canalización que no hay ningún sombreador de píxeles (establezca la fase del sombreador de píxeles en **null** con [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) y deshabilite la prueba de profundidad y estarcido (establezca **DepthEnable** y **StencilEnable** en **false** en [**D3D11 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span><span class="sxs-lookup"><span data-stu-id="2b84d-110">You may disable rasterization by telling the pipeline there is no pixel shader (set the pixel shader stage to **NULL** with [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)), and disabling depth and stencil testing (set **DepthEnable** and **StencilEnable** to **FALSE** in [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).</span></span> <span data-ttu-id="2b84d-111">Mientras estén deshabilitadas, los contadores de la canalización relacionados con la rasterización no se actualizarán.</span><span class="sxs-lookup"><span data-stu-id="2b84d-111">While disabled, rasterization-related pipeline counters will not update.</span></span> <span data-ttu-id="2b84d-112">También hay una descripción completa de las [reglas de rasterización](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span><span class="sxs-lookup"><span data-stu-id="2b84d-112">There is also a complete description of the [rasterization rules](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).</span></span>

<span data-ttu-id="2b84d-113">En el hardware que implementa las optimizaciones jerárquicas del búfer Z, puede habilitar la carga previa del búfer z Si establece la fase del sombreador de píxeles en **null** mientras habilita las pruebas de profundidad y estarcido.</span><span class="sxs-lookup"><span data-stu-id="2b84d-113">On hardware that implements hierarchical Z-buffer optimizations, you may enable preloading the z-buffer by setting the pixel shader stage to **NULL** while enabling depth and stencil testing.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="2b84d-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2b84d-114">In this section</span></span>



| <span data-ttu-id="2b84d-115">Tema</span><span class="sxs-lookup"><span data-stu-id="2b84d-115">Topic</span></span>                                                                                                                         | <span data-ttu-id="2b84d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2b84d-116">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b84d-117">Introducción con la fase de rasterizador</span><span class="sxs-lookup"><span data-stu-id="2b84d-117">Getting Started with the Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | <span data-ttu-id="2b84d-118">En esta sección se describe la configuración de la ventanilla, el rectángulo de tijeras, el estado de rasterizador y el muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="2b84d-118">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="2b84d-119">Reglas de rasterización</span><span class="sxs-lookup"><span data-stu-id="2b84d-119">Rasterization Rules</span></span>](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | <span data-ttu-id="2b84d-120">Las reglas de rasterización definen cómo se asignan los datos vectoriales a los datos de tramas.</span><span class="sxs-lookup"><span data-stu-id="2b84d-120">Rasterization rules define how vector data is mapped into raster data.</span></span> <span data-ttu-id="2b84d-121">Los datos de trama se ajustan a las ubicaciones de enteros que se seleccionan y recortan (para dibujar el número mínimo de píxeles), y los atributos por píxel se interpolan (a partir de los atributos por vértice) antes de que se pasen a un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2b84d-121">The raster data is snapped to integer locations that are then culled and clipped (to draw the minimum number of pixels), and per-pixel attributes are interpolated (from per-vertex attributes) before being passed to a pixel shader.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2b84d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b84d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b84d-123">Canalización de gráficos</span><span class="sxs-lookup"><span data-stu-id="2b84d-123">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="2b84d-124">Fases de canalización (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="2b84d-124">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

