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
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245036"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) H [](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M N](m.md) [](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Cara**
</dt> <dd>

Un lado de un polígono. Cada polígono tiene dos caras: una cara frontal y una cara posterior. Solo se puede ver una cara en la ventana. Si la cara posterior o frontal está visible se determina de forma eficaz después de que el polígono se proyecte en la ventana. Después de esta proyección, si los bordes del polígono se dirigen en el sentido de las agujas del reloj, una de las caras está visible; si se dirige en sentido contrario a las agujas del reloj, la otra cara está visible. El programador de OpenGL determina si corresponde en el sentido de las agujas del reloj a la parte delantera (y en sentido contrario a la parte posterior o frontal).

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**sombreado plano**
</dt> <dd>

Hace referencia a la coloración de una primitiva con un único color constante en toda su extensión, en lugar de interpolar los colores sin problemas en la primitiva. Consulte [Sombreado de Gouraud.](g.md)

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Niebla**
</dt> <dd>

Técnica de representación que se puede usar para simular efectos atmosféricos, como la haze, la desvanecha y el desvaneo de los colores de objeto a un color de fondo en función de la distancia desde el visor. La música también ayuda a la percepción de la distancia desde el visor, lo que proporciona una indicación de profundidad. Consulte también [la indicación de profundidad](d.md).

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Fuente**
</dt> <dd>

Un grupo de representaciones de caracteres gráficos que normalmente se usan para mostrar cadenas de texto. Los caracteres pueden ser letras de román, símbolos matemáticos, ideogramas asiáticos, hieroglyphs desasociables, y así sucesivamente.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Fragmento**
</dt> <dd>

Datos gráficos generados por la rasterización de primitivas. Cada fragmento corresponde a un solo píxel e incluye valores de color, profundidad y, a veces, de coordenadas de textura.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Framebuffer**
</dt> <dd>

Pila de bitplanes. Todos los búferes de una ventana o contexto determinados. A veces incluye toda la memoria de píxeles del acelerador de hardware gráfico. Consulte también [bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front-face**
</dt> <dd>

Ver cara.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**
</dt> <dd>

Volumen de vista deformado por división de perspectiva.

</dd> </dl>

 

 




