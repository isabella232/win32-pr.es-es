---
title: Registro temporal (referencia de PS de HLSL)
description: Los registros temporales de entrada del sombreador de píxeles se utilizan para almacenar resultados intermedios.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103904316"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="7624c-103">Registro temporal (referencia de PS de HLSL)</span><span class="sxs-lookup"><span data-stu-id="7624c-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="7624c-104">Los registros temporales de entrada del sombreador de píxeles se utilizan para almacenar resultados intermedios.</span><span class="sxs-lookup"><span data-stu-id="7624c-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="7624c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7624c-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="7624c-106">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7624c-106">Pixel shader versions</span></span> | <span data-ttu-id="7624c-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="7624c-107">1\_1</span></span> | <span data-ttu-id="7624c-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="7624c-108">1\_2</span></span> | <span data-ttu-id="7624c-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7624c-109">1\_3</span></span> | <span data-ttu-id="7624c-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="7624c-110">1\_4</span></span> | <span data-ttu-id="7624c-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7624c-111">2\_0</span></span> | <span data-ttu-id="7624c-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7624c-112">2\_sw</span></span> | <span data-ttu-id="7624c-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7624c-113">2\_x</span></span> | <span data-ttu-id="7624c-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7624c-114">3\_0</span></span> | <span data-ttu-id="7624c-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7624c-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="7624c-116">Registro temporal</span><span class="sxs-lookup"><span data-stu-id="7624c-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="7624c-117">x</span><span class="sxs-lookup"><span data-stu-id="7624c-117">x</span></span>    | <span data-ttu-id="7624c-118">x</span><span class="sxs-lookup"><span data-stu-id="7624c-118">x</span></span>     | <span data-ttu-id="7624c-119">x</span><span class="sxs-lookup"><span data-stu-id="7624c-119">x</span></span>    | <span data-ttu-id="7624c-120">x</span><span class="sxs-lookup"><span data-stu-id="7624c-120">x</span></span>    | <span data-ttu-id="7624c-121">x</span><span class="sxs-lookup"><span data-stu-id="7624c-121">x</span></span>     |



 

-   <span data-ttu-id="7624c-122">Hay 12 registros temporales del sombreador de píxeles: R0 a R11.</span><span class="sxs-lookup"><span data-stu-id="7624c-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="7624c-123">Estos registros se utilizan para almacenar resultados intermedios durante los cálculos.</span><span class="sxs-lookup"><span data-stu-id="7624c-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="7624c-124">Si un registro temporal usa componentes que no están definidos en el código anterior, se producirá un error en la validación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="7624c-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="7624c-125">Se trata de una precisión de punto flotante como mínimo.</span><span class="sxs-lookup"><span data-stu-id="7624c-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="7624c-126">Se puede usar un máximo de tres en una sola instrucción.</span><span class="sxs-lookup"><span data-stu-id="7624c-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7624c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7624c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7624c-128">Registra</span><span class="sxs-lookup"><span data-stu-id="7624c-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




