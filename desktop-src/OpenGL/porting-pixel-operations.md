---
title: Trasladar operaciones de píxeles
description: Trasladar operaciones de píxeles
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Puerto de GL de IRIS, píxeles
- trasladar de IRIS GL, píxeles
- portabilidad a OpenGL desde IRIS GL, píxeles
- Exportación de OpenGL de IRIS GL, píxeles
- píxeles, portabilidad de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778043"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="feac9-108">Trasladar operaciones de píxeles</span><span class="sxs-lookup"><span data-stu-id="feac9-108">Porting Pixel Operations</span></span>

<span data-ttu-id="feac9-109">Al trasladar código que implique operaciones en píxeles, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="feac9-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="feac9-110">Las operaciones de píxeles lógicos no se aplican a los búferes de color RGBA.</span><span class="sxs-lookup"><span data-stu-id="feac9-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="feac9-111">Para obtener más información, vea [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="feac9-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="feac9-112">En general, IRIS GL usa el formato ABGR para píxeles, mientras que OpenGL usa RGBA.</span><span class="sxs-lookup"><span data-stu-id="feac9-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="feac9-113">Puede cambiar el formato con [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="feac9-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="feac9-114">Al migrar funciones de **lrectwrite** , tenga cuidado de tener en cuenta dónde se escribe **lrectwrite** (por ejemplo, podría estar escribiendo en el búfer de profundidad).</span><span class="sxs-lookup"><span data-stu-id="feac9-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="feac9-115">OpenGL proporciona una flexibilidad adicional en las operaciones de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="feac9-116">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para las operaciones de píxeles y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="feac9-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="feac9-117">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="feac9-117">IRIS GL function</span></span>                                   | <span data-ttu-id="feac9-118">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="feac9-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="feac9-119">Significado</span><span class="sxs-lookup"><span data-stu-id="feac9-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="feac9-120">**lrectread**, **rectread**,**readRGB**</span><span class="sxs-lookup"><span data-stu-id="feac9-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="feac9-121">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="feac9-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="feac9-122">Lee un bloque de píxeles de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="feac9-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="feac9-123">**lrectwrite**, **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="feac9-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="feac9-124">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="feac9-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="feac9-125">Escribe un bloque de píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="feac9-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="feac9-126">**rectcopy**</span><span class="sxs-lookup"><span data-stu-id="feac9-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="feac9-127">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="feac9-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="feac9-128">Copia píxeles en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="feac9-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="feac9-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="feac9-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="feac9-130">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="feac9-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="feac9-131">Especifica los factores de zoom de píxel para **glDrawPixels** y **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="feac9-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="feac9-132">**cmov**</span><span class="sxs-lookup"><span data-stu-id="feac9-132">**cmov**</span></span>                                           | [<span data-ttu-id="feac9-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="feac9-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="feac9-134">Especifica la posición de trama para las operaciones de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="feac9-135">**readsource**</span><span class="sxs-lookup"><span data-stu-id="feac9-135">**readsource**</span></span>                                     | [<span data-ttu-id="feac9-136">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="feac9-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="feac9-137">Selecciona un origen de búfer de color para los píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="feac9-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="feac9-138">**pixmode**</span></span>                                        | <span data-ttu-id="feac9-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="feac9-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="feac9-140">Establece modos de almacenamiento en píxeles. Establecer modos de transferencia de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="feac9-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="feac9-141">**logicop**</span></span>                                        | [<span data-ttu-id="feac9-142">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="feac9-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="feac9-143">Especifica una operación lógica para escrituras de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="feac9-144">[**glEnable**](glenable.md) ( \_ OP Logical \_ )</span><span class="sxs-lookup"><span data-stu-id="feac9-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="feac9-145">Activa las operaciones de lógica de píxeles.</span><span class="sxs-lookup"><span data-stu-id="feac9-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="feac9-146">Para obtener una lista completa de las operaciones lógicas posibles, vea [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="feac9-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="feac9-147">Este ejemplo de código de GL de IRIS muestra una escritura de píxel típica:</span><span class="sxs-lookup"><span data-stu-id="feac9-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="feac9-148">El código anterior tiene este aspecto cuando se traduce a OpenGL:</span><span class="sxs-lookup"><span data-stu-id="feac9-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





