---
description: Una declaración de vértice define el diseño del búfer de vértices y programa el motor de teselación.
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: Declaración de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714687"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="f72e6-103">Declaración de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="f72e6-104">Una declaración de vértice define el diseño del búfer de vértices y programa el motor de teselación.</span><span class="sxs-lookup"><span data-stu-id="f72e6-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="f72e6-105">A partir de Direct3D 9, los flujos de vértices se expresan como una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) (en lugar de usar códigos de formato de vértice flexible (FVF)).</span><span class="sxs-lookup"><span data-stu-id="f72e6-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="f72e6-106">Cada elemento de la matriz describe cada tipo de datos por vértice.</span><span class="sxs-lookup"><span data-stu-id="f72e6-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="f72e6-107">En los temas siguientes se describe cómo convertir códigos de> de FVF en el nuevo formato:</span><span class="sxs-lookup"><span data-stu-id="f72e6-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="f72e6-108">Asignación de códigos FVF a una declaración de Direct3D 9 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="f72e6-109">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="f72e6-110">Asignación entre una declaración de Direct3D y códigos de FVF (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="f72e6-111">Asignación entre una declaración de Direct3D 9 y una declaración de Direct3D 8 (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="f72e6-112">Programar una o más secuencias (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f72e6-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="f72e6-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f72e6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f72e6-114">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="f72e6-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



