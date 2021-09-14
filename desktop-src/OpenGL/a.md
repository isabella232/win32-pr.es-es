---
title: A (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- Aliasing
- alpha
- animación
- suavizado de contorno
- recorte específico de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245048"
---
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](g.md) [I](h.md) [](i.md) [J K](jk.md) L [M](l.md) [N](m.md) [O](n.md) [](o.md) [P P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**Aliasing**
</dt> <dd>

Técnica de representación que asigna a píxeles el color de la primitiva que se representa, independientemente de si esa primitiva cubre todo o parte del área del píxel. El alias da como resultado bordes irregulares o jajajas. Consulte también [japones](jk.md).

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**
</dt> <dd>

Un cuarto componente de color que se usa normalmente para controlar la combinación de colores. El componente alfa nunca se muestra directamente. Por convención, OpenGL alpha indica opacidad y transparencia en una escala de 0,0 a 1,0. Un valor alfa de 1,0 implica una opacidad completa, un valor alfa de 0,0 implica una transparencia completa.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animación**
</dt> <dd>

La generación de representaciones repetidas de una escena lo suficientemente rápido, con puntos de vista u posiciones de objeto que cambian sin problemas, que se logra la sensación de movimiento. La animación OpenGL casi siempre usa el almacenamiento en búfer doble.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**Antialiasing**
</dt> <dd>

Técnica de representación que asigna colores a píxeles en función de la fracción del área de píxeles cubierta por la primitiva que se representa. La representación con suavizado de contorno reduce o elimina los japones resultantes de la representación con alias. Consulte también [ja renders](jk.md), [rendering](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**recorte específico de la aplicación** 
</dt> <dd>

Recorte de primitivas en planos en coordenadas de los ojos. La aplicación especifica los planos mediante [**glClipPlane.**](glclipplane.md) Vea también las [coordenadas de los ojos.](e.md)

</dd> </dl>

 

 




