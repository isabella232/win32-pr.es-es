---
title: D (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- profundidad cueing
- Mostrar listas
- interpolación
- doble búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800775"
---
# <a name="d-opengl"></a><span data-ttu-id="98b89-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="98b89-108">D (OpenGL)</span></span>

<span data-ttu-id="98b89-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="98b89-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="98b89-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**amplia**</span><span class="sxs-lookup"><span data-stu-id="98b89-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="98b89-111">Normalmente hace referencia a la coordenada de la ventana z.</span><span class="sxs-lookup"><span data-stu-id="98b89-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="98b89-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**profundidad cueing**</span><span class="sxs-lookup"><span data-stu-id="98b89-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="98b89-113">Técnica de representación que asigna color en función de la distancia desde el punto de vista.</span><span class="sxs-lookup"><span data-stu-id="98b89-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="98b89-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**Mostrar lista**</span><span class="sxs-lookup"><span data-stu-id="98b89-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="98b89-115">Lista con nombre de comandos de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="98b89-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="98b89-116">Las listas de visualización siempre se almacenan en el servidor, por lo que las listas de visualización se pueden usar para reducir el tráfico de red en entornos cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="98b89-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="98b89-117">El contenido de una lista de visualización se puede preprocesar y, por tanto, se puede ejecutar de forma más eficaz que el mismo conjunto de comandos OpenGL que se ejecutan en modo inmediato.</span><span class="sxs-lookup"><span data-stu-id="98b89-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="98b89-118">Este preprocesamiento es especialmente importante para computar comandos intensivos como [**glTexImage**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="98b89-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="98b89-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**interpolación**</span><span class="sxs-lookup"><span data-stu-id="98b89-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="98b89-120">Técnica para aumentar el intervalo de colores percibido en una imagen a costa de la resolución espacial.</span><span class="sxs-lookup"><span data-stu-id="98b89-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="98b89-121">A los píxeles adyacentes se les asignan valores de color diferentes.</span><span class="sxs-lookup"><span data-stu-id="98b89-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="98b89-122">Cuando se ven desde una distancia, estos colores parecen fusionarse en un solo color intermedio.</span><span class="sxs-lookup"><span data-stu-id="98b89-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="98b89-123">La técnica es similar a la mitad del tono que se usa en las publicaciones en blanco y negro para conseguir tonalidades de gris.</span><span class="sxs-lookup"><span data-stu-id="98b89-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="98b89-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**doble búfer**</span><span class="sxs-lookup"><span data-stu-id="98b89-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="98b89-125">Usar contextos de OpenGL en los que los búferes de color delantero y de fondo se almacenan en búfer doble.</span><span class="sxs-lookup"><span data-stu-id="98b89-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="98b89-126">La animación suave se logra mediante la representación solo en el búfer de reserva (que no se muestra), lo que hace que se intercambien los búferes frontal y trasero.</span><span class="sxs-lookup"><span data-stu-id="98b89-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




