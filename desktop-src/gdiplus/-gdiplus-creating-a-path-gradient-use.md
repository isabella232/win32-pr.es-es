---
description: La clase PathGradientBrush permite personalizar la manera de rellenar una forma con colores que cambian gradualmente.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Crear un degradado de trazado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564678"
---
# <a name="creating-a-path-gradient"></a><span data-ttu-id="99a85-103">Crear un degradado de trazado</span><span class="sxs-lookup"><span data-stu-id="99a85-103">Creating a Path Gradient</span></span>

<span data-ttu-id="99a85-104">La clase [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) permite personalizar la manera de rellenar una forma con colores que cambian gradualmente.</span><span class="sxs-lookup"><span data-stu-id="99a85-104">The [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class allows you to customize the way you fill a shape with gradually changing colors.</span></span> <span data-ttu-id="99a85-105">Un objeto **PathGradientBrush** tiene una ruta de acceso de límite y un punto central.</span><span class="sxs-lookup"><span data-stu-id="99a85-105">A **PathGradientBrush** object has a boundary path and a center point.</span></span> <span data-ttu-id="99a85-106">Puede especificar un color para el punto central y otro color para el límite.</span><span class="sxs-lookup"><span data-stu-id="99a85-106">You can specify one color for the center point and another color for the boundary.</span></span> <span data-ttu-id="99a85-107">También puede especificar colores independientes para cada uno de varios puntos a lo largo del límite.</span><span class="sxs-lookup"><span data-stu-id="99a85-107">You can also specify separate colors for each of several points along the boundary.</span></span>

> [!Note]  
> <span data-ttu-id="99a85-108">En GDI+, una ruta de acceso es una secuencia de líneas y curvas mantenida por un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="99a85-108">In GDI+, a path is a sequence of lines and curves maintained by a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="99a85-109">Para obtener más información sobre las rutas de acceso de GDI+, vea [rutas](-gdiplus-paths-about.md) de acceso y [construir y dibujar trazados](-gdiplus-constructing-and-drawing-paths-use.md).</span><span class="sxs-lookup"><span data-stu-id="99a85-109">For more information about GDI+ paths, see [Paths](-gdiplus-paths-about.md) and [Constructing and Drawing Paths](-gdiplus-constructing-and-drawing-paths-use.md).</span></span>

 

<span data-ttu-id="99a85-110">En el ejemplo siguiente se rellena una elipse con un pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-110">The following example fills an ellipse with a path gradient brush.</span></span> <span data-ttu-id="99a85-111">El color central se establece en azul y el color del límite se establece en aguamarina.</span><span class="sxs-lookup"><span data-stu-id="99a85-111">The center color is set to blue and the boundary color is set to aqua.</span></span>


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



<span data-ttu-id="99a85-112">En la ilustración siguiente se muestra la elipse rellenada.</span><span class="sxs-lookup"><span data-stu-id="99a85-112">The following illustration shows the filled ellipse.</span></span>

![Ilustración que muestra una elipse con un relleno de degradado](images/pathgradient1.png)

<span data-ttu-id="99a85-114">De forma predeterminada, un pincel de degradado de trazado no se extiende fuera del límite de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="99a85-114">By default, a path gradient brush does not extend outside the boundary of the path.</span></span> <span data-ttu-id="99a85-115">Si usa el pincel de degradado de trazado para rellenar una forma que se extiende más allá del límite de la ruta de acceso, el área de la pantalla fuera de la ruta de acceso no se rellenará.</span><span class="sxs-lookup"><span data-stu-id="99a85-115">If you use the path gradient brush to fill a shape that extends beyond the boundary of the path, the area of the screen outside the path will not be filled.</span></span> <span data-ttu-id="99a85-116">En la ilustración siguiente se muestra lo que ocurre si se cambia la llamada a [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) en el código anterior a `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .</span><span class="sxs-lookup"><span data-stu-id="99a85-116">The following illustration shows what happens if you change the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) call in the preceding code to `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)`.</span></span>

![Ilustración que muestra un segmento horizontal de la elipse anterior](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a><span data-ttu-id="99a85-118">Especificar puntos en el límite</span><span class="sxs-lookup"><span data-stu-id="99a85-118">Specifying Points on the Boundary</span></span>

<span data-ttu-id="99a85-119">En el ejemplo siguiente se crea un pincel de degradado de trazado a partir de un trazado en forma de estrella.</span><span class="sxs-lookup"><span data-stu-id="99a85-119">The following example constructs a path gradient brush from a star-shaped path.</span></span> <span data-ttu-id="99a85-120">El código llama al método [**PathGradientBrush:: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) para establecer el color en el centroide de la estrella en rojo.</span><span class="sxs-lookup"><span data-stu-id="99a85-120">The code calls the [**PathGradientBrush::SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) method to set the color at the centroid of the star to red.</span></span> <span data-ttu-id="99a85-121">A continuación, el código llama al método [**PathGradientBrush:: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) para especificar varios colores (almacenados en la matriz de [**colores**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) en los puntos individuales de la matriz de [**puntos**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="99a85-121">Then the code calls the [**PathGradientBrush::SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) method to specify various colors (stored in the [**colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) array) at the individual points in the [**points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) array.</span></span> <span data-ttu-id="99a85-122">La instrucción de código final rellena el trazado en forma de estrella con el pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-122">The final code statement fills the star-shaped path with the path gradient brush.</span></span>


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



<span data-ttu-id="99a85-123">En la ilustración siguiente se muestra la estrella rellena.</span><span class="sxs-lookup"><span data-stu-id="99a85-123">The following illustration shows the filled star.</span></span>

![Ilustración en la que se muestra una estrella de cinco puntas que rellena desde rojo en el centro hasta varios colores en cada punto de la estrella](images/pathgradient3.png)

<span data-ttu-id="99a85-125">En el ejemplo siguiente se crea un pincel de degradado de trazado basado en una matriz de puntos.</span><span class="sxs-lookup"><span data-stu-id="99a85-125">The following example constructs a path gradient brush based on an array of points.</span></span> <span data-ttu-id="99a85-126">Se asigna un color a cada uno de los cinco puntos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="99a85-126">A color is assigned to each of the five points in the array.</span></span> <span data-ttu-id="99a85-127">Si fuera a conectar los cinco puntos por líneas rectas, obtendría un polígono de cinco caras.</span><span class="sxs-lookup"><span data-stu-id="99a85-127">If you were to connect the five points by straight lines, you would get a five-sided polygon.</span></span> <span data-ttu-id="99a85-128">También se asigna un color al centro (centroide) de ese polígono; en este ejemplo, el centro (80, 75) se establece en blanco.</span><span class="sxs-lookup"><span data-stu-id="99a85-128">A color is also assigned to the center (centroid) of that polygon — in this example, the center (80, 75) is set to white.</span></span> <span data-ttu-id="99a85-129">La instrucción de código final del ejemplo rellena un rectángulo con el pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-129">The final code statement in the example fills a rectangle with the path gradient brush.</span></span>

<span data-ttu-id="99a85-130">El color usado para rellenar el rectángulo está en blanco en (80, 75) y cambia gradualmente a medida que se aleja de (80, 75) hacia los puntos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="99a85-130">The color used to fill the rectangle is white at (80, 75) and changes gradually as you move away from (80, 75) toward the points in the array.</span></span> <span data-ttu-id="99a85-131">Por ejemplo, a medida que se mueve de (80, 75) a (0,0), el color cambia gradualmente de blanco a rojo y, al pasar de (80, 75) a (160, 0), el color cambia gradualmente de blanco a verde.</span><span class="sxs-lookup"><span data-stu-id="99a85-131">For example, as you move from (80, 75) to (0, 0), the color changes gradually from white to red, and as you move from (80, 75) to (160, 0), the color changes gradually from white to green.</span></span>


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



<span data-ttu-id="99a85-132">Tenga en cuenta que no hay ningún objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) en el código anterior.</span><span class="sxs-lookup"><span data-stu-id="99a85-132">Note that there is no [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object in the preceding code.</span></span> <span data-ttu-id="99a85-133">El constructor [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) determinado del ejemplo recibe un puntero a una matriz de puntos, pero no requiere un objeto **GraphicsPath** .</span><span class="sxs-lookup"><span data-stu-id="99a85-133">The particular [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) constructor in the example receives a pointer to an array of points but does not require a **GraphicsPath** object.</span></span> <span data-ttu-id="99a85-134">Además, tenga en cuenta que el pincel de degradado de trazado se usa para rellenar un rectángulo, no una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="99a85-134">Also, note that the path gradient brush is used to fill a rectangle, not a path.</span></span> <span data-ttu-id="99a85-135">El rectángulo es mayor que la ruta de acceso que se usa para definir el pincel, por lo que el pincel no pinta parte del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="99a85-135">The rectangle is larger than the path used to define the brush, so some of the rectangle is not painted by the brush.</span></span> <span data-ttu-id="99a85-136">En la ilustración siguiente se muestra el rectángulo (línea de puntos) y la parte del rectángulo pintada por el pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-136">The following illustration shows the rectangle (dotted line) and the portion of the rectangle painted by the path gradient brush.</span></span>

![Ilustración que muestra un rectángulo delimitado por una línea de puntos, parcialmente pintado por un degradado de varios colores](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a><span data-ttu-id="99a85-138">Personalización de un degradado de trazado</span><span class="sxs-lookup"><span data-stu-id="99a85-138">Customizing a Path Gradient</span></span>

<span data-ttu-id="99a85-139">Una manera de personalizar un pincel de degradado de trazado es establecer sus escalas de foco.</span><span class="sxs-lookup"><span data-stu-id="99a85-139">One way to customize a path gradient brush is to set its focus scales.</span></span> <span data-ttu-id="99a85-140">Las escalas de foco especifican una ruta de acceso interna que se encuentra dentro de la ruta de acceso principal.</span><span class="sxs-lookup"><span data-stu-id="99a85-140">The focus scales specify an inner path that lies inside the main path.</span></span> <span data-ttu-id="99a85-141">El color del centro se muestra en cualquier parte dentro de la ruta de acceso interior en lugar de solo en el punto central.</span><span class="sxs-lookup"><span data-stu-id="99a85-141">The center color is displayed everywhere inside that inner path rather than only at the center point.</span></span> <span data-ttu-id="99a85-142">Para establecer las escalas de foco de un pincel de degradado de trazado, llame al método [**PathGradientBrush:: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .</span><span class="sxs-lookup"><span data-stu-id="99a85-142">To set the focus scales of a path gradient brush, call the [**PathGradientBrush::SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) method.</span></span>

<span data-ttu-id="99a85-143">En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un trazado elíptico.</span><span class="sxs-lookup"><span data-stu-id="99a85-143">The following example creates a path gradient brush based on an elliptical path.</span></span> <span data-ttu-id="99a85-144">El código establece el color del límite en azul, establece el color central en aguamarina y, a continuación, usa el pincel de degradado de trazado para rellenar el trazado elíptico.</span><span class="sxs-lookup"><span data-stu-id="99a85-144">The code sets the boundary color to blue, sets the center color to aqua, and then uses the path gradient brush to fill the elliptical path.</span></span>

<span data-ttu-id="99a85-145">A continuación, el código establece las escalas de foco del pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-145">Next the code sets the focus scales of the path gradient brush.</span></span> <span data-ttu-id="99a85-146">La escala de enfoque x está establecida en 0,3 y la escala de enfoque y se establece en 0,8.</span><span class="sxs-lookup"><span data-stu-id="99a85-146">The x focus scale is set to 0.3, and the y focus scale is set to 0.8.</span></span> <span data-ttu-id="99a85-147">El código llama al método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para que la siguiente llamada a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) Rellene una elipse situada a la derecha de la primera elipse.</span><span class="sxs-lookup"><span data-stu-id="99a85-147">The code calls the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills an ellipse that sits to the right of the first ellipse.</span></span>

<span data-ttu-id="99a85-148">Para ver el efecto de las escalas de foco, imagine una elipse pequeña que comparta su centro con la elipse principal.</span><span class="sxs-lookup"><span data-stu-id="99a85-148">To see the effect of the focus scales, imagine a small ellipse that shares its center with the main ellipse.</span></span> <span data-ttu-id="99a85-149">La elipse pequeña (interna) es la elipse principal escalada (alrededor de su centro) horizontalmente por un factor de 0,3 y verticalmente según un factor de 0,8.</span><span class="sxs-lookup"><span data-stu-id="99a85-149">The small (inner) ellipse is the main ellipse scaled (about its center) horizontally by a factor of 0.3 and vertically by a factor of 0.8.</span></span> <span data-ttu-id="99a85-150">A medida que se desplaza desde el límite de la elipse externa hasta el límite de la elipse interna, el color cambia gradualmente de azul a aguamarina.</span><span class="sxs-lookup"><span data-stu-id="99a85-150">As you move from the boundary of the outer ellipse to the boundary of the inner ellipse, the color changes gradually from blue to aqua.</span></span> <span data-ttu-id="99a85-151">A medida que se desplaza desde el límite de la elipse interna al centro compartido, el color se mantiene en aguamarina.</span><span class="sxs-lookup"><span data-stu-id="99a85-151">As you move from the boundary of the inner ellipse to the shared center, the color remains aqua.</span></span>


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



<span data-ttu-id="99a85-152">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="99a85-152">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="99a85-153">La elipse de la izquierda es aguamarina solo en el punto central.</span><span class="sxs-lookup"><span data-stu-id="99a85-153">The ellipse on the left is aqua only at the center point.</span></span> <span data-ttu-id="99a85-154">La elipse de la derecha es de aguamarina en cualquier parte dentro de la ruta de acceso interna.</span><span class="sxs-lookup"><span data-stu-id="99a85-154">The ellipse on the right is aqua everywhere inside the inner path.</span></span>

![Ilustración que muestra dos elipses que sombrean de aguamarina a azul: el primero tiene muy poco aguamarina; el segundo tiene mucho más](images/focusscales1.png)

<span data-ttu-id="99a85-156">Otra manera de personalizar un pincel de degradado de trazado es especificar una matriz de colores preestablecidos y una matriz de posiciones de interpolación.</span><span class="sxs-lookup"><span data-stu-id="99a85-156">Another way to customize a path gradient brush is to specify an array of preset colors and an array of interpolation positions.</span></span>

<span data-ttu-id="99a85-157">En el ejemplo siguiente se crea un pincel de degradado de trazado basado en un triángulo.</span><span class="sxs-lookup"><span data-stu-id="99a85-157">The following example creates a path gradient brush based on a triangle.</span></span> <span data-ttu-id="99a85-158">El código llama al método [**PathGradientBrush:: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) del pincel de degradado de trazado para especificar una matriz de colores de interpolación (verde oscuro, aguamarina, azul) y una matriz de posiciones de interpolación (0, 0,25, 1).</span><span class="sxs-lookup"><span data-stu-id="99a85-158">The code calls the [**PathGradientBrush::SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) method of the path gradient brush to specify an array of interpolation colors (dark green, aqua, blue) and an array of interpolation positions (0, 0.25, 1).</span></span> <span data-ttu-id="99a85-159">A medida que se desplaza desde el límite del triángulo hasta el punto central, el color cambia gradualmente de verde oscuro a aguamarina y, a continuación, de aguamarina a azul.</span><span class="sxs-lookup"><span data-stu-id="99a85-159">As you move from the boundary of the triangle to the center point, the color changes gradually from dark green to aqua and then from aqua to blue.</span></span> <span data-ttu-id="99a85-160">El cambio de verde oscuro a Aguamarina sucede en un 25 por ciento de la distancia de verde oscuro a azul.</span><span class="sxs-lookup"><span data-stu-id="99a85-160">The change from dark green to aqua happens in 25 percent of the distance from dark green to blue.</span></span>


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



<span data-ttu-id="99a85-161">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="99a85-161">The following illustration shows the output of the preceding code.</span></span>

![Ilustración en la que se muestra un triángulo que sombrea de azul en el centro, a aguamarina, a verde en los bordes](images/pathgradient4.png)

## <a name="setting-the-center-point"></a><span data-ttu-id="99a85-163">Establecer el punto central</span><span class="sxs-lookup"><span data-stu-id="99a85-163">Setting the Center Point</span></span>

<span data-ttu-id="99a85-164">De forma predeterminada, el punto central de un pincel de degradado de trazado está en el centroide de la ruta de acceso que se usa para construir el pincel.</span><span class="sxs-lookup"><span data-stu-id="99a85-164">By default, the center point of a path gradient brush is at the centroid of the path used to construct the brush.</span></span> <span data-ttu-id="99a85-165">Puede cambiar la ubicación del punto central llamando al método [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) de la clase [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="99a85-165">You can change the location of the center point by calling the [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) method of the [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) class.</span></span>

<span data-ttu-id="99a85-166">En el ejemplo siguiente se crea un pincel de degradado de trazado basado en una elipse.</span><span class="sxs-lookup"><span data-stu-id="99a85-166">The following example creates a path gradient brush based on an ellipse.</span></span> <span data-ttu-id="99a85-167">El centro de la elipse está en (70, 35), pero el punto central del pincel de degradado de trazado se establece en (120, 40).</span><span class="sxs-lookup"><span data-stu-id="99a85-167">The center of the ellipse is at (70, 35), but the center point of the path gradient brush is set to (120, 40).</span></span>


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



<span data-ttu-id="99a85-168">En la ilustración siguiente se muestra la elipse rellena y el punto central del pincel de degradado de trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-168">The following illustration shows the filled ellipse and the center point of the path gradient brush.</span></span>

![Ilustración en la que se muestra una elipse de azul a Aguamarina desde un punto central cerca de un extremo](images/pathgradient5.png)

<span data-ttu-id="99a85-170">Puede establecer el punto central de un pincel de degradado de trazado en una ubicación fuera de la ruta de acceso que se usó para construir el pincel.</span><span class="sxs-lookup"><span data-stu-id="99a85-170">You can set the center point of a path gradient brush to a location outside the path that was used to construct the brush.</span></span> <span data-ttu-id="99a85-171">En el código anterior, si reemplaza la llamada a [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) con `pthGrBrush.SetCenterPoint(Point(145, 35))` , obtendrá el siguiente resultado.</span><span class="sxs-lookup"><span data-stu-id="99a85-171">In the preceding code, if you replace the call to [**PathGradientBrush::SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) with `pthGrBrush.SetCenterPoint(Point(145, 35))`, you will get the following result.</span></span>

![Ilustración que muestra una elipse que se llena de rojo a amarillo desde un punto central que está fuera del borde de la elipse](images/pathgradient6.png)

<span data-ttu-id="99a85-173">En la ilustración anterior, los puntos en el extremo derecho de la elipse no son azules puros (aunque son muy cercanos).</span><span class="sxs-lookup"><span data-stu-id="99a85-173">In the preceding illustration, the points at the far right of the ellipse are not pure blue (although they are very close).</span></span> <span data-ttu-id="99a85-174">Los colores del degradado se colocan como si se hubiera permitido que el relleno alcanzara el punto (145, 35), el color habría alcanzado el azul puro (255 0,0).</span><span class="sxs-lookup"><span data-stu-id="99a85-174">The colors in the gradient are positioned as if the fill had been allowed to reach the point (145, 35), the color would have reached pure blue (0, 0, 255).</span></span> <span data-ttu-id="99a85-175">Pero el relleno nunca alcanza (145, 35) porque un pincel de degradado de trazado solo pinta dentro de su trazado.</span><span class="sxs-lookup"><span data-stu-id="99a85-175">But the fill never reaches (145, 35) because a path gradient brush paints only inside its path.</span></span>

 

 
