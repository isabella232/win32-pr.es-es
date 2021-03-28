---
description: Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples. Recuerde de la información general de los gráficos vectoriales que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Rutas de acceso (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556951"
---
# <a name="paths-gdi"></a><span data-ttu-id="c2d19-104">Rutas de acceso (GDI+)</span><span class="sxs-lookup"><span data-stu-id="c2d19-104">Paths (GDI+)</span></span>

<span data-ttu-id="c2d19-105">Las rutas de acceso se forman combinando líneas, rectángulos y curvas simples.</span><span class="sxs-lookup"><span data-stu-id="c2d19-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="c2d19-106">Recuerde de la [información general de los gráficos vectoriales](-gdiplus-overview-of-vector-graphics-about.md) que los siguientes bloques de creación básicos han demostrado ser los más útiles para dibujar imágenes.</span><span class="sxs-lookup"><span data-stu-id="c2d19-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="c2d19-107">Líneas</span><span class="sxs-lookup"><span data-stu-id="c2d19-107">Lines</span></span>
-   <span data-ttu-id="c2d19-108">Rectángulos</span><span class="sxs-lookup"><span data-stu-id="c2d19-108">Rectangles</span></span>
-   <span data-ttu-id="c2d19-109">Puntos suspensivos</span><span class="sxs-lookup"><span data-stu-id="c2d19-109">Ellipses</span></span>
-   <span data-ttu-id="c2d19-110">-</span><span class="sxs-lookup"><span data-stu-id="c2d19-110">Arcs</span></span>
-   <span data-ttu-id="c2d19-111">Polígonos</span><span class="sxs-lookup"><span data-stu-id="c2d19-111">Polygons</span></span>
-   <span data-ttu-id="c2d19-112">Curvas spline cardinales</span><span class="sxs-lookup"><span data-stu-id="c2d19-112">Cardinal splines</span></span>
-   <span data-ttu-id="c2d19-113">Curvas spline de Bézier</span><span class="sxs-lookup"><span data-stu-id="c2d19-113">Bézier splines</span></span>

<span data-ttu-id="c2d19-114">En Windows GDI+, el objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) permite recopilar una secuencia de estos bloques de creación en una sola unidad.</span><span class="sxs-lookup"><span data-stu-id="c2d19-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="c2d19-115">A continuación, se puede dibujar toda la secuencia de líneas, rectángulos, polígonos y curvas con una llamada al método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c2d19-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="c2d19-116">En la ilustración siguiente se muestra una ruta de acceso creada mediante la combinación de una línea, un arco, una curva spline de Bézier y una curva spline cardinal.</span><span class="sxs-lookup"><span data-stu-id="c2d19-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![Ilustración de una ruta de acceso que combina una línea, un arco, una curva spline de Bézier y una curva spline cardinal](images/aboutgdip02-art14.png)

<span data-ttu-id="c2d19-118">La clase [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) proporciona los métodos siguientes para crear una secuencia de elementos que se van a dibujar: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (para curvas spline cardinales) y [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="c2d19-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="c2d19-119">Cada uno de estos métodos está sobrecargado; es decir, cada método se incluye en varias variaciones con listas de parámetros diferentes.</span><span class="sxs-lookup"><span data-stu-id="c2d19-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="c2d19-120">Por ejemplo, una variación del método AddLine recibe cuatro enteros y otra variación del método AddLine recibe dos objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="c2d19-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="c2d19-121">Los métodos para agregar líneas, rectángulos y curvas spline de Bézier a un trazado tienen métodos complementarios en plural que agregan varios elementos a la ruta de acceso en una sola llamada: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))y [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="c2d19-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="c2d19-122">Además, el método [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) tiene un método complementario, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), que agrega una curva cerrada a la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c2d19-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="c2d19-123">Para dibujar una ruta de acceso, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y un objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="c2d19-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="c2d19-124">El objeto **Graphics** proporciona el método [**graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) y el objeto **Pen** almacena los atributos de la ruta de acceso, como el ancho y el color de la línea.</span><span class="sxs-lookup"><span data-stu-id="c2d19-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="c2d19-125">El objeto **GraphicsPath** almacena la secuencia de líneas, rectángulos y curvas que componen la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c2d19-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="c2d19-126">Las direcciones del objeto **Pen** y el objeto **GraphicsPath** se pasan como argumentos al método **Graphics::D rawpath** .</span><span class="sxs-lookup"><span data-stu-id="c2d19-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="c2d19-127">En el ejemplo siguiente se dibuja un trazado que consta de una línea, una elipse y una curva spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="c2d19-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="c2d19-128">En la ilustración siguiente se muestra la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c2d19-128">The following illustration shows the path.</span></span>

![Ilustración de una ruta de acceso formada por una línea, una elipse y una curva spline de Bézier](images/aboutgdip02-art15.png)

<span data-ttu-id="c2d19-130">Además de agregar líneas, rectángulos y curvas a un trazado, puede Agregar trazados a un trazado.</span><span class="sxs-lookup"><span data-stu-id="c2d19-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="c2d19-131">Esto le permite combinar las rutas de acceso existentes para formar rutas de acceso complejas y grandes.</span><span class="sxs-lookup"><span data-stu-id="c2d19-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="c2d19-132">El código siguiente agrega **graphicsPath1** y **graphicsPath2** a **myGraphicsPath**.</span><span class="sxs-lookup"><span data-stu-id="c2d19-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="c2d19-133">El segundo parámetro del método [**GraphicsPath:: AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) especifica si la ruta de acceso agregada está conectada a la ruta de acceso existente.</span><span class="sxs-lookup"><span data-stu-id="c2d19-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="c2d19-134">Hay otros dos elementos que puede Agregar a una ruta de acceso: cadenas y gráficos circulares.</span><span class="sxs-lookup"><span data-stu-id="c2d19-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="c2d19-135">Un gráfico circular es una parte del interior de una elipse.</span><span class="sxs-lookup"><span data-stu-id="c2d19-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="c2d19-136">En el ejemplo siguiente se crea una ruta de acceso a partir de un arco, una curva spline cardinal, una cadena y un gráfico circular.</span><span class="sxs-lookup"><span data-stu-id="c2d19-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="c2d19-137">En la ilustración siguiente se muestra la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c2d19-137">The following illustration shows the path.</span></span> <span data-ttu-id="c2d19-138">Tenga en cuenta que no es necesario conectar una ruta de acceso; el arco, la curva spline cardinal, la cadena y el gráfico circular se separan.</span><span class="sxs-lookup"><span data-stu-id="c2d19-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![Ilustración de una ruta de acceso formada por líneas desconectadas: un arco, una curva spline cardinal, una cadena y un gráfico circular](images/aboutgdip02-art16.png)

 

 



