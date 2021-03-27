---
description: Puede limitar la cantidad de dibujo que realiza la aplicación al procesar el mensaje de \_ Paint de WM determinando el tamaño y la ubicación de la región de actualización.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Volver a dibujar en la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997308"
---
# <a name="redrawing-in-the-update-region"></a><span data-ttu-id="5984a-103">Volver a dibujar en la región de actualización</span><span class="sxs-lookup"><span data-stu-id="5984a-103">Redrawing in the Update Region</span></span>

<span data-ttu-id="5984a-104">Puede limitar la cantidad de dibujo que realiza la aplicación al procesar el mensaje [**de \_ Paint de WM**](wm-paint.md) determinando el tamaño y la ubicación de la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="5984a-104">You can limit the amount of drawing your application carries out when processing the [**WM\_PAINT**](wm-paint.md) message by determining the size and location of the update region.</span></span> <span data-ttu-id="5984a-105">Dado que el sistema utiliza la región de actualización al crear la región de recorte para el contexto de dispositivo de pantalla de la ventana, puede determinar indirectamente la región de actualización examinando la región de recorte.</span><span class="sxs-lookup"><span data-stu-id="5984a-105">Because the system uses the update region when creating the clipping region for the window's display device context, you can indirectly determine the update region by examining the clipping region.</span></span>

<span data-ttu-id="5984a-106">En el ejemplo siguiente, el procedimiento de ventana dibuja un triángulo, un rectángulo, un Pentágono y un hexágono, pero solo si todo o una parte de cada figura está dentro de la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="5984a-106">In the following example, the window procedure draws a triangle, a rectangle, a pentagon, and a hexagon, but only if all or a portion of each figure lies within the update region.</span></span> <span data-ttu-id="5984a-107">El procedimiento de ventana usa la función [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) y un rectángulo 100 por 100 para determinar si una figura está dentro de la región de recorte (y, por lo tanto, la región de actualización) del contexto de dispositivo común recuperado por [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span><span class="sxs-lookup"><span data-stu-id="5984a-107">The window procedure uses the [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) function and a 100-by-100 rectangle to determine whether a figure is within the clipping region (and therefore the update region) for the common device context retrieved by [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).</span></span>


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



<span data-ttu-id="5984a-108">Las coordenadas de cada figura en este ejemplo se encuentran dentro del mismo rectángulo 100 por 100.</span><span class="sxs-lookup"><span data-stu-id="5984a-108">The coordinates of each figure in this example lie within the same 100-by-100 rectangle.</span></span> <span data-ttu-id="5984a-109">Antes de dibujar una figura, el procedimiento de ventana establece el origen de la ventanilla en una parte diferente del área cliente mediante la función [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) .</span><span class="sxs-lookup"><span data-stu-id="5984a-109">Before drawing a figure, the window procedure sets the viewport origin to a different part of the client area by using the [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) function.</span></span> <span data-ttu-id="5984a-110">Esto evita que las figuras se dibujen una encima de la otra.</span><span class="sxs-lookup"><span data-stu-id="5984a-110">This prevents figures from being drawn one on top of the other.</span></span> <span data-ttu-id="5984a-111">Cambiar el origen de la ventanilla no afecta a la región de recorte, pero afecta a cómo se interpretan las coordenadas del rectángulo pasado a [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .</span><span class="sxs-lookup"><span data-stu-id="5984a-111">Changing the viewport origin does not affect the clipping region, but does affect how the coordinates of the rectangle passed to [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) are interpreted.</span></span> <span data-ttu-id="5984a-112">Cambiar el origen también permite usar un solo rectángulo para comprobar la región de actualización en lugar de rectángulos individuales para cada ilustración.</span><span class="sxs-lookup"><span data-stu-id="5984a-112">Changing the origin also allows you to use a single rectangle to check the update region rather than individual rectangles for each figure.</span></span>

 

 



