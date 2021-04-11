---
description: En Direct3D y en la programación de ventanas, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rectángulos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151974"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="855a1-103">Rectángulos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="855a1-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="855a1-104">En Direct3D y en la programación de ventanas, se hace referencia a los objetos de la pantalla en términos de rectángulos delimitadores.</span><span class="sxs-lookup"><span data-stu-id="855a1-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="855a1-105">Los lados de un rectángulo delimitador siempre son paralelos a los lados de la pantalla, por lo que el rectángulo puede describirse mediante dos puntos, la esquina superior izquierda y la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="855a1-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="855a1-106">La mayoría de las aplicaciones usan la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para llevar información sobre un rectángulo delimitador que se usará al blitting a la pantalla o al realizar la detección de aciertos.</span><span class="sxs-lookup"><span data-stu-id="855a1-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="855a1-107">En C++, la estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) tiene la siguiente definición.</span><span class="sxs-lookup"><span data-stu-id="855a1-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="855a1-108">En el ejemplo anterior, los miembros izquierdo y superior son las coordenadas x e y de la esquina superior izquierda de un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="855a1-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="855a1-109">Del mismo modo, los miembros derecho e inferior forman las coordenadas de la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="855a1-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="855a1-110">En la ilustración siguiente se muestra cómo puede visualizar estos valores.</span><span class="sxs-lookup"><span data-stu-id="855a1-110">The following illustration shows how you can visualize these values.</span></span>

![Ilustración del rectángulo delimitado por los valores izquierdo, superior, derecho e inferior](images/rect.png)

<span data-ttu-id="855a1-112">La columna de píxeles en el borde derecho y la fila de píxeles en el borde inferior no se incluyen en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="855a1-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="855a1-113">Por ejemplo, si se bloquea un RECT con miembros {10, 10, 138, 138}, se obtiene un objeto de 128 píxeles de ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="855a1-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="855a1-114">En aras de la eficacia, la coherencia y la facilidad de uso, todas las funciones de presentación de Direct3D funcionan con los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="855a1-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="855a1-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="855a1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855a1-116">Sistemas de coordenadas y geometría</span><span class="sxs-lookup"><span data-stu-id="855a1-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
