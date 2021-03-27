---
description: En las secciones siguientes se describen algunas de las nuevas características de Windows GDI+.
ms.assetid: 0257a23c-560e-472e-863a-6ab5881dc156
title: Nuevas características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79ddb4cabd14cc2eaa2493033a78cc7377f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809655"
---
# <a name="new-features"></a>Nuevas características

En las secciones siguientes se describen algunas de las nuevas características de Windows GDI+.

-   [Pinceles de degradado](#gradient-brushes)
-   [Curvas spline cardinales](#cardinal-splines)
-   [Objetos de ruta de acceso independientes](#independent-path-objects)
-   [Transformaciones y el objeto de matriz](#transformations-and-the-matrix-object)
-   [Regiones escalables](#scalable-regions)
-   [Combinación alfa](#alpha-blending)
-   [Compatibilidad con varios formatos de imagen](#support-for-multiple-image-formats)

## <a name="gradient-brushes"></a>Pinceles de degradado

GDI+ se expande en Windows Interfaz de dispositivo gráfico (GDI) proporcionando pinceles de degradado lineal y degradado de trazado para rellenar formas, rutas de acceso y regiones. Los pinceles de degradado también se pueden usar para dibujar líneas, curvas y trazados. Al rellenar una forma con un pincel de degradado lineal, el color cambia gradualmente a medida que se desplaza por la forma. Por ejemplo, suponga que crea un pincel de degradado horizontal especificando Blue en el borde izquierdo de una forma y verde en el borde derecho. Al rellenar la forma con el pincel de degradado horizontal, se cambiará gradualmente de azul a verde a medida que se desplaza desde el borde izquierdo hasta el borde derecho. Del mismo modo, una forma rellenada con un pincel de degradado vertical cambiará de color a medida que se desplaza de arriba abajo. En la ilustración siguiente se muestra una elipse rellena con un pincel de degradado horizontal y una región rellena con un pincel de degradado diagonal.

![Ilustración de una forma rellenada por un degradado horizontal y una archivada por un degradado diagonal](images/aboutgdip01-art01.png)

Al rellenar una forma con un pincel de degradado de trazado, tiene varias opciones para especificar cómo cambian los colores a medida que se mueve de una parte de la forma a otra. Una opción es tener un color central y un color de límite para que los píxeles cambien gradualmente de un color al otro a medida que se desplaza desde el centro de la forma hacia los bordes exteriores. En la ilustración siguiente se muestra una ruta de acceso (creada a partir de un par de curvas spline de Bézier) rellena con un pincel de degradado de trazado.

![Ilustración de una forma similar a un signo de infinito, rellenado de azul en el que las mitades se unen a Aguamarina en los bordes](images/aboutgdip01-art02.png)

## <a name="cardinal-splines"></a>Curvas spline cardinales

GDI+ admite las curvas spline cardinales, que no se admiten en GDI. Una curva spline cardinal es una secuencia de curvas individuales Unidas para formar una curva mayor. La spline se especifica mediante una matriz de puntos y pasa a través de cada punto de la matriz. Una curva spline cardinal pasa sin problemas (sin esquinas vivas) a través de cada punto de la matriz y, por tanto, es más refinada que una ruta de acceso creada mediante la conexión de líneas rectas. En la ilustración siguiente se muestran dos trazados, uno creado mediante la conexión de líneas rectas y otro creado como spline cardinal.

![Ilustración que muestra los mismos cinco puntos dos veces: una vez conectado mediante una curva spline cardinal, la otra por segmentos de línea](images/aboutgdip01-art03.png)

## <a name="independent-path-objects"></a>Objetos de ruta de acceso independientes

En GDI, una ruta de acceso pertenece a un contexto de dispositivo y la ruta de acceso se destruye a medida que se dibuja. Con GDI+, el dibujo lo realiza un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , y puede crear y mantener varios objetos [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) que son independientes del objeto **Graphics** . La acción de dibujo no destruye un objeto **GraphicsPath** , por lo que puede usar el mismo objeto **GraphicsPath** para dibujar un trazado varias veces.

## <a name="transformations-and-the-matrix-object"></a>Transformaciones y el objeto de matriz

GDI+ proporciona el objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , una herramienta eficaz que hace que las transformaciones (giros, traslaciones, etc.) sean sencillas y flexibles. Un objeto de matriz funciona junto con los objetos que se transforman. Por ejemplo, un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tiene un método [**GraphicsPath:: transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que recibe la dirección de un objeto de **matriz** como argumento. Una sola matriz de 3 × 3 puede almacenar una transformación o una secuencia de transformaciones. En la ilustración siguiente se muestra una ruta de acceso antes y después de una secuencia de dos transformaciones (primera escala y después giro).

![Ilustración que muestra el contorno de una forma y, a continuación, el mismo contorno pero más estrecho y girado](images/aboutgdip01-art04.png)

## <a name="scalable-regions"></a>Regiones escalables

GDI+ se expande en gran medida en GDI con su compatibilidad con regiones. En GDI, las regiones se almacenan en coordenadas de dispositivo y la única transformación que se puede aplicar a una región es una traducción. GDI+ almacena regiones en coordenadas universales y permite a una región someterse a cualquier transformación (escalado, por ejemplo) que se puede almacenar en una matriz de transformación. En la ilustración siguiente se muestra una región antes y después de una secuencia de tres transformaciones: escalar, girar y trasladar.

![Ilustración que muestra una forma centrada en ejes de coordenadas, la misma forma pero mayor, girada y traducida a la derecha](images/aboutgdip01-art05.png)

## <a name="alpha-blending"></a>Combinación alfa

Tenga en cuenta que en la ilustración anterior, puede ver la región no transformada (rellena con rojo) a través de la región transformada (rellena con un pincel de trama). Esto es posible gracias a la combinación alfa, que es compatible con GDI+. Con la combinación alfa, puede especificar la transparencia de un color de relleno. Un color transparente se combina con el color de fondo; cuanto más transparente sea el color de relleno, más se mostrará el fondo. En la ilustración siguiente se muestran cuatro elipses que se rellenan con el mismo color (rojo) en distintos niveles de transparencia.

![Ilustración que muestra cuatro puntos suspensivos de transparencia variable que se superpone a un rectángulo semitransparente](images/aboutgdip01-art06.png)

## <a name="support-for-multiple-image-formats"></a>Compatibilidad con varios formatos de imagen

GDI+ proporciona las clases [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)y [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que permiten cargar, guardar y manipular las imágenes en diversos formatos. Se admiten los siguientes formatos:

-   BMP
-   Formato de intercambio de gráficos (GIF)
-   JPEG
-   Exif
-   PNG
-   TIFF
-   ICON
-   WMF
-   EMF

 

 



