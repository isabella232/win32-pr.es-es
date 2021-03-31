---
title: P (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parámetros
- División de perspectiva
- píxeles
- puntos
- polígonos
- Primitives
- matrices de proyección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995849"
---
# <a name="p-opengl"></a><span data-ttu-id="07b0b-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="07b0b-110">P (OpenGL)</span></span>

<span data-ttu-id="07b0b-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) p [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="07b0b-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="07b0b-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parámetro**</span><span class="sxs-lookup"><span data-stu-id="07b0b-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-113">Un valor que se pasa como argumento a un comando de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="07b0b-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="07b0b-114">A veces uno de los valores pasados por referencia a un comando de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="07b0b-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**División de perspectiva**</span><span class="sxs-lookup"><span data-stu-id="07b0b-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-116">División de x, y y z, que se lleva a cabo en coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="07b0b-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="07b0b-117">Vea también [coordenadas de recorte](c.md).</span><span class="sxs-lookup"><span data-stu-id="07b0b-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**píxel**</span><span class="sxs-lookup"><span data-stu-id="07b0b-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-119">Elemento de imagen.</span><span class="sxs-lookup"><span data-stu-id="07b0b-119">Picture element.</span></span> <span data-ttu-id="07b0b-120">Los bits en la ubicación (x, y) de todos los bitplanes de fotogramas constituyen el único píxel (x, y).</span><span class="sxs-lookup"><span data-stu-id="07b0b-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="07b0b-121">En una imagen de la memoria del cliente, un píxel es un grupo de elementos.</span><span class="sxs-lookup"><span data-stu-id="07b0b-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="07b0b-122">En las coordenadas de la ventana de OpenGL, cada píxel corresponde a un área de pantalla 1.0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="07b0b-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="07b0b-123">Las coordenadas de la esquina inferior izquierda de los nombres de píxeles x, y son (x, y) y la esquina superior derecha son (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="07b0b-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**Elija**</span><span class="sxs-lookup"><span data-stu-id="07b0b-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-125">Una ubicación exacta en el espacio, que se representa como un punto finito-diámetro.</span><span class="sxs-lookup"><span data-stu-id="07b0b-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**Polígono**</span><span class="sxs-lookup"><span data-stu-id="07b0b-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-127">Una superficie casi plana delimitada por los bordes especificados por los vértices.</span><span class="sxs-lookup"><span data-stu-id="07b0b-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="07b0b-128">Cada triángulo de una malla de triángulo es un polígono, como es cada cuadrangular de una malla de cuadrangular.</span><span class="sxs-lookup"><span data-stu-id="07b0b-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="07b0b-129">El rectángulo especificado por glRect también es un polígono.</span><span class="sxs-lookup"><span data-stu-id="07b0b-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**Rectangle**</span><span class="sxs-lookup"><span data-stu-id="07b0b-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-131">Una forma (como un punto, una línea, un polígono, un mapa de bits o una imagen) que se puede dibujar, almacenar y manipular como entidad discreta; elementos de los que se crean diseños gráficos de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="07b0b-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="07b0b-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**matriz de proyección**</span><span class="sxs-lookup"><span data-stu-id="07b0b-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="07b0b-133">Matriz 4x4 que transforma puntos, líneas, polígonos y posiciones de tramas de coordenadas de ojo a coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="07b0b-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




