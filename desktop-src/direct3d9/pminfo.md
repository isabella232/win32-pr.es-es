---
description: 'PMInfo: no compatible. DirectX lo usa internamente.'
ms.assetid: 8a07357f-d4e8-4104-9d21-51c3e8b8d6d2
title: PMInfo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cfc0edb59d22a14ca5ffefbded3a8c830161c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090177"
---
# <a name="pminfo"></a><span data-ttu-id="51e1b-104">PMInfo</span><span class="sxs-lookup"><span data-stu-id="51e1b-104">PMInfo</span></span>

<span data-ttu-id="51e1b-105">No compatible.</span><span class="sxs-lookup"><span data-stu-id="51e1b-105">Not supported.</span></span> <span data-ttu-id="51e1b-106">DirectX lo usa internamente.</span><span class="sxs-lookup"><span data-stu-id="51e1b-106">Used internally by DirectX.</span></span>

``` syntax
template PMInfo 
{ 
    < B6C3E656-EC8B-4b92-9B62-681659522947 > 
    DWORD nAttributes; 
    array PMAttributeRange attributeRanges[nAttributes]; 
    DWORD nMaxValence; 
    DWORD nMinLogicalVertices; 
    DWORD nMaxLogicalVertices; 
    DWORD nVSplits; 
    array PMVSplitRecord splitRecords[nVSplits]; 
    DWORD nAttributeMispredicts; 
    array DWORD attributeMispredicts[nAttributeMispredicts]; 
}
```

## <a name="see-also"></a><span data-ttu-id="51e1b-107">Consulte también</span><span class="sxs-lookup"><span data-stu-id="51e1b-107">See also</span></span>

<dl> <dt>

<span data-ttu-id="51e1b-108">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="51e1b-108">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



