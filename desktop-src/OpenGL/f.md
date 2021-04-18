---
title: F (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- sombreado plano
- luz
- fuentes
- fragments
- framebuffers
- cara frontal
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676541"
---
# <a name="f-opengl"></a><span data-ttu-id="e71da-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="e71da-111">F (OpenGL)</span></span>

<span data-ttu-id="e71da-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="e71da-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="e71da-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Portada**</span><span class="sxs-lookup"><span data-stu-id="e71da-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-114">Un lado de un polígono.</span><span class="sxs-lookup"><span data-stu-id="e71da-114">One side of a polygon.</span></span> <span data-ttu-id="e71da-115">Cada polígono tiene dos caras: una cara frontal y otra cara.</span><span class="sxs-lookup"><span data-stu-id="e71da-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="e71da-116">Solo una de las caras está visible en la ventana.</span><span class="sxs-lookup"><span data-stu-id="e71da-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="e71da-117">El hecho de que la cara trasera o frontal esté visible se determina de forma eficaz una vez que se proyecta el polígono en la ventana.</span><span class="sxs-lookup"><span data-stu-id="e71da-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="e71da-118">Después de esta proyección, si los bordes del polígono se dirigen a la derecha, una de las caras es visible; Si se dirige en sentido contrario a las agujas del reloj, el otro aspecto es visible.</span><span class="sxs-lookup"><span data-stu-id="e71da-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="e71da-119">Tanto si el reloj se corresponde hacia delante como hacia atrás (y en sentido contrario a las agujas del reloj), lo determina el programador de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e71da-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="e71da-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**sombreado plano**</span><span class="sxs-lookup"><span data-stu-id="e71da-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-121">Hace referencia a la coloración de un tipo primitivo con un único color constante a lo largo de su extensión, en lugar de interpolar sin problemas los colores en el primitivo.</span><span class="sxs-lookup"><span data-stu-id="e71da-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="e71da-122">Vea [sombreado Gouraud](g.md).</span><span class="sxs-lookup"><span data-stu-id="e71da-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71da-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**luz**</span><span class="sxs-lookup"><span data-stu-id="e71da-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-124">Técnica de representación que se puede usar para simular efectos atmosféricos como Haze, niebla y smog mediante la difuminación de los colores del objeto a un color de fondo en función de la distancia del visor.</span><span class="sxs-lookup"><span data-stu-id="e71da-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="e71da-125">La niebla también ayuda a la percepción de distancia desde el visor, lo que permite una indicación de profundidad.</span><span class="sxs-lookup"><span data-stu-id="e71da-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="e71da-126">Vea también [Depth-cueing](d.md).</span><span class="sxs-lookup"><span data-stu-id="e71da-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71da-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**tipo**</span><span class="sxs-lookup"><span data-stu-id="e71da-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-128">Grupo de representaciones de caracteres gráficos que se suelen usar para mostrar cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="e71da-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="e71da-129">Los caracteres pueden ser letras romanos, símbolos matemáticos, ideogramas mostrados asiáticos, jeroglíficos egipcio, etc.</span><span class="sxs-lookup"><span data-stu-id="e71da-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e71da-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Fragment**</span><span class="sxs-lookup"><span data-stu-id="e71da-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-131">Datos gráficos generados por la rasterización de primitivas.</span><span class="sxs-lookup"><span data-stu-id="e71da-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="e71da-132">Cada fragmento corresponde a un solo píxel e incluye valores de color, profundidad y, a veces, valores de coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="e71da-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="e71da-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**fotogramas**</span><span class="sxs-lookup"><span data-stu-id="e71da-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-134">Una pila de bitplanes.</span><span class="sxs-lookup"><span data-stu-id="e71da-134">A stack of bitplanes.</span></span> <span data-ttu-id="e71da-135">Todos los búferes de una ventana o un contexto determinados.</span><span class="sxs-lookup"><span data-stu-id="e71da-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="e71da-136">A veces incluye toda la memoria en píxeles del acelerador de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e71da-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="e71da-137">Vea también [Bitplane](b.md).</span><span class="sxs-lookup"><span data-stu-id="e71da-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71da-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**cara frontal**</span><span class="sxs-lookup"><span data-stu-id="e71da-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-139">Vea la esfera.</span><span class="sxs-lookup"><span data-stu-id="e71da-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="e71da-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span><span class="sxs-lookup"><span data-stu-id="e71da-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="e71da-141">El volumen de la vista detorcido por la división de la perspectiva.</span><span class="sxs-lookup"><span data-stu-id="e71da-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




