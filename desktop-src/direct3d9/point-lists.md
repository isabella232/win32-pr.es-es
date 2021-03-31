---
description: Una lista de puntos es una colección de vértices que se representan como puntos aislados. La aplicación puede utilizarlos en escenas 3D para los campos de estrella o líneas de puntos en la superficie de un polígono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Listas de puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806235"
---
# <a name="point-lists"></a><span data-ttu-id="1daf7-104">Listas de puntos</span><span class="sxs-lookup"><span data-stu-id="1daf7-104">Point Lists</span></span>

<span data-ttu-id="1daf7-105">Una lista de puntos es una colección de vértices que se representan como puntos aislados.</span><span class="sxs-lookup"><span data-stu-id="1daf7-105">A point list is a collection of vertices that are rendered as isolated points.</span></span> <span data-ttu-id="1daf7-106">La aplicación puede utilizarlos en escenas 3D para los campos de estrella o líneas de puntos en la superficie de un polígono.</span><span class="sxs-lookup"><span data-stu-id="1daf7-106">Your application can use them in 3D scenes for star fields, or dotted lines on the surface of a polygon.</span></span>

<span data-ttu-id="1daf7-107">En la ilustración siguiente se muestra una lista de puntos representados.</span><span class="sxs-lookup"><span data-stu-id="1daf7-107">The following illustration depicts a rendered point list.</span></span>

![Ilustración de una lista de puntos](images/pointlst.png)

<span data-ttu-id="1daf7-109">La aplicación puede aplicar materiales y texturas a una lista de puntos.</span><span class="sxs-lookup"><span data-stu-id="1daf7-109">Your application can apply materials and textures to a point list.</span></span> <span data-ttu-id="1daf7-110">Los colores del material o la textura solo aparecen en los puntos dibujados y no en cualquier punto entre los puntos.</span><span class="sxs-lookup"><span data-stu-id="1daf7-110">The colors in the material or texture appear only at the points drawn, and not anywhere between the points.</span></span>

<span data-ttu-id="1daf7-111">En el código siguiente se muestra cómo crear vértices para esta lista de puntos.</span><span class="sxs-lookup"><span data-stu-id="1daf7-111">The following code shows how to create vertices for this point list.</span></span>


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



<span data-ttu-id="1daf7-112">En el ejemplo de código siguiente se muestra cómo representar esta lista de puntos en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="1daf7-112">The code example below shows how to render this point list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a><span data-ttu-id="1daf7-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1daf7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1daf7-114">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="1daf7-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
