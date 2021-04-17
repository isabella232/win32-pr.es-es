---
description: Una lista de triángulo es una lista de triángulos aislados. Pueden estar o no cercanos entre sí. Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible por tres.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Listas de triángulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705252"
---
# <a name="triangle-lists"></a><span data-ttu-id="79555-105">Listas de triángulos</span><span class="sxs-lookup"><span data-stu-id="79555-105">Triangle Lists</span></span>

<span data-ttu-id="79555-106">Una lista de triángulo es una lista de triángulos aislados.</span><span class="sxs-lookup"><span data-stu-id="79555-106">A triangle list is a list of isolated triangles.</span></span> <span data-ttu-id="79555-107">Pueden estar o no cercanos entre sí.</span><span class="sxs-lookup"><span data-stu-id="79555-107">They might or might not be near each other.</span></span> <span data-ttu-id="79555-108">Una lista de triángulos debe tener al menos tres vértices y el número total de vértices debe ser divisible por tres.</span><span class="sxs-lookup"><span data-stu-id="79555-108">A triangle list must have at least three vertices and the total number of vertices must be divisible by three.</span></span>

<span data-ttu-id="79555-109">Use listas de triángulos para crear un objeto compuesto por piezas disjuntos.</span><span class="sxs-lookup"><span data-stu-id="79555-109">Use triangle lists to create an object that is composed of disjoint pieces.</span></span> <span data-ttu-id="79555-110">Por ejemplo, una forma de crear un muro de campo forzada en un juego 3D es especificar una lista grande de triángulos pequeños y no conectados.</span><span class="sxs-lookup"><span data-stu-id="79555-110">For instance, one way to create a force-field wall in a 3D game is to specify a large list of small, unconnected triangles.</span></span> <span data-ttu-id="79555-111">A continuación, aplique un material y una textura que parezcan emitir luz a la lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="79555-111">Then apply a material and texture that appears to emit light to the triangle list.</span></span> <span data-ttu-id="79555-112">Cada triángulo de la pared aparece iluminado.</span><span class="sxs-lookup"><span data-stu-id="79555-112">Each triangle in the wall appears to glow.</span></span> <span data-ttu-id="79555-113">La escena detrás de la pared se hace visible parcialmente a través de los huecos entre los triángulos, ya que un reproductor podría esperar al mirar un campo de fuerza.</span><span class="sxs-lookup"><span data-stu-id="79555-113">The scene behind the wall becomes partially visible through the gaps between the triangles, as a player might expect when looking at a force field.</span></span>

<span data-ttu-id="79555-114">Las listas de triángulos también son útiles para crear primitivas que tienen bordes nítidos y se sombrean con sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="79555-114">Triangle lists are also useful for creating primitives that have sharp edges and are shaded with Gouraud shading.</span></span> <span data-ttu-id="79555-115">Consulte [vectores normales de cara y vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="79555-115">See [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

<span data-ttu-id="79555-116">En la ilustración siguiente se muestra una lista de triángulos representada.</span><span class="sxs-lookup"><span data-stu-id="79555-116">The following illustration depicts a rendered triangle list.</span></span>

![Ilustración de una lista de triángulos representada](images/trilist.png)

<span data-ttu-id="79555-118">En el código siguiente se muestra cómo crear vértices para esta lista de triángulos.</span><span class="sxs-lookup"><span data-stu-id="79555-118">The following code shows how to create vertices for this triangle list.</span></span>


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



<span data-ttu-id="79555-119">En el ejemplo de código siguiente se muestra cómo representar esta lista de triángulos en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="79555-119">The code example below shows how to render this triangle list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



<span data-ttu-id="79555-120">También puede usar bandas triangulares para representar triángulos que no están conectados entre sí.</span><span class="sxs-lookup"><span data-stu-id="79555-120">You can also use triangle strips to render triangles that are not connected to one another.</span></span> <span data-ttu-id="79555-121">Para ello, especifique un triángulo degenerado (es decir, un triángulo con tamaño cero) en la lista; Esto creará una línea entre los dos triángulos que no aparecerá durante la representación.</span><span class="sxs-lookup"><span data-stu-id="79555-121">To do this, specify a degenerate triangle (that is, a triangle with zero size) in the list; this will create a line between the two triangles which will not appear during rendering.</span></span> <span data-ttu-id="79555-122">Por ejemplo, para representar solo el primer y último triángulo del ejemplo anterior, inicialice el búfer de vértices con los siguientes vértices:</span><span class="sxs-lookup"><span data-stu-id="79555-122">For example, to render only the first and last triangle from the previous example, initialize the vertex buffer with the following vertices:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="79555-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79555-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79555-124">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="79555-124">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
