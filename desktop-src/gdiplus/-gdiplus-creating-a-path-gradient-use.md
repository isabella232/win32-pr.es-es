---
description: La clase PathGradientBrush permite personalizar la forma de rellenar una forma con colores que cambian gradualmente.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Crear un degradado de trazado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241575"
---
# <a name="creating-a-path-gradient"></a>Crear un degradado de trazado

La [**clase PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) permite personalizar la forma de rellenar una forma con colores que cambian gradualmente. Un **objeto PathGradientBrush** tiene una ruta de acceso de límite y un punto central. Puede especificar un color para el punto central y otro color para el límite. También puede especificar colores independientes para cada uno de los puntos a lo largo del límite.

> [!Note]  
> En GDI+, una ruta de acceso es una secuencia de líneas y curvas mantenida por un [**objeto GraphicsPath.**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) Para obtener más información sobre GDI+ rutas de acceso, vea [Trazados](-gdiplus-paths-about.md) y [construcción y dibujo de rutas de acceso](-gdiplus-constructing-and-drawing-paths-use.md).

 

En el ejemplo siguiente se rellena una elipse con un pincel de degradado de trazado. El color central se establece en azul y el color de límite se establece en aqua.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



En la ilustración siguiente se muestra la elipse rellena.

![ilustración que muestra una elipse con un relleno de degradado](images/pathgradient1.png)

