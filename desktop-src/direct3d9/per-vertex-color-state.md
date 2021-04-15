---
description: El motor de iluminación de Direct3D puede usar los datos de color por vértice al realizar la iluminación si se indica al tiempo de ejecución que los datos están presentes.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex estado de color (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422748"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="9a9ab-103">Per-Vertex estado de color (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9a9ab-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="9a9ab-104">El motor de iluminación de Direct3D puede usar los datos de color por vértice al realizar la iluminación si se indica al tiempo de ejecución que los datos están presentes.</span><span class="sxs-lookup"><span data-stu-id="9a9ab-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="9a9ab-105">Esto se realiza activando el siguiente estado de representación:</span><span class="sxs-lookup"><span data-stu-id="9a9ab-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="9a9ab-106">Si el color por vértice está habilitado, las aplicaciones pueden configurar el origen desde el que el sistema recupera la información de color de un vértice.</span><span class="sxs-lookup"><span data-stu-id="9a9ab-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="9a9ab-107">Los \_ Estados de representación D3DRS AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE controlan los orígenes de componentes de color ambiente, difuso, emisor y especular, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9a9ab-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="9a9ab-108">Cada Estado se puede establecer en los miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) , que define las constantes que indican al sistema que utilice el material actual, el color difuso o el color especular como origen para el componente de color especificado.</span><span class="sxs-lookup"><span data-stu-id="9a9ab-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a9ab-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a9ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a9ab-110">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="9a9ab-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
