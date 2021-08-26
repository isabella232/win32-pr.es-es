---
description: 'Los servicios de Windows GDI+ en las tres categorías generales siguientes:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Las tres partes de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5547702ca98cce86ace0f672b7aeed2dc8fc0ecee63534aaa15fac05bdcb024b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014655"
---
# <a name="the-three-parts-of-gdi"></a>Las tres partes de GDI+

Los servicios de Windows GDI+ en las tres categorías generales siguientes:

-   [gráficos vectoriales 2D](#2-d-vector-graphics)
-   [Creación de imágenes](#imaging)
-   [Tipografía](#typography)

## <a name="2-d-vector-graphics"></a>gráficos vectoriales 2D

Los gráficos vectoriales implican dibujar primitivas (como líneas, curvas y figuras) que se especifican mediante conjuntos de puntos en un sistema de coordenadas. Por ejemplo, sus dos puntos de conexión pueden especificar una línea recta y un rectángulo se puede especificar mediante un punto que da la ubicación de su esquina superior izquierda y un par de números que dan su ancho y alto. Una ruta de acceso simple se puede especificar mediante una matriz de puntos que se conectarán mediante líneas rectas. Una curva spline de Bézier es una curva sofisticada especificada por cuatro puntos de control.

GDI+ proporciona clases que almacenan información sobre los propios primitivos, clases que almacenan información sobre cómo se van a dibujar las primitivas y clases que realmente hacen el dibujo. Por ejemplo, la **clase Rect** almacena la ubicación y el tamaño de un rectángulo; la **clase Pen** almacena información sobre el color de línea, el ancho de línea y el estilo de línea; y la **clase Graphics** tiene métodos para dibujar líneas, rectángulos, trazados y otras figuras. También hay varias clases **Brush** que almacenan información sobre cómo se van a rellenar las figuras cerradas y las rutas de acceso con colores o patrones.

## <a name="imaging"></a>Creación de imágenes

Ciertos tipos de imágenes son difíciles o imposibles de mostrar con las técnicas de gráficos vectoriales. Por ejemplo, las imágenes de los botones de la barra de herramientas y las imágenes que aparecen como iconos serían difíciles de especificar como colecciones de líneas y curvas. Una fotografía digital de alta resolución de un partido de béisbol abarrotado sería incluso más difícil de crear con técnicas vectoriales. Las imágenes de este tipo se almacenan como mapas de bits, matrices de números que representan los colores de puntos individuales en la pantalla. Las estructuras de datos que almacenan información sobre mapas de bits tienden a ser más complejas que las necesarias para los gráficos vectoriales, por lo que hay varias clases en GDI+ dedicadas a este propósito. Un ejemplo de este tipo de clase es **CachedBitmap**, que se usa para almacenar un mapa de bits en memoria para un acceso y una visualización rápidos.

## <a name="typography"></a>Tipografía

La tipografía se refiere a la presentación de texto en una variedad de fuentes, tamaños y estilos. GDI+ proporciona una gran cantidad de compatibilidad para esta tarea compleja. Una de las nuevas características de GDI+ es el suavizado de contorno de subpíxeles, que proporciona un aspecto más suave al texto representado en una pantalla DE LAC.

 

 



