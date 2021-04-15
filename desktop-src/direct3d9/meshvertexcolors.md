---
description: Especifica los colores de los vértices de una malla, en lugar de aplicar un material por caras o por malla.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: MeshVertexColors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422825"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="677e9-103">MeshVertexColors</span><span class="sxs-lookup"><span data-stu-id="677e9-103">MeshVertexColors</span></span>

<span data-ttu-id="677e9-104">Especifica los colores de los vértices de una malla, en lugar de aplicar un material por caras o por malla.</span><span class="sxs-lookup"><span data-stu-id="677e9-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="677e9-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="677e9-105">Where:</span></span>

-   <span data-ttu-id="677e9-106">nVertexColors: número de colores.</span><span class="sxs-lookup"><span data-stu-id="677e9-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="677e9-107">Coincide con el número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="677e9-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="677e9-108">array IndexColor vertexColors \[ nVertexColors \] : matriz de colores indexados.</span><span class="sxs-lookup"><span data-stu-id="677e9-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="677e9-109">Vea [**IndexedColor**](indexedcolor.md).</span><span class="sxs-lookup"><span data-stu-id="677e9-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="677e9-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="677e9-110">See also</span></span>

<dl> <dt>

<span data-ttu-id="677e9-111">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="677e9-111">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



