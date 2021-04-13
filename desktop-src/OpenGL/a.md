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
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**
</dt> <dd>

Técnica de representación que asigna a píxeles el color de la primitiva que se está representando, tanto si el primitivo abarca todo el área del píxel como parte del mismo. El alias produce resultados en bordes dentados o jaggies. Vea también [jaggies](jk.md).

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**canal**
</dt> <dd>

Un cuarto componente de color que se suele usar para controlar la combinación de colores. El componente alfa nunca se muestra directamente. Por Convención, OpenGL Alpha indica opacidad y transparencia en una escala de 0,0 a 1,0. Un valor alfa de 1,0 implica una opacidad completa, un valor alfa de 0,0 implica una transparencia completa.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animación**
</dt> <dd>

La generación de representaciones repetidas de una escena lo suficientemente rápido, con un cambio sin problemas de punto de vista u objeto, que se consigue con la ilusión de movimiento. La animación OpenGL casi siempre usa el almacenamiento en búfer doble.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**suavizado**
</dt> <dd>

Técnica de representación que asigna colores a píxeles en función de la fracción del área de píxeles que está incluida en el primitivo que se representa. La representación con suavizado de contorno reduce o elimina el jaggies resultante de la representación con alias. Vea también [jaggies](jk.md), [representación](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**recorte específico de la aplicación** 
</dt> <dd>

Recorte de primitivas en planos en coordenadas de ojo. Los planos se especifican mediante la aplicación mediante [**glClipPlane**](glclipplane.md). Vea también [coordenadas de ojo](e.md).

</dd> </dl>

 

 




