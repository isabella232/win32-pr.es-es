---
description: Define las coordenadas de textura de una malla.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: MeshTextureCoords
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974ec31f4358578277cfac46dc014f34752df46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805305"
---
# <a name="meshtexturecoords"></a><span data-ttu-id="29492-103">MeshTextureCoords</span><span class="sxs-lookup"><span data-stu-id="29492-103">MeshTextureCoords</span></span>

<span data-ttu-id="29492-104">Define las coordenadas de textura de una malla.</span><span class="sxs-lookup"><span data-stu-id="29492-104">Defines a mesh's texture coordinates.</span></span>

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

<span data-ttu-id="29492-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="29492-105">Where:</span></span>

-   <span data-ttu-id="29492-106">nTextureCoords: número de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="29492-106">nTextureCoords - Number of texture coordinates.</span></span>
-   <span data-ttu-id="29492-107">array Coords2d textureCoords \[ nTextureCoords \] : matriz de coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="29492-107">array Coords2d textureCoords\[nTextureCoords\] - Array of 2D texture coordinates.</span></span> <span data-ttu-id="29492-108">Vea [**Coords2d**](coords2d.md).</span><span class="sxs-lookup"><span data-stu-id="29492-108">See [**Coords2d**](coords2d.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="29492-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="29492-109">See also</span></span>

<dl> <dt>

<span data-ttu-id="29492-110">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="29492-110">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



