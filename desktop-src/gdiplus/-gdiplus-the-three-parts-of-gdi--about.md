---
description: 'Los servicios de Windows GDI+ se dividen en las siguientes tres amplias categorías:'
ms.assetid: d5bef8e4-7a4c-4ac4-938a-7034ad3d743f
title: Las tres partes de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2021260e9fe3b3d927131c2ba1856aeed0ed07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997457"
---
# <a name="the-three-parts-of-gdi"></a>Las tres partes de GDI+

Los servicios de Windows GDI+ se dividen en las siguientes tres amplias categorías:

-   [gráficos vectoriales 2D](#2-d-vector-graphics)
-   [Creación de imágenes](#imaging)
-   [Tipografía](#typography)

## <a name="2-d-vector-graphics"></a>gráficos vectoriales 2D

Los gráficos vectoriales implican el dibujo de primitivas (como líneas, curvas y figuras) que se especifican mediante conjuntos de puntos en un sistema de coordenadas. Por ejemplo, una línea recta puede especificarse mediante sus dos puntos de conexión y un rectángulo puede especificarse mediante un punto que proporcione la ubicación de la esquina superior izquierda y un par de números que den su ancho y alto. Una ruta de acceso simple puede especificarse mediante una matriz de puntos que se va a conectar mediante líneas rectas. Una curva spline de Bézier es una curva sofisticada especificada por cuatro puntos de control.

GDI+ proporciona clases que almacenan información sobre los propios tipos primitivos, las clases que almacenan información sobre cómo se van a dibujar los primitivos y las clases que realmente realizan el dibujo. Por ejemplo, la clase **Rect** almacena la ubicación y el tamaño de un rectángulo. la clase **Pen** almacena información sobre el color de línea, el ancho de línea y el estilo de línea; y la clase **Graphics** tiene métodos para dibujar líneas, rectángulos, trazados y otras figuras. También hay varias clases **Brush** que almacenan información sobre cómo se van a rellenar las figuras y trazados cerrados con colores o patrones.

## <a name="imaging"></a>Creación de imágenes

Ciertos tipos de imágenes son difíciles o imposibles de mostrar con las técnicas de gráficos vectoriales. Por ejemplo, las imágenes de los botones de la barra de herramientas y las imágenes que aparecen como iconos serían difíciles de especificar como colecciones de líneas y curvas. Una fotografía digital de alta resolución de un estadio de béisbol abarrotado sería aún más difícil de crear con técnicas vectoriales. Las imágenes de este tipo se almacenan como mapas de bits, matrices de números que representan los colores de los puntos individuales de la pantalla. Las estructuras de datos que almacenan información sobre los mapas de bits suelen ser más complejas que las necesarias para los gráficos vectoriales, por lo que hay varias clases en GDI+ dedicadas a este propósito. Un ejemplo de este tipo de clase es **CachedBitmap**, que se usa para almacenar un mapa de bits en la memoria para obtener un acceso rápido y mostrarlo.

## <a name="typography"></a>Tipografía

La tipografía está relacionada con la presentación de texto en una variedad de fuentes, tamaños y estilos. GDI+ proporciona una cantidad impresionante de compatibilidad para esta tarea compleja. Una de las nuevas características de GDI+ es el suavizado de contorno de subpíxeles, que proporciona un aspecto más suave al texto representado en una pantalla LCD.

 

 



