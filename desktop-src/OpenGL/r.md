---
title: R (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- rasterización
- rectángulos
- rendering
- RGBA
- Modo RGBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904943"
---
# <a name="r-opengl"></a><span data-ttu-id="230cf-108">R (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="230cf-108">R (OpenGL)</span></span>

<span data-ttu-id="230cf-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) R [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="230cf-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="230cf-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterizador**</span><span class="sxs-lookup"><span data-stu-id="230cf-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="230cf-111">Para convertir un punto, línea o polígono proyectado, o los píxeles de un mapa de bits o imagen, en fragmentos, cada uno de los cuales corresponde a un píxel en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="230cf-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="230cf-112">Tenga en cuenta que se rasterizan todos los primitivos, no solo los puntos, líneas y polígonos.</span><span class="sxs-lookup"><span data-stu-id="230cf-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="230cf-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectángulo**</span><span class="sxs-lookup"><span data-stu-id="230cf-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="230cf-114">Cuadrangular cuyos bordes alternativos son paralelos entre sí en coordenadas de objeto.</span><span class="sxs-lookup"><span data-stu-id="230cf-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="230cf-115">Los polígonos especificados con glRect \* () siempre son rectángulos; otros quadrilaterals podrían ser rectángulos.</span><span class="sxs-lookup"><span data-stu-id="230cf-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="230cf-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**representación**</span><span class="sxs-lookup"><span data-stu-id="230cf-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="230cf-117">Conversión de primitivas especificadas en coordenadas de objeto en una imagen de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="230cf-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="230cf-118">La representación es la operación principal de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="230cf-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="230cf-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="230cf-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="230cf-120">Los componentes de color rojo, verde, azul y alfa del modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="230cf-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="230cf-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**Modo RGBA**</span><span class="sxs-lookup"><span data-stu-id="230cf-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="230cf-122">Contexto de OpenGL en el que sus búferes de color almacenan componentes de color rojo, verde, azul y alfa, en lugar de índices de color.</span><span class="sxs-lookup"><span data-stu-id="230cf-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 




