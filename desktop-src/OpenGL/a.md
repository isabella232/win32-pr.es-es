---
title: A (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- alias
- alpha
- animación
- suavizado de contorno
- recorte específico de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421835"
---
# <a name="a-opengl"></a><span data-ttu-id="b2b4f-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="b2b4f-108">A (OpenGL)</span></span>

<span data-ttu-id="b2b4f-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="b2b4f-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="b2b4f-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**</span><span class="sxs-lookup"><span data-stu-id="b2b4f-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="b2b4f-111">Técnica de representación que asigna a píxeles el color de la primitiva que se está representando, tanto si el primitivo abarca todo el área del píxel como parte del mismo.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="b2b4f-112">El alias produce resultados en bordes dentados o jaggies.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="b2b4f-113">Vea también [jaggies](jk.md).</span><span class="sxs-lookup"><span data-stu-id="b2b4f-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b4f-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**canal**</span><span class="sxs-lookup"><span data-stu-id="b2b4f-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="b2b4f-115">Un cuarto componente de color que se suele usar para controlar la combinación de colores.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="b2b4f-116">El componente alfa nunca se muestra directamente.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="b2b4f-117">Por Convención, OpenGL Alpha indica opacidad y transparencia en una escala de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="b2b4f-118">Un valor alfa de 1,0 implica una opacidad completa, un valor alfa de 0,0 implica una transparencia completa.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="b2b4f-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animación**</span><span class="sxs-lookup"><span data-stu-id="b2b4f-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="b2b4f-120">La generación de representaciones repetidas de una escena lo suficientemente rápido, con un cambio sin problemas de punto de vista u objeto, que se consigue con la ilusión de movimiento.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="b2b4f-121">La animación OpenGL casi siempre usa el almacenamiento en búfer doble.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="b2b4f-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**suavizado**</span><span class="sxs-lookup"><span data-stu-id="b2b4f-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="b2b4f-123">Técnica de representación que asigna colores a píxeles en función de la fracción del área de píxeles que está incluida en el primitivo que se representa.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="b2b4f-124">La representación con suavizado de contorno reduce o elimina el jaggies resultante de la representación con alias.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="b2b4f-125">Vea también [jaggies](jk.md), [representación](r.md).</span><span class="sxs-lookup"><span data-stu-id="b2b4f-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2b4f-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**recorte específico de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="b2b4f-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="b2b4f-127">Recorte de primitivas en planos en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="b2b4f-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="b2b4f-128">Los planos se especifican mediante la aplicación mediante [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="b2b4f-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="b2b4f-129">Vea también [coordenadas de ojo](e.md).</span><span class="sxs-lookup"><span data-stu-id="b2b4f-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




