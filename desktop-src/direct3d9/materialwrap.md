---
description: Define un conjunto de dos valores booleanos que se usan en la plantilla MeshFaceWraps para definir la topología de textura de una sola persona. Use en lugar de Boolean2d cuando las coordenadas de textura (u, v) abarquen el intervalo de 0 a 2 en lugar de 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714690"
---
# <a name="materialwrap"></a><span data-ttu-id="41f4a-104">MaterialWrap</span><span class="sxs-lookup"><span data-stu-id="41f4a-104">MaterialWrap</span></span>

<span data-ttu-id="41f4a-105">Define un conjunto de dos valores booleanos que se usan en la plantilla [**MeshFaceWraps**](meshfacewraps.md) para definir la topología de textura de una sola persona.</span><span class="sxs-lookup"><span data-stu-id="41f4a-105">Defines a set of two Boolean values used in the [**MeshFaceWraps**](meshfacewraps.md) template to define the texture topology of an individual face.</span></span> <span data-ttu-id="41f4a-106">Use en lugar de [**Boolean2d**](boolean2d.md) cuando las coordenadas de textura (u, v) abarquen el intervalo de 0 a 2 en lugar de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="41f4a-106">Use instead of [**Boolean2d**](boolean2d.md) when the texture coordinates (u, v) span the range of 0 to 2 instead of 0 to 1.</span></span>

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

<span data-ttu-id="41f4a-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="41f4a-107">Where:</span></span>

-   <span data-ttu-id="41f4a-108">valor u-booleano.</span><span class="sxs-lookup"><span data-stu-id="41f4a-108">u - Boolean value.</span></span> <span data-ttu-id="41f4a-109">Vea [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="41f4a-109">See [**Boolean**](boolean.md).</span></span>
-   <span data-ttu-id="41f4a-110">valor booleano v.</span><span class="sxs-lookup"><span data-stu-id="41f4a-110">v - Boolean value.</span></span> <span data-ttu-id="41f4a-111">Vea [**Boolean**](boolean.md).</span><span class="sxs-lookup"><span data-stu-id="41f4a-111">See [**Boolean**](boolean.md).</span></span>

> [!Note]  
> <span data-ttu-id="41f4a-112">Ya no se usa la plantilla [**MeshFaceWraps**](meshfacewraps.md) .</span><span class="sxs-lookup"><span data-stu-id="41f4a-112">The [**MeshFaceWraps**](meshfacewraps.md) template is no longer used.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="41f4a-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="41f4a-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="41f4a-114">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="41f4a-114">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



