---
description: Para dibujar líneas con GDI+ de Windows, debe crear un objeto Graphics y un objeto Pen.
ms.assetid: d91562ab-41e6-4bca-a320-74f490a4f88f
title: Lápices, líneas y rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e9749b1c1af6ca4808e797d016267bb251e6fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985139"
---
# <a name="pens-lines-and-rectangles"></a><span data-ttu-id="5bc71-103">Lápices, líneas y rectángulos</span><span class="sxs-lookup"><span data-stu-id="5bc71-103">Pens, Lines, and Rectangles</span></span>

<span data-ttu-id="5bc71-104">Para dibujar líneas con GDI+ de Windows, debe crear un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="5bc71-104">To draw lines with Windows GDI+ you need to create a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="5bc71-105">El objeto **Graphics** proporciona los métodos que realmente realizan el dibujo y el objeto **Pen** almacena los atributos de la línea, como el color, el ancho y el estilo.</span><span class="sxs-lookup"><span data-stu-id="5bc71-105">The **Graphics** object provides the methods that actually do the drawing, and the **Pen** object stores attributes of the line, such as color, width, and style.</span></span> <span data-ttu-id="5bc71-106">Dibujar una línea es simplemente cuestión de llamar al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) del objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="5bc71-106">Drawing a line is simply a matter of calling the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the **Graphics** object.</span></span> <span data-ttu-id="5bc71-107">La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawLine.</span><span class="sxs-lookup"><span data-stu-id="5bc71-107">The address of the **Pen** object is passed as one of the arguments to the DrawLine method.</span></span> <span data-ttu-id="5bc71-108">En el ejemplo siguiente se dibuja una línea desde el punto (4, 2) hasta el punto (12, 6).</span><span class="sxs-lookup"><span data-stu-id="5bc71-108">The following example draws a line from the point (4, 2) to the point (12, 6).</span></span>


```
myGraphics.DrawLine(&myPen, 4, 2, 12, 6);
```



<span data-ttu-id="5bc71-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) es un método sobrecargado de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos.</span><span class="sxs-lookup"><span data-stu-id="5bc71-109">[DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="5bc71-110">Por ejemplo, puede construir dos objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) y pasar referencias a los objetos **Point** como argumentos al método DrawLine.</span><span class="sxs-lookup"><span data-stu-id="5bc71-110">For example, you can construct two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects and pass references to the **Point** objects as arguments to the DrawLine method.</span></span>


```
Point myStartPoint(4, 2);
Point myEndPoint(12, 6);
myGraphics.DrawLine(&myPen, myStartPoint, myEndPoint);
```



<span data-ttu-id="5bc71-111">Puede especificar ciertos atributos al construir un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="5bc71-111">You can specify certain attributes when you construct a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="5bc71-112">Por ejemplo, un constructor [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) permite especificar el color y el ancho.</span><span class="sxs-lookup"><span data-stu-id="5bc71-112">For example, one [Pen](/windows/win32/api/gdipluspen/nf-gdipluspen-pen-pen(constpen_)) constructor allows you to specify color and width.</span></span> <span data-ttu-id="5bc71-113">En el ejemplo siguiente se dibuja una línea azul de ancho 2 de (0,0) a (60, 30).</span><span class="sxs-lookup"><span data-stu-id="5bc71-113">The following example draws a blue line of width 2 from (0, 0) to (60, 30).</span></span>


```
Pen myPen(Color(255, 0, 0, 255), 2);
myGraphics.DrawLine(&myPen, 0, 0, 60, 30);
```



