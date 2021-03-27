---
description: Para dibujar líneas y rectángulos, necesita un objeto Graphics y un objeto Pen. El objeto Graphics proporciona el método DrawLine y el objeto Pen almacena características de la línea, como el color y el ancho.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso de un lápiz para dibujar líneas y rectángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001658"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a><span data-ttu-id="4369c-104">Uso de un lápiz para dibujar líneas y rectángulos</span><span class="sxs-lookup"><span data-stu-id="4369c-104">Using a Pen to Draw Lines and Rectangles</span></span>

<span data-ttu-id="4369c-105">Para dibujar líneas y rectángulos, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="4369c-105">To draw lines and rectangles, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="4369c-106">El objeto **Graphics** proporciona el método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y el objeto **Pen** almacena características de la línea, como el color y el ancho.</span><span class="sxs-lookup"><span data-stu-id="4369c-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object stores features of the line, such as color and width.</span></span>

<span data-ttu-id="4369c-107">En el ejemplo siguiente se dibuja una línea de (20, 10) a (300, 100).</span><span class="sxs-lookup"><span data-stu-id="4369c-107">The following example draws a line from (20, 10) to (300, 100).</span></span> <span data-ttu-id="4369c-108">Supongamos que los **gráficos** son objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existentes.</span><span class="sxs-lookup"><span data-stu-id="4369c-108">Assume **graphics** is an existing [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



<span data-ttu-id="4369c-109">La primera instrucción de código usa el constructor de clase [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) para crear un lápiz negro.</span><span class="sxs-lookup"><span data-stu-id="4369c-109">The first statement of code uses the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) class constructor to create a black pen.</span></span> <span data-ttu-id="4369c-110">El argumento que se pasa al constructor **Pen** es un objeto de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="4369c-110">The one argument passed to the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="4369c-111">Los valores utilizados para construir el objeto de **color** (255, 0, 0), corresponden a los componentes alfa, rojo, verde y azul del color.</span><span class="sxs-lookup"><span data-stu-id="4369c-111">The values used to construct the **Color** object — (255, 0, 0, 0) — correspond to the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="4369c-112">Estos valores definen un lápiz negro opaco.</span><span class="sxs-lookup"><span data-stu-id="4369c-112">These values define an opaque black pen.</span></span>

<span data-ttu-id="4369c-113">En el ejemplo siguiente se dibuja un rectángulo con la esquina superior izquierda en (10, 10).</span><span class="sxs-lookup"><span data-stu-id="4369c-113">The following example draws a rectangle with its upper-left corner at (10, 10).</span></span> <span data-ttu-id="4369c-114">El rectángulo tiene un ancho de 100 y un alto de 50.</span><span class="sxs-lookup"><span data-stu-id="4369c-114">The rectangle has a width of 100 and a height of 50.</span></span> <span data-ttu-id="4369c-115">El segundo argumento que se pasa al constructor [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica que el ancho del lápiz es de 5 píxeles.</span><span class="sxs-lookup"><span data-stu-id="4369c-115">The second argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor indicates that the pen width is 5 pixels.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



<span data-ttu-id="4369c-116">Cuando se dibuja el rectángulo, el lápiz se centra en el límite del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="4369c-116">When the rectangle is drawn, the pen is centered on the rectangle's boundary.</span></span> <span data-ttu-id="4369c-117">Dado que el ancho del lápiz es 5, los lados del rectángulo se dibujan en 5 píxeles de ancho, de modo que 1 píxel se dibuja en el límite, se dibujan 2 píxeles en el interior y se dibujan 2 píxeles en el exterior.</span><span class="sxs-lookup"><span data-stu-id="4369c-117">Because the pen width is 5, the sides of the rectangle are drawn 5 pixels wide, such that 1 pixel is drawn on the boundary itself, 2 pixels are drawn on the inside, and 2 pixels are drawn on the outside.</span></span> <span data-ttu-id="4369c-118">Para obtener más información sobre la alineación del lápiz, vea [establecer el ancho y la alineación del lápiz](-gdiplus-setting-pen-width-and-alignment-use.md).</span><span class="sxs-lookup"><span data-stu-id="4369c-118">For more details on pen alignment, see [Setting Pen Width and Alignment](-gdiplus-setting-pen-width-and-alignment-use.md).</span></span>

<span data-ttu-id="4369c-119">En la ilustración siguiente se muestra el rectángulo resultante.</span><span class="sxs-lookup"><span data-stu-id="4369c-119">The following illustration shows the resulting rectangle.</span></span> <span data-ttu-id="4369c-120">Las líneas de puntos muestran dónde se habría dibujado el rectángulo si el ancho del lápiz hubiera sido un píxel.</span><span class="sxs-lookup"><span data-stu-id="4369c-120">The dotted lines show where the rectangle would have been drawn if the pen width had been one pixel.</span></span> <span data-ttu-id="4369c-121">La vista ampliada de la esquina superior izquierda del rectángulo muestra que las líneas negras gruesas se centran en esas líneas de puntos.</span><span class="sxs-lookup"><span data-stu-id="4369c-121">The enlarged view of the upper-left corner of the rectangle shows that the thick black lines are centered on those dotted lines.</span></span>

![Ilustración de un rectángulo dibujado con una línea gruesa de color negro que rodea una línea de guiones fino y gris](images/pens1.png)

 

 



