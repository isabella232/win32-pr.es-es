---
description: Define las normales para una malla.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274735"
---
# <a name="meshnormals"></a><span data-ttu-id="03dab-103">MeshNormals</span><span class="sxs-lookup"><span data-stu-id="03dab-103">MeshNormals</span></span>

<span data-ttu-id="03dab-104">Define las normales para una malla.</span><span class="sxs-lookup"><span data-stu-id="03dab-104">Defines normals for a mesh.</span></span> <span data-ttu-id="03dab-105">La primera matriz de vectores son los vectores normales y la segunda matriz es una matriz de índices que especifican qué normales se deben aplicar a una cara determinada.</span><span class="sxs-lookup"><span data-stu-id="03dab-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="03dab-106">El valor del miembro nFaceNormals debe ser igual al número de caras de una malla.</span><span class="sxs-lookup"><span data-stu-id="03dab-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

<span data-ttu-id="03dab-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="03dab-107">Where:</span></span>

-   <span data-ttu-id="03dab-108">nNormals: número de normales.</span><span class="sxs-lookup"><span data-stu-id="03dab-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="03dab-109">Vector de matriz normaliza \[ nNormals \] : matriz de normales.</span><span class="sxs-lookup"><span data-stu-id="03dab-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="03dab-110">Consulte [**Vector**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="03dab-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="03dab-111">nFaceNormals: número de normales de caras.</span><span class="sxs-lookup"><span data-stu-id="03dab-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="03dab-112">array MeshFace faceNormals \[ nFaceNormals \] : matriz de normales de cara de malla.</span><span class="sxs-lookup"><span data-stu-id="03dab-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="03dab-113">Vea [**MeshFace**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="03dab-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="03dab-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="03dab-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="03dab-115">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="03dab-115">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



