---
description: Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel. Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje ensamblador, querrá escribir funciones.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Sintaxis de la función Effect (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536832"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="2b386-104">Sintaxis de la función Effect (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2b386-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="2b386-105">Una función es el bloque de creación de un sombreador creado en el lenguaje de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="2b386-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="2b386-106">Si prefiere escribir sombreadores en un lenguaje de estilo C en lugar de en lenguaje ensamblador, querrá escribir funciones.</span><span class="sxs-lookup"><span data-stu-id="2b386-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b386-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b386-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="2b386-108">Las funciones no cambian los valores de los parámetros de un efecto.</span><span class="sxs-lookup"><span data-stu-id="2b386-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="2b386-109">Type: cualquier [referencia válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) el tipo HLSL.</span><span class="sxs-lookup"><span data-stu-id="2b386-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="2b386-110">ID: un nombre único.</span><span class="sxs-lookup"><span data-stu-id="2b386-110">id - A unique name.</span></span>
-   <span data-ttu-id="2b386-111">parámetros: parámetros de función.</span><span class="sxs-lookup"><span data-stu-id="2b386-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="2b386-112">cuerpo: el cuerpo de la función.</span><span class="sxs-lookup"><span data-stu-id="2b386-112">body - The body of the function.</span></span>

<span data-ttu-id="2b386-113">Las funciones se compilan a partir del lenguaje de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="2b386-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="2b386-114">Consulte [referencia de HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2b386-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b386-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b386-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b386-116">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="2b386-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