De forma predeterminada, un pincel de degradado de trazado no se extiende fuera del límite del trazado. Si usa el pincel de degradado de trazado para rellenar una forma que se extiende más allá del límite del trazado, el área de la pantalla fuera del trazado no se rellenará. En la ilustración siguiente se muestra lo que sucede si cambia la llamada [**a Graphics::FillVelopse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) en el código anterior a `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![ilustración que muestra un segmento horizontal de la elipse anterior](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Especificar puntos en el límite

En el ejemplo siguiente se construye un pincel de degradado de trazado a partir de un trazado con forma de estrella. El código llama al [**método PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) para establecer el color del centroide de la estrella en rojo. A continuación, el código llama al método [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) para especificar varios colores (almacenados en la matriz [**de**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) colores) en los puntos individuales de la matriz [**de**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) puntos. La instrucción de código final rellena la ruta de acceso con forma de estrella con el pincel de degradado de trazado.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



En la ilustración siguiente se muestra la estrella rellena.

![ilustración que muestra una estrella de cinco puntas que se rellena de rojo en el centro a varios colores en cada punto de la estrella](images/pathgradient3.png)

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en una matriz de puntos. Se asigna un color a cada uno de los cinco puntos de la matriz. Si conectara los cinco puntos mediante líneas rectas, tendría un polígono de cinco lados. También se asigna un color al centro (centroide) de ese polígono; en este ejemplo, el centro (80, 75) se establece en blanco. La instrucción de código final del ejemplo rellena un rectángulo con el pincel de degradado de trazado.

El color que se usa para rellenar el rectángulo es blanco en (80, 75) y cambia gradualmente a medida que se aleja de (80, 75) hacia los puntos de la matriz. Por ejemplo, al pasar de (80, 75) a (0, 0), el color cambia gradualmente de blanco a rojo y, a medida que se mueve de (80, 75) a (160, 0), el color cambia gradualmente de blanco a verde.


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



Tenga en cuenta que no hay ningún [**objeto GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) en el código anterior. El constructor [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) concreto del ejemplo recibe un puntero a una matriz de puntos, pero no requiere un **objeto GraphicsPath.** Además, tenga en cuenta que el pincel de degradado de trazado se usa para rellenar un rectángulo, no un trazado. El rectángulo es mayor que el trazado utilizado para definir el pincel, por lo que parte del rectángulo no se pinta con el pincel. En la ilustración siguiente se muestra el rectángulo (línea de puntos) y la parte del rectángulo dibujada por el pincel de degradado del trazado.

![ilustración que muestra un rectángulo delimitado por una línea de puntos, parcialmente dibujado por un degradado de varios colores](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Personalización de un degradado de trazado

Una manera de personalizar un pincel de degradado de trazado es establecer sus escalas de foco. Las escalas de foco especifican una ruta de acceso interna que se encuentra dentro de la ruta de acceso principal. El color central se muestra en todas partes dentro de ese trazado interno en lugar de solo en el punto central. Para establecer las escalas de foco de un pincel de degradado de trazado, llame al [**método PathGradientBrush::SetFocusScales.**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales)

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un trazado elíptico. El código establece el color de límite en azul, establece el color central en aqua y, a continuación, usa el pincel de degradado de trazado para rellenar la ruta de acceso elíptica.

A continuación, el código establece las escalas de foco del pincel de degradado de trazado. La escala de foco x se establece en 0,3 y la escala de foco y se establece en 0,8. El código llama al método [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que la llamada subsiguiente a [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellene una elipse que se encuentra a la derecha de la primera elipse.

Para ver el efecto de las escalas de foco, imagine una elipse pequeña que comparte su centro con la elipse principal. La elipse pequeña (interna) es la elipse principal escalada horizontalmente (alrededor de su centro) por un factor de 0,3 y verticalmente por un factor de 0,8. A medida que se mueve desde el límite de la elipse externa hasta el límite de la elipse interna, el color cambia gradualmente de azul a aqua. A medida que se mueve desde el límite de la elipse interna hasta el centro compartido, el color sigue siendo aqua.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



En la ilustración siguiente se muestra la salida del código anterior. El botón de puntos suspensivos de la izquierda es aqua solo en el punto central. La elipse de la derecha es aqua en todas partes dentro del trazado interno.

![ilustración en la que se muestran dos puntos suspensivos que sombren desde el aguacua al azul: el primero tiene muy poco aguacua; el segundo tiene mucho más](images/focusscales1.png)

Otra manera de personalizar un pincel de degradado de trazado es especificar una matriz de colores preestablecidos y una matriz de posiciones de interpolación.

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un triángulo. El código llama al método [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) del pincel de degradado de ruta de acceso para especificar una matriz de colores de interpolación (verde oscuro, azul, azul) y una matriz de posiciones de interpolación (0, 0,25, 1). A medida que se mueve desde el límite del triángulo hasta el punto central, el color cambia gradualmente de verde oscuro a azul y, a continuación, de azul a azul. El cambio de verde oscuro a azul azul se produce en el 25 por ciento de la distancia de verde oscuro a azul.


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



En la ilustración siguiente se muestra la salida del código anterior.

![ilustración en la que se muestra un triángulo que sombrea de azul en el centro, a aguacua, a verde en los bordes](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Establecer el punto central

De forma predeterminada, el punto central de un pincel de degradado de trazado se encuentra en el centroide del trazado utilizado para construir el pincel. Puede cambiar la ubicación del punto central llamando al método [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) de la [**clase PathGradientBrush.**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush)

En el ejemplo siguiente se crea un pincel de degradado de trazado basado en una elipse. El centro de la elipse está en (70, 35), pero el punto central del pincel de degradado de trazado se establece en (120, 40).


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



En la ilustración siguiente se muestra la elipse rellena y el punto central del pincel de degradado de trazado.

![ilustración en la que se muestra una elipse que se rellena de azul a aqua desde un punto central cerca de un extremo](images/pathgradient5.png)

Puede establecer el punto central de un pincel de degradado de trazado en una ubicación fuera del trazado que se usó para construir el pincel. En el código anterior, si reemplaza la llamada a [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) por `pthGrBrush.SetCenterPoint(Point(145, 35))` , se obtiene el siguiente resultado.

![ilustración que muestra una elipse que se rellena de rojo a amarillo desde un punto central que está fuera del borde de la elipse](images/pathgradient6.png)

En la ilustración anterior, los puntos situados en el extremo derecho de la elipse no son azul puro (aunque están muy cerca). Los colores del degradado se sitúan como si el relleno hubiera podido alcanzar el punto (145, 35), el color habría alcanzado el azul puro (0, 0, 255). Pero el relleno nunca llega (145, 35) porque un pincel de degradado de trazado solo pinta dentro de su trazado.

 

 
