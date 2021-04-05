---
title: C (OpenGL)
description: Definiciones de términos de OpenGL que comienzan por la letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- equipos cliente
- memoria de cliente
- coordenadas de recorte
- recortar
- Índice de color
- modo de índice de color
- mapas de colores
- components
- contextos
- tengan
- envoltura convexa
- sistema de coordenadas
- selección
- matriz actual
- posición de la trama actual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078764"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [o](o.md) [p](p.md) [Q](q.md) [R](r.md) [s](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**equipo cliente**
</dt> <dd>

El equipo desde el que se emiten los comandos de OpenGL. El equipo que emite comandos OpenGL se puede conectar a través de una red a otro equipo que ejecute los comandos, o bien se pueden emitir y ejecutar comandos en el mismo equipo. Vea también [servidor](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria de cliente**
</dt> <dd>

La memoria principal (donde se almacenan las variables de programa) del equipo cliente.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas de recorte**
</dt> <dd>

El sistema de coordenadas que sigue la transformación por la matriz de proyección y precede a la división de la perspectiva. Vista: el recorte del volumen se realiza en las coordenadas del clip, pero no en el recorte específico de la aplicación. Vea también [recorte específico de la aplicación](a.md).

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**salte**
</dt> <dd>

Eliminar la parte de una primitiva geométrica que está fuera del espacio medio definido por un plano de recorte. Los puntos simplemente se rechazan si están fuera. Se elimina la parte de una línea o de un polígono que se encuentra fuera del espacio medio, y se generan vértices adicionales según sea necesario para completar el primitivo dentro de la mitad del espacio de recorte. Las primitivas geométricas y la posición de la trama actual (cuando se especifica) siempre se recortan en los seis semiespacios definidos por los planos izquierdo, derecho, inferior, superior, Near y Far del volumen de la vista. Las aplicaciones pueden especificar los planos de recorte específicos de la aplicación opcionales que se van a aplicar en coordenadas oculares.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**Índice de color**
</dt> <dd>

Un valor único que representa un color por nombre, en lugar de por valor. Los índices de color de OpenGL se tratan como valores continuos (por ejemplo, números de punto flotante) mientras que las operaciones como la interpolación y el tramado se realizan en ellos. Sin embargo, los índices de color almacenados en el búfer de fotogramas son siempre valores enteros. Los índices de punto flotante se convierten en enteros redondeando al valor entero más cercano.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de color**
</dt> <dd>

Modo de contexto de OpenGL en el que sus búferes de color almacenan índices de color, en lugar de componentes de color rojo, verde, azul y alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de colores**
</dt> <dd>

Una tabla de asignaciones de índice a RGB a la que se tiene acceso mediante el hardware de pantalla. Cada índice de color se lee desde el búfer de color, se convierte en un triple por búsqueda en el mapa de colores y se envía al monitor.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**pone**
</dt> <dd>

Un valor único, continuo (por ejemplo, punto flotante) que representa una intensidad o una cantidad. Normalmente, un valor de componente de cero representa el valor o la intensidad mínimos y un valor de componente de uno representa el valor o la intensidad máximos, aunque a veces se usan otras normalización. Dado que los valores de componente se interpretan en un intervalo normalizado, se especifican independientemente de la resolución real. Por ejemplo, el triple RGB (1,1) es blanco, independientemente de si los búferes de color almacenan 4, 8 o 12 bits cada uno. Los componentes fuera del intervalo se fijan normalmente en el intervalo normalizado, no se truncan ni se interpretan de otra manera. Por ejemplo, el triple RGB (1,4, 1,5, 0,9) se fija a (1,0, 1,0, 0,9) antes de que se use para actualizar el búfer de color. Rojo, verde, azul, alfa y profundidad siempre se tratan como componentes, nunca como índices.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contexto**
</dt> <dd>

Un conjunto completo de variables de estado de OpenGL. Tenga en cuenta que el contenido de fotogramas no forma parte del estado de OpenGL, pero que la configuración de fotogramas es.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**tengan**
</dt> <dd>

Condición de un polígono en el que ninguna línea recta del plano del polígono forma una intersección con el polígono más de dos veces.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**casco convexo**
</dt> <dd>

La región convexa más pequeña que incluye un grupo de puntos especificado. En dos dimensiones, el casco convexo se encuentra conceptualmente mediante la expansión de una banda elástica alrededor de los puntos para que todos los puntos se encuentren dentro de la banda.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**
</dt> <dd>

En un espacio n-dimensional, conjunto de vectores n-linealmente independientes anclados a un punto (denominado origen). Un grupo de coordenadas especifica un punto en el espacio de n dimensiones, un conjunto de n vectores de forma lineal anclados a un punto (denominado origen). Un grupo de coordenadas especifica un punto en el espacio (o un vector desde el origen) indicando la distancia que hay que recorrer a lo largo de cada vector para alcanzar el punto (o el extremo del vector). (o un vector desde el origen) indicando la distancia que hay que recorrer a lo largo de cada vector para alcanzar el punto (o la punta del vector).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**selección**
</dt> <dd>

El proceso de eliminación de una cara frontal o de una cara posterior de un polígono para que no se dibuje la cara.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matriz actual**
</dt> <dd>

Matriz que transforma las coordenadas de un sistema de coordenadas en coordenadas de otro sistema. Hay tres matrices actuales en OpenGL: la matriz MODELVIEW, que transforma las coordenadas de objeto (coordenadas especificadas por el programador) en coordenadas oculares; la matriz de perspectiva, que transforma las coordenadas del ojo en coordenadas de recorte. y la matriz de textura, que transforma las coordenadas de textura especificadas o generadas como se describe en la matriz. Cada matriz actual es el elemento superior de una pila de matrices. Cada una de las tres pilas se puede manipular con comandos de manipulación de matrices de OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posición de la trama actual**
</dt> <dd>

Una posición de la coordenada de la ventana que especifica la posición de una primitiva de imagen cuando se rasteriza. La posición de la trama actual y otros parámetros de Raster actuales se actualizan cuando se llama a glRasterpos.

</dd> </dl>

 

 




