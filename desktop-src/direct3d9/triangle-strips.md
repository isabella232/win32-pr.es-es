---
description: Una franja de triángulo es una serie de triángulos conectados.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Bandas de triángulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555720"
---
# <a name="triangle-strips"></a><span data-ttu-id="6e1cb-103">Bandas de triángulo</span><span class="sxs-lookup"><span data-stu-id="6e1cb-103">Triangle Strips</span></span>

<span data-ttu-id="6e1cb-104">Una franja de triángulo es una serie de triángulos conectados.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-104">A triangle strip is a series of connected triangles.</span></span> <span data-ttu-id="6e1cb-105">Dado que los triángulos están conectados, no es necesario que la aplicación especifique repetidamente los tres vértices para cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-105">Because the triangles are connected, the application does not need to repeatedly specify all three vertices for each triangle.</span></span> <span data-ttu-id="6e1cb-106">Por ejemplo, solo necesita siete vértices para definir la franja de triángulo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-106">For example, you need only seven vertices to define the following triangle strip.</span></span>

![Ilustración de una franja de triángulo con siete vértices](images/tristrip.png)

<span data-ttu-id="6e1cb-108">El sistema utiliza los vértices v1, V2 y v3 para dibujar el primer triángulo; V2, V4 y v3 para dibujar el segundo triángulo; V3, V4 y V5 para dibujar el tercero; V4, V6 y V5 para dibujar el cuarto; etc.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-108">The system uses vertices v1, v2, and v3 to draw the first triangle; v2, v4, and v3 to draw the second triangle; v3, v4, and v5 to draw the third; v4, v6, and v5 to draw the fourth; and so on.</span></span> <span data-ttu-id="6e1cb-109">Observe que los vértices de los triángulos segundo y cuarto están desordenados; Esto es necesario para asegurarse de que todos los triángulos se dibujan en una orientación en el sentido de las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-109">Notice that the vertices of the second and fourth triangles are out of order; this is required to make sure that all the triangles are drawn in a clockwise orientation.</span></span>

<span data-ttu-id="6e1cb-110">La mayoría de los objetos de escenas 3D se componen de bandas de triángulo.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-110">Most objects in 3D scenes are composed of triangle strips.</span></span> <span data-ttu-id="6e1cb-111">Esto se debe a que las franjas de triángulos se pueden usar para especificar objetos complejos de una manera que haga un uso eficaz de la memoria y el tiempo de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-111">This is because triangle strips can be used to specify complex objects in a way that makes efficient use of memory and processing time.</span></span>

<span data-ttu-id="6e1cb-112">En la ilustración siguiente se muestra una franja de triángulo representada.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-112">The following illustration depicts a rendered triangle strip.</span></span>

![Ilustración de una franja de triángulo representada](images/tstrip2.png)

<span data-ttu-id="6e1cb-114">En el código siguiente se muestra cómo crear vértices para esta franja de triángulo.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-114">The following code shows how to create vertices for this triangle strip.</span></span>


```
struct CUSTOMVERTEX
{
float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



<span data-ttu-id="6e1cb-115">En el ejemplo de código siguiente se muestra cómo representar esta franja de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="6e1cb-115">The code example below shows how to render this triangle strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



<span data-ttu-id="6e1cb-116">Use una franja de triángulo para representar triángulos que no estén conectados entre sí.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-116">Use a triangle strip to render triangles that are not connected to one another.</span></span> <span data-ttu-id="6e1cb-117">Para ello, especifique un triángulo degenerado (es decir, un triángulo cuya área sea cero) en la lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-117">To do this, specify a degenerate triangle (that is, a triangle whose area is zero) in the triangle list.</span></span> <span data-ttu-id="6e1cb-118">Esto crea una línea entre los dos triángulos que no se representarán.</span><span class="sxs-lookup"><span data-stu-id="6e1cb-118">This creates a line between the two triangles which will not render.</span></span> <span data-ttu-id="6e1cb-119">Para representar solo los triángulos primero y último del ejemplo anterior, modifique el búfer de vértices como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="6e1cb-119">To render only the first and last triangles from the previous example, modify the vertex buffer as shown here:</span></span>


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a><span data-ttu-id="6e1cb-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e1cb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e1cb-121">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="6e1cb-121">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
