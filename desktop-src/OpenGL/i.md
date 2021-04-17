---
title: I (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- primitivas de imagen
- modo inmediato
- índice
- IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533651"
---
# <a name="i-opengl"></a><span data-ttu-id="b6be5-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="b6be5-108">I (OpenGL)</span></span>

<span data-ttu-id="b6be5-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="b6be5-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="b6be5-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**impresión**</span><span class="sxs-lookup"><span data-stu-id="b6be5-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="b6be5-111">Matriz rectangular de píxeles, ya sea en la memoria del cliente o en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b6be5-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="b6be5-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**primitiva de imagen**</span><span class="sxs-lookup"><span data-stu-id="b6be5-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="b6be5-113">Mapa de bits o imagen.</span><span class="sxs-lookup"><span data-stu-id="b6be5-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="b6be5-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**modo inmediato**</span><span class="sxs-lookup"><span data-stu-id="b6be5-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="b6be5-115">Modo en el que se llama a un comando OpenGL directamente, en lugar de a partir de una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b6be5-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="b6be5-116">No existe ningún bit de modo inmediato; el modo en modo inmediato hace referencia al uso de OpenGL, en lugar de a un bit específico del estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b6be5-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="b6be5-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**ajustar**</span><span class="sxs-lookup"><span data-stu-id="b6be5-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="b6be5-118">Un valor único que se interpreta como un valor absoluto, en lugar de como un valor normalizado en un intervalo especificado (como un componente).</span><span class="sxs-lookup"><span data-stu-id="b6be5-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="b6be5-119">Los índices de color son los nombres de los colores a los que se desreferencia el hardware de pantalla mediante el mapa de colores.</span><span class="sxs-lookup"><span data-stu-id="b6be5-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="b6be5-120">Los índices normalmente se enmascaran, en lugar de estar fijados, cuando están fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b6be5-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="b6be5-121">Por ejemplo, el índice 0xf7 se enmascara a 0X7 cuando se escribe en un búfer de 4 bits (color o galería de símbolos).</span><span class="sxs-lookup"><span data-stu-id="b6be5-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="b6be5-122">Los índices de color y los índices de estarcido siempre se tratan como índices, nunca como componentes.</span><span class="sxs-lookup"><span data-stu-id="b6be5-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="b6be5-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span><span class="sxs-lookup"><span data-stu-id="b6be5-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="b6be5-124">Biblioteca de gráficos patentada de Silicon Graphics, desarrollada de 1982 a 1992.</span><span class="sxs-lookup"><span data-stu-id="b6be5-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="b6be5-125">OpenGL se diseñó con IRIS GL como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="b6be5-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




