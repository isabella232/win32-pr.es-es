---
title: Trasladar el código de color, sombreado y Writemask
description: Trasladar el código de color, sombreado y Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Puerto de GL de IRIS, color
- portabilidad de IRIS GL, color
- trasladar a OpenGL desde IRIS GL, color
- Exportación de OpenGL desde IRIS GL, color
- Migración de la contabilidad de IRIS, sombreado
- portabilidad de IRIS GL, sombreado
- trasladar a OpenGL desde IRIS GL, sombreado
- Exportación de OpenGL desde IRIS GL, sombreado
- Migración de la contabilidad de IRIS, writemask
- portabilidad de IRIS GL, writemask
- migración a OpenGL desde IRIS GL, writemask
- Exportación de OpenGL desde IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774004"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="a05db-115">Trasladar el código de color, sombreado y Writemask</span><span class="sxs-lookup"><span data-stu-id="a05db-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="a05db-116">Al migrar el código de color, sombreado y writemask a OpenGL, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="a05db-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="a05db-117">Aunque puede establecer índices de mapa de colores con la función [glIndex](glindex-functions.md) de OpenGL, OpenGL no tiene una función para cargar índices de mapa de colores.</span><span class="sxs-lookup"><span data-stu-id="a05db-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="a05db-118">Los valores de color se normalizan en su tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a05db-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="a05db-119">(Para obtener información sobre los valores de color, vea [glColor](glcolor-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="a05db-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="a05db-120">No hay ningún equivalente simple para **cpack**.</span><span class="sxs-lookup"><span data-stu-id="a05db-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="a05db-121">Es posible que tenga que traducir el código que incluye las funciones de **c** o **color** a [**glClearColor**](glclearcolor.md) o [**glClearIndex**](glclearindex.md) en lugar de **glColor** o **glIndex**.</span><span class="sxs-lookup"><span data-stu-id="a05db-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="a05db-122">El writemask RGBA se aplica a cada componente, pero no a cada bit.</span><span class="sxs-lookup"><span data-stu-id="a05db-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="a05db-123">IRIS GL proporciona constantes de color definidas: negro, azul, rojo, verde, MAGENTA, aguamarina, amarillo y blanco.</span><span class="sxs-lookup"><span data-stu-id="a05db-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="a05db-124">OpenGL no proporciona estas constantes.</span><span class="sxs-lookup"><span data-stu-id="a05db-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="a05db-125">En este tema se incluye información sobre lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a05db-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="a05db-126">Trasladar llamadas de color</span><span class="sxs-lookup"><span data-stu-id="a05db-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="a05db-127">Trasladar modelos de sombreado</span><span class="sxs-lookup"><span data-stu-id="a05db-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




