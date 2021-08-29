---
title: D (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- indicaciones de profundidad
- mostrar listas
- Tramado
- doble búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebc4d797371a966020fbdaff3d62d845ecbbfdc5f21f6e37393e01b2defad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554625"
---
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) G [H](g.md) [I](h.md) [](i.md) [J K](jk.md) L [M](l.md) [N](m.md) [O](n.md) [](o.md) [P P](p.md) [](q.md) [Q R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**Profundidad**
</dt> <dd>

Por lo general, hace referencia a la coordenada de la ventana z.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**indicaciones de profundidad**
</dt> <dd>

Técnica de representación que asigna color en función de la distancia desde el punto de vista.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**mostrar lista**
</dt> <dd>

Lista con nombre de comandos OpenGL. Las listas de presentación siempre se almacenan en el servidor, por lo que se pueden usar listas de presentación para reducir el tráfico de red en entornos cliente/servidor. El contenido de una lista de visualización se puede preprocesar y, por tanto, podría ejecutarse de forma más eficaz que el mismo conjunto de comandos OpenGL ejecutados en modo inmediato. Este preprocesamiento es especialmente importante para calcular comandos intensivos, como [**glTexImage.**](glteximage1d.md)

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**Tramado**
</dt> <dd>

Técnica para aumentar el rango percibido de colores de una imagen a costa de la resolución espacial. A los píxeles adyacentes se les asignan valores de color diferentes. Cuando se ven desde una distancia, estos colores parecen combinarse en un único color intermedio. La técnica es similar a la media toning que se usa en las publicaciones en blanco y negro para lograr tonos de gris.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**almacenamiento en búfer doble**
</dt> <dd>

Uso de contextos OpenGL en los que los búferes de color frontal y posterior están almacenados en doble búfer. La animación suave se logra mediante la representación solo en el búfer de reserva (que no se muestra) y, a continuación, provoca el intercambio de los búferes de entrada y de atrás.

</dd> </dl>

 

 




