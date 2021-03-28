---
description: 'La clase Graphics proporciona una variedad de métodos de dibujo, incluidos los que se muestran en la lista siguiente:'
ms.assetid: d3c8d16c-858a-42a9-a512-3fcfa144f5fc
title: Utilizar lápiz para dibujar líneas y formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904f53149038d6109365adddc11d3c37881a8def
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154214"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="e3450-103">Utilizar lápiz para dibujar líneas y formas</span><span class="sxs-lookup"><span data-stu-id="e3450-103">Using a Pen to Draw Lines and Shapes</span></span>

<span data-ttu-id="e3450-104">La clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona una variedad de métodos de dibujo, incluidos los que se muestran en la lista siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3450-104">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides a variety of drawing methods including those shown in the following list:</span></span>

-   <span data-ttu-id="e3450-105">[DrawLine (métodos)](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span><span class="sxs-lookup"><span data-stu-id="e3450-105">[DrawLine Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))</span></span>
-   <span data-ttu-id="e3450-106">[DrawRectangle (métodos)](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="e3450-106">[DrawRectangle Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="e3450-107">[Métodos DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span><span class="sxs-lookup"><span data-stu-id="e3450-107">[DrawEllipse Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_))</span></span>
-   <span data-ttu-id="e3450-108">[DrawArc (métodos)](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span><span class="sxs-lookup"><span data-stu-id="e3450-108">[DrawArc Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal))</span></span>
-   [<span data-ttu-id="e3450-109">**Gráficos::D rawPath**</span><span class="sxs-lookup"><span data-stu-id="e3450-109">**Graphics::DrawPath**</span></span>](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath)
-   <span data-ttu-id="e3450-110">[DrawCurve (métodos)](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="e3450-110">[DrawCurve Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint))</span></span>
-   <span data-ttu-id="e3450-111">[Métodos DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span><span class="sxs-lookup"><span data-stu-id="e3450-111">[DrawBezier Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpointf__inconstpointf__inconstpointf__inconstpointf_))</span></span>

<span data-ttu-id="e3450-112">Uno de los argumentos que se pasan a este método de dibujo es la dirección de un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e3450-112">One of the arguments that you pass to such a drawing method is the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object.</span></span>

<span data-ttu-id="e3450-113">En los temas siguientes se trata el uso de lápices con más detalle:</span><span class="sxs-lookup"><span data-stu-id="e3450-113">The following topics cover the use of pens in more detail:</span></span>

-   [<span data-ttu-id="e3450-114">Uso de un lápiz para dibujar líneas y rectángulos</span><span class="sxs-lookup"><span data-stu-id="e3450-114">Using a Pen to Draw Lines and Rectangles</span></span>](-gdiplus-using-a-pen-to-draw-lines-and-rectangles-use.md)
-   [<span data-ttu-id="e3450-115">Establecer el ancho y la alineación del lápiz</span><span class="sxs-lookup"><span data-stu-id="e3450-115">Setting Pen Width and Alignment</span></span>](-gdiplus-setting-pen-width-and-alignment-use.md)
-   [<span data-ttu-id="e3450-116">Dibujar una línea con extremos de línea</span><span class="sxs-lookup"><span data-stu-id="e3450-116">Drawing a Line with Line Caps</span></span>](-gdiplus-drawing-a-line-with-line-caps-use.md)
-   [<span data-ttu-id="e3450-117">Combinar líneas</span><span class="sxs-lookup"><span data-stu-id="e3450-117">Joining Lines</span></span>](-gdiplus-joining-lines-use.md)
-   [<span data-ttu-id="e3450-118">Dibujar una línea discontinua personalizada</span><span class="sxs-lookup"><span data-stu-id="e3450-118">Drawing a Custom Dashed Line</span></span>](-gdiplus-drawing-a-custom-dashed-line-use.md)
-   [<span data-ttu-id="e3450-119">Dibujar una línea rellena con una textura</span><span class="sxs-lookup"><span data-stu-id="e3450-119">Drawing a Line Filled with a Texture</span></span>](-gdiplus-drawing-a-line-filled-with-a-texture-use.md)

 

 



