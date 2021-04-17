---
description: Un ventilador de triángulo es similar a una franja de triángulo, excepto en que todos los triángulos comparten un vértice, tal como se muestra en la siguiente ilustración.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventiladores de triángulo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553776"
---
# <a name="triangle-fans-direct3d-9"></a><span data-ttu-id="ee8bd-103">Ventiladores de triángulo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ee8bd-103">Triangle Fans (Direct3D 9)</span></span>

<span data-ttu-id="ee8bd-104">Un ventilador de triángulo es similar a una franja de triángulo, excepto en que todos los triángulos comparten un vértice, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-104">A triangle fan is similar to a triangle strip, except that all the triangles share one vertex, as shown in the following illustration.</span></span>

![Ilustración de un ventilador de triángulo](images/trifan.gif)

<span data-ttu-id="ee8bd-106">El sistema utiliza los vértices V2, V3 y V1 para dibujar el primer triángulo; V3, V4 y V1 para dibujar el segundo triángulo; V4, V5 y V1 para dibujar el tercer triángulo; etc.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-106">The system uses vertices v2, v3, and v1 to draw the first triangle; v3, v4, and v1 to draw the second triangle; v4, v5, and v1 to draw the third triangle; and so on.</span></span> <span data-ttu-id="ee8bd-107">Cuando está habilitado el sombreado plano, el sistema sombrea el triángulo con el color del primer vértice.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-107">When flat shading is enabled, the system shades the triangle with the color from its first vertex.</span></span>

<span data-ttu-id="ee8bd-108">En la ilustración siguiente se muestra un ventilador de triángulo representado.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-108">The following illustration depicts a rendered triangle fan.</span></span>

![Ilustración de un ventilador de triángulo representado](images/tfan2.gif)

<span data-ttu-id="ee8bd-110">En el código siguiente se muestra cómo crear vértices para este ventilador de triángulo.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-110">The following code shows how to create vertices for this triangle fan.</span></span>


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



<span data-ttu-id="ee8bd-111">En el ejemplo de código siguiente se muestra cómo representar este ventilador de triángulo en Direct3D 9 mediante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="ee8bd-111">The code example below shows how to render this triangle fan in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



<span data-ttu-id="ee8bd-112">Los ventiladores de triángulo no se admiten en Direct3D 10 o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ee8bd-112">Triangle fans are not supported in Direct3D 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee8bd-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee8bd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee8bd-114">Elementos primitivos</span><span class="sxs-lookup"><span data-stu-id="ee8bd-114">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
