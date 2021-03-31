---
title: Código de puerto que necesita una posición de gráficos actual
description: OpenGL no mantiene una posición de gráficos actual. Las funciones de GL de IRIS que dependen de la posición actual de los gráficos, como Move, Draw y RMV, no tienen ningún equivalente en OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Migración de la contabilidad de IRIS, posición de gráficos actual
- trasladar de IRIS GL, posición de gráficos actual
- trasladar a OpenGL desde IRIS GL, posición de gráficos actual
- Exportación de OpenGL desde IRIS GL, posición de gráficos actual
- posición de los gráficos actuales
- posiciones de trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/27/2019
ms.locfileid: "103785134"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="b3ac3-110">Código de puerto que necesita una posición de gráficos actual</span><span class="sxs-lookup"><span data-stu-id="b3ac3-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="b3ac3-111">OpenGL no mantiene una posición de gráficos actual.</span><span class="sxs-lookup"><span data-stu-id="b3ac3-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="b3ac3-112">Las funciones de GL de IRIS que dependen de la posición actual de los gráficos, como **Move**, **Draw** y **RMV**, no tienen ningún equivalente en OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b3ac3-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="b3ac3-113">Las versiones anteriores de IRIS GL incluían comandos de dibujo que se basan en la posición actual de los gráficos, aunque no se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="b3ac3-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="b3ac3-114">Tendrá que volver a escribir el código si se basó en la posición actual de los gráficos de cualquier manera, o si se usara cualquiera de las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="b3ac3-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="b3ac3-115">**dibujar** y **desplace**</span><span class="sxs-lookup"><span data-stu-id="b3ac3-115">**draw** and **move**</span></span>
-   <span data-ttu-id="b3ac3-116">**PMV**, **PDR** y **PCLOS**</span><span class="sxs-lookup"><span data-stu-id="b3ac3-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="b3ac3-117">**RDR**, **RMV**, **rpdr** y **rpmv**</span><span class="sxs-lookup"><span data-stu-id="b3ac3-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="b3ac3-118">**getgpos**</span><span class="sxs-lookup"><span data-stu-id="b3ac3-118">**getgpos**</span></span>

<span data-ttu-id="b3ac3-119">OpenGL tiene un concepto de posición de trama que corresponde a la posición de carácter actual de la contabilidad de IRIS.</span><span class="sxs-lookup"><span data-stu-id="b3ac3-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="b3ac3-120">Para obtener más información sobre el posicionamiento de tramas, vea [portar operaciones de píxeles](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b3ac3-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="b3ac3-121">En este tema se incluye información sobre lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b3ac3-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="b3ac3-122">Trasladar comandos de borrado de pantalla y de búfer</span><span class="sxs-lookup"><span data-stu-id="b3ac3-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="b3ac3-123">Portabilidad de funciones de transformación y de matriz</span><span class="sxs-lookup"><span data-stu-id="b3ac3-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="b3ac3-124">Trasladar código de modo MSINGLE</span><span class="sxs-lookup"><span data-stu-id="b3ac3-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="b3ac3-125">Portabilidad de funciones que obtienen matrices y transformaciones</span><span class="sxs-lookup"><span data-stu-id="b3ac3-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="b3ac3-126">Trasladar las ventanillas, Screenmasks y Scrboxes</span><span class="sxs-lookup"><span data-stu-id="b3ac3-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="b3ac3-127">Trasladar los planos de recorte</span><span class="sxs-lookup"><span data-stu-id="b3ac3-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




