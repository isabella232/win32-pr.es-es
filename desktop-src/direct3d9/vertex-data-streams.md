---
description: Las interfaces de representación de Direct3D se componen de métodos que representan primitivos de los datos de vértice almacenados en uno o más búferes de datos.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flujos de datos de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805726"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="b8165-103">Flujos de datos de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b8165-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="b8165-104">Las interfaces de representación de Direct3D se componen de métodos que representan primitivos de los datos de vértice almacenados en uno o más búferes de datos.</span><span class="sxs-lookup"><span data-stu-id="b8165-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="b8165-105">Los datos de vértice se componen de elementos de vértice combinados para formar componentes de vértice.</span><span class="sxs-lookup"><span data-stu-id="b8165-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="b8165-106">Los elementos de vértice, la unidad más pequeña de un vértice, representan entidades como posición, normal o color.</span><span class="sxs-lookup"><span data-stu-id="b8165-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="b8165-107">Los componentes de vértice son uno o más elementos de vértice almacenados de forma contigua (intercalados por vértice) en un búfer de memoria único.</span><span class="sxs-lookup"><span data-stu-id="b8165-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="b8165-108">Un vértice completo consta de uno o varios componentes, donde cada componente está en un búfer de memoria independiente.</span><span class="sxs-lookup"><span data-stu-id="b8165-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="b8165-109">Para representar un primitivo, se leen y ensamblan varios componentes de vértice para que los vértices completos estén disponibles para el procesamiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="b8165-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="b8165-110">En el diagrama siguiente se muestra el proceso de representación de primitivas mediante componentes de vértices.</span><span class="sxs-lookup"><span data-stu-id="b8165-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![diagrama del proceso para representar primitivas mediante componentes de vértice](images/vertexdata.png)

<span data-ttu-id="b8165-112">La representación de primitivas consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="b8165-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="b8165-113">En primer lugar, configure uno o varios flujos de componentes de vértices; en segundo lugar, invoque un método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) para representarlo desde esos flujos.</span><span class="sxs-lookup"><span data-stu-id="b8165-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="b8165-114">La identificación de los elementos de vértice dentro de estos flujos de componentes se especifica mediante el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="b8165-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="b8165-115">Los métodos [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) especifican un desplazamiento en los flujos de datos de vértices para que se pueda representar un subconjunto contiguo arbitrario de los primitivos dentro de un conjunto de datos de vértices con cada invocación de dibujo.</span><span class="sxs-lookup"><span data-stu-id="b8165-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="b8165-116">Esto le permite cambiar el estado de representación del dispositivo entre grupos de primitivas que se representan a partir de los mismos búferes de vértices.</span><span class="sxs-lookup"><span data-stu-id="b8165-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="b8165-117">Se admiten los métodos de dibujo indexados y no indexados.</span><span class="sxs-lookup"><span data-stu-id="b8165-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="b8165-118">Para obtener más información, vea [representar a partir de búferes de vértices y de índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="b8165-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8165-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8165-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8165-120">Representación de primitivas</span><span class="sxs-lookup"><span data-stu-id="b8165-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
