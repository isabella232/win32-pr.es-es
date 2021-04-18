---
title: F (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- sombreado plano
- luz
- fuentes
- fragments
- framebuffers
- cara frontal
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676541"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Portada**
</dt> <dd>

Un lado de un polígono. Cada polígono tiene dos caras: una cara frontal y otra cara. Solo una de las caras está visible en la ventana. El hecho de que la cara trasera o frontal esté visible se determina de forma eficaz una vez que se proyecta el polígono en la ventana. Después de esta proyección, si los bordes del polígono se dirigen a la derecha, una de las caras es visible; Si se dirige en sentido contrario a las agujas del reloj, el otro aspecto es visible. Tanto si el reloj se corresponde hacia delante como hacia atrás (y en sentido contrario a las agujas del reloj), lo determina el programador de OpenGL.

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**sombreado plano**
</dt> <dd>

Hace referencia a la coloración de un tipo primitivo con un único color constante a lo largo de su extensión, en lugar de interpolar sin problemas los colores en el primitivo. Vea [sombreado Gouraud](g.md).

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**luz**
</dt> <dd>

Técnica de representación que se puede usar para simular efectos atmosféricos como Haze, niebla y smog mediante la difuminación de los colores del objeto a un color de fondo en función de la distancia del visor. La niebla también ayuda a la percepción de distancia desde el visor, lo que permite una indicación de profundidad. Vea también [Depth-cueing](d.md).

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**tipo**
</dt> <dd>

Grupo de representaciones de caracteres gráficos que se suelen usar para mostrar cadenas de texto. Los caracteres pueden ser letras romanos, símbolos matemáticos, ideogramas mostrados asiáticos, jeroglíficos egipcio, etc.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Fragment**
</dt> <dd>

Datos gráficos generados por la rasterización de primitivas. Cada fragmento corresponde a un solo píxel e incluye valores de color, profundidad y, a veces, valores de coordenada de textura.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**fotogramas**
</dt> <dd>

Una pila de bitplanes. Todos los búferes de una ventana o un contexto determinados. A veces incluye toda la memoria en píxeles del acelerador de hardware de gráficos. Vea también [Bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**cara frontal**
</dt> <dd>

Vea la esfera.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**
</dt> <dd>

El volumen de la vista detorcido por la división de la perspectiva.

</dd> </dl>

 

 




