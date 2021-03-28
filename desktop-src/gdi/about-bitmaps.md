---
description: Un mapa de bits es uno de los objetos GDI que se puede seleccionar en un contexto de dispositivo (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Acerca de los mapas de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dbba516734dc255ce33005a7a9073865765785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543635"
---
# <a name="about-bitmaps"></a>Acerca de los mapas de bits

Un mapa de bits es uno de los objetos GDI que se puede seleccionar en un *contexto de dispositivo* (DC). Los [contextos de dispositivo](device-contexts.md) son estructuras que definen un conjunto de objetos gráficos y sus atributos asociados, así como modos gráficos que afectan a la salida. En la tabla siguiente se describen los objetos GDI que se pueden seleccionar en un contexto de dispositivo.



| Objeto gráfico                         | Descripción                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapas de bits](bitmaps.md)                 | Crea, manipula (escala, desplaza, gira y pinta) y almacena las imágenes como archivos en un disco.                                                                                                       |
| [Pinceles](brushes.md)                 | Pinta el interior de los polígonos, elipses y trazados.                                                                                                                                                |
| [Fuentes](fonts-and-text.md)            | Dibuja texto en pantallas de vídeo y otros dispositivos de salida.                                                                                                                                               |
| [Paleta lógica](logical-palette.md) | Paleta de colores creada por una aplicación y asociada a un contexto de dispositivo determinado.                                                                                                                |
| [Paths](paths.md)                     | Una o más figuras (o formas) que se rellenan o se describen.                                                                                                                                     |
| [Lápices](pens.md)                       | Herramienta de gráficos que usa una aplicación para dibujar líneas y curvas.                                                                                                                                   |
| [Regiones](regions.md)                 | Rectángulo, polígono o elipse (o una combinación de dos o más de estas formas) que se puede rellenar, pintar, invertir, tramar y usar para realizar la prueba de posicionamiento (probar la ubicación del cursor). |



 

Desde la perspectiva del desarrollador, un mapa de bits se compone de una colección de estructuras que especifican o contienen los elementos siguientes:

-   Encabezado que describe la resolución del dispositivo en el que se creó el rectángulo de píxeles, las dimensiones del rectángulo, el tamaño de la matriz de bits, etc.
-   Una paleta lógica.
-   Matriz de bits que define la relación entre los píxeles de la imagen de mapa de bits y las entradas de la paleta lógica.

Un tamaño de mapa de bits está relacionado con el tipo de imagen que contiene. Las imágenes de mapa de bits pueden ser monocromáticas o de color. En una imagen, cada píxel corresponde a uno o varios bits de un mapa de bits. Las imágenes monocromáticas tienen una proporción de 1 bit por píxel (BPP). La creación de imágenes en color es más compleja. El número de colores que puede mostrar un mapa de bits es igual a dos elevado al número de bits por píxel. Por lo tanto, un mapa de bits de 256 colores requiere 8 BPP (2 ^ 8 = 256).

Las aplicaciones del panel de control son ejemplos de aplicaciones que usan mapas de bits. Cuando se selecciona un fondo (o papel tapiz) para el escritorio, en realidad se selecciona un mapa de bits que el sistema utiliza para pintar el fondo del escritorio. El sistema crea el patrón de fondo seleccionado dibujando repetidamente un patrón de píxel 32 por 32 en el escritorio.

En la ilustración siguiente se muestra la perspectiva del desarrollador del mapa de bits que se encuentra en el Redbrick.bmp de archivos. Muestra una matriz de paleta, un rectángulo de 32 por 32 píxeles y la matriz de índices que asigna colores de la paleta a píxeles del rectángulo.

![Ilustración del rectángulo de píxeles, la matriz de paleta y la matriz de índices de redbrick.bmp](images/csbmp-01.png)

En el ejemplo anterior, se creó el rectángulo de píxeles en un dispositivo de pantalla VGA con una paleta de 16 colores. Una paleta de 16 colores requiere índices de 4 bits. por lo tanto, la matriz que asigna los colores de la paleta a los colores de píxeles también se compone de índices de 4 bits. (Para obtener más información sobre las paletas de colores lógicas, vea [colores](colors.md)).

> [!Note]
>
> En el mapa de bits anterior, el sistema asigna índices a píxeles que comienzan con la línea de exploración inferior de la región rectangular y terminan con la línea de exploración superior. Una *línea de recorrido* es una fila única de píxeles adyacentes en una pantalla de vídeo. Por ejemplo, la primera fila de la matriz (fila 0) corresponde a la fila inferior de píxeles, la línea de análisis 31. Esto se debe a que el mapa de bits anterior es un mapa de bits independiente del dispositivo (DIB) de nivel inferior, un tipo común de mapa de bits. En los DIB de arriba abajo y en los mapas de bits dependientes del dispositivo (DDB), el sistema asigna índices a píxeles que comienzan con la línea de exploración superior.

 

En los temas siguientes se describen distintas áreas de mapas de bits.

-   [Clasificaciones de mapas de bits](bitmap-classifications.md)
-   [Tipos de encabezado de mapa de bits](bitmap-header-types.md)
-   [Extensiones JPEG y PNG para estructuras y funciones de mapa de bits específicas](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Mapas de bits, contextos de dispositivo y superficies de dibujo](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Creación de mapas de bits](bitmap-creation.md)
-   [Rotación de mapas de bits](bitmap-rotation.md)
-   [Escala de mapas de bits](bitmap-scaling.md)
-   [Mapas de bits como pinceles](bitmaps-as-brushes.md)
-   [Almacenamiento de mapas de bits](bitmap-storage.md)
-   [Compresión de mapa de bits](bitmap-compression.md)
-   [Combinación alfa](alpha-blending.md)
-   [Sombreado suave](smooth-shading.md)
-   [Funciones de mapa de bits habilitadas para ICM](icm-enabled-bitmap-functions.md)

 

 



