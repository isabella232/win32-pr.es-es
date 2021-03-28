---
title: Control de flujo
description: La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea y ejecutar cada instrucción de HLSL una vez.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356917"
---
# <a name="flow-control"></a><span data-ttu-id="68e1d-103">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="68e1d-103">Flow Control</span></span>

<span data-ttu-id="68e1d-104">La mayoría del hardware está diseñado para ejecutar el código del sombreador línea a línea y ejecutar cada instrucción de HLSL una vez.</span><span class="sxs-lookup"><span data-stu-id="68e1d-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="68e1d-105">Una instrucción de control de flujo determina en tiempo de ejecución el bloque de instrucciones de HLSL que se ejecutará a continuación.</span><span class="sxs-lookup"><span data-stu-id="68e1d-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="68e1d-106">Mediante una instrucción de control de flujo, un sombreador puede recorrer en bucle un conjunto de instrucciones, o saltar (bifurcar) a una instrucción distinta de la de la línea siguiente.</span><span class="sxs-lookup"><span data-stu-id="68e1d-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="68e1d-107">Algunas instrucciones de control de flujo admiten el control estático especificado en tiempo de compilación; otros ofrecen control de predicado, que es una decisión por componente tomada en tiempo de ejecución y otras admiten el control dinámico, que es una decisión tomada en tiempo de ejecución basada en el contenido de una variable.</span><span class="sxs-lookup"><span data-stu-id="68e1d-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="68e1d-108">HLSL admite las siguientes instrucciones de control de flujo.</span><span class="sxs-lookup"><span data-stu-id="68e1d-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="68e1d-109">break</span><span class="sxs-lookup"><span data-stu-id="68e1d-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="68e1d-110">continue</span><span class="sxs-lookup"><span data-stu-id="68e1d-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="68e1d-111">omiti</span><span class="sxs-lookup"><span data-stu-id="68e1d-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="68e1d-112">do</span><span class="sxs-lookup"><span data-stu-id="68e1d-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="68e1d-113">for</span><span class="sxs-lookup"><span data-stu-id="68e1d-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="68e1d-114">if</span><span class="sxs-lookup"><span data-stu-id="68e1d-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="68e1d-115">switch</span><span class="sxs-lookup"><span data-stu-id="68e1d-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="68e1d-116">while</span><span class="sxs-lookup"><span data-stu-id="68e1d-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="68e1d-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="68e1d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68e1d-118">Sintaxis del lenguaje (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="68e1d-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




