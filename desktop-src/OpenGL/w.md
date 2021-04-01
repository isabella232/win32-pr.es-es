---
title: W (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- Windows
- alineado por ventana
- coordenadas de la ventana
- estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800607"
---
# <a name="w-opengl"></a><span data-ttu-id="1c946-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="1c946-107">W (OpenGL)</span></span>

<span data-ttu-id="1c946-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="1c946-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="1c946-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**ventana**</span><span class="sxs-lookup"><span data-stu-id="1c946-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="1c946-110">Subregión de fotogramas, normalmente rectangular, cuyos píxeles tienen la misma configuración de búfer.</span><span class="sxs-lookup"><span data-stu-id="1c946-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="1c946-111">Un contexto de OpenGL se representa en una ventana a la vez.</span><span class="sxs-lookup"><span data-stu-id="1c946-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="1c946-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**alineado por ventana**</span><span class="sxs-lookup"><span data-stu-id="1c946-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="1c946-113">Cuando se hace referencia a segmentos de línea o bordes de polígono, implica que son paralelos a los límites de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1c946-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="1c946-114">(En OpenGL, la ventana es rectangular, con bordes horizontales y verticales).</span><span class="sxs-lookup"><span data-stu-id="1c946-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="1c946-115">Cuando se hace referencia a un patrón de polígono, implica que el patrón es fijo en relación con el origen de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1c946-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="1c946-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**coordenadas de la ventana**</span><span class="sxs-lookup"><span data-stu-id="1c946-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="1c946-117">El sistema de coordenadas de una ventana.</span><span class="sxs-lookup"><span data-stu-id="1c946-117">The coordinate system of a window.</span></span> <span data-ttu-id="1c946-118">Es importante distinguir entre los nombres de los píxeles, que son discretos, y el sistema de coordenadas de ventana, que es continuo.</span><span class="sxs-lookup"><span data-stu-id="1c946-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="1c946-119">Por ejemplo, el píxel en la esquina inferior izquierda de una ventana es píxel (0,0); las coordenadas de la ventana del centro de este píxel son (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="1c946-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="1c946-120">Tenga en cuenta que las coordenadas de la ventana incluyen un componente Depth, o z, y que este componente también es continuo.</span><span class="sxs-lookup"><span data-stu-id="1c946-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="1c946-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**estructura**</span><span class="sxs-lookup"><span data-stu-id="1c946-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="1c946-122">Representación de un objeto que contiene solo segmentos de línea.</span><span class="sxs-lookup"><span data-stu-id="1c946-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="1c946-123">Normalmente, los segmentos de línea indican bordes de polígono.</span><span class="sxs-lookup"><span data-stu-id="1c946-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




