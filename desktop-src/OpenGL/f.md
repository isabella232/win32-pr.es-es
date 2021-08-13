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
- front-face
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 748eb0fade84ef76c133453165db53d8540326dae3111ac04f3b7a6819ae825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618190"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F G [H](g.md) [I](h.md) [](i.md) [J K](jk.md) L [M](l.md) [N](m.md) [O](n.md) [](o.md) [P P](p.md) [](q.md) [Q R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Cara**
</dt> <dd>

Un lado de un polígono. Cada polígono tiene dos caras: una cara frontal y una cara posterior. Solo una cara es visible en la ventana. Si la cara posterior o frontal está visible se determina de forma eficaz después de que el polígono se proyecte en la ventana. Después de esta proyección, si los bordes del polígono se dirigen en el sentido de las agujas del reloj, una de las caras está visible; si se dirige en sentido contrario a las agujas del reloj, la otra cara está visible. El programador de OpenGL determina si el sentido de las agujas del reloj corresponde a delante o atrás (y en sentido contrario a las agujas del reloj se corresponde con atrás o delante).

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**sombreado plano**
</dt> <dd>

Hace referencia a la coloración de una primitiva con un único color constante en toda su extensión, en lugar de interpolar colores sin problemas en la primitiva. Vea [Sombreado de Gouraud.](g.md)

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Niebla**
</dt> <dd>

Técnica de representación que se puede usar para simular efectos atmosféricos, como la bruma, el ruido y el eslaz, mediante la desvanecha de los colores de objeto a un color de fondo basado en la distancia desde el visor. La cola también ayuda a la percepción de la distancia desde el visor, lo que proporciona una indicación de profundidad. Consulte también [indicaciones de profundidad.](d.md)

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Fuente**
</dt> <dd>

Grupo de representaciones gráficas de caracteres que normalmente se usan para mostrar cadenas de texto. Los caracteres pueden ser letras román, símbolos matemáticos, ideogramas asiáticos, hieroglyphs desfasados, y así sucesivamente.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Fragmento**
</dt> <dd>

Datos gráficos generados por la rasterización de primitivas. Cada fragmento corresponde a un solo píxel e incluye valores de color, profundidad y, a veces, coordenadas de textura.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Framebuffer**
</dt> <dd>

Una pila de planos de bits. Todos los búferes de una ventana o contexto determinados. A veces incluye toda la memoria de píxeles del acelerador de hardware gráfico. Consulte también [bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front-face**
</dt> <dd>

Ver cara.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**
</dt> <dd>

Volumen de vista deformado por la división de perspectiva.

</dd> </dl>

 

 




