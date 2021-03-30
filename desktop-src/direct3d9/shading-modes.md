---
description: El modo de sombreado que se usa para representar un polígono tiene un efecto profundo en su aspecto. Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una esfera de polígono. Direct3D admite dos modos de sombreado.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554669"
---
# <a name="shading-modes-direct3d-9"></a><span data-ttu-id="6c734-105">Modos de sombreado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6c734-105">Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="6c734-106">El modo de sombreado que se usa para representar un polígono tiene un efecto profundo en su aspecto.</span><span class="sxs-lookup"><span data-stu-id="6c734-106">The shading mode used to render a polygon has a profound effect on its appearance.</span></span> <span data-ttu-id="6c734-107">Los modos de sombreado determinan la intensidad del color y la iluminación en cualquier punto de una esfera de polígono.</span><span class="sxs-lookup"><span data-stu-id="6c734-107">Shading modes determine the intensity of color and lighting at any point on a polygon face.</span></span> <span data-ttu-id="6c734-108">Direct3D admite dos modos de sombreado.</span><span class="sxs-lookup"><span data-stu-id="6c734-108">Direct3D supports two shading modes.</span></span>

-   [<span data-ttu-id="6c734-109">Sombreado plano</span><span class="sxs-lookup"><span data-stu-id="6c734-109">Flat Shading</span></span>](#flat-shading)
-   [<span data-ttu-id="6c734-110">Sombreado Gouraud</span><span class="sxs-lookup"><span data-stu-id="6c734-110">Gouraud Shading</span></span>](#gouraud-shading)

## <a name="flat-shading"></a><span data-ttu-id="6c734-111">Sombreado plano</span><span class="sxs-lookup"><span data-stu-id="6c734-111">Flat Shading</span></span>

<span data-ttu-id="6c734-112">En el modo de sombreado plano, la canalización de representación de Direct3D representa un polígono, utilizando el color del material del polígono en su primer vértice como color para todo el polígono.</span><span class="sxs-lookup"><span data-stu-id="6c734-112">In the flat shading mode, the Direct3D rendering pipeline renders a polygon, using the color of the polygon material at its first vertex as the color for the entire polygon.</span></span> <span data-ttu-id="6c734-113">los objetos 3D que se representan con sombreado plano tienen bordes muy nítidos entre polígonos si no son coplanares.</span><span class="sxs-lookup"><span data-stu-id="6c734-113">3D objects that are rendered with flat shading have visibly sharp edges between polygons if they are not coplanar.</span></span>

<span data-ttu-id="6c734-114">En la ilustración siguiente se muestra un tetera representado con sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="6c734-114">The following illustration shows a teapot rendered with flat shading.</span></span> <span data-ttu-id="6c734-115">El contorno de cada polígono es claramente visible.</span><span class="sxs-lookup"><span data-stu-id="6c734-115">The outline of each polygon is clearly visible.</span></span> <span data-ttu-id="6c734-116">El sombreado plano es la forma más rápida de sombreado.</span><span class="sxs-lookup"><span data-stu-id="6c734-116">Flat shading is the fastest form of shading.</span></span>

![Ilustración de un tetera mediante el sombreado plano](images/flattea.png)

## <a name="gouraud-shading"></a><span data-ttu-id="6c734-118">Sombreado Gouraud</span><span class="sxs-lookup"><span data-stu-id="6c734-118">Gouraud Shading</span></span>

<span data-ttu-id="6c734-119">Cuando Direct3D representa un polígono mediante el sombreado Gouraud, calcula un color para cada vértice mediante los parámetros normales de vértice y de iluminación.</span><span class="sxs-lookup"><span data-stu-id="6c734-119">When Direct3D renders a polygon using Gouraud shading, it computes a color for each vertex by using the vertex normal and lighting parameters.</span></span> <span data-ttu-id="6c734-120">A continuación, interpola el color a lo largo de la superficie de los polígonos, la interpolación se realiza linealmente.</span><span class="sxs-lookup"><span data-stu-id="6c734-120">Then, it interpolates the color across the face of the polygons The interpolation is done linearly.</span></span> <span data-ttu-id="6c734-121">Por ejemplo, si el componente rojo del color del vértice 1 es 0,8 y el componente rojo del vértice 2 es 0,4, mediante el modo de sombreado Gouraud y el modelo de color RGB, el módulo de iluminación de Direct3D asigna un componente rojo de 0,6 al píxel en el punto medio de la línea entre estos vértices.</span><span class="sxs-lookup"><span data-stu-id="6c734-121">For example, if the red component of the color of vertex 1 is 0.8 and the red component of vertex 2 is 0.4, using the Gouraud shading mode and the RGB color model, the Direct3D lighting module assigns a red component of 0.6 to the pixel at the midpoint of the line between these vertices.</span></span>

<span data-ttu-id="6c734-122">En la ilustración siguiente se muestra el sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="6c734-122">The following illustration demonstrates Gouraud shading.</span></span> <span data-ttu-id="6c734-123">Este tetera se compone de muchos polígonos planos y triangulares.</span><span class="sxs-lookup"><span data-stu-id="6c734-123">This teapot is composed of many flat, triangular polygons.</span></span> <span data-ttu-id="6c734-124">Sin embargo, el sombreado Gouraud hace que la superficie del objeto aparezca curvada y suave.</span><span class="sxs-lookup"><span data-stu-id="6c734-124">However, Gouraud shading makes the surface of the object appear curved and smooth.</span></span>

![Ilustración de tetera mediante el sombreado Gouraud](images/gourtea.png)

<span data-ttu-id="6c734-126">El sombreado Gouraud también se puede usar para mostrar objetos con bordes nítidos.</span><span class="sxs-lookup"><span data-stu-id="6c734-126">Gouraud shading can also be used to display objects with sharp edges.</span></span>

<span data-ttu-id="6c734-127">Para obtener más información, consulte [vectores normales de cara y vértice (Direct3D 9)](face-and-vertex-normal-vectors.md).</span><span class="sxs-lookup"><span data-stu-id="6c734-127">For more information, see [Face and Vertex Normal Vectors (Direct3D 9)](face-and-vertex-normal-vectors.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c734-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c734-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c734-129">Sombreado</span><span class="sxs-lookup"><span data-stu-id="6c734-129">Shading</span></span>](shading.md)
</dt> </dl>

 

 



