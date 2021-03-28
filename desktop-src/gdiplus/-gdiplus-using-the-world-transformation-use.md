---
description: La transformación universal es una propiedad de la clase Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizar la transformación de coordenadas universales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275372"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="e8784-103">Utilizar la transformación de coordenadas universales</span><span class="sxs-lookup"><span data-stu-id="e8784-103">Using the World Transformation</span></span>

<span data-ttu-id="e8784-104">La transformación universal es una propiedad de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e8784-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e8784-105">Los números que especifican la transformación universal se almacenan en un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , que representa una matriz de 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="e8784-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="e8784-106">Las clases **Matrix** y **Graphics** tienen varios métodos para establecer los números en la matriz de transformación universal.</span><span class="sxs-lookup"><span data-stu-id="e8784-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="e8784-107">En los ejemplos de esta sección se manipulan los rectángulos porque los rectángulos son fáciles de dibujar y resulta sencillo ver los efectos de las transformaciones en los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="e8784-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="e8784-108">Comenzaremos creando un rectángulo de 50 por 50 y buscándolo en el origen (0,0).</span><span class="sxs-lookup"><span data-stu-id="e8784-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="e8784-109">El origen se encuentra en la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="e8784-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e8784-110">En el código siguiente se aplica una transformación de escala que expande el rectángulo por un factor de 1,75 en la dirección x y reduce el rectángulo entre un factor de 0,5 en la dirección y:</span><span class="sxs-lookup"><span data-stu-id="e8784-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e8784-111">El resultado es un rectángulo que es más largo en la dirección x y más corto en la dirección y que el original.</span><span class="sxs-lookup"><span data-stu-id="e8784-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="e8784-112">Para girar el rectángulo en lugar de escalarlo, use el código siguiente en lugar del código anterior:</span><span class="sxs-lookup"><span data-stu-id="e8784-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e8784-113">Para traducir el rectángulo, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e8784-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



