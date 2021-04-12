---
title: Trasladar líneas
description: Trasladar el código de GL de IRIS que dibuja las líneas es bastante sencillo, aunque debe tener en cuenta las diferencias en la forma en que se puntea en OpenGL. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar líneas y sus funciones de OpenGL equivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Puertos de GL de IRIS, líneas
- trasladar de IRIS GL, líneas
- trasladar a OpenGL desde el GL de IRIS, líneas
- Exportación de OpenGL desde IRIS GL, líneas
- dibujar funciones, líneas
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269166"
---
# <a name="porting-lines"></a><span data-ttu-id="f67e7-110">Trasladar líneas</span><span class="sxs-lookup"><span data-stu-id="f67e7-110">Porting Lines</span></span>

<span data-ttu-id="f67e7-111">Trasladar el código de GL de IRIS que dibuja las líneas es bastante sencillo, aunque debe tener en cuenta las diferencias en la forma en que se puntea en OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f67e7-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="f67e7-112">En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS para dibujar líneas y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="f67e7-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f67e7-113">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="f67e7-113">IRIS GL function</span></span>                               | <span data-ttu-id="f67e7-114">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="f67e7-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="f67e7-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f67e7-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67e7-116">**bgnclosedline**,**endclosedline**</span><span class="sxs-lookup"><span data-stu-id="f67e7-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="f67e7-117">[**glBegin**](glbegin.md) (bucle de línea de contabilidad \_ \_ )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="f67e7-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="f67e7-118">Dibuja una línea cerrada.</span><span class="sxs-lookup"><span data-stu-id="f67e7-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="f67e7-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="f67e7-119">**bgnline**</span></span>                                    | <span data-ttu-id="f67e7-120">[**glBegin**](glbegin.md) (franja de línea de contabilidad \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f67e7-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="f67e7-121">Dibuja segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="f67e7-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="f67e7-122">**linewidth**</span><span class="sxs-lookup"><span data-stu-id="f67e7-122">**linewidth**</span></span>                                  | [<span data-ttu-id="f67e7-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="f67e7-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="f67e7-124">Establece el ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="f67e7-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="f67e7-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="f67e7-125">**getlwidth**</span></span>                                  | <span data-ttu-id="f67e7-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (ancho de línea de contabilidad \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="f67e7-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="f67e7-127">Devuelve el ancho de línea actual.</span><span class="sxs-lookup"><span data-stu-id="f67e7-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="f67e7-128">**deflinestyle**,**setlinestyle**</span><span class="sxs-lookup"><span data-stu-id="f67e7-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="f67e7-129">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f67e7-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="f67e7-130">Especifica un patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="f67e7-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="f67e7-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="f67e7-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="f67e7-132">argumento factor de **glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f67e7-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="f67e7-133">Establece un factor de repetición para el estilo de línea.</span><span class="sxs-lookup"><span data-stu-id="f67e7-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="f67e7-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="f67e7-134">**getlstyle**</span></span>                                  | <span data-ttu-id="f67e7-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ \_ patrón punteado de línea de contabilidad \_ )</span><span class="sxs-lookup"><span data-stu-id="f67e7-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="f67e7-136">Devuelve el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="f67e7-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="f67e7-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="f67e7-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="f67e7-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (repetición de línea de contabilidad \_ \_ punteada \_ )</span><span class="sxs-lookup"><span data-stu-id="f67e7-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="f67e7-139">Devuelve el factor de repetición.</span><span class="sxs-lookup"><span data-stu-id="f67e7-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="f67e7-140">**linesmooth**, **smoothline**</span><span class="sxs-lookup"><span data-stu-id="f67e7-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="f67e7-141">[**glEnable**](glenable.md) (línea de contabilidad \_ \_ suave)</span><span class="sxs-lookup"><span data-stu-id="f67e7-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="f67e7-142">Activa el suavizado de contorno de línea (para obtener más información sobre el suavizado de contorno, consulte [portabilidad de las funciones de suavizado](porting-antialiasing-functions.md)de contorno).</span><span class="sxs-lookup"><span data-stu-id="f67e7-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="f67e7-143">OpenGL no utiliza tablas para las líneas punteadas; mantiene solo un patrón de línea-punteado.</span><span class="sxs-lookup"><span data-stu-id="f67e7-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="f67e7-144">Puede usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para cambiar entre distintos patrones de punteado.</span><span class="sxs-lookup"><span data-stu-id="f67e7-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="f67e7-145">OpenGL no admite las funciones de estilo de línea de la contabilidad de IRIS anterior (como **Draw**, **LSBackup**, **getlsbackup**, etc.).</span><span class="sxs-lookup"><span data-stu-id="f67e7-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="f67e7-146">Para obtener información sobre cómo dibujar líneas con suavizado de contorno, consulte [portabilidad de las funciones de suavizado de contorno](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f67e7-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="f67e7-147">??</span><span class="sxs-lookup"><span data-stu-id="f67e7-147">??</span></span>

 

 





