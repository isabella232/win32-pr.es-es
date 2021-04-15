---
description: La mezcla de vértices indizados amplía la compatibilidad de mezcla de vértices en Direct3D para permitir el uso de matrices para la fusión.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusión de vértices indizados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494290"
---
# <a name="indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="f00c5-103">Fusión de vértices indizados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f00c5-103">Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="f00c5-104">La mezcla de vértices indizados amplía la compatibilidad de mezcla de vértices en Direct3D para permitir el uso de matrices para la fusión.</span><span class="sxs-lookup"><span data-stu-id="f00c5-104">Indexed vertex blending extends the vertex blending support in Direct3D to allow matrices to be used for blending.</span></span> <span data-ttu-id="f00c5-105">Se hace referencia a estas matrices mediante el uso de un índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="f00c5-105">These matrices are referred to by using a matrix index.</span></span> <span data-ttu-id="f00c5-106">Estos índices se proporcionan en cada vértice y hacen referencia a una paleta de hasta 256 matrices.</span><span class="sxs-lookup"><span data-stu-id="f00c5-106">These indices are supplied on a per-vertex basis and refer to a palette of up to 256 matrices.</span></span> <span data-ttu-id="f00c5-107">Cada índice es de 8 bits y cada vértice puede tener hasta cuatro índices, lo que permite mezclar cuatro matrices por vértice.</span><span class="sxs-lookup"><span data-stu-id="f00c5-107">Each index is 8 bits and each vertex can have up to four indices, which allows four matrices to be blended per vertex.</span></span> <span data-ttu-id="f00c5-108">Los índices se empaquetan en un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="f00c5-108">The indices are packed into a DWORD.</span></span> <span data-ttu-id="f00c5-109">Dado que los índices se especifican en función de cada vértice, hasta 12 matrices pueden afectar a un solo triángulo y cualquier matriz de la paleta puede afectar a los vértices de una llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="f00c5-109">Because indices are specified on a per-vertex basis, up to 12 matrices can affect a single triangle, and any matrix in the palette can affect the vertices of one draw call.</span></span> <span data-ttu-id="f00c5-110">Este enfoque tiene las ventajas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f00c5-110">This approach has the following advantages.</span></span>

-   <span data-ttu-id="f00c5-111">Permite que más matrices afecten a un solo triángulo.</span><span class="sxs-lookup"><span data-stu-id="f00c5-111">It enables more matrices to affect a single triangle.</span></span>
-   <span data-ttu-id="f00c5-112">Permite que se pasen más triángulos combinados en la misma llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="f00c5-112">It enables more blended triangles to be passed in the same draw call.</span></span>
-   <span data-ttu-id="f00c5-113">Hace que la mezcla de vértices sea independiente de los índices de triángulo.</span><span class="sxs-lookup"><span data-stu-id="f00c5-113">It makes vertex blending independent of triangle indices.</span></span> <span data-ttu-id="f00c5-114">Esto permite que las mallas progresivas funcionen junto con la combinación de vértices.</span><span class="sxs-lookup"><span data-stu-id="f00c5-114">This enables progressive meshes to work in conjunction with vertex blending.</span></span>

<span data-ttu-id="f00c5-115">Una desventaja de este enfoque es que no funciona con primitivas de superficie curvada cuando se produce teselación antes del procesamiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="f00c5-115">One disadvantage of this approach is that it does not work with curved-surface primitives when tessellation occurs before vertex processing.</span></span>

<span data-ttu-id="f00c5-116">En el diagrama siguiente se muestra cómo pueden afectar cuatro matrices a un vértice.</span><span class="sxs-lookup"><span data-stu-id="f00c5-116">The following diagram demonstrates how four matrices can affect a vertex.</span></span> <span data-ttu-id="f00c5-117">Cada vértice tiene hasta cuatro índices, por lo que se pueden mezclar cuatro matrices por vértice.</span><span class="sxs-lookup"><span data-stu-id="f00c5-117">Each vertex has up to four indices, so four matrices can be blended per vertex.</span></span> <span data-ttu-id="f00c5-118">El diagrama utiliza las matrices indizadas en 0, 2, 5 y 6.</span><span class="sxs-lookup"><span data-stu-id="f00c5-118">The diagram uses the matrices indexed at 0, 2, 5, and 6.</span></span>

![diagrama de fusión de vértices indexados con 4 de 256 matrices disponibles](images/dword1.png)

<span data-ttu-id="f00c5-120">En el diagrama siguiente se muestra cómo hasta 12 matrices pueden afectar a un triángulo.</span><span class="sxs-lookup"><span data-stu-id="f00c5-120">The following diagram demonstrates how up to 12 matrices can affect a triangle.</span></span> <span data-ttu-id="f00c5-121">Con los índices especificados en cada vértice, hasta 12 matrices pueden afectar al triángulo.</span><span class="sxs-lookup"><span data-stu-id="f00c5-121">Using indices specified on a per-vertex basis, up to 12 matrices can affect the triangle.</span></span>

![diagrama de la mezcla de vértices indexados para un triángulo mediante 12 de 256 matrices disponibles](images/dword2.png)

<span data-ttu-id="f00c5-123">La ecuación siguiente determina el caso general de cómo afectan las matrices a un vértice.</span><span class="sxs-lookup"><span data-stu-id="f00c5-123">The following equation determines the general case for how matrices effect a vertex.</span></span>

![ecuación de la mezcla de vértices indexados](images/indexedvblend.png)

<span data-ttu-id="f00c5-125">El <sub>modelo</sub> V es la posición del vértice del espacio del modelo de entrada.</span><span class="sxs-lookup"><span data-stu-id="f00c5-125">V <sub>model</sub> is the input model space vertex position.</span></span> <span data-ttu-id="f00c5-126">Index0.. Index3 son los índices de matriz por vértice empaquetados en un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="f00c5-126">Index0..Index3 are the per-vertex matrix indices packed into a DWORD.</span></span> <span data-ttu-id="f00c5-127">M \[ \] es la matriz de matrices mundiales que se indexan en.</span><span class="sxs-lookup"><span data-stu-id="f00c5-127">M\[\] is the array of world matrices that get indexed into.</span></span> <span data-ttu-id="f00c5-128">b ₀... b ₂ son los pesos de la mezcla.</span><span class="sxs-lookup"><span data-stu-id="f00c5-128">b₀..b₂ are the blend weights.</span></span> <span data-ttu-id="f00c5-129">El<sub>mundo</sub> V es la posición del vértice del espacio del mundo de salida.</span><span class="sxs-lookup"><span data-stu-id="f00c5-129">V<sub>world</sub> is the output world space vertex position.</span></span>

<span data-ttu-id="f00c5-130">Para obtener más información sobre la mezcla de vértices indizados, vea [usar la combinación de vértices indizada (Direct3D 9)](using-indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="f00c5-130">For more information about indexed vertex blending, see [Using Indexed Vertex Blending (Direct3D 9)](using-indexed-vertex-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f00c5-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f00c5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f00c5-132">Combinación de geometría</span><span class="sxs-lookup"><span data-stu-id="f00c5-132">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



