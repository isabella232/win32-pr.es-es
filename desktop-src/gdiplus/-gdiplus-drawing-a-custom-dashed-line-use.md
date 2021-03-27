---
description: Windows GDI+ proporciona varios estilos de guión que se enumeran en la enumeración DashStyle. Si esos estilos de guiones estándar no se adaptan a sus necesidades, puede crear un patrón de guiones personalizado.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Dibujar una línea discontinua personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988205"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="d6913-104">Dibujar una línea discontinua personalizada</span><span class="sxs-lookup"><span data-stu-id="d6913-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="d6913-105">Windows GDI+ proporciona varios estilos de guión que se enumeran en la enumeración [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) .</span><span class="sxs-lookup"><span data-stu-id="d6913-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="d6913-106">Si esos estilos de guiones estándar no se adaptan a sus necesidades, puede crear un patrón de guiones personalizado.</span><span class="sxs-lookup"><span data-stu-id="d6913-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="d6913-107">Para dibujar una línea discontinua personalizada, coloque las longitudes de los guiones y espacios en una matriz y pase la dirección de la matriz como argumento al método [**Pen:: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) de un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="d6913-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="d6913-108">En el ejemplo siguiente se dibuja una línea discontinua personalizada basada en la matriz {5, 2, 15, 4}.</span><span class="sxs-lookup"><span data-stu-id="d6913-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="d6913-109">Si multiplica los elementos de la matriz por el ancho del lápiz de 5, obtendrá {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="d6913-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="d6913-110">Los guiones mostrados alternan la longitud entre 25 y 75, y los espacios alternan entre 10 y 20.</span><span class="sxs-lookup"><span data-stu-id="d6913-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="d6913-111">En la ilustración siguiente se muestra la línea discontinua resultante.</span><span class="sxs-lookup"><span data-stu-id="d6913-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="d6913-112">Tenga en cuenta que el guión final tiene que tener menos de 25 unidades para que la línea pueda acabar en (405).</span><span class="sxs-lookup"><span data-stu-id="d6913-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![Ilustración que muestra una línea discontinua; cada segmento es una línea corta seguida de una larga](images/pens6.png)

 

 



