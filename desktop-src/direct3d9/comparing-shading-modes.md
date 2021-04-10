---
description: En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes. En el modo de sombreado Gouraud, sin embargo, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparar modos de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153576"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="479d0-104">Comparar modos de sombreado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="479d0-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="479d0-105">En el modo de sombreado plano, se muestra la siguiente pirámide con un borde nítido entre caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="479d0-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="479d0-106">En el modo de sombreado Gouraud, sin embargo, los valores de sombreado se interpolan en el borde y la apariencia final es de una superficie curva.</span><span class="sxs-lookup"><span data-stu-id="479d0-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![Ilustración de una pirámide con bordes nítidos y flechas que apuntan a las normales de cara](images/shade2.png)

<span data-ttu-id="479d0-108">El sombreado Gouraud muestra superficies planas más realista que el sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="479d0-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="479d0-109">Una superficie en el modo de sombreado plano es un color uniforme, pero el sombreado Gouraud permite que la luz se sitúe en una esfera más correctamente.</span><span class="sxs-lookup"><span data-stu-id="479d0-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="479d0-110">Este efecto es especialmente obvio si hay un origen de punto cercano.</span><span class="sxs-lookup"><span data-stu-id="479d0-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="479d0-111">El sombreado Gouraud suaviza los bordes nítidos entre polígonos que están visibles con sombreado plano.</span><span class="sxs-lookup"><span data-stu-id="479d0-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="479d0-112">Sin embargo, puede dar lugar a bandas de Mach, que son bandas de color o luz que no se combinan suavemente en polígonos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="479d0-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="479d0-113">La aplicación puede reducir la apariencia de las bandas de Mach aumentando el número de polígonos en un objeto, aumentando la resolución de la pantalla o aumentando la profundidad de color de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="479d0-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="479d0-114">El sombreado Gouraud puede omitir algunos detalles.</span><span class="sxs-lookup"><span data-stu-id="479d0-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="479d0-115">Por ejemplo, en la siguiente ilustración, una parte destacada se encuentra completamente dentro de una esfera de polígono.</span><span class="sxs-lookup"><span data-stu-id="479d0-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![Ilustración de un foco dentro de una esfera de polígono](images/gouraud.png)

<span data-ttu-id="479d0-117">En este caso, el sombreado Gouraud, que se interpola entre vértices, omitiría el foco por completo; la superficie se representaría como si no existiera el foco.</span><span class="sxs-lookup"><span data-stu-id="479d0-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="479d0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="479d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="479d0-119">Sombreado</span><span class="sxs-lookup"><span data-stu-id="479d0-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



