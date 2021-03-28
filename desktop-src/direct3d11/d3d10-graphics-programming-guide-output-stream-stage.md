---
title: Stream-Output fase
description: El propósito de la fase de salida de flujo es la salida continua (o secuencia) de datos de vértices de la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) en uno o varios búferes de la memoria (vea Introducción con la fase Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- fase de salida de flujo (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488573"
---
# <a name="stream-output-stage"></a><span data-ttu-id="e2e2e-104">Stream-Output fase</span><span class="sxs-lookup"><span data-stu-id="e2e2e-104">Stream-Output Stage</span></span>

<span data-ttu-id="e2e2e-105">El propósito de la fase de salida de flujo es la salida continua (o secuencia) de datos de vértices de la fase del sombreador de geometría (o la fase del sombreador de vértices si la fase del sombreador de geometría está inactiva) en uno o varios búferes de la memoria (vea [Introducción con la fase Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="e2e2e-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="e2e2e-106">La fase de salida de flujo (para) se encuentra en la canalización justo después de la fase de sombreador de geometría y justo antes de la fase de rasterización, como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![diagrama de la ubicación de la fase de salida de flujo en la canalización](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="e2e2e-108">Los datos que se transmiten a la memoria se pueden volver a leer en la canalización en una fase de representación subsiguiente, o bien se pueden copiar en un recurso de almacenamiento provisional (de modo que la CPU pueda leerlos).</span><span class="sxs-lookup"><span data-stu-id="e2e2e-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="e2e2e-109">La cantidad de datos transmitidos puede variar; la API [**ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) está diseñada para controlar los datos sin necesidad de consultar (la GPU) la cantidad de datos escritos.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="e2e2e-110">Cuando un triángulo o una franja de líneas está enlazada a la fase del ensamblador de entrada, cada franja se convierte en una lista antes de que se transmitan. Los vértices siempre se escriben como tipos primitivos completos (por ejemplo, 3 vértices a la vez para triángulos). los primitivos incompletos nunca se transmiten por secuencias. Los tipos primitivos con adyacencias descartan los datos de adyacencia antes de la transmisión de datos.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="e2e2e-111">Hay dos maneras de alimentar los datos de salida de flujo en la canalización:</span><span class="sxs-lookup"><span data-stu-id="e2e2e-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="e2e2e-112">Los datos de salida de flujo se pueden volver a alimentar en la fase de ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="e2e2e-113">Los datos de salida de flujo se pueden leer mediante sombreadores programables mediante funciones de carga (como la [carga](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span><span class="sxs-lookup"><span data-stu-id="e2e2e-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="e2e2e-114">Para usar un búfer como un recurso de salida de flujo, cree el búfer con la marca de [**\_ salida de \_ flujo \_ de enlace D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="e2e2e-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="e2e2e-115">La fase Stream-Output admite hasta 4 búferes simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="e2e2e-116">Si está transmitiendo datos en varios búferes, cada búfer solo puede capturar un único elemento (hasta 4 componentes) de datos por vértice, con un intervalo de datos implícito igual al ancho del elemento en cada búfer (compatible con la forma en que se pueden enlazar los búferes de un solo elemento para la entrada en fases del sombreador).</span><span class="sxs-lookup"><span data-stu-id="e2e2e-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="e2e2e-117">Además, si los búferes tienen tamaños diferentes, la escritura se detiene en cuanto uno de los búferes esté lleno.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="e2e2e-118">Si está transmitiendo datos en un solo búfer, el búfer puede capturar hasta 64 componentes escalares de datos por vértice (256 bytes o menos) o el intervalo de vértices puede tener hasta 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e2e2e-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e2e2e-119">In this section</span></span>



| <span data-ttu-id="e2e2e-120">Tema</span><span class="sxs-lookup"><span data-stu-id="e2e2e-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="e2e2e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2e2e-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2e2e-122">Introducción con la fase de Stream-Output</span><span class="sxs-lookup"><span data-stu-id="e2e2e-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="e2e2e-123">En esta sección se describe cómo usar un sombreador de geometría con la fase de salida de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e2e2e-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e2e2e-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2e2e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2e2e-125">Canalización de gráficos</span><span class="sxs-lookup"><span data-stu-id="e2e2e-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="e2e2e-126">Fases de canalización (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e2e2e-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

