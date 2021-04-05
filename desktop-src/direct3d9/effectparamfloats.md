---
description: Define los números de punto flotante de efecto. Esta plantilla reemplaza la plantilla EffectFloats.
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079949"
---
# <a name="effectparamfloats"></a><span data-ttu-id="53a3c-104">EffectParamFloats</span><span class="sxs-lookup"><span data-stu-id="53a3c-104">EffectParamFloats</span></span>

<span data-ttu-id="53a3c-105">Define los números de punto flotante de efecto.</span><span class="sxs-lookup"><span data-stu-id="53a3c-105">Defines effect floating-point numbers.</span></span> <span data-ttu-id="53a3c-106">Esta plantilla reemplaza la plantilla [**EffectFloats**](effectfloats.md) .</span><span class="sxs-lookup"><span data-stu-id="53a3c-106">This template replaces the [**EffectFloats**](effectfloats.md) template.</span></span>

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

<span data-ttu-id="53a3c-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="53a3c-107">Where:</span></span>

-   <span data-ttu-id="53a3c-108">ParamName: nombre de la matriz de floats.</span><span class="sxs-lookup"><span data-stu-id="53a3c-108">ParamName - Name of the array of floats.</span></span>
-   <span data-ttu-id="53a3c-109">nFloats: número de valores de punto flotante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="53a3c-109">nFloats - Number of floating-point values in the array.</span></span>
-   <span data-ttu-id="53a3c-110">Flota \[ nFloats \] : matriz de valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="53a3c-110">Floats\[nFloats\] - Array of floating-point values.</span></span>

## <a name="see-also"></a><span data-ttu-id="53a3c-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="53a3c-111">See also</span></span>

<dl> <dt>

<span data-ttu-id="53a3c-112">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="53a3c-112">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> </dl>

 

 