<span data-ttu-id="5bc71-114">El objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) también tiene atributos, como el estilo Dash, que puede usar para especificar las características de la línea.</span><span class="sxs-lookup"><span data-stu-id="5bc71-114">The [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object also has attributes, such as dash style, that you can use to specify features of the line.</span></span> <span data-ttu-id="5bc71-115">Por ejemplo, en el ejemplo siguiente se dibuja una línea discontinua de (100, 50) a (300, 80).</span><span class="sxs-lookup"><span data-stu-id="5bc71-115">For example, the following example draws a dashed line from (100, 50) to (300, 80).</span></span>


```
myPen.SetDashStyle(DashStyleDash);
myGraphics.DrawLine(&myPen, 100, 50, 300, 80);
```



<span data-ttu-id="5bc71-116">Puede usar varios métodos del objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para establecer muchos más atributos de la línea.</span><span class="sxs-lookup"><span data-stu-id="5bc71-116">You can use various methods of the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to set many more attributes of the line.</span></span> <span data-ttu-id="5bc71-117">Los métodos [**Pen:: SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) y [**Pen:: SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) especifican la apariencia de los extremos de la línea; los extremos pueden ser plano, cuadrado, redondeado, triangular o una forma personalizada.</span><span class="sxs-lookup"><span data-stu-id="5bc71-117">The [**Pen::SetStartCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setstartcap) and [**Pen::SetEndCap**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setendcap) methods specify the appearance of the ends of the line; the ends can be flat, square, rounded, triangular, or a custom shape.</span></span> <span data-ttu-id="5bc71-118">El método [**Pen:: SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) le permite especificar si las líneas conectadas están en ángulo (Unidas con esquinas vivas), biseladas, redondeadas o recortadas.</span><span class="sxs-lookup"><span data-stu-id="5bc71-118">The [**Pen::SetLineJoin**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method lets you specify whether connected lines are mitered (joined with sharp corners), beveled, rounded, or clipped.</span></span> <span data-ttu-id="5bc71-119">En la ilustración siguiente se muestran líneas con varios estilos de extremo y de combinación.</span><span class="sxs-lookup"><span data-stu-id="5bc71-119">The following illustration shows lines with various cap and join styles.</span></span>

![Ilustración de dos líneas que muestran extremos redondeados y circulares, esquinas redondeadas y en ángulo y dos estilos de flecha](images/aboutgdip02-art04.png)

<span data-ttu-id="5bc71-121">Dibujar rectángulos con GDI+ es similar a las líneas de dibujo.</span><span class="sxs-lookup"><span data-stu-id="5bc71-121">Drawing rectangles with GDI+ is similar to drawing lines.</span></span> <span data-ttu-id="5bc71-122">Para dibujar un rectángulo, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="5bc71-122">To draw a rectangle, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="5bc71-123">El objeto **Graphics** proporciona un método [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) y el objeto **Pen** almacena atributos, como el color y el ancho de línea.</span><span class="sxs-lookup"><span data-stu-id="5bc71-123">The **Graphics** object provides a [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores attributes, such as line width and color.</span></span> <span data-ttu-id="5bc71-124">La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="5bc71-124">The address of the **Pen** object is passed as one of the arguments to the DrawRectangle method.</span></span> <span data-ttu-id="5bc71-125">En el ejemplo siguiente se dibuja un rectángulo con la esquina superior izquierda en (100, 50), un ancho de 80 y un alto de 40.</span><span class="sxs-lookup"><span data-stu-id="5bc71-125">The following example draws a rectangle with its upper-left corner at (100, 50), a width of 80, and a height of 40.</span></span>


```
myGraphics.DrawRectangle(&myPen, 100, 50, 80, 40);
```



<span data-ttu-id="5bc71-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) es un método sobrecargado de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos.</span><span class="sxs-lookup"><span data-stu-id="5bc71-126">[DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) is an overloaded method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="5bc71-127">Por ejemplo, puede construir un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) y pasar una referencia al objeto **Rect** como argumento para el método DrawRectangle.</span><span class="sxs-lookup"><span data-stu-id="5bc71-127">For example, you can construct a [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawRectangle method.</span></span>


```
Rect myRect(100, 50, 80, 40);
myGraphics.DrawRectangle(&myPen, myRect);
```



<span data-ttu-id="5bc71-128">Un objeto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) tiene métodos para manipular y recopilar información sobre el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5bc71-128">A [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) object has methods for manipulating and gathering information about the rectangle.</span></span> <span data-ttu-id="5bc71-129">Por ejemplo, los métodos [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) y [offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) cambian el tamaño y la posición del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5bc71-129">For example, the [Inflate](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inint_inint)) and [Offset](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-offset(inconstpoint_)) methods change the size and position of the rectangle.</span></span> <span data-ttu-id="5bc71-130">El método [**Rect:: IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) indica si el rectángulo forma una intersección con otro rectángulo determinado y el método [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) indica si un punto determinado se encuentra dentro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="5bc71-130">The [**Rect::IntersectsWith**](/windows/win32/api/Gdiplustypes/nf-gdiplustypes-rect-intersectswith) method tells you whether the rectangle intersects another given rectangle, and the [Contains](/windows/win32/api/gdiplustypes/nf-gdiplustypes-rect-contains(inint_inint)) method tells you whether a given point is inside the rectangle.</span></span>

 

 
