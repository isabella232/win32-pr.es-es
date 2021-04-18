---
description: Se usa en un objeto Mesh para especificar qué material se aplica a qué caras. El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican el material que se va a aplicar.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714667"
---
# <a name="meshmateriallist"></a><span data-ttu-id="14b78-104">MeshMaterialList</span><span class="sxs-lookup"><span data-stu-id="14b78-104">MeshMaterialList</span></span>

<span data-ttu-id="14b78-105">Se usa en un objeto Mesh para especificar qué material se aplica a qué caras.</span><span class="sxs-lookup"><span data-stu-id="14b78-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="14b78-106">El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican el material que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="14b78-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="14b78-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="14b78-107">Where:</span></span>

-   <span data-ttu-id="14b78-108">nMaterials: un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="14b78-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="14b78-109">El número de materiales.</span><span class="sxs-lookup"><span data-stu-id="14b78-109">The number of materials.</span></span>
-   <span data-ttu-id="14b78-110">nFaceIndexes: un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="14b78-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="14b78-111">Número de índices.</span><span class="sxs-lookup"><span data-stu-id="14b78-111">The number of indices.</span></span>
-   <span data-ttu-id="14b78-112">faceIndexes \[ nFaceIndexes \] : una matriz de DWORD que contiene los índices de caras.</span><span class="sxs-lookup"><span data-stu-id="14b78-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="14b78-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="14b78-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="14b78-114">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="14b78-114">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



