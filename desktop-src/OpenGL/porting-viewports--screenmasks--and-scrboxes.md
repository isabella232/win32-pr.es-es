---
title: Trasladar las ventanillas, Screenmasks y Scrboxes
description: Las siguientes funciones de ventanilla GL de IRIS no tienen ningún equivalente de OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Migración de GL de IRIS, funciones de ventanilla
- trasladar de IRIS GL, funciones de ventanilla
- trasladar a OpenGL desde IRIS GL, funciones de ventanilla
- Exportación de OpenGL desde IRIS GL, funciones de ventanilla
- funciones de ventanilla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665621"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="2cb82-108">Trasladar las ventanillas, Screenmasks y Scrboxes</span><span class="sxs-lookup"><span data-stu-id="2cb82-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="2cb82-109">Las siguientes funciones de ventanilla GL de IRIS no tienen ningún equivalente de OpenGL:</span><span class="sxs-lookup"><span data-stu-id="2cb82-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="2cb82-110">**reshapeviewport**</span><span class="sxs-lookup"><span data-stu-id="2cb82-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="2cb82-111">**scrbox**</span><span class="sxs-lookup"><span data-stu-id="2cb82-111">**scrbox**</span></span>
-   <span data-ttu-id="2cb82-112">**getscrbox**</span><span class="sxs-lookup"><span data-stu-id="2cb82-112">**getscrbox**</span></span>

<span data-ttu-id="2cb82-113">Con la función **VIEWPORT** GL de iris, se especifican las coordenadas x (en píxeles) de la izquierda y la derecha de un rectángulo de la ventanilla y las coordenadas y de la parte superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="2cb82-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="2cb82-114">Sin embargo, con la función [**glViewport**](glviewport.md) de OpenGL, se especifican las coordenadas x e y (en píxeles) de la esquina inferior izquierda del rectángulo de la ventanilla junto con el ancho y el alto.</span><span class="sxs-lookup"><span data-stu-id="2cb82-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="2cb82-115">En la tabla siguiente se enumeran las funciones de ventanilla GL de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="2cb82-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="2cb82-116">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="2cb82-116">IRIS GL function</span></span>                          | <span data-ttu-id="2cb82-117">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="2cb82-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="2cb82-118">Significado</span><span class="sxs-lookup"><span data-stu-id="2cb82-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="2cb82-119">**ventanilla** (izquierda, derecha, abajo, superior)</span><span class="sxs-lookup"><span data-stu-id="2cb82-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="2cb82-120">[**glViewport**](glviewport.md) (x, y, ancho y alto)</span><span class="sxs-lookup"><span data-stu-id="2cb82-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="2cb82-121">Establece la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="2cb82-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="2cb82-122">**popviewportpushviewport**</span><span class="sxs-lookup"><span data-stu-id="2cb82-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="2cb82-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) (bit de la ventanilla de contabilidad \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="2cb82-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="2cb82-124">Envía y extrae la pila.</span><span class="sxs-lookup"><span data-stu-id="2cb82-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="2cb82-125">**getviewport**</span><span class="sxs-lookup"><span data-stu-id="2cb82-125">**getviewport**</span></span>                           | <span data-ttu-id="2cb82-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (ventanilla de GL \_ )</span><span class="sxs-lookup"><span data-stu-id="2cb82-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="2cb82-127">Devuelve las dimensiones de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="2cb82-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="2cb82-128">??</span><span class="sxs-lookup"><span data-stu-id="2cb82-128">??</span></span>

 

 





