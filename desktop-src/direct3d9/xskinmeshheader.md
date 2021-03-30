---
description: Se crea una instancia de esta plantilla por cada malla solo en mallas que contienen información de la piel exportada. La finalidad de esta plantilla es proporcionar información sobre la naturaleza de la información de la piel que se exportó.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423052"
---
# <a name="xskinmeshheader"></a><span data-ttu-id="22754-104">XSkinMeshHeader</span><span class="sxs-lookup"><span data-stu-id="22754-104">XSkinMeshHeader</span></span>

<span data-ttu-id="22754-105">Se crea una instancia de esta plantilla por cada malla solo en mallas que contienen información de la piel exportada.</span><span class="sxs-lookup"><span data-stu-id="22754-105">This template is instantiated on a per-mesh basis only in meshes that contain exported skinning information.</span></span> <span data-ttu-id="22754-106">La finalidad de esta plantilla es proporcionar información sobre la naturaleza de la información de la piel que se exportó.</span><span class="sxs-lookup"><span data-stu-id="22754-106">The purpose of this template is to provide information about the nature of the skinning information that was exported.</span></span>

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

<span data-ttu-id="22754-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="22754-107">Where:</span></span>

-   <span data-ttu-id="22754-108">nMaxSkinWeightsPerVertex: número máximo de transformaciones que afectan a un vértice en la malla.</span><span class="sxs-lookup"><span data-stu-id="22754-108">nMaxSkinWeightsPerVertex - Maximum number of transforms that affect a vertex in the mesh.</span></span>
-   <span data-ttu-id="22754-109">nMaxSkinWeightsPerFace: número máximo de transformaciones únicas que afectan a los tres vértices de cualquier aspecto.</span><span class="sxs-lookup"><span data-stu-id="22754-109">nMaxSkinWeightsPerFace - Maximum number of unique transforms that affect the three vertices of any face.</span></span>
-   <span data-ttu-id="22754-110">nBones: número de huesos que afectan a los vértices de esta malla.</span><span class="sxs-lookup"><span data-stu-id="22754-110">nBones - Number of bones that affect vertices in this mesh.</span></span>

## <a name="see-also"></a><span data-ttu-id="22754-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="22754-111">See also</span></span>

<dl> <dt>

<span data-ttu-id="22754-112">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="22754-112">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



