---
title: Porte de polígonos y cuadráteros
description: Tenga en cuenta los siguientes puntos al porte de polígonos y cuadráteros.
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Porte de IRIS GL, cuadriláteros
- porting from IRIS GL,quadriteros
- porte a OpenGL desde IRIS GL, cuadriteros
- Porte de OpenGL desde IRIS GL, cuadriteros
- funciones de dibujo, cuadriláteros
- Cuadriláteros
- Porte de IRIS GL, polígonos
- porting from IRIS GL,polygons
- porte a OpenGL desde IRIS GL, polygons
- Porte de OpenGL desde IRIS GL,polygons
- funciones de dibujo, polígonos
- polygons,porting from IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908463"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="067d3-115">Porte de polígonos y cuadráteros</span><span class="sxs-lookup"><span data-stu-id="067d3-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="067d3-116">Tenga en cuenta los siguientes puntos al porte de polígonos y cuadráteros:</span><span class="sxs-lookup"><span data-stu-id="067d3-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="067d3-117">No hay ningún equivalente directo para **cóncavo\*\*\*\*(TRUE).**</span><span class="sxs-lookup"><span data-stu-id="067d3-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="067d3-118">En su lugar, puede usar las rutinas de teselación en GLU, descritas en [Tessellating Polygons ( Polígonos de teselación).](tessellating-polygons.md)</span><span class="sxs-lookup"><span data-stu-id="067d3-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="067d3-119">Los modos de polígono se establecen de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="067d3-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="067d3-120">Estas funciones de dibujo de polígono no tienen equivalentes directos en OpenGL: la **familia poly** de rutinas; la **familia de rutinas polf;** **pmv**, **pdr** y **pclos**; **rpmv** y **rpdr**; **splf**; y **spclos**.</span><span class="sxs-lookup"><span data-stu-id="067d3-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="067d3-121">Si el código GL de IRIS usa estas funciones, tendrá que volver a escribir el código mediante [**glBegin**](glbegin.md) \_ (GL POLYGON).</span><span class="sxs-lookup"><span data-stu-id="067d3-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="067d3-122">En la tabla siguiente se enumeran las funciones de dibujo de polígonos IRIS GL y sus funciones OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="067d3-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="067d3-123">Función IRIS GL</span><span class="sxs-lookup"><span data-stu-id="067d3-123">IRIS GL function</span></span>         | <span data-ttu-id="067d3-124">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="067d3-124">OpenGL function</span></span>                                                    | <span data-ttu-id="067d3-125">Significado</span><span class="sxs-lookup"><span data-stu-id="067d3-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="067d3-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="067d3-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="067d3-127">[**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="067d3-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="067d3-128">Los vértices definen el límite de un polígono convexa simple.</span><span class="sxs-lookup"><span data-stu-id="067d3-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="067d3-129">**glBegin**(GL \_ QUADS )**glEnd**</span><span class="sxs-lookup"><span data-stu-id="067d3-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="067d3-130">Interpreta los vértices de los vértices como cuadrículos.</span><span class="sxs-lookup"><span data-stu-id="067d3-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="067d3-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="067d3-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="067d3-132">[**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**</span><span class="sxs-lookup"><span data-stu-id="067d3-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="067d3-133">Interpreta los vértices como franjas vinculadas de cuadrículos.</span><span class="sxs-lookup"><span data-stu-id="067d3-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="067d3-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="067d3-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="067d3-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="067d3-135">**polymode**</span></span>             | [<span data-ttu-id="067d3-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="067d3-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="067d3-137">Establece el modo de dibujo de polígono.</span><span class="sxs-lookup"><span data-stu-id="067d3-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="067d3-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="067d3-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="067d3-139">glRect</span><span class="sxs-lookup"><span data-stu-id="067d3-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="067d3-140">Dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="067d3-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="067d3-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="067d3-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="067d3-142">Dibuja un rectángulo alineado con la pantalla.</span><span class="sxs-lookup"><span data-stu-id="067d3-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="067d3-143">??</span><span class="sxs-lookup"><span data-stu-id="067d3-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="067d3-144">Porte de modos de polígono</span><span class="sxs-lookup"><span data-stu-id="067d3-144">Porting Polygon Modes</span></span>

<span data-ttu-id="067d3-145">La función OpenGL [**glPolygonMode**](glpolygonmode.md) permite especificar a qué lado de un polígono (atrás o delante) se aplica el modo.</span><span class="sxs-lookup"><span data-stu-id="067d3-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="067d3-146">La sintaxis es:</span><span class="sxs-lookup"><span data-stu-id="067d3-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="067d3-147">donde face es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="067d3-147">where face is one of:</span></span>



|<span data-ttu-id="067d3-148">Valor de GLenum</span><span class="sxs-lookup"><span data-stu-id="067d3-148">GLenum value</span></span>                      |  <span data-ttu-id="067d3-149">Significado</span><span class="sxs-lookup"><span data-stu-id="067d3-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="067d3-150">GL \_ FRONT</span><span class="sxs-lookup"><span data-stu-id="067d3-150">GL\_FRONT</span></span>            | <span data-ttu-id="067d3-151">modo que se aplica a los polígonos orientados al frente</span><span class="sxs-lookup"><span data-stu-id="067d3-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="067d3-152">GL \_ BACK</span><span class="sxs-lookup"><span data-stu-id="067d3-152">GL\_BACK</span></span>             | <span data-ttu-id="067d3-153">modo que se aplica a los polígonos orientados hacia atrás</span><span class="sxs-lookup"><span data-stu-id="067d3-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="067d3-154">GL \_ FRONT \_ AND \_ BACK</span><span class="sxs-lookup"><span data-stu-id="067d3-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="067d3-155">modo que se aplica a los polígonos orientados hacia delante y hacia atrás</span><span class="sxs-lookup"><span data-stu-id="067d3-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="067d3-156">El modo FRONT AND BACK de GL \_ es equivalente a la función \_ \_ **polymode** DE IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="067d3-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="067d3-157">En la tabla siguiente se enumeran los modos de polígono IRIS GL y sus modos OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="067d3-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="067d3-158">Modo GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="067d3-158">IRIS GL mode</span></span> | <span data-ttu-id="067d3-159">Modo OpenGL</span><span class="sxs-lookup"><span data-stu-id="067d3-159">OpenGL mode</span></span> | <span data-ttu-id="067d3-160">Significado</span><span class="sxs-lookup"><span data-stu-id="067d3-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="067d3-161">PYM \_ POINT</span><span class="sxs-lookup"><span data-stu-id="067d3-161">PYM\_POINT</span></span>   | <span data-ttu-id="067d3-162">GL \_ POINT</span><span class="sxs-lookup"><span data-stu-id="067d3-162">GL\_POINT</span></span>   | <span data-ttu-id="067d3-163">Dibuja los vértices como puntos.</span><span class="sxs-lookup"><span data-stu-id="067d3-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="067d3-164">LÍNEA \_ PYM</span><span class="sxs-lookup"><span data-stu-id="067d3-164">PYM\_LINE</span></span>    | <span data-ttu-id="067d3-165">LÍNEA \_ GL</span><span class="sxs-lookup"><span data-stu-id="067d3-165">GL\_LINE</span></span>    | <span data-ttu-id="067d3-166">Dibuja los bordes de los límites como segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="067d3-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="067d3-167">PYM \_ FILL</span><span class="sxs-lookup"><span data-stu-id="067d3-167">PYM\_FILL</span></span>    | <span data-ttu-id="067d3-168">GL \_ FILL</span><span class="sxs-lookup"><span data-stu-id="067d3-168">GL\_FILL</span></span>    | <span data-ttu-id="067d3-169">Dibuja relleno interior de polígono.</span><span class="sxs-lookup"><span data-stu-id="067d3-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="067d3-170">PYM \_ HOLLOW</span><span class="sxs-lookup"><span data-stu-id="067d3-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="067d3-171">Rellena solo los píxeles interiores en los límites.</span><span class="sxs-lookup"><span data-stu-id="067d3-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="067d3-172">Porting Polygon PolygonPples</span><span class="sxs-lookup"><span data-stu-id="067d3-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="067d3-173">Al portear polígonos IRIS GL, tenga en cuenta los siguientes puntos:</span><span class="sxs-lookup"><span data-stu-id="067d3-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="067d3-174">OpenGL no usa tablas para polígonos de polígonos. solo se mantiene un patrón detippla.</span><span class="sxs-lookup"><span data-stu-id="067d3-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="067d3-175">Puede usar listas para mostrar para almacenar diferentes patrones de información sobre la información.</span><span class="sxs-lookup"><span data-stu-id="067d3-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="067d3-176">El tamaño del mapa de bits de latippla de polígono OpenGL siempre es un patrón de 32 x 32 bits.</span><span class="sxs-lookup"><span data-stu-id="067d3-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="067d3-177">La codificación de stipple se ve afectada [**por glPixelStore.**](glpixelstore-functions.md)</span><span class="sxs-lookup"><span data-stu-id="067d3-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="067d3-178">Para obtener más información sobre cómo portear polígonos, vea [Porting Pixel Operations](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="067d3-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="067d3-179">En la tabla siguiente se enumeran las funciones detippla de polígono de IRIS GL y sus funciones OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="067d3-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="067d3-180">Función IRIS GL</span><span class="sxs-lookup"><span data-stu-id="067d3-180">IRIS GL function</span></span> | <span data-ttu-id="067d3-181">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="067d3-181">OpenGL function</span></span>                                    | <span data-ttu-id="067d3-182">Significado</span><span class="sxs-lookup"><span data-stu-id="067d3-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="067d3-183">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="067d3-183">**defpattern**</span></span>   | [<span data-ttu-id="067d3-184">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="067d3-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="067d3-185">Establece el patrón detippla.</span><span class="sxs-lookup"><span data-stu-id="067d3-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="067d3-186">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="067d3-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="067d3-187">OpenGL mantiene solo un patrón detippla de polígono.</span><span class="sxs-lookup"><span data-stu-id="067d3-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="067d3-188">**getpattern**</span><span class="sxs-lookup"><span data-stu-id="067d3-188">**getpattern**</span></span>   | [<span data-ttu-id="067d3-189">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="067d3-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="067d3-190">Devuelve el mapa de bits de stipple (que se usa para devolver un índice).</span><span class="sxs-lookup"><span data-stu-id="067d3-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="067d3-191">En OpenGL, puede habilitar y deshabilitar el contrabando de polígonos pasando GL POLYGON STIPPLE como parámetro para \_ \_ [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="067d3-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="067d3-192">En el siguiente ejemplo de código OpenGL se muestra el contrabando de polígonos:</span><span class="sxs-lookup"><span data-stu-id="067d3-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="067d3-193">Porte de polígonos teselados</span><span class="sxs-lookup"><span data-stu-id="067d3-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="067d3-194">En IRIS GL, se usa **cóncavo\*\*\*\*(TRUE)** y, a continuación, **bgnpolygon** para dibujar polígonos cóncavos.</span><span class="sxs-lookup"><span data-stu-id="067d3-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="067d3-195">OpenGL GLU incluye funciones que puede usar para dibujar polígonos cóncavos.</span><span class="sxs-lookup"><span data-stu-id="067d3-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="067d3-196">**Para dibujar un polígono cóncavo con OpenGL**</span><span class="sxs-lookup"><span data-stu-id="067d3-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="067d3-197">Cree un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="067d3-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="067d3-198">Defina las devoluciones de llamada que se usarán para procesar los triángulos generados por el teselador.</span><span class="sxs-lookup"><span data-stu-id="067d3-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="067d3-199">Especifique el polígono cóncavo que se va a teselar.</span><span class="sxs-lookup"><span data-stu-id="067d3-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="067d3-200">En la tabla siguiente se enumeran las funciones OpenGL para dibujar polígonos teselados.</span><span class="sxs-lookup"><span data-stu-id="067d3-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="067d3-201">Función GLU de OpenGL</span><span class="sxs-lookup"><span data-stu-id="067d3-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="067d3-202">Significado</span><span class="sxs-lookup"><span data-stu-id="067d3-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="067d3-203">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="067d3-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="067d3-204">Crea un nuevo objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="067d3-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="067d3-205">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="067d3-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="067d3-206">Elimina un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="067d3-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="067d3-207">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="067d3-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="067d3-208">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="067d3-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="067d3-209">Comienza la especificación del polígono.</span><span class="sxs-lookup"><span data-stu-id="067d3-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="067d3-210">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="067d3-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="067d3-211">Especifica un vértice de polígono en un contorno.</span><span class="sxs-lookup"><span data-stu-id="067d3-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="067d3-212">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="067d3-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="067d3-213">Indica que la siguiente serie de vértices describe un nuevo contorno.</span><span class="sxs-lookup"><span data-stu-id="067d3-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="067d3-214">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="067d3-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="067d3-215">Finaliza la especificación del polígono.</span><span class="sxs-lookup"><span data-stu-id="067d3-215">Ends the polygon specification.</span></span>                                    |



 

 

 





