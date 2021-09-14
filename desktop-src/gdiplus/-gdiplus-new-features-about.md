---
description: En las secciones siguientes se describen varias de las nuevas características de Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Nuevas características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072419"
---
# <a name="new-features"></a>Nuevas características

En las secciones siguientes se describen varias de las nuevas características de Windows GDI+.

-   [Pinceles de degradado](#gradient-brushes)
-   [Curvas spline cardinales](#cardinal-splines)
-   [Objetos de ruta de acceso independientes](#independent-path-objects)
-   [Transformaciones y el objeto Matrix](#transformations-and-the-matrix-object)
-   [Regiones escalables](#scalable-regions)
-   [Combinación alfa](#alpha-blending)
-   [Compatibilidad con varios formatos de imagen](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pinceles de degradado

GDI+ se expande en Windows Interfaz de dispositivo gráfico (GDI) proporcionando pinceles de degradado lineal y degradado de trazado para rellenar formas, trazados y regiones. Los pinceles de degradado también se pueden usar para dibujar líneas, curvas y trazados. Al rellenar una forma con un pincel de degradado lineal, el color cambia gradualmente a medida que se mueve por la forma. Por ejemplo, supongamos que crea un pincel de degradado horizontal especificando azul en el borde izquierdo de una forma y verde en el borde derecho. Al rellenar esa forma con el pincel de degradado horizontal, cambiará gradualmente de azul a verde a medida que se mueve de su borde izquierdo a su borde derecho. De forma similar, una forma rellena con un pincel de degradado vertical cambiará de color a medida que se mueve de arriba abajo. En la ilustración siguiente se muestra una elipse rellena con un pincel de degradado horizontal y una región rellena con un pincel de degradado diagonal.

![ilustración de una forma rellenada por un degradado horizontal y una que se ha presentado mediante un degradado diagonal](images/aboutgdip01-art01.png)

Al rellenar una forma con un pincel de degradado de trazado, tiene una variedad de opciones para especificar cómo cambian los colores a medida que se mueve de una parte de la forma a otra. Una opción es tener un color central y un color de límite para que los píxeles cambien gradualmente de un color a otro a medida que se mueven desde el centro de la forma hacia los bordes exteriores. En la ilustración siguiente se muestra una ruta de acceso (creada a partir de un par de curvas spline de Bézier) rellenada con un pincel de degradado de trazado.

![ilustración de una forma similar a un signo infinito, relleno de azul donde las mitades se reúnen para el agua acuargada en los bordes](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Curvas spline cardinales

GDI+ admite splines cardinales, que no se admiten en GDI. Una curva spline cardinal es una secuencia de curvas individuales unidas para formar una curva mayor. La spline se especifica mediante una matriz de puntos y pasa a través de cada punto de esa matriz. Una curva spline cardinal pasa sin problemas (sin esquinas cortas) a través de cada punto de la matriz y, por tanto, es más refinada que una ruta de acceso creada mediante la conexión de líneas rectas. En la ilustración siguiente se muestran dos rutas de acceso, una creada mediante la conexión de líneas rectas y otra creada como una curva spline cardinal.

![ilustración en la que se muestran los mismos cinco puntos dos veces: una vez conectada por una curva spline cardinal y la otra por segmentos de línea](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Objetos de ruta de acceso independientes

En GDI, una ruta de acceso pertenece a un contexto de dispositivo y la ruta de acceso se destruye a medida que se dibuja. Con GDI+, un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) realiza el dibujo y puede crear y mantener varios objetos [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) que son independientes del **objeto Graphics.** La acción de dibujo no destruye un objeto **GraphicsPath,** por lo que puede usar el mismo objeto **GraphicsPath** para dibujar una ruta de acceso varias veces.

## <a name="transformations-and-the-matrix-object"></a>Transformaciones y el objeto Matrix

GDI+ proporciona el [**objeto Matrix,**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) una herramienta eficaz que hace que las transformaciones (rotaciones, traducciones, entre otras) sea fácil y flexible. Un objeto de matriz funciona junto con los objetos que se transforman. Por ejemplo, un [**objeto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tiene un [**método GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que recibe la dirección de un objeto **Matrix** como argumento. Una sola matriz de 3 ×3 puede almacenar una transformación o una secuencia de transformaciones. En la ilustración siguiente se muestra una ruta de acceso antes y después de una secuencia de dos transformaciones (primera escala y luego rotación).

![ilustración en la que se muestra el contorno de una forma y, a continuación, el mismo contorno, pero más estrecho y girado](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Regiones escalables

GDI+ amplia en gran parte en GDI con su compatibilidad con regiones. En GDI, las regiones se almacenan en coordenadas de dispositivo y la única transformación que se puede aplicar a una región es una traducción. GDI+ las regiones en coordenadas globales y permite que una región se someta a cualquier transformación (escalado, por ejemplo) que se pueda almacenar en una matriz de transformación. En la ilustración siguiente se muestra una región antes y después de una secuencia de tres transformaciones: escalado, rotación y traducción.

![ilustración en la que se muestra una forma centrada en ejes de coordenadas y, a continuación, la misma forma, pero mayor, girada y traducida a la derecha](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Combinación alfa

Tenga en cuenta que en la ilustración anterior, puede ver la región sin transformar (rellenada con rojo) a través de la región transformada (rellenada con un pincel de sombreado). Esto es posible mediante la combinación alfa, que es compatible con GDI+. Con la combinación alfa, puede especificar la transparencia de un color de relleno. Un color transparente se combina con el color de fondo: más transparente se hace un color de relleno, más se muestra el fondo. En la ilustración siguiente se muestran cuatro puntos suspensivos que se rellenan con el mismo color (rojo) en distintos niveles de transparencia.

![ilustración en la que se muestran cuatro puntos suspensivos de transparencia variable que se superponen a un rectángulo semitransparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Compatibilidad con varios formatos de imagen

GDI+ proporciona las [**clases Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)y [**Metafile,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) que permiten cargar, guardar y manipular imágenes en una variedad de formatos. Se admiten los siguientes formatos:

-   BMP
-   Formato de intercambio de gráficos (GIF)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICON
-   WMF
-   EMF

 

 



