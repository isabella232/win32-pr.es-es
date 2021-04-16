---
description: Define una malla simple. La primera matriz es una lista de vértices y la segunda matriz define las caras de la malla mediante la indexación en la matriz de vértices.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: En malla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494278"
---
# <a name="mesh"></a><span data-ttu-id="a2f72-104">En malla</span><span class="sxs-lookup"><span data-stu-id="a2f72-104">Mesh</span></span>

<span data-ttu-id="a2f72-105">Define una malla simple.</span><span class="sxs-lookup"><span data-stu-id="a2f72-105">Defines a simple mesh.</span></span> <span data-ttu-id="a2f72-106">La primera matriz es una lista de vértices y la segunda matriz define las caras de la malla mediante la indexación en la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="a2f72-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

<span data-ttu-id="a2f72-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="a2f72-107">Where:</span></span>

-   <span data-ttu-id="a2f72-108">nVertices: número de vértices.</span><span class="sxs-lookup"><span data-stu-id="a2f72-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="a2f72-109">los vértices del vector de matriz \[ nVertices \] -matriz de vértices, cada uno de tipo vector.</span><span class="sxs-lookup"><span data-stu-id="a2f72-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="a2f72-110">Consulte [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="a2f72-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="a2f72-111">nFaces: número de caras.</span><span class="sxs-lookup"><span data-stu-id="a2f72-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="a2f72-112">array MeshFace Face \[ nFaces \] -Array of Faces, cada una de tipo MeshFace.</span><span class="sxs-lookup"><span data-stu-id="a2f72-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="a2f72-113">Vea [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="a2f72-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="a2f72-114">\[ ... \] -Aquí puede usarse cualquier plantilla de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="a2f72-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="a2f72-115">Esto hace que la arquitectura sea extensible.</span><span class="sxs-lookup"><span data-stu-id="a2f72-115">This makes the architecture extensible.</span></span> <span data-ttu-id="a2f72-116">Normalmente se usan plantillas de [**material**](material.md) y [**TextureFilename**](texturefilename.md) .</span><span class="sxs-lookup"><span data-stu-id="a2f72-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2f72-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2f72-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2f72-118">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="a2f72-118">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



