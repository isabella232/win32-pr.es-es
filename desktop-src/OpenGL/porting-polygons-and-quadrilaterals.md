---
title: Trasladar polígonos y Quadrilaterals
description: Tenga en cuenta los siguientes puntos al trasladar polígonos y quadrilaterals
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Migración de la contabilidad de IRIS, quadrilaterals
- portabilidad de IRIS GL, quadrilaterals
- migración a OpenGL desde IRIS GL, quadrilaterals
- Exportación de OpenGL desde IRIS GL, quadrilaterals
- funciones de dibujo, quadrilaterals
- quadrilaterals
- Migración de la contabilidad de IRIS, polígonos
- portabilidad de IRIS GL, polígonos
- trasladar a OpenGL desde IRIS GL, polígonos
- Exportación de OpenGL desde IRIS GL, polígonos
- dibujar funciones, polígonos
- polígonos, portabilidad de IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778037"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="5cd46-115">Trasladar polígonos y Quadrilaterals</span><span class="sxs-lookup"><span data-stu-id="5cd46-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="5cd46-116">Tenga en cuenta los siguientes puntos al trasladar polígonos y quadrilaterals:</span><span class="sxs-lookup"><span data-stu-id="5cd46-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="5cd46-117">No hay ningún equivalente directo para **cóncava**(**true**).</span><span class="sxs-lookup"><span data-stu-id="5cd46-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="5cd46-118">En su lugar, puede usar las rutinas de teselación en GLU, que se describen en [polígonos de teselar](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="5cd46-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="5cd46-119">Los modos de polígono se establecen de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="5cd46-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="5cd46-120">Estas funciones de dibujo de polígonos no tienen equivalentes directos en OpenGL **: la familia** de rutinas. familia **POLF** de rutinas; **PMV**, **PDR** y **PCLOS**; **rpmv** y **rpdr**; **SPLF**; y **spclos**.</span><span class="sxs-lookup"><span data-stu-id="5cd46-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="5cd46-121">Si el código de la contabilidad de IRIS usa estas funciones, tendrá que volver a escribir el código mediante [**glBegin**](glbegin.md)(GL \_ Polygon).</span><span class="sxs-lookup"><span data-stu-id="5cd46-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="5cd46-122">En la tabla siguiente se enumeran las funciones de dibujo de polígono GL de IRIS y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5cd46-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="5cd46-123">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="5cd46-123">IRIS GL function</span></span>         | <span data-ttu-id="5cd46-124">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="5cd46-124">OpenGL function</span></span>                                                    | <span data-ttu-id="5cd46-125">Significado</span><span class="sxs-lookup"><span data-stu-id="5cd46-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5cd46-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="5cd46-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="5cd46-127">[**glBegin**](glbegin.md) (GL \_ polígono)[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="5cd46-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="5cd46-128">Los vértices definen el límite de un polígono convexo simple.</span><span class="sxs-lookup"><span data-stu-id="5cd46-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="5cd46-129">**glBegin**(GL \_ cuádruples)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5cd46-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="5cd46-130">Interpreta cuadruplican de los vértices como quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="5cd46-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="5cd46-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="5cd46-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="5cd46-132">[**glBegin**](glbegin.md) (GL \_ de \_ banda cuádruple)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5cd46-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="5cd46-133">Interpreta los vértices como franjas vinculadas de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="5cd46-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="5cd46-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="5cd46-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="5cd46-135">**Polimoda**</span><span class="sxs-lookup"><span data-stu-id="5cd46-135">**polymode**</span></span>             | [<span data-ttu-id="5cd46-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="5cd46-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="5cd46-137">Establece el modo de dibujo de polígono.</span><span class="sxs-lookup"><span data-stu-id="5cd46-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="5cd46-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="5cd46-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="5cd46-139">glRect</span><span class="sxs-lookup"><span data-stu-id="5cd46-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="5cd46-140">Dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5cd46-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="5cd46-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="5cd46-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="5cd46-142">Dibuja un rectángulo alineado en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5cd46-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="5cd46-143">??</span><span class="sxs-lookup"><span data-stu-id="5cd46-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="5cd46-144">Trasladar modos de polígono</span><span class="sxs-lookup"><span data-stu-id="5cd46-144">Porting Polygon Modes</span></span>

<span data-ttu-id="5cd46-145">La función [**glPolygonMode**](glpolygonmode.md) de OpenGL le permite especificar a qué lado de un polígono (hacia atrás o hacia delante) se aplica el modo.</span><span class="sxs-lookup"><span data-stu-id="5cd46-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="5cd46-146">La sintaxis es:</span><span class="sxs-lookup"><span data-stu-id="5cd46-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="5cd46-147">donde la superficie es una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="5cd46-147">where face is one of:</span></span>



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="5cd46-148">frontal de GL \_</span><span class="sxs-lookup"><span data-stu-id="5cd46-148">GL\_FRONT</span></span>            | <span data-ttu-id="5cd46-149">modo que se aplica a los polígonos frontales</span><span class="sxs-lookup"><span data-stu-id="5cd46-149">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="5cd46-150">libro \_ de contabilidad</span><span class="sxs-lookup"><span data-stu-id="5cd46-150">GL\_BACK</span></span>             | <span data-ttu-id="5cd46-151">el modo que se aplica a los polígonos de orientación</span><span class="sxs-lookup"><span data-stu-id="5cd46-151">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="5cd46-152">\_anverso \_ y \_ atrás de GL</span><span class="sxs-lookup"><span data-stu-id="5cd46-152">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="5cd46-153">modo que se aplica a los polígonos frontal y hacia delante</span><span class="sxs-lookup"><span data-stu-id="5cd46-153">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="5cd46-154">El \_ modo frontal \_ y \_ trasero de contabilidad es equivalente a la función de **multimodo** de la contabilidad de iris.</span><span class="sxs-lookup"><span data-stu-id="5cd46-154">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="5cd46-155">En la tabla siguiente se enumeran los modos de polígono de la contabilidad de IRIS y sus modos de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5cd46-155">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="5cd46-156">Modo de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="5cd46-156">IRIS GL mode</span></span> | <span data-ttu-id="5cd46-157">Modo OpenGL</span><span class="sxs-lookup"><span data-stu-id="5cd46-157">OpenGL mode</span></span> | <span data-ttu-id="5cd46-158">Significado</span><span class="sxs-lookup"><span data-stu-id="5cd46-158">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="5cd46-159">\_punto PYM</span><span class="sxs-lookup"><span data-stu-id="5cd46-159">PYM\_POINT</span></span>   | <span data-ttu-id="5cd46-160">punto de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5cd46-160">GL\_POINT</span></span>   | <span data-ttu-id="5cd46-161">Dibuja vértices como puntos.</span><span class="sxs-lookup"><span data-stu-id="5cd46-161">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="5cd46-162">\_línea PYM</span><span class="sxs-lookup"><span data-stu-id="5cd46-162">PYM\_LINE</span></span>    | <span data-ttu-id="5cd46-163">línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5cd46-163">GL\_LINE</span></span>    | <span data-ttu-id="5cd46-164">Dibuja los bordes del límite como segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="5cd46-164">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="5cd46-165">relleno de PYM \_</span><span class="sxs-lookup"><span data-stu-id="5cd46-165">PYM\_FILL</span></span>    | <span data-ttu-id="5cd46-166">relleno de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5cd46-166">GL\_FILL</span></span>    | <span data-ttu-id="5cd46-167">Dibuja el interior del polígono relleno.</span><span class="sxs-lookup"><span data-stu-id="5cd46-167">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="5cd46-168">PYM \_ hueco</span><span class="sxs-lookup"><span data-stu-id="5cd46-168">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="5cd46-169">Rellena solo los píxeles interiores en los límites.</span><span class="sxs-lookup"><span data-stu-id="5cd46-169">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="5cd46-170">Trasladar punteas de polígono</span><span class="sxs-lookup"><span data-stu-id="5cd46-170">Porting Polygon Stipples</span></span>

<span data-ttu-id="5cd46-171">Al migrar los elementos punteados de la contabilidad de IRIS, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5cd46-171">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="5cd46-172">OpenGL no usa tablas para los punteados de polígonos; solo se mantiene un patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="5cd46-172">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="5cd46-173">Puede usar listas de visualización para almacenar diferentes patrones de punteado.</span><span class="sxs-lookup"><span data-stu-id="5cd46-173">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="5cd46-174">El tamaño del mapa de bits punteado de OpenGL es siempre un patrón de bits de 32x32.</span><span class="sxs-lookup"><span data-stu-id="5cd46-174">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="5cd46-175">La codificación en forma de punteado se ve afectada por [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5cd46-175">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="5cd46-176">Para obtener más información sobre cómo trasladar a los polígonos, vea [portar las operaciones de píxeles](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="5cd46-176">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="5cd46-177">En la tabla siguiente se enumeran las funciones de los elementos punteados de IRIS GL y sus funciones de OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="5cd46-177">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="5cd46-178">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="5cd46-178">IRIS GL function</span></span> | <span data-ttu-id="5cd46-179">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="5cd46-179">OpenGL function</span></span>                                    | <span data-ttu-id="5cd46-180">Significado</span><span class="sxs-lookup"><span data-stu-id="5cd46-180">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="5cd46-181">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="5cd46-181">**defpattern**</span></span>   | [<span data-ttu-id="5cd46-182">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="5cd46-182">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="5cd46-183">Establece el patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="5cd46-183">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="5cd46-184">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="5cd46-184">**setpattern**</span></span>   |                                                    | <span data-ttu-id="5cd46-185">OpenGL solo mantiene un patrón punteado de polígono.</span><span class="sxs-lookup"><span data-stu-id="5cd46-185">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="5cd46-186">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="5cd46-186">**getpattern**</span></span>   | [<span data-ttu-id="5cd46-187">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="5cd46-187">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="5cd46-188">Devuelve el mapa de bits punteado (que se usa para devolver un índice).</span><span class="sxs-lookup"><span data-stu-id="5cd46-188">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="5cd46-189">En OpenGL, puede habilitar y deshabilitar el punteado de polígono pasando GL \_ Polygon \_ punteada como un parámetro para [**glEnable**](glenable.md) y [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="5cd46-189">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="5cd46-190">El siguiente ejemplo de código OpenGL muestra el punteado de polígono:</span><span class="sxs-lookup"><span data-stu-id="5cd46-190">The following OpenGL code sample demonstrates polygon stippling:</span></span>


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



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="5cd46-191">Trasladar polígonos teselados</span><span class="sxs-lookup"><span data-stu-id="5cd46-191">Porting Tessellated Polygons</span></span>

<span data-ttu-id="5cd46-192">En IRIS GL, use **cóncava**(**true**) y, a continuación, **bgnpolygon** para dibujar polígonos cóncavos.</span><span class="sxs-lookup"><span data-stu-id="5cd46-192">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="5cd46-193">OpenGL GLU incluye funciones que se pueden usar para dibujar polígonos cóncavos.</span><span class="sxs-lookup"><span data-stu-id="5cd46-193">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="5cd46-194">**Para dibujar un polígono cóncavo con OpenGL**</span><span class="sxs-lookup"><span data-stu-id="5cd46-194">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="5cd46-195">Cree un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="5cd46-195">Create a tessellation object.</span></span>
2.  <span data-ttu-id="5cd46-196">Defina devoluciones de llamada que se usarán para procesar los triángulos generados por del teselador.</span><span class="sxs-lookup"><span data-stu-id="5cd46-196">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="5cd46-197">Especifique el polígono cóncavo que se va a teselar.</span><span class="sxs-lookup"><span data-stu-id="5cd46-197">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="5cd46-198">En la tabla siguiente se enumeran las funciones de OpenGL para dibujar polígonos teselados.</span><span class="sxs-lookup"><span data-stu-id="5cd46-198">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="5cd46-199">Función GLU de OpenGL</span><span class="sxs-lookup"><span data-stu-id="5cd46-199">OpenGL GLU function</span></span>                        | <span data-ttu-id="5cd46-200">Significado</span><span class="sxs-lookup"><span data-stu-id="5cd46-200">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="5cd46-201">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="5cd46-201">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="5cd46-202">Crea un nuevo objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="5cd46-202">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="5cd46-203">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="5cd46-203">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="5cd46-204">Elimina un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="5cd46-204">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="5cd46-205">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="5cd46-205">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="5cd46-206">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="5cd46-206">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="5cd46-207">Comienza la especificación de polígono.</span><span class="sxs-lookup"><span data-stu-id="5cd46-207">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="5cd46-208">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="5cd46-208">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="5cd46-209">Especifica un vértice de polígono en un contorno.</span><span class="sxs-lookup"><span data-stu-id="5cd46-209">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="5cd46-210">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="5cd46-210">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="5cd46-211">Indica que la siguiente serie de vértices describe un nuevo contorno.</span><span class="sxs-lookup"><span data-stu-id="5cd46-211">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="5cd46-212">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="5cd46-212">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="5cd46-213">Finaliza la especificación de polígono.</span><span class="sxs-lookup"><span data-stu-id="5cd46-213">Ends the polygon specification.</span></span>                                    |



 

 

 





