---
description: 'En la ilustración siguiente se muestran dos curvas: una abierta y otra cerrada.'
ms.assetid: e0fb8ba1-1783-4b36-93d8-f1242425d8bd
title: Curvas abiertas y cerradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7587ec950f8a0abc21f8c9cfb000a7333e87297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560331"
---
# <a name="open-and-closed-curves"></a><span data-ttu-id="07394-103">Curvas abiertas y cerradas</span><span class="sxs-lookup"><span data-stu-id="07394-103">Open and Closed Curves</span></span>

<span data-ttu-id="07394-104">En la ilustración siguiente se muestran dos curvas: una abierta y otra cerrada.</span><span class="sxs-lookup"><span data-stu-id="07394-104">The following illustration shows two curves: one open and one closed.</span></span>

![Ilustración de una curva abierta (una línea curva) y una curva cerrada (el contorno de una forma)](images/aboutgdip02-art24.png)

<span data-ttu-id="07394-106">Las curvas cerradas tienen un interior y, por lo tanto, se pueden rellenar con un pincel.</span><span class="sxs-lookup"><span data-stu-id="07394-106">Closed curves have an interior and therefore can be filled with a brush.</span></span> <span data-ttu-id="07394-107">La clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) de Windows GDI+ proporciona los siguientes métodos para rellenar figuras y curvas cerradas: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath)y [**Graphics:: FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span><span class="sxs-lookup"><span data-stu-id="07394-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class in Windows GDI+ provides the following methods for filling closed figures and curves: [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(constbrush_constrect_)), [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(constbrush_constrect_)), [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)), [FillPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpoint_inint)), [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)), [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath), and [**Graphics::FillRegion**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillregion).</span></span> <span data-ttu-id="07394-108">Siempre que llame a uno de estos métodos, debe pasar la dirección de uno de los tipos de pincel específicos ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)o [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) como argumento.</span><span class="sxs-lookup"><span data-stu-id="07394-108">Whenever you call one of these methods, you must pass the address of one of the specific brush types ([**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), or [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush)) as an argument.</span></span>

<span data-ttu-id="07394-109">El método [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) es un complemento del método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) .</span><span class="sxs-lookup"><span data-stu-id="07394-109">The [FillPie](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpie(inconstbrush_inreal_inreal_inreal_inreal_inreal_inreal)) method is a companion to the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method.</span></span> <span data-ttu-id="07394-110">Del mismo modo que el método DrawArc dibuja una parte del contorno de una elipse, el método FillPie rellena una parte del interior de una elipse.</span><span class="sxs-lookup"><span data-stu-id="07394-110">Just as the DrawArc method draws a portion of the outline of an ellipse, the FillPie method fills a portion of the interior of an ellipse.</span></span> <span data-ttu-id="07394-111">En el ejemplo siguiente se dibuja un arco y se rellena la parte correspondiente del interior de la elipse.</span><span class="sxs-lookup"><span data-stu-id="07394-111">The following example draws an arc and fills the corresponding portion of the interior of the ellipse.</span></span>


```
myGraphics.FillPie(&mySolidBrush, 0, 0, 140, 70, 0, 120);
myGraphics.DrawArc(&myPen, 0, 0, 140, 70, 0, 120);
```



<span data-ttu-id="07394-112">En la ilustración siguiente se muestra el arco y el gráfico circular relleno.</span><span class="sxs-lookup"><span data-stu-id="07394-112">The following illustration shows the arc and the filled pie.</span></span>

![Ilustración que muestra un segmento de una elipse rellena](images/aboutgdip02-art25.png)

<span data-ttu-id="07394-114">El método [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) es un complemento para el método [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="07394-114">The [FillClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpoint_inint)) method is a companion to the [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="07394-115">Ambos métodos cierran automáticamente la curva conectando el punto final con el punto inicial.</span><span class="sxs-lookup"><span data-stu-id="07394-115">Both methods automatically close the curve by connecting the ending point to the starting point.</span></span> <span data-ttu-id="07394-116">En el ejemplo siguiente se dibuja una curva que pasa a través de (0,0), (60, 20) y (40, 50).</span><span class="sxs-lookup"><span data-stu-id="07394-116">The following example draws a curve that passes through (0, 0), (60, 20), and (40, 50).</span></span> <span data-ttu-id="07394-117">A continuación, la curva se cierra automáticamente conectando (40, 50) al punto inicial (0,0) y el interior se rellena con un color sólido.</span><span class="sxs-lookup"><span data-stu-id="07394-117">Then, the curve is automatically closed by connecting (40, 50) to the starting point (0, 0), and the interior is filled with a solid color.</span></span>


```
Point myPointArray[] =
   {Point(10, 10), Point(60, 20),Point(40, 50)};
myGraphics.DrawClosedCurve(&myPen, myPointArray, 3);
myGraphics.FillClosedCurve(&mySolidBrush, myPointArray, 3, FillModeAlternate)
```



<span data-ttu-id="07394-118">Una ruta de acceso puede constar de varias figuras (subtrazados).</span><span class="sxs-lookup"><span data-stu-id="07394-118">A path can consist of several figures (subpaths).</span></span> <span data-ttu-id="07394-119">El método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellena el interior de cada ilustración.</span><span class="sxs-lookup"><span data-stu-id="07394-119">The [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the interior of each figure.</span></span> <span data-ttu-id="07394-120">Si una figura no está cerrada, el método **Graphics:: FillPath** rellena el área que se incluiría si se cerrara la figura.</span><span class="sxs-lookup"><span data-stu-id="07394-120">If a figure is not closed, the **Graphics::FillPath** method fills the area that would be enclosed if the figure were closed.</span></span> <span data-ttu-id="07394-121">En el siguiente ejemplo se dibuja y rellena un trazado compuesto por un arco, una curva spline cardinal, una cadena y un gráfico circular.</span><span class="sxs-lookup"><span data-stu-id="07394-121">The following example draws and fills a path that consists of an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphics.FillPath(&mySolidBrush, &myGraphicsPath);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="07394-122">En la ilustración siguiente se muestra la ruta de acceso antes y después de rellenarse con un pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="07394-122">The following illustration shows the path before and after it is filled with a solid brush.</span></span> <span data-ttu-id="07394-123">Tenga en cuenta que el texto de la cadena se describe, pero no se rellena, por el método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) .</span><span class="sxs-lookup"><span data-stu-id="07394-123">Note that the text in the string is outlined, but not filled, by the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method.</span></span> <span data-ttu-id="07394-124">Es el método [**Graphics:: FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) que pinta el interior de los caracteres de la cadena.</span><span class="sxs-lookup"><span data-stu-id="07394-124">It is the [**Graphics::FillPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method that paints the interiors of the characters in the string.</span></span>

![Ilustración que muestra dos veces texto y una curva abierta y cerrada; están vacías la primera vez y se rellenan la segunda vez](images/aboutgdip02-art26.png)

 

 



