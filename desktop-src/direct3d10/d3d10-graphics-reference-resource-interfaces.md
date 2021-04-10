---
description: 'Direct3D 10 define un número de interfaces para los dos tipos básicos de recursos: búferes y texturas.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfaces de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153014"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="213f7-103">Interfaces de recursos (gráficos de Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="213f7-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="213f7-104">Direct3D 10 define un número de interfaces para los dos tipos básicos de recursos: [búferes](d3d10-graphics-programming-guide-resources-types.md) y texturas.</span><span class="sxs-lookup"><span data-stu-id="213f7-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="213f7-105">Interfaces</span><span class="sxs-lookup"><span data-stu-id="213f7-105">Interfaces</span></span>                                           | <span data-ttu-id="213f7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="213f7-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="213f7-107">**Interfaz ID3D10Buffer**</span><span class="sxs-lookup"><span data-stu-id="213f7-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="213f7-108">Obtiene acceso a los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="213f7-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="213f7-109">**Interfaz ID3D10Resource**</span><span class="sxs-lookup"><span data-stu-id="213f7-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="213f7-110">Clase base de un recurso.</span><span class="sxs-lookup"><span data-stu-id="213f7-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="213f7-111">**Interfaz ID3D10Texture1D**</span><span class="sxs-lookup"><span data-stu-id="213f7-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="213f7-112">Obtiene acceso a los datos de una textura 1D o de una matriz de textura 1D.</span><span class="sxs-lookup"><span data-stu-id="213f7-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="213f7-113">**Interfaz ID3D10Texture2D**</span><span class="sxs-lookup"><span data-stu-id="213f7-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="213f7-114">Obtiene acceso a los datos de una textura 2D o de una matriz de textura 2D</span><span class="sxs-lookup"><span data-stu-id="213f7-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="213f7-115">**Interfaz ID3D10Texture3D**</span><span class="sxs-lookup"><span data-stu-id="213f7-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="213f7-116">Obtiene acceso a los datos de una textura 3D o de una matriz de textura 3D.</span><span class="sxs-lookup"><span data-stu-id="213f7-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="213f7-117">Una aplicación utiliza una vista para enlazar un recurso a una [fase de canalización](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="213f7-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="213f7-118">La [vista](d3d10-graphics-programming-guide-resources-access-views.md) define cómo se puede tener acceso al recurso durante la representación.</span><span class="sxs-lookup"><span data-stu-id="213f7-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="213f7-119">La API contiene estas interfaces de vista.</span><span class="sxs-lookup"><span data-stu-id="213f7-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="213f7-120">Interfaces</span><span class="sxs-lookup"><span data-stu-id="213f7-120">Interfaces</span></span>                                                               | <span data-ttu-id="213f7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="213f7-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="213f7-122">**Interfaz ID3D10DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="213f7-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="213f7-123">Obtiene acceso a los datos en una textura [de estarcido de profundidad](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) .</span><span class="sxs-lookup"><span data-stu-id="213f7-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="213f7-124">**Interfaz ID3D10RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="213f7-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="213f7-125">Obtiene acceso a los datos de un [destino de representación](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="213f7-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="213f7-126">**Interfaz ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="213f7-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="213f7-127">Obtiene acceso a los datos de un sombreador-Resource en Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="213f7-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="213f7-128">**Interfaz ID3D10ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="213f7-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="213f7-129">Obtiene acceso a los datos de un sombreador-Resource en Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="213f7-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="213f7-130">**Interfaz ID3D10View**</span><span class="sxs-lookup"><span data-stu-id="213f7-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="213f7-131">Clase base para una vista.</span><span class="sxs-lookup"><span data-stu-id="213f7-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="213f7-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="213f7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="213f7-133">Referencia de recursos</span><span class="sxs-lookup"><span data-stu-id="213f7-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
