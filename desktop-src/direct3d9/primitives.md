---
description: Un primitivo 3D es una colección de vértices que forman una única entidad 3D. El primitivo más sencillo es una colección de puntos en un sistema de coordenadas 3D, que se denomina lista de puntos.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitivas (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151973"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="ad0b5-104">Primitivas (gráficos de Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ad0b5-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="ad0b5-105">Un primitivo 3D es una colección de vértices que forman una única entidad 3D.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="ad0b5-106">El primitivo más sencillo es una colección de puntos en un sistema de coordenadas 3D, que se denomina lista de puntos.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="ad0b5-107">A menudo, las primitivas 3D son polígonos.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="ad0b5-108">Un polígono es una ilustración en 3D cerrada delimitada por al menos tres vértices.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="ad0b5-109">El polígono más sencillo es un triángulo.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="ad0b5-110">Microsoft Direct3D usa triángulos para componer la mayoría de sus polígonos, ya que se garantiza que los tres vértices de un triángulo son coplanares.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="ad0b5-111">La representación de vértices no planos es ineficaz.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="ad0b5-112">Puede combinar triángulos para formar polígonos y mallas grandes y complejos.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="ad0b5-113">En la ilustración siguiente se muestra un cubo.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-113">The following illustration shows a cube.</span></span> <span data-ttu-id="ad0b5-114">Dos triángulos forman cada una de las caras del cubo.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="ad0b5-115">El conjunto completo de triángulos forma un primitivo cúbico.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="ad0b5-116">Puede aplicar texturas y materiales a las superficies de primitivas para que parezcan una única forma sólida.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="ad0b5-117">Para obtener más información, vea [materiales (Direct3D 9)](materials.md) y [texturas de Direct3D (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="ad0b5-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![Ilustración de un cubo con dos triángulos en cada superficie](images/cube3d.png)

<span data-ttu-id="ad0b5-119">También puede utilizar triángulos para crear primitivas cuyas superficies parezcan curvas suaves.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="ad0b5-120">En la ilustración siguiente se muestra cómo se puede simular una esfera con triángulos.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="ad0b5-121">Una vez aplicado un material, la esfera tiene un aspecto curvo cuando se representa.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="ad0b5-122">Esto es especialmente cierto si usa el sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="ad0b5-123">Para obtener más información, vea [sombreado Gouraud](shading-modes.md).</span><span class="sxs-lookup"><span data-stu-id="ad0b5-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![Ilustración de una esfera que se simula mediante triángulos](images/sphere3d.png)

<span data-ttu-id="ad0b5-125">Los dispositivos Direct3D pueden crear y manipular los siguientes tipos de primitivas.</span><span class="sxs-lookup"><span data-stu-id="ad0b5-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="ad0b5-126">Listas de puntos</span><span class="sxs-lookup"><span data-stu-id="ad0b5-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="ad0b5-127">Listas de líneas</span><span class="sxs-lookup"><span data-stu-id="ad0b5-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="ad0b5-128">Bandas de líneas</span><span class="sxs-lookup"><span data-stu-id="ad0b5-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="ad0b5-129">Listas de triángulos</span><span class="sxs-lookup"><span data-stu-id="ad0b5-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="ad0b5-130">Bandas de triángulo</span><span class="sxs-lookup"><span data-stu-id="ad0b5-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="ad0b5-131">Ventiladores de triángulo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ad0b5-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="ad0b5-132">Puede representar tipos primitivos desde una aplicación de C++ con cualquiera de los métodos de representación de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="ad0b5-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad0b5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad0b5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad0b5-134">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="ad0b5-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
