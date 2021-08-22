---
title: C (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- equipos cliente
- memoria de cliente
- coordenadas de clip
- recortar
- índice de color
- modo de índice de color
- mapas de colores
- components
- contextos
- Convexo
- envoltura convexa
- sistema de coordenadas
- Sacrificio
- Matriz actual
- posición de trama actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39007e4719e1f4507555bf5aafa3187a897756d1d33580e9facc8fa0f6d8fa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675995"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) H [](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M N](m.md) [](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**equipo cliente**
</dt> <dd>

Equipo desde el que se emiten los comandos OpenGL. El equipo que emite comandos OpenGL se puede conectar a través de una red a otro equipo que ejecute los comandos, o bien los comandos se pueden emitir y ejecutar en el mismo equipo. Consulte también [servidor](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria de cliente**
</dt> <dd>

Memoria principal (donde se almacenan las variables de programa) del equipo cliente.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas de clip**
</dt> <dd>

Sistema de coordenadas que sigue la transformación por la matriz de proyección y precede a la división de perspectiva. El recorte de volumen de vista se realiza en coordenadas de recorte, pero el recorte específico de la aplicación no. Consulte también recorte [específico de la aplicación.](a.md)

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Recorte**
</dt> <dd>

Eliminar la parte de una primitiva geométrica que está fuera del espacio medio definido por un plano de recorte. Los puntos simplemente se rechazan si están fuera. Se elimina la parte de una línea o de un polígono que está fuera del espacio medio y se generan vértices adicionales según sea necesario para completar la primitiva dentro del espacio medio de recorte. Las primitivas geométricas y la posición de trama actual (cuando se especifican) siempre se recortan en los seis espacios medio definidos por los planos izquierdo, derecho, inferior, superior, cercano y lejano del volumen de vista. Las aplicaciones pueden especificar planos de recorte específicos de la aplicación opcionales que se aplicarán en coordenadas oculares.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**índice de color**
</dt> <dd>

Valor único que representa un color por nombre, en lugar de por valor. Los índices de color OpenGL se tratan como valores continuos (por ejemplo, números de punto flotante) mientras que en ellos se realizan operaciones como interpolación y dithering. Sin embargo, los índices de color almacenados en el búfer de fotogramas siempre son valores enteros. Los índices de punto flotante se convierten en enteros redondeando al valor entero más cercano.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de color**
</dt> <dd>

Modo de un contexto OpenGL en el que sus búferes de color almacenan índices de color, en lugar de componentes de color rojo, verde, azul y alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de colores**
</dt> <dd>

Tabla de asignaciones de índice a RGB a las que tiene acceso el hardware de presentación. Cada índice de color se lee desde el búfer de color, se convierte en un triple RGB mediante una búsqueda en el mapa de colores y se envía al monitor.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Componente**
</dt> <dd>

Valor único continuo (por ejemplo, punto flotante) que representa una intensidad o una cantidad. Normalmente, un valor de componente de cero representa el valor mínimo o la intensidad, y un valor de componente de uno representa el valor máximo o la intensidad, aunque a veces se usan otras normalizaciones. Dado que los valores de componente se interpretan en un intervalo normalizado, se especifican independientemente de la resolución real. Por ejemplo, el triple RGB (1, 1, 1) es blanco, independientemente de si los búferes de color almacenan 4, 8 o 12 bits cada uno. Los componentes fuera del intervalo normalmente se fijan al intervalo normalizado, no se truncan ni se interpretan de otro modo. Por ejemplo, el triple RGB (1,4, 1,5, 0,9) se fija en (1,0, 1,0, 0,9) antes de que se utilice para actualizar el búfer de color. Rojo, verde, azul, alfa y profundidad siempre se tratan como componentes, nunca como índices.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Contexto**
</dt> <dd>

Un conjunto completo de variables de estado OpenGL. Tenga en cuenta que el contenido del búfer de fotogramas no forma parte del estado OpenGL, pero que la configuración del búfer de fotogramas es .

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**Convexo**
</dt> <dd>

Condición de un polígono en el que ninguna línea recta en el plano del polígono forma una intersección con el polígono más de dos veces.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**casco convexa**
</dt> <dd>

La región convexa más pequeña que incluye un grupo de puntos especificado. En dos dimensiones, la casco convexa se encuentra conceptualmente mediante la extensión de una banda de hule alrededor de los puntos para que todos los puntos se encuentran dentro de la banda.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**
</dt> <dd>

En un espacio n-dimensional, conjunto de vectores n-linealmente independientes anclados a un punto (denominado origen). Un grupo de coordenadas especifica un punto en spaceEn n-dimensional space, un conjunto de n vectores independientes linealmente delimitados a un punto (denominado origen). Un grupo de coordenadas especifica un punto en el espacio (o un vector desde el origen) indicando la distancia que hay que recorrer a lo largo de cada vector para alcanzar el punto (o el extremo del vector). (o un vector del origen) indicando la distancia a la que se desplaza cada vector para alcanzar el punto (o la punta del vector).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**Sacrificio**
</dt> <dd>

Proceso de eliminación de una cara frontal o cara posterior de un polígono para que no se dibuja la cara.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**Matriz actual**
</dt> <dd>

Matriz que transforma las coordenadas de un sistema de coordenadas en coordenadas de otro sistema. Hay tres matrices actuales en OpenGL: la matriz modelview, que transforma las coordenadas de objeto (coordenadas especificadas por el programador) en coordenadas oculares. la matriz de perspectiva, que transforma las coordenadas de los ojos en coordenadas de recorte; y la matriz de textura, que transforma las coordenadas de textura especificadas o generadas como se describe en la matriz. Cada matriz actual es el elemento superior de una pila de matrices. Cada una de las tres pilas se puede manipular con comandos de manipulación de matrices OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posición de trama actual**
</dt> <dd>

Posición de coordenada de ventana que especifica la ubicación de una primitiva de imagen cuando se rasteriza. La posición de trama actual y otros parámetros de trama actuales se actualizan cuando se llama a glRasterpos.

</dd> </dl>

 

 




