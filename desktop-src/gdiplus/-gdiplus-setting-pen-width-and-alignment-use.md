---
description: 'Al crear un objeto Pen, puede proporcionar el ancho del lápiz como uno de los argumentos del constructor. También puede cambiar el ancho del lápiz con el método Pen:: SetWidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Establecer el ancho y la alineación del lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564653"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="6e92d-104">Establecer el ancho y la alineación del lápiz</span><span class="sxs-lookup"><span data-stu-id="6e92d-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="6e92d-105">Al crear un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , puede proporcionar el ancho del lápiz como uno de los argumentos del constructor.</span><span class="sxs-lookup"><span data-stu-id="6e92d-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="6e92d-106">También puede cambiar el ancho del lápiz con el método [**Pen:: SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .</span><span class="sxs-lookup"><span data-stu-id="6e92d-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="6e92d-107">Una línea teórica tiene un ancho de cero.</span><span class="sxs-lookup"><span data-stu-id="6e92d-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="6e92d-108">Al dibujar una línea, los píxeles se centran en la línea teórica.</span><span class="sxs-lookup"><span data-stu-id="6e92d-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="6e92d-109">En el ejemplo siguiente se dibuja una línea especificada dos veces: una vez con un lápiz negro de ancho 1 y otra con un lápiz verde de ancho 10.</span><span class="sxs-lookup"><span data-stu-id="6e92d-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="6e92d-110">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="6e92d-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="6e92d-111">Los píxeles verdes y los píxeles negros están centrados en la línea teórica.</span><span class="sxs-lookup"><span data-stu-id="6e92d-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="6e92d-112">Ilustración en la que se muestra una línea fina, diagonal y negra rodeada por una línea verde ancha</span><span class="sxs-lookup"><span data-stu-id="6e92d-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="6e92d-113">En el ejemplo siguiente se dibuja un rectángulo especificado dos veces: una vez con un lápiz negro de ancho 1 y otra con un lápiz verde de ancho 10.</span><span class="sxs-lookup"><span data-stu-id="6e92d-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="6e92d-114">El código pasa el valor **PenAlignmentCenter** (un elemento de la enumeración [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) al método [**Pen:: SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) para especificar que los píxeles dibujados con el lápiz verde están centrados en el límite del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6e92d-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="6e92d-115">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="6e92d-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="6e92d-116">Los píxeles verdes están centrados en el rectángulo teórico, que se representa mediante los píxeles negros.</span><span class="sxs-lookup"><span data-stu-id="6e92d-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![Ilustración en la que se muestra una línea negra fina en la forma de un rectángulo, rodeada por una línea verde más ancha](images/pens2.png)

<span data-ttu-id="6e92d-118">Puede cambiar la alineación del lápiz verde modificando la tercera instrucción del ejemplo anterior como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6e92d-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="6e92d-119">Ahora los píxeles de la línea verde ancha aparecen en el interior del rectángulo, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="6e92d-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![Ilustración en la que se muestra una línea negra fina en la forma de un Rectange, que incluye una línea verde ancha de la misma forma](images/pens3.png)

 

 



