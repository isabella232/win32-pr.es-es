---
description: Define un conjunto de claves de animación. Una clave de matriz es útil para los conjuntos de datos de animación que deben representarse como matrices de transformación.
ms.assetid: bf007541-7fea-423e-910b-fa5f45271608
title: AnimationKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05728f124ae01962a1291547f8fe8b7fcebd175a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705337"
---
# <a name="animationkey"></a><span data-ttu-id="f4f56-104">AnimationKey</span><span class="sxs-lookup"><span data-stu-id="f4f56-104">AnimationKey</span></span>

<span data-ttu-id="f4f56-105">Define un conjunto de claves de animación.</span><span class="sxs-lookup"><span data-stu-id="f4f56-105">Defines a set of animation keys.</span></span> <span data-ttu-id="f4f56-106">Una clave de matriz es útil para los conjuntos de datos de animación que deben representarse como matrices de transformación.</span><span class="sxs-lookup"><span data-stu-id="f4f56-106">A matrix key is useful for sets of animation data that need to be represented as transformation matrices.</span></span>

``` syntax
template AnimationKey
{
    < 10DD46A8-775B-11CF-8F52-0040333594A3 >
    DWORD keyType;
    DWORD nKeys;
    array TimedFloatKeys keys[nKeys];
} 
```

<span data-ttu-id="f4f56-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="f4f56-107">Where:</span></span>

-   <span data-ttu-id="f4f56-108">keyType: especifica si las claves son las claves de rotación, escala, posición o matriz (con los enteros 0, 1, 2 o 3, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="f4f56-108">keyType - Specifies whether the keys are rotation, scale, position, or matrix keys (using the integers 0, 1, 2, or 3, respectively).</span></span>
-   <span data-ttu-id="f4f56-109">nKeys: número de claves.</span><span class="sxs-lookup"><span data-stu-id="f4f56-109">nKeys - Number of keys.</span></span>
-   <span data-ttu-id="f4f56-110">Keys: una matriz de claves.</span><span class="sxs-lookup"><span data-stu-id="f4f56-110">keys - An array of keys.</span></span> <span data-ttu-id="f4f56-111">Vea [**TimedFloatKeys**](timedfloatkeys.md).</span><span class="sxs-lookup"><span data-stu-id="f4f56-111">See [**TimedFloatKeys**](timedfloatkeys.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f4f56-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4f56-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4f56-113">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="f4f56-113">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



