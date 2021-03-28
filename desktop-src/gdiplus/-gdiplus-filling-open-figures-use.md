---
description: 'Puede rellenar una ruta de acceso pasando la dirección de un objeto GraphicsPath al método Graphics:: FillPath.'
ms.assetid: 4cf293cf-5155-4ce2-afeb-cc9ca9395764
title: Rellenar figuras abiertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f4a4608b787d8b0af8b9e9c7100a43c0c76dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564315"
---
# <a name="filling-open-figures"></a><span data-ttu-id="dfc59-103">Rellenar figuras abiertas</span><span class="sxs-lookup"><span data-stu-id="dfc59-103">Filling Open Figures</span></span>

<span data-ttu-id="dfc59-104">Puede rellenar una ruta de acceso pasando la dirección de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) al método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) .</span><span class="sxs-lookup"><span data-stu-id="dfc59-104">You can fill a path by passing the address of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object to the [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method.</span></span> <span data-ttu-id="dfc59-105">El método **Graphics:: FillPath** rellena la ruta de acceso según el modo de relleno (alternativo o bobinado) establecido actualmente para la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="dfc59-105">The **Graphics::FillPath** method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="dfc59-106">Si la ruta de acceso tiene figuras abiertas, la ruta de acceso se rellena como si esas figuras estuvieran cerradas.</span><span class="sxs-lookup"><span data-stu-id="dfc59-106">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="dfc59-107">GDI+ cierra una figura dibujando una línea recta desde su punto final hasta su punto inicial.</span><span class="sxs-lookup"><span data-stu-id="dfc59-107">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>

<span data-ttu-id="dfc59-108">En el ejemplo siguiente se crea una ruta de acceso que tiene una figura abierta (un arco) y una figura cerrada (una elipse).</span><span class="sxs-lookup"><span data-stu-id="dfc59-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="dfc59-109">El método [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) rellena la ruta de acceso según el modo de relleno predeterminado, que es FillModeAlternate.</span><span class="sxs-lookup"><span data-stu-id="dfc59-109">The [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) method fills the path according to the default fill mode, which is FillModeAlternate.</span></span>


```
GraphicsPath path;

// Add an open figure.
path.AddArc(0, 0, 150, 120, 30, 120);

// Add an intrinsically closed figure.
path.AddEllipse(50, 50, 50, 100);

Pen pen(Color(128, 0, 0, 255), 5);
SolidBrush brush(Color(255, 255, 0, 0));

// The fill mode is FillModeAlternate by default.
graphics.FillPath(&brush, &path);
graphics.DrawPath(&pen, &path);
```



<span data-ttu-id="dfc59-110">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="dfc59-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="dfc59-111">Tenga en cuenta que la ruta de acceso se rellena (según FillModeAlternate) como si la figura abierta se cerrara con una línea recta desde su punto final hasta su punto inicial.</span><span class="sxs-lookup"><span data-stu-id="dfc59-111">Note that path is filled (according to FillModeAlternate) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>

![Ilustración que muestra una elipse de alto que se superpone a la mitad inferior de una elipse ancha; la Unión se rellena pero la intersección está vacía](images/fillopenpath.png)

 

 



