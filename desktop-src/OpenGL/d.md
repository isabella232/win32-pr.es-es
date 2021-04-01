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
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**amplia**
</dt> <dd>

Normalmente hace referencia a la coordenada de la ventana z.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**profundidad cueing**
</dt> <dd>

Técnica de representación que asigna color en función de la distancia desde el punto de vista.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**Mostrar lista**
</dt> <dd>

Lista con nombre de comandos de OpenGL. Las listas de visualización siempre se almacenan en el servidor, por lo que las listas de visualización se pueden usar para reducir el tráfico de red en entornos cliente/servidor. El contenido de una lista de visualización se puede preprocesar y, por tanto, se puede ejecutar de forma más eficaz que el mismo conjunto de comandos OpenGL que se ejecutan en modo inmediato. Este preprocesamiento es especialmente importante para computar comandos intensivos como [**glTexImage**](glteximage1d.md).

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**interpolación**
</dt> <dd>

Técnica para aumentar el intervalo de colores percibido en una imagen a costa de la resolución espacial. A los píxeles adyacentes se les asignan valores de color diferentes. Cuando se ven desde una distancia, estos colores parecen fusionarse en un solo color intermedio. La técnica es similar a la mitad del tono que se usa en las publicaciones en blanco y negro para conseguir tonalidades de gris.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**doble búfer**
</dt> <dd>

Usar contextos de OpenGL en los que los búferes de color delantero y de fondo se almacenan en búfer doble. La animación suave se logra mediante la representación solo en el búfer de reserva (que no se muestra), lo que hace que se intercambien los búferes frontal y trasero.

</dd> </dl>

 

 




