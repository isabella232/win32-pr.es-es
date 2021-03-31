---
title: Trasladar comandos BGN/end
description: IRIS GL usa el paradigma Begin/end, pero tiene una función diferente para cada primitiva de gráficos.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Comandos de migración de GL de IRIS, BGN/end
- portabilidad de los comandos de BGN/end de IRIS GL
- trasladar a OpenGL desde los comandos de BGN/end de IRIS GL
- Exportación de OpenGL desde los comandos de BGN/end de IRIS GL
- funciones de dibujo, comandos BGN/end
- comandos BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419024"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="b1db3-109">Trasladar comandos BGN/end</span><span class="sxs-lookup"><span data-stu-id="b1db3-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="b1db3-110">IRIS GL usa el paradigma Begin/end, pero tiene una función diferente para cada primitiva de gráficos.</span><span class="sxs-lookup"><span data-stu-id="b1db3-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="b1db3-111">Por ejemplo, es probable que use **bgnpolygon** y **endpolygon** para dibujar polígonos y **bgnline** y **EndLine** para dibujar líneas.</span><span class="sxs-lookup"><span data-stu-id="b1db3-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="b1db3-112">En OpenGL, se usa la estructura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) para ambos.</span><span class="sxs-lookup"><span data-stu-id="b1db3-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="b1db3-113">En OpenGL se dibuja la mayoría de los objetos geométricos mediante la inclusión de una serie de funciones que especifican vértices, normales, texturas y colores entre pares de llamadas a **glBegin** y **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="b1db3-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="b1db3-114">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b1db3-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="b1db3-115">La función **glBegin** toma un parámetro único que especifica el modo de dibujo y, por tanto, el primitivo.</span><span class="sxs-lookup"><span data-stu-id="b1db3-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="b1db3-116">A continuación se muestra un ejemplo de código OpenGL que dibuja un polígono y, a continuación, una línea:</span><span class="sxs-lookup"><span data-stu-id="b1db3-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="b1db3-117">Con OpenGL, se dibujan diferentes objetos geométricos mediante la especificación de parámetros diferentes para [**glBegin**](glbegin.md).</span><span class="sxs-lookup"><span data-stu-id="b1db3-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="b1db3-118">En la tabla siguiente se enumeran los parámetros de **glBegin** de OpenGL que corresponden a las funciones de contabilidad de iris equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b1db3-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="b1db3-119">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="b1db3-119">IRIS GL function</span></span>  | <span data-ttu-id="b1db3-120">Valor del modo glBegin</span><span class="sxs-lookup"><span data-stu-id="b1db3-120">Value of glBegin mode</span></span> | <span data-ttu-id="b1db3-121">Significado</span><span class="sxs-lookup"><span data-stu-id="b1db3-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1db3-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="b1db3-122">**bgnpoint**</span></span>      | <span data-ttu-id="b1db3-123">puntos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-123">GL\_POINTS</span></span>            | <span data-ttu-id="b1db3-124">Puntos individuales.</span><span class="sxs-lookup"><span data-stu-id="b1db3-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="b1db3-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="b1db3-125">**bgnline**</span></span>       | <span data-ttu-id="b1db3-126">\_franja de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="b1db3-127">Serie de segmentos de línea conectados.</span><span class="sxs-lookup"><span data-stu-id="b1db3-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="b1db3-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="b1db3-128">**bgnclosedline**</span></span> | <span data-ttu-id="b1db3-129">\_bucle de línea de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="b1db3-130">Serie de segmentos de línea conectados, con un segmento agregado entre los vértices primero y último.</span><span class="sxs-lookup"><span data-stu-id="b1db3-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="b1db3-131">líneas de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-131">GL\_LINES</span></span>             | <span data-ttu-id="b1db3-132">Pares de vértices interpretados como segmentos de línea individuales.</span><span class="sxs-lookup"><span data-stu-id="b1db3-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="b1db3-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="b1db3-133">**bgnpolygon**</span></span>    | <span data-ttu-id="b1db3-134">Polígono de GL \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-134">GL\_POLYGON</span></span>           | <span data-ttu-id="b1db3-135">Límite de un polígono convexo simple.</span><span class="sxs-lookup"><span data-stu-id="b1db3-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="b1db3-136">triángulos de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="b1db3-137">Las tripas de los vértices se interpretan como triángulos.</span><span class="sxs-lookup"><span data-stu-id="b1db3-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="b1db3-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="b1db3-138">**bgntmesh**</span></span>      | <span data-ttu-id="b1db3-139">\_franja de triángulo de GL \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="b1db3-140">Bandas de triángulos vinculadas.</span><span class="sxs-lookup"><span data-stu-id="b1db3-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="b1db3-141">\_ventilador de triángulo GL \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="b1db3-142">Ventiladores vinculados de triángulos.</span><span class="sxs-lookup"><span data-stu-id="b1db3-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="b1db3-143">\_cuádruples de GL</span><span class="sxs-lookup"><span data-stu-id="b1db3-143">GL\_QUADS</span></span>             | <span data-ttu-id="b1db3-144">Cuadruplican de los vértices interpretados como quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="b1db3-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="b1db3-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="b1db3-145">**bgnqstrip**</span></span>     | <span data-ttu-id="b1db3-146">\_banda cuádruple de GL \_</span><span class="sxs-lookup"><span data-stu-id="b1db3-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="b1db3-147">Tiras vinculadas de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="b1db3-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="b1db3-148">Para obtener una explicación detallada de las diferencias entre las mallas de triángulo, las tiras y los ventiladores, consulte [migración de triángulos](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="b1db3-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="b1db3-149">No hay ningún límite en el número de vértices que puede especificar entre un par de glEnd de [**glBegin**](glbegin.md)  /  [](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="b1db3-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="b1db3-150">Además de especificar los vértices dentro de un par **glBegin**  /  **glEnd** , puede especificar una actual, las coordenadas de textura actuales y el color actual.</span><span class="sxs-lookup"><span data-stu-id="b1db3-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="b1db3-151">En la tabla siguiente se enumeran los comandos válidos dentro de un par **glBegin**  /  **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="b1db3-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="b1db3-152">Función de GL de IRIS</span><span class="sxs-lookup"><span data-stu-id="b1db3-152">IRIS GL function</span></span>        | <span data-ttu-id="b1db3-153">Función OpenGL</span><span class="sxs-lookup"><span data-stu-id="b1db3-153">OpenGL function</span></span>                                                      | <span data-ttu-id="b1db3-154">Significado</span><span class="sxs-lookup"><span data-stu-id="b1db3-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="b1db3-155">**V2**, **V3**, **V4**</span><span class="sxs-lookup"><span data-stu-id="b1db3-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="b1db3-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="b1db3-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="b1db3-157">Establece las coordenadas del vértice.</span><span class="sxs-lookup"><span data-stu-id="b1db3-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="b1db3-158">**RGBColor**, **cpack**</span><span class="sxs-lookup"><span data-stu-id="b1db3-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="b1db3-159">glColor</span><span class="sxs-lookup"><span data-stu-id="b1db3-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="b1db3-160">Establece el color actual.</span><span class="sxs-lookup"><span data-stu-id="b1db3-160">Sets current color.</span></span>                              |
| <span data-ttu-id="b1db3-161">**color**</span><span class="sxs-lookup"><span data-stu-id="b1db3-161">**color**</span></span>               | [<span data-ttu-id="b1db3-162">glIndex</span><span class="sxs-lookup"><span data-stu-id="b1db3-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="b1db3-163">Establece el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="b1db3-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="b1db3-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="b1db3-164">**n3f**</span></span>                 | [<span data-ttu-id="b1db3-165">glNormal</span><span class="sxs-lookup"><span data-stu-id="b1db3-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="b1db3-166">Establece coordenadas normales del vector.</span><span class="sxs-lookup"><span data-stu-id="b1db3-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="b1db3-167">glEvalCoord</span><span class="sxs-lookup"><span data-stu-id="b1db3-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="b1db3-168">Evalúa las asignaciones de uno y dos dimensiones habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b1db3-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="b1db3-169">**callobj**</span><span class="sxs-lookup"><span data-stu-id="b1db3-169">**callobj**</span></span>             | <span data-ttu-id="b1db3-170">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="b1db3-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="b1db3-171">Ejecuta listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="b1db3-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="b1db3-172">**T2**</span><span class="sxs-lookup"><span data-stu-id="b1db3-172">**t2**</span></span>                  | [<span data-ttu-id="b1db3-173">glTexCoord</span><span class="sxs-lookup"><span data-stu-id="b1db3-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="b1db3-174">Establece coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b1db3-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="b1db3-175">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="b1db3-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="b1db3-176">Controla los bordes del dibujo.</span><span class="sxs-lookup"><span data-stu-id="b1db3-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="b1db3-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="b1db3-177">**lmbind**</span></span>              | [<span data-ttu-id="b1db3-178">glMaterial</span><span class="sxs-lookup"><span data-stu-id="b1db3-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="b1db3-179">Establece las propiedades del material.</span><span class="sxs-lookup"><span data-stu-id="b1db3-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="b1db3-180">Si usa cualquier función de OpenGL que no sea la que se muestra en la tabla anterior dentro de un par de glEnd de [**glBegin**](glbegin.md)  /  [](glend.md) , obtendrá resultados imprevisibles o, posiblemente, un error.</span><span class="sxs-lookup"><span data-stu-id="b1db3-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




