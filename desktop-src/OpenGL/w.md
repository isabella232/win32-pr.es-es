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
# <a name="w-opengl"></a>W (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**ventana**
</dt> <dd>

Subregión de fotogramas, normalmente rectangular, cuyos píxeles tienen la misma configuración de búfer. Un contexto de OpenGL se representa en una ventana a la vez.

</dd> <dt>

<span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**alineado por ventana**
</dt> <dd>

Cuando se hace referencia a segmentos de línea o bordes de polígono, implica que son paralelos a los límites de la ventana. (En OpenGL, la ventana es rectangular, con bordes horizontales y verticales). Cuando se hace referencia a un patrón de polígono, implica que el patrón es fijo en relación con el origen de la ventana.

</dd> <dt>

<span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**coordenadas de la ventana**
</dt> <dd>

El sistema de coordenadas de una ventana. Es importante distinguir entre los nombres de los píxeles, que son discretos, y el sistema de coordenadas de ventana, que es continuo. Por ejemplo, el píxel en la esquina inferior izquierda de una ventana es píxel (0,0); las coordenadas de la ventana del centro de este píxel son (0,5, 0,5, z). Tenga en cuenta que las coordenadas de la ventana incluyen un componente Depth, o z, y que este componente también es continuo.

</dd> <dt>

<span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**estructura**
</dt> <dd>

Representación de un objeto que contiene solo segmentos de línea. Normalmente, los segmentos de línea indican bordes de polígono.

</dd> </dl>

 

 




