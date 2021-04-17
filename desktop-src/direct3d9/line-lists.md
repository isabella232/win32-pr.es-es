---
description: Una lista de líneas es una lista de segmentos de línea recta aislados.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Listas de líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714725"
---
# <a name="line-lists"></a><span data-ttu-id="bad29-103">Listas de líneas</span><span class="sxs-lookup"><span data-stu-id="bad29-103">Line Lists</span></span>

<span data-ttu-id="bad29-104">Una lista de líneas es una lista de segmentos de línea recta aislados.</span><span class="sxs-lookup"><span data-stu-id="bad29-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="bad29-105">Las listas de líneas son útiles para tareas como agregar sleet o una lluvia pesada a una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="bad29-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="bad29-106">Las aplicaciones crean una lista de líneas rellenando una matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="bad29-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="bad29-107">Tenga en cuenta que el número de vértices de una lista de líneas debe ser un número par mayor o igual que dos.</span><span class="sxs-lookup"><span data-stu-id="bad29-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="bad29-108">En la ilustración siguiente se muestra una lista de líneas representadas.</span><span class="sxs-lookup"><span data-stu-id="bad29-108">The following illustration shows a rendered line list.</span></span>

![Ilustración de una lista de líneas](images/linelst.png)

<span data-ttu-id="bad29-110">Puede aplicar materiales y texturas a una lista de líneas.</span><span class="sxs-lookup"><span data-stu-id="bad29-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="bad29-111">Los colores del material o la textura solo aparecen a lo largo de las líneas dibujadas, no en cualquier punto de entre las líneas.</span><span class="sxs-lookup"><span data-stu-id="bad29-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="bad29-112">En el código siguiente se muestra cómo crear vértices para esta lista de líneas.</span><span class="sxs-lookup"><span data-stu-id="bad29-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="bad29-113">En el ejemplo de código siguiente se muestra cómo representar una lista de líneas en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="bad29-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="bad29-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bad29-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad29-115">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="bad29-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
