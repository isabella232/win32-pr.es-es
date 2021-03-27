---
description: Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Rellenar formas con un pincel de degradado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997493"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="7ea8c-103">Rellenar formas con un pincel de degradado</span><span class="sxs-lookup"><span data-stu-id="7ea8c-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="7ea8c-104">Puede usar un pincel de degradado para rellenar una forma con un color que cambia gradualmente.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="7ea8c-105">Por ejemplo, puede usar un degradado horizontal para rellenar una forma con un color que cambie gradualmente a medida que se desplaza desde el borde izquierdo de la forma hasta el borde derecho.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="7ea8c-106">Imagine un rectángulo con un borde izquierdo que sea negro (representado por los componentes rojo, verde y azul 0, 0, 0) y un borde derecho rojo (representado por 255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="7ea8c-107">Si el rectángulo tiene una anchura de 256 píxeles, el componente rojo de un píxel determinado será uno mayor que el componente rojo del píxel situado a su izquierda.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="7ea8c-108">El píxel situado más a la izquierda de una fila tiene componentes de color (0,0), el segundo píxel (1, 0, 0), el tercer píxel tiene (2, 0, 0), y así sucesivamente, hasta que llegue al píxel más a la derecha, que tiene componentes de color (255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="7ea8c-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="7ea8c-109">Estos valores de color interpolados constituyen el degradado de color.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="7ea8c-110">Un degradado lineal cambia el color a medida que se mueve horizontalmente, verticalmente o en paralelo a una línea inclinada especificada.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="7ea8c-111">Un degradado de trazado cambia el color a medida que se mueve sobre el interior y el límite de un trazado.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="7ea8c-112">Puede personalizar los degradados de trazado para lograr una gran variedad de efectos.</span><span class="sxs-lookup"><span data-stu-id="7ea8c-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="7ea8c-113">GDI+ proporciona las clases [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) y [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , que heredan de la clase [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="7ea8c-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="7ea8c-114">En los temas siguientes se tratan los degradados lineales y de trazado con más detalle:</span><span class="sxs-lookup"><span data-stu-id="7ea8c-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="7ea8c-115">Crear un degradado lineal</span><span class="sxs-lookup"><span data-stu-id="7ea8c-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="7ea8c-116">Crear un degradado de trazado</span><span class="sxs-lookup"><span data-stu-id="7ea8c-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="7ea8c-117">Aplicar la corrección gamma a un degradado</span><span class="sxs-lookup"><span data-stu-id="7ea8c-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



