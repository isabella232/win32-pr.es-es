---
description: Un mapa de bits es uno de los objetos GDI que se pueden seleccionar en un contexto de dispositivo (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Acerca de los mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb155a2d96b32303c38438663cb7cc9b893a1560e8f33956ff894d309f055010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355515"
---
# <a name="about-bitmaps"></a>Acerca de los mapas de bits

Un mapa de bits es uno de los objetos GDI que se pueden seleccionar en un *contexto de dispositivo* (DC). [Los contextos de dispositivo](device-contexts.md) son estructuras que definen un conjunto de objetos gráficos y sus atributos asociados, y modos gráficos que afectan a la salida. En la tabla siguiente se describen los objetos GDI que se pueden seleccionar en un contexto de dispositivo.



| Objeto gráfico                         | Descripción                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapas de bits](bitmaps.md)                 | Crea, manipula (escala, desplazamiento, rotación y pintura) y almacena imágenes como archivos en un disco.                                                                                                       |
| [Pinceles](brushes.md)                 | Pinta el interior de polígonos, puntos suspensivos y trazados.                                                                                                                                                |
| [Fuentes](fonts-and-text.md)            | Dibuja texto en las pantallas de vídeo y otros dispositivos de salida.                                                                                                                                               |
| [Paleta lógica](logical-palette.md) | Paleta de colores creada por una aplicación y asociada a un contexto de dispositivo determinado.                                                                                                                |
| [Paths](paths.md)                     | Una o varias figuras (o formas) que se rellenan o se describen.                                                                                                                                     |
| [Lápices](pens.md)                       | Herramienta de gráficos que una aplicación usa para dibujar líneas y curvas.                                                                                                                                   |
| [Regiones](regions.md)                 | Rectángulo, polígono o elipse (o una combinación de dos o más de estas formas) que se puede rellenar, pintar, invertir, enmarcar y usar para realizar pruebas de acceso (pruebas de la ubicación del cursor). |



 

Desde la perspectiva de un desarrollador, un mapa de bits consta de una colección de estructuras que especifican o contienen los siguientes elementos:

-   Encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, y así sucesivamente.
-   Paleta lógica.
-   Matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica.

Un tamaño de mapa de bits está relacionado con el tipo de imagen que contiene. Las imágenes de mapa de bits pueden ser monocromáticas o de color. En una imagen, cada píxel corresponde a uno o varios bits de un mapa de bits. Las imágenes monocromáticas tienen una proporción de 1 bit por píxel (bpp). La creación de imágenes de color es más compleja. El número de colores que puede mostrar un mapa de bits es igual a dos elevados al número de bits por píxel. Por lo tanto, un mapa de bits de 256 colores requiere 8 bpp (2^8 = 256).

Panel de control son ejemplos de aplicaciones que usan mapas de bits. Al seleccionar un fondo (o fondo de pantalla) para el escritorio, realmente se selecciona un mapa de bits, que el sistema usa para pintar el fondo del escritorio. El sistema crea el patrón de fondo seleccionado dibujando repetidamente un patrón de 32 por 32 píxeles en el escritorio.

En la ilustración siguiente se muestra la perspectiva del desarrollador del mapa de bits que se encuentra en el archivo Redbrick.bmp. Muestra una matriz de paletas, un rectángulo de 32 por 32 píxeles y la matriz de índices que asigna los colores de la paleta a los píxeles del rectángulo.

![ilustración del rectángulo de píxeles, la matriz de paleta y la matriz de índices de redbrick.bmp](images/csbmp-01.png)

En el ejemplo anterior, el rectángulo de píxeles se creó en un dispositivo de visualización VGA mediante una paleta de 16 colores. Una paleta de 16 colores requiere índices de 4 bits; Por lo tanto, la matriz que asigna los colores de la paleta a los colores de píxeles se compone también de índices de 4 bits. (Para obtener más información sobre las paletas de colores lógicas, vea [Colores).](colors.md)

> [!Note]
>
> En el mapa de bits anterior, el sistema asigna índices a píxeles empezando por la línea de análisis inferior de la región rectangular y finalizando con la línea de examen superior. Una *línea de examen* es una sola fila de píxeles adyacentes en una pantalla de vídeo. Por ejemplo, la primera fila de la matriz (fila 0) corresponde a la fila inferior de píxeles, línea de examen 31. Esto se debe a que el mapa de bits anterior es un mapa de bits independiente del dispositivo (DIB) de abajo hacia arriba, un tipo común de mapa de bits. En dibs de arriba abajo y en mapas de bits dependientes del dispositivo (DDB), el sistema asigna índices a píxeles a partir de la línea de examen superior.

 

En los temas siguientes se describen diferentes áreas de mapas de bits.

-   [Clasificaciones de mapa de bits](bitmap-classifications.md)
-   [Tipos de encabezado de mapa de bits](bitmap-header-types.md)
-   [Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Mapas de bits, contextos de dispositivo y superficies de dibujo](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Creación de mapas de bits](bitmap-creation.md)
-   [Rotación de mapa de bits](bitmap-rotation.md)
-   [Escalado de mapa de bits](bitmap-scaling.md)
-   [Mapas de bits como pinceles](bitmaps-as-brushes.md)
-   [Mapa de bits Storage](bitmap-storage.md)
-   [Compresión de mapa de bits](bitmap-compression.md)
-   [Alpha Blending](alpha-blending.md)
-   [Sombreado suave](smooth-shading.md)
-   [ICM funciones de mapa de bits habilitadas para el usuario](icm-enabled-bitmap-functions.md)

 

 



