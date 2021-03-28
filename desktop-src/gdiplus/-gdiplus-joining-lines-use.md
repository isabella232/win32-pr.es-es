---
description: Una combinación de líneas es el área común formada por dos líneas cuyos extremos coinciden o superponen.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Combinar líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551054"
---
# <a name="joining-lines"></a><span data-ttu-id="e0312-103">Combinar líneas</span><span class="sxs-lookup"><span data-stu-id="e0312-103">Joining Lines</span></span>

<span data-ttu-id="e0312-104">Una combinación de líneas es el área común formada por dos líneas cuyos extremos coinciden o superponen.</span><span class="sxs-lookup"><span data-stu-id="e0312-104">A line join is the common area that is formed by two lines whose ends meet or overlap.</span></span> <span data-ttu-id="e0312-105">GDI+ de Windows proporciona cuatro estilos de combinación de líneas: angular, bisel, redondo y angular.</span><span class="sxs-lookup"><span data-stu-id="e0312-105">Windows GDI+ provides four line join styles: miter, bevel, round, and miter clipped.</span></span> <span data-ttu-id="e0312-106">El estilo de combinación de líneas es una propiedad de la clase [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e0312-106">Line join style is a property of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="e0312-107">Cuando se especifica un estilo de combinación de líneas para un lápiz y, a continuación, se usa ese lápiz para dibujar un trazado, el estilo de combinación especificado se aplica a todas las líneas conectadas en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="e0312-107">When you specify a line join style for a pen and then use that pen to draw a path, the specified join style is applied to all the connected lines in the path.</span></span>

<span data-ttu-id="e0312-108">Puede especificar el estilo de unión de línea mediante el método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) de la clase [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e0312-108">You can specify the line join style by using the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method of the [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) class.</span></span> <span data-ttu-id="e0312-109">En el ejemplo siguiente se muestra una combinación de líneas biseladas entre una línea horizontal y una línea vertical:</span><span class="sxs-lookup"><span data-stu-id="e0312-109">The following example demonstrates a beveled line join between a horizontal line and a vertical line:</span></span>


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



<span data-ttu-id="e0312-110">En la ilustración siguiente se muestra la combinación de línea biselada resultante.</span><span class="sxs-lookup"><span data-stu-id="e0312-110">The following illustration shows the resulting beveled line join.</span></span>

![Ilustración que muestra dos líneas que se comparan en un ángulo recto, con una combinación biselada](images/pens5.png)

<span data-ttu-id="e0312-112">En el ejemplo anterior, el valor (**LineJoinBevel**) que se pasa al método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) es un elemento de la enumeración [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .</span><span class="sxs-lookup"><span data-stu-id="e0312-112">In the preceding example, the value (**LineJoinBevel**) passed to the [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) method is an element of the [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) enumeration.</span></span>

 

 



