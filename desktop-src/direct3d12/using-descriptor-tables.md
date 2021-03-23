---
title: Usar tablas de descriptores
description: Las tablas de descriptores, cada una de las cuales identifican un intervalo en un montón de descriptores, se enlazan en las ranuras definidas por la firma raíz actual en una lista de comandos.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103667"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="f6523-103">Usar tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="f6523-103">Using Descriptor Tables</span></span>

<span data-ttu-id="f6523-104">Las tablas de descriptores, cada una de las cuales identifican un intervalo en un montón de descriptores, se enlazan en las ranuras definidas por la firma raíz actual en una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="f6523-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="f6523-105">Indexación de tablas de descriptor</span><span class="sxs-lookup"><span data-stu-id="f6523-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="f6523-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6523-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="f6523-107">Los sombreadores pueden buscar recursos a los que hacen referencia los descriptores que componen la tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="f6523-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="f6523-108">Otros enlaces de recursos: los búferes de índice, el búfer de vértices, los búferes de salida de secuencias, los destinos de representación y la galería de símbolos de profundidad se realizan directamente en una lista de comandos, en lugar de hacerlo a través de descriptores.</span><span class="sxs-lookup"><span data-stu-id="f6523-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="f6523-109">En resumen:</span><span class="sxs-lookup"><span data-stu-id="f6523-109">To summarize:</span></span>

<span data-ttu-id="f6523-110">Las referencias de recursos siguientes pueden compartir la misma tabla de descriptores y el montón:</span><span class="sxs-lookup"><span data-stu-id="f6523-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="f6523-111">Vistas de recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="f6523-111">Shader resource views</span></span>
-   <span data-ttu-id="f6523-112">Vistas de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="f6523-112">Unordered access views</span></span>
-   <span data-ttu-id="f6523-113">Vistas de búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="f6523-113">Constant buffer views</span></span>

<span data-ttu-id="f6523-114">Las siguientes referencias de recursos deben estar en su propio montón de descriptores:</span><span class="sxs-lookup"><span data-stu-id="f6523-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="f6523-115">Muestras</span><span class="sxs-lookup"><span data-stu-id="f6523-115">Samplers</span></span>

<span data-ttu-id="f6523-116">Los siguientes recursos no se colocan en tablas o montones de descriptores, pero se enlazan directamente mediante listas de comandos:</span><span class="sxs-lookup"><span data-stu-id="f6523-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="f6523-117">Búferes de índices</span><span class="sxs-lookup"><span data-stu-id="f6523-117">Index buffers</span></span>
-   <span data-ttu-id="f6523-118">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="f6523-118">Vertex buffers</span></span>
-   <span data-ttu-id="f6523-119">Búferes de salida de flujo</span><span class="sxs-lookup"><span data-stu-id="f6523-119">Stream output buffers</span></span>
-   <span data-ttu-id="f6523-120">Destinos de representación</span><span class="sxs-lookup"><span data-stu-id="f6523-120">Render targets</span></span>
-   <span data-ttu-id="f6523-121">Vistas de estarcido de profundidad</span><span class="sxs-lookup"><span data-stu-id="f6523-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="f6523-122">Indexación de tablas de descriptor</span><span class="sxs-lookup"><span data-stu-id="f6523-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="f6523-123">Los sombreadores no pueden indexar dinámicamente los límites de la tabla de descriptores de un sitio de llamada dado en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="f6523-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="f6523-124">Sin embargo, la selección de un descriptor dentro de una tabla de descriptores puede indexarse dinámicamente en el código del sombreador dentro de los intervalos del mismo tipo de descriptor (por ejemplo, la indexación en una región contigua de SRVs).</span><span class="sxs-lookup"><span data-stu-id="f6523-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6523-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6523-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6523-126">Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="f6523-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




