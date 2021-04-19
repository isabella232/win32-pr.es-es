---
description: Una franja de líneas es un primitivo compuesto por segmentos de línea conectados.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Bandas de líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537617"
---
# <a name="line-strips"></a><span data-ttu-id="c2fd9-103">Bandas de líneas</span><span class="sxs-lookup"><span data-stu-id="c2fd9-103">Line Strips</span></span>

<span data-ttu-id="c2fd9-104">Una franja de líneas es un primitivo compuesto por segmentos de línea conectados.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-104">A line strip is a primitive that is composed of connected line segments.</span></span> <span data-ttu-id="c2fd9-105">La aplicación puede usar bandas de líneas para crear polígonos que no están cerrados.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-105">Your application can use line strips for creating polygons that are not closed.</span></span> <span data-ttu-id="c2fd9-106">Un polígono cerrado es un polígono cuyo último vértice está conectado al primer vértice por un segmento de línea.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-106">A closed polygon is a polygon whose last vertex is connected to its first vertex by a line segment.</span></span> <span data-ttu-id="c2fd9-107">Si la aplicación crea polígonos basados en franjas de líneas, no se garantiza que los vértices sean coplanares.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-107">If your application makes polygons based on line strips, the vertices are not guaranteed to be coplanar.</span></span>

<span data-ttu-id="c2fd9-108">En la ilustración siguiente se muestra una franja de líneas representada.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-108">The following illustration shows a rendered line strip.</span></span>

![Ilustración de una franja de líneas](images/linstrip.gif)

<span data-ttu-id="c2fd9-110">En el código siguiente se muestra cómo crear vértices para esta franja de líneas.</span><span class="sxs-lookup"><span data-stu-id="c2fd9-110">The following code shows how to create vertices for this line strip.</span></span>


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



<span data-ttu-id="c2fd9-111">En el ejemplo de código siguiente se muestra cómo representar una franja de líneas en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="c2fd9-111">The code example below shows how to render a line strip in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a><span data-ttu-id="c2fd9-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2fd9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2fd9-113">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="c2fd9-113">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
