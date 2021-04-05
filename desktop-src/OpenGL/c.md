---
title: C (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- equipos cliente
- memoria de cliente
- coordenadas de recorte
- recortar
- Índice de color
- modo de índice de color
- mapas de colores
- components
- contextos
- tengan
- envoltura convexa
- sistema de coordenadas
- selección
- matriz actual
- posición de la trama actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078764"
---
# <a name="c-opengl"></a><span data-ttu-id="c023a-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="c023a-118">C (OpenGL)</span></span>

<span data-ttu-id="c023a-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="c023a-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="c023a-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**equipo cliente**</span><span class="sxs-lookup"><span data-stu-id="c023a-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-121">El equipo desde el que se emiten los comandos de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c023a-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="c023a-122">El equipo que emite comandos OpenGL se puede conectar a través de una red a otro equipo que ejecute los comandos, o bien se pueden emitir y ejecutar comandos en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="c023a-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="c023a-123">Vea también [servidor](s.md).</span><span class="sxs-lookup"><span data-stu-id="c023a-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="c023a-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria de cliente**</span><span class="sxs-lookup"><span data-stu-id="c023a-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-125">La memoria principal (donde se almacenan las variables de programa) del equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="c023a-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas de recorte**</span><span class="sxs-lookup"><span data-stu-id="c023a-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-127">El sistema de coordenadas que sigue la transformación por la matriz de proyección y precede a la división de la perspectiva.</span><span class="sxs-lookup"><span data-stu-id="c023a-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="c023a-128">Vista: el recorte del volumen se realiza en las coordenadas del clip, pero no en el recorte específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c023a-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="c023a-129">Vea también [recorte específico de la aplicación](a.md).</span><span class="sxs-lookup"><span data-stu-id="c023a-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="c023a-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**salte**</span><span class="sxs-lookup"><span data-stu-id="c023a-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-131">Eliminar la parte de una primitiva geométrica que está fuera del espacio medio definido por un plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="c023a-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="c023a-132">Los puntos simplemente se rechazan si están fuera.</span><span class="sxs-lookup"><span data-stu-id="c023a-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="c023a-133">Se elimina la parte de una línea o de un polígono que se encuentra fuera del espacio medio, y se generan vértices adicionales según sea necesario para completar el primitivo dentro de la mitad del espacio de recorte.</span><span class="sxs-lookup"><span data-stu-id="c023a-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="c023a-134">Las primitivas geométricas y la posición de la trama actual (cuando se especifica) siempre se recortan en los seis semiespacios definidos por los planos izquierdo, derecho, inferior, superior, Near y Far del volumen de la vista.</span><span class="sxs-lookup"><span data-stu-id="c023a-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="c023a-135">Las aplicaciones pueden especificar los planos de recorte específicos de la aplicación opcionales que se van a aplicar en coordenadas oculares.</span><span class="sxs-lookup"><span data-stu-id="c023a-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**Índice de color**</span><span class="sxs-lookup"><span data-stu-id="c023a-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-137">Un valor único que representa un color por nombre, en lugar de por valor.</span><span class="sxs-lookup"><span data-stu-id="c023a-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="c023a-138">Los índices de color de OpenGL se tratan como valores continuos (por ejemplo, números de punto flotante) mientras que las operaciones como la interpolación y el tramado se realizan en ellos.</span><span class="sxs-lookup"><span data-stu-id="c023a-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="c023a-139">Sin embargo, los índices de color almacenados en el búfer de fotogramas son siempre valores enteros.</span><span class="sxs-lookup"><span data-stu-id="c023a-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="c023a-140">Los índices de punto flotante se convierten en enteros redondeando al valor entero más cercano.</span><span class="sxs-lookup"><span data-stu-id="c023a-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de color**</span><span class="sxs-lookup"><span data-stu-id="c023a-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-142">Modo de contexto de OpenGL en el que sus búferes de color almacenan índices de color, en lugar de componentes de color rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="c023a-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de colores**</span><span class="sxs-lookup"><span data-stu-id="c023a-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-144">Una tabla de asignaciones de índice a RGB a la que se tiene acceso mediante el hardware de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c023a-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="c023a-145">Cada índice de color se lee desde el búfer de color, se convierte en un triple por búsqueda en el mapa de colores y se envía al monitor.</span><span class="sxs-lookup"><span data-stu-id="c023a-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**pone**</span><span class="sxs-lookup"><span data-stu-id="c023a-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-147">Un valor único, continuo (por ejemplo, punto flotante) que representa una intensidad o una cantidad.</span><span class="sxs-lookup"><span data-stu-id="c023a-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="c023a-148">Normalmente, un valor de componente de cero representa el valor o la intensidad mínimos y un valor de componente de uno representa el valor o la intensidad máximos, aunque a veces se usan otras normalización.</span><span class="sxs-lookup"><span data-stu-id="c023a-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="c023a-149">Dado que los valores de componente se interpretan en un intervalo normalizado, se especifican independientemente de la resolución real.</span><span class="sxs-lookup"><span data-stu-id="c023a-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="c023a-150">Por ejemplo, el triple RGB (1,1) es blanco, independientemente de si los búferes de color almacenan 4, 8 o 12 bits cada uno.</span><span class="sxs-lookup"><span data-stu-id="c023a-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="c023a-151">Los componentes fuera del intervalo se fijan normalmente en el intervalo normalizado, no se truncan ni se interpretan de otra manera.</span><span class="sxs-lookup"><span data-stu-id="c023a-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="c023a-152">Por ejemplo, el triple RGB (1,4, 1,5, 0,9) se fija a (1,0, 1,0, 0,9) antes de que se use para actualizar el búfer de color.</span><span class="sxs-lookup"><span data-stu-id="c023a-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="c023a-153">Rojo, verde, azul, alfa y profundidad siempre se tratan como componentes, nunca como índices.</span><span class="sxs-lookup"><span data-stu-id="c023a-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contexto**</span><span class="sxs-lookup"><span data-stu-id="c023a-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-155">Un conjunto completo de variables de estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c023a-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="c023a-156">Tenga en cuenta que el contenido de fotogramas no forma parte del estado de OpenGL, pero que la configuración de fotogramas es.</span><span class="sxs-lookup"><span data-stu-id="c023a-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**tengan**</span><span class="sxs-lookup"><span data-stu-id="c023a-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-158">Condición de un polígono en el que ninguna línea recta del plano del polígono forma una intersección con el polígono más de dos veces.</span><span class="sxs-lookup"><span data-stu-id="c023a-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**casco convexo**</span><span class="sxs-lookup"><span data-stu-id="c023a-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-160">La región convexa más pequeña que incluye un grupo de puntos especificado.</span><span class="sxs-lookup"><span data-stu-id="c023a-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="c023a-161">En dos dimensiones, el casco convexo se encuentra conceptualmente mediante la expansión de una banda elástica alrededor de los puntos para que todos los puntos se encuentren dentro de la banda.</span><span class="sxs-lookup"><span data-stu-id="c023a-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**</span><span class="sxs-lookup"><span data-stu-id="c023a-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-163">En un espacio n-dimensional, conjunto de vectores n-linealmente independientes anclados a un punto (denominado origen).</span><span class="sxs-lookup"><span data-stu-id="c023a-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="c023a-164">Un grupo de coordenadas especifica un punto en el espacio de n dimensiones, un conjunto de n vectores de forma lineal anclados a un punto (denominado origen).</span><span class="sxs-lookup"><span data-stu-id="c023a-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="c023a-165">Un grupo de coordenadas especifica un punto en el espacio (o un vector desde el origen) indicando la distancia que hay que recorrer a lo largo de cada vector para alcanzar el punto (o el extremo del vector).</span><span class="sxs-lookup"><span data-stu-id="c023a-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="c023a-166">(o un vector desde el origen) indicando la distancia que hay que recorrer a lo largo de cada vector para alcanzar el punto (o la punta del vector).</span><span class="sxs-lookup"><span data-stu-id="c023a-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="c023a-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**selección**</span><span class="sxs-lookup"><span data-stu-id="c023a-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-168">El proceso de eliminación de una cara frontal o de una cara posterior de un polígono para que no se dibuje la cara.</span><span class="sxs-lookup"><span data-stu-id="c023a-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matriz actual**</span><span class="sxs-lookup"><span data-stu-id="c023a-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-170">Matriz que transforma las coordenadas de un sistema de coordenadas en coordenadas de otro sistema.</span><span class="sxs-lookup"><span data-stu-id="c023a-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="c023a-171">Hay tres matrices actuales en OpenGL: la matriz MODELVIEW, que transforma las coordenadas de objeto (coordenadas especificadas por el programador) en coordenadas oculares; la matriz de perspectiva, que transforma las coordenadas del ojo en coordenadas de recorte. y la matriz de textura, que transforma las coordenadas de textura especificadas o generadas como se describe en la matriz.</span><span class="sxs-lookup"><span data-stu-id="c023a-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="c023a-172">Cada matriz actual es el elemento superior de una pila de matrices.</span><span class="sxs-lookup"><span data-stu-id="c023a-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="c023a-173">Cada una de las tres pilas se puede manipular con comandos de manipulación de matrices de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="c023a-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="c023a-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posición de la trama actual**</span><span class="sxs-lookup"><span data-stu-id="c023a-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="c023a-175">Una posición de la coordenada de la ventana que especifica la posición de una primitiva de imagen cuando se rasteriza.</span><span class="sxs-lookup"><span data-stu-id="c023a-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="c023a-176">La posición de la trama actual y otros parámetros de Raster actuales se actualizan cuando se llama a glRasterpos.</span><span class="sxs-lookup"><span data-stu-id="c023a-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




