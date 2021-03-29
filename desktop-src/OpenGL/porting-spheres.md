---
title: Ámbitos de portabilidad
description: 'Al trasladar esferas a OpenGL, tenga en cuenta los puntos siguientes:'
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Migración de la contabilidad de IRIS, esferas
- portabilidad de IRIS GL, esferas
- trasladar a OpenGL desde IRIS GL, esferas
- Exportación de OpenGL desde IRIS GL, esferas
- dibujar funciones, esferas
- esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418873"
---
# <a name="porting-spheres"></a><span data-ttu-id="5e2b1-109">Ámbitos de portabilidad</span><span class="sxs-lookup"><span data-stu-id="5e2b1-109">Porting Spheres</span></span>

<span data-ttu-id="5e2b1-110">Al trasladar esferas a OpenGL, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5e2b1-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="5e2b1-111">No se puede controlar el tipo de primitivas que se usan para dibujar la esfera.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="5e2b1-112">Puede controlar la precisión del dibujo de otra manera: usar los parámetros de segmentos y pilas.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="5e2b1-113">Los sectores son longitudinales; las pilas son latitudinal.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="5e2b1-114">Los esferas se dibujan centrados en el origen.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="5e2b1-115">En lugar de especificar la ubicación, como se hace con la función **sphdraw** de la contabilidad de iris, preceda a una llamada a la función Glu [**gluSphere**](glusphere.md) con una traducción.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="5e2b1-116">La biblioteca de esfera todavía no está disponible para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="5e2b1-117">En la tabla siguiente se enumeran las funciones de GL de IRIS para dibujar esferas y sus funciones equivalentes de GLU cuando están disponibles.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="5e2b1-118">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="5e2b1-118">IRIS GL function</span></span> | <span data-ttu-id="5e2b1-119">GLU función)</span><span class="sxs-lookup"><span data-stu-id="5e2b1-119">GLU function</span></span>                                 | <span data-ttu-id="5e2b1-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5e2b1-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="5e2b1-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-121">**sphobj**</span></span>       | [<span data-ttu-id="5e2b1-122">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="5e2b1-123">Crea un nuevo objeto sphere.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="5e2b1-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-124">**sphfree**</span></span>      | [<span data-ttu-id="5e2b1-125">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="5e2b1-126">Elimina el objeto de esfera y la memoria libre utilizada.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="5e2b1-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-127">**sphdraw**</span></span>      | [<span data-ttu-id="5e2b1-128">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="5e2b1-129">Dibuja una esfera.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="5e2b1-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="5e2b1-131">Establece atributos de esfera.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="5e2b1-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="5e2b1-133">Controla la orientación de esfera.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="5e2b1-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="5e2b1-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="5e2b1-135">Devuelve el número de polígonos en la esfera actual.</span><span class="sxs-lookup"><span data-stu-id="5e2b1-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="5e2b1-136">??</span><span class="sxs-lookup"><span data-stu-id="5e2b1-136">??</span></span>

 

 




