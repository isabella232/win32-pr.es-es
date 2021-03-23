---
title: Uso de descriptores directamente en la firma raíz
description: Las aplicaciones pueden poner descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/15/2020
ms.locfileid: "104549174"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="c9629-103">Uso de descriptores directamente en la firma raíz</span><span class="sxs-lookup"><span data-stu-id="c9629-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="c9629-104">Las aplicaciones pueden poner descriptores directamente en la firma raíz para evitar tener que pasar por un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="c9629-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="c9629-105">Estos descriptores ocupan mucho espacio en la firma raíz (consulte la sección límites de la firma raíz), por lo que las aplicaciones tienen que usarlos con moderación.</span><span class="sxs-lookup"><span data-stu-id="c9629-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="c9629-106">Un uso de ejemplo sería poner una vista de búfer de constantes (CBV) que cambie por dibujo en el diseño raíz para que no sea necesario que la aplicación asigne espacio en el montón de descriptores (y guarde el puntero a una tabla de descriptores en la nueva ubicación del montón de descriptores).</span><span class="sxs-lookup"><span data-stu-id="c9629-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="c9629-107">Al colocar algo en la firma raíz, la aplicación simplemente está entregando la responsabilidad de control de versiones al controlador, pero se trata de una infraestructura que ya tiene.</span><span class="sxs-lookup"><span data-stu-id="c9629-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="c9629-108">En el caso de la representación que usa muy pocos recursos, es posible que no sea necesario usar el uso de la tabla de descriptores o del montón si todos los descriptores necesarios se pueden colocar directamente en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="c9629-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="c9629-109">Los únicos tipos de descriptores que se admiten en la firma raíz son:</span><span class="sxs-lookup"><span data-stu-id="c9629-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="c9629-110">CBVs.</span><span class="sxs-lookup"><span data-stu-id="c9629-110">CBVs.</span></span>
- <span data-ttu-id="c9629-111">Vistas de recursos del sombreador (SRVs)/Unordered vistas de acceso (UAVs) de recursos de búfer en los que el formato SRV/UAV contiene solo componentes FLOAT/UINT/SINT de 32 bits (no hay conversión de formato).</span><span class="sxs-lookup"><span data-stu-id="c9629-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="c9629-112">SRVs de estructuras de aceleración de raytracing, en firmas de raíz locales o globales.</span><span class="sxs-lookup"><span data-stu-id="c9629-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="c9629-113">UAVs en la raíz no puede tener contadores asociados.</span><span class="sxs-lookup"><span data-stu-id="c9629-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="c9629-114">Los descriptores de la firma raíz aparecen cada uno como descriptores independientes individuales &mdash; que no se pueden indexar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="c9629-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="c9629-115">En el ejemplo anterior, `mySceneData` no se puede declarar como una matriz, como en si se va `cbuffer mySceneData[2]` a asignar a un descriptor en la firma raíz, ya que la indización en los descriptores no se admite en la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="c9629-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="c9629-116">La aplicación puede definir búferes de constantes individuales independientes y definirlos como una entrada independiente en la firma raíz si se desea.</span><span class="sxs-lookup"><span data-stu-id="c9629-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="c9629-117">Tenga en cuenta que, dentro de `mySceneData` lo anterior, hay una matriz `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="c9629-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="c9629-118">La indexación dinámica dentro del búfer de constantes es válida: un descriptor de la signatura raíz se comporta igual que el mismo descriptor si se obtiene acceso a él a través de un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="c9629-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="c9629-119">Esto contrasta con las constantes de inserción directamente en la firma raíz, que también aparece como un búfer de constantes excepto con la restricción de que no se permite la indexación dinámica dentro de las constantes insertadas, por lo que `bar[2]` no se permitiría allí.</span><span class="sxs-lookup"><span data-stu-id="c9629-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="c9629-120">Las siguientes API (de la interfaz [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) son para establecer los descriptores directamente en la firma raíz:</span><span class="sxs-lookup"><span data-stu-id="c9629-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="c9629-121">**SetComputeRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="c9629-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="c9629-122">**SetGraphicsRootConstantBufferView**</span><span class="sxs-lookup"><span data-stu-id="c9629-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="c9629-123">**SetComputeRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c9629-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="c9629-124">**SetGraphicsRootShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="c9629-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="c9629-125">**SetComputeRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c9629-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="c9629-126">**SetGraphicsRootUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="c9629-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="c9629-127">No hay ningún concepto de "matriz de descriptores raíz" en Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c9629-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="c9629-128">Las matrices de descriptor solo se admiten en montones de descriptor.</span><span class="sxs-lookup"><span data-stu-id="c9629-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9629-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9629-129">Related topics</span></span>

[<span data-ttu-id="c9629-130">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="c9629-130">Root Signatures</span></span>](root-signatures.md)
