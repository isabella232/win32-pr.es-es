---
description: Una elipse se especifica mediante su rectángulo delimitador. En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.
ms.assetid: 45e80501-4d64-480b-a7c7-3af52c00a0aa
title: Elipses y arcos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b1aaaff5ff27191ed7f0bf64ddbcb414be6319
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156192"
---
# <a name="ellipses-and-arcs"></a><span data-ttu-id="e86ec-104">Elipses y arcos</span><span class="sxs-lookup"><span data-stu-id="e86ec-104">Ellipses and Arcs</span></span>

<span data-ttu-id="e86ec-105">Una elipse se especifica mediante su rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e86ec-105">An ellipse is specified by its bounding rectangle.</span></span> <span data-ttu-id="e86ec-106">En la ilustración siguiente se muestra una elipse junto con su rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e86ec-106">The following illustration shows an ellipse along with its bounding rectangle.</span></span>

![Ilustración de una elipse incluida dentro de un rectángulo delimitador](images/aboutgdip02-art05.png)

<span data-ttu-id="e86ec-108">Para dibujar una elipse, necesita un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="e86ec-108">To draw an ellipse, you need a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="e86ec-109">El objeto **Graphics** proporciona el método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) y el objeto **Pen** almacena atributos de la elipse, como el ancho y el color de la línea.</span><span class="sxs-lookup"><span data-stu-id="e86ec-109">The **Graphics** object provides the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, and the **Pen** object stores attributes of the ellipse, such as line width and color.</span></span> <span data-ttu-id="e86ec-110">La dirección del objeto **Pen** se pasa como uno de los argumentos al método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="e86ec-110">The address of the **Pen** object is passed as one of the arguments to the DrawEllipse method.</span></span> <span data-ttu-id="e86ec-111">Los argumentos restantes pasados al método DrawEllipse especifican el rectángulo delimitador de la elipse.</span><span class="sxs-lookup"><span data-stu-id="e86ec-111">The remaining arguments passed to the DrawEllipse method specify the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="e86ec-112">En el ejemplo siguiente se dibuja una elipse; el rectángulo delimitador tiene un ancho de 160, un alto de 80 y una esquina superior izquierda de (100, 50).</span><span class="sxs-lookup"><span data-stu-id="e86ec-112">The following example draws an ellipse; the bounding rectangle has a width of 160, a height of 80, and an upper-left corner of (100, 50).</span></span>


```
myGraphics.DrawEllipse(&myPen, 100, 50, 160, 80);
```



<span data-ttu-id="e86ec-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) es un método sobrecargado de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , por lo que hay varias formas de proporcionarle argumentos.</span><span class="sxs-lookup"><span data-stu-id="e86ec-113">[DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) is an overloaded method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class, so there are several ways you can supply it with arguments.</span></span> <span data-ttu-id="e86ec-114">Por ejemplo, puede construir un objeto [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) y pasar una referencia al objeto **Rect** como argumento al método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="e86ec-114">For example, you can construct a [**Rect**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect) object and pass a reference to the **Rect** object as an argument to the DrawEllipse method.</span></span>


```
Rect myRect(100, 50, 160, 80);
myGraphics.DrawEllipse(&myPen, myRect);
```



<span data-ttu-id="e86ec-115">Un arco es una parte de una elipse.</span><span class="sxs-lookup"><span data-stu-id="e86ec-115">An arc is a portion of an ellipse.</span></span> <span data-ttu-id="e86ec-116">Para dibujar un arco, se llama al método [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="e86ec-116">To draw an arc, you call the [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inint_inint_inint_inint_inreal_inreal)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="e86ec-117">Los parámetros del método DrawArc son los mismos que los parámetros del método [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) , salvo que DrawArc requiere un ángulo inicial y un ángulo de barrido.</span><span class="sxs-lookup"><span data-stu-id="e86ec-117">The parameters of the DrawArc method are the same as the parameters of the [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrect_)) method, except that DrawArc requires a starting angle and sweep angle.</span></span> <span data-ttu-id="e86ec-118">En el ejemplo siguiente se dibuja un arco con un ángulo inicial de 30 grados y un ángulo de barrido de 180 grados.</span><span class="sxs-lookup"><span data-stu-id="e86ec-118">The following example draws an arc with a starting angle of 30 degrees and a sweep angle of 180 degrees.</span></span>


```
myGraphics.DrawArc(&myPen, 100, 50, 160, 80, 30, 180);
```



<span data-ttu-id="e86ec-119">En la ilustración siguiente se muestra el arco, la elipse y el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="e86ec-119">The following illustration shows the arc, the ellipse, and the bounding rectangle.</span></span>

![Ilustración de una elipse dentro de un rectángulo delimitador; la mitad inferior izquierda de la elipse se dibuja en rojo](images/aboutgdip02-art06.png)

 

 



