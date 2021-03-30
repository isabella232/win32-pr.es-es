---
description: A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla. Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulo para decidir qué píxeles se aplican a un triángulo determinado.
ms.assetid: 919b36f1-d4de-4d5d-ba1a-0605bf59a6cd
title: Reglas de rasterización (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b2f12e0064202fcbca58f52cb163166d0a82
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279716"
---
# <a name="rasterization-rules-direct3d-9"></a><span data-ttu-id="21927-104">Reglas de rasterización (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="21927-104">Rasterization Rules (Direct3D 9)</span></span>

<span data-ttu-id="21927-105">A menudo, los puntos especificados para los vértices no coinciden exactamente con los píxeles de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="21927-105">Often, the points specified for vertices do not precisely match the pixels on the screen.</span></span> <span data-ttu-id="21927-106">Cuando esto sucede, Direct3D aplica reglas de rasterización de triángulo para decidir qué píxeles se aplican a un triángulo determinado.</span><span class="sxs-lookup"><span data-stu-id="21927-106">When this happens, Direct3D applies triangle rasterization rules to decide which pixels apply to a given triangle.</span></span>

-   [<span data-ttu-id="21927-107">Reglas de rasterización de triángulos</span><span class="sxs-lookup"><span data-stu-id="21927-107">Triangle Rasterization Rules</span></span>](#triangle-rasterization-rules)
-   [<span data-ttu-id="21927-108">Reglas de punto y línea</span><span class="sxs-lookup"><span data-stu-id="21927-108">Point and Line Rules</span></span>](#point-and-line-rules)
-   [<span data-ttu-id="21927-109">Reglas de Sprite de punto</span><span class="sxs-lookup"><span data-stu-id="21927-109">Point Sprite Rules</span></span>](#point-sprite-rules)

## <a name="triangle-rasterization-rules"></a><span data-ttu-id="21927-110">Reglas de rasterización de triángulos</span><span class="sxs-lookup"><span data-stu-id="21927-110">Triangle Rasterization Rules</span></span>

<span data-ttu-id="21927-111">Direct3D usa una Convención de llenado superior izquierda para rellenar la geometría.</span><span class="sxs-lookup"><span data-stu-id="21927-111">Direct3D uses a top-left filling convention for filling geometry.</span></span> <span data-ttu-id="21927-112">Se trata de la misma Convención que se usa para los rectángulos en GDI y OpenGL.</span><span class="sxs-lookup"><span data-stu-id="21927-112">This is the same convention that is used for rectangles in GDI and OpenGL.</span></span> <span data-ttu-id="21927-113">En Direct3D, el centro del píxel es el punto decisivo.</span><span class="sxs-lookup"><span data-stu-id="21927-113">In Direct3D, the center of the pixel is the decisive point.</span></span> <span data-ttu-id="21927-114">Si el centro está dentro de un triángulo, el píxel es parte del triángulo.</span><span class="sxs-lookup"><span data-stu-id="21927-114">If the center is inside a triangle, the pixel is part of the triangle.</span></span> <span data-ttu-id="21927-115">Los centros de píxeles están en coordenadas de enteros.</span><span class="sxs-lookup"><span data-stu-id="21927-115">Pixel centers are at integer coordinates.</span></span>

<span data-ttu-id="21927-116">Esta descripción de las reglas de rasterización triangular que usa Direct3D no se aplica necesariamente a todo el hardware disponible.</span><span class="sxs-lookup"><span data-stu-id="21927-116">This description of triangle-rasterization rules used by Direct3D does not necessarily apply to all available hardware.</span></span> <span data-ttu-id="21927-117">Las pruebas pueden revelar pequeñas variaciones en la implementación de estas reglas.</span><span class="sxs-lookup"><span data-stu-id="21927-117">Your testing may uncover minor variations in the implementation of these rules.</span></span>

<span data-ttu-id="21927-118">En la ilustración siguiente se muestra un rectángulo cuya esquina superior izquierda está en (0,0) y cuya esquina inferior derecha está en (5, 5).</span><span class="sxs-lookup"><span data-stu-id="21927-118">The following illustration shows a rectangle whose upper-left corner is at (0, 0) and whose lower-right corner is at (5, 5).</span></span> <span data-ttu-id="21927-119">Este rectángulo rellena 25 píxeles, tal y como cabría esperar.</span><span class="sxs-lookup"><span data-stu-id="21927-119">This rectangle fills 25 pixels, just as you would expect.</span></span> <span data-ttu-id="21927-120">El ancho del rectángulo se define como Right menos a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="21927-120">The width of the rectangle is defined as right minus left.</span></span> <span data-ttu-id="21927-121">El alto se define como inferior menos superior.</span><span class="sxs-lookup"><span data-stu-id="21927-121">The height is defined as bottom minus top.</span></span>

![Ilustración de un cuadrado numerado dividido en seis filas y columnas](images/pixmap.png)

<span data-ttu-id="21927-123">En la Convención de llenado superior izquierda, la *parte superior* se refiere a la ubicación vertical de los intervalos horizontales y a la *izquierda* hace referencia a la ubicación horizontal de los píxeles dentro de un intervalo.</span><span class="sxs-lookup"><span data-stu-id="21927-123">In the top-left filling convention, *top* refers to the vertical location of horizontal spans, and *left* refers to the horizontal location of pixels within a span.</span></span> <span data-ttu-id="21927-124">Un borde no puede ser un borde superior a menos que sea horizontal.</span><span class="sxs-lookup"><span data-stu-id="21927-124">An edge cannot be a top edge unless it is horizontal.</span></span> <span data-ttu-id="21927-125">En general, la mayoría de los triángulos solo tienen bordes izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="21927-125">In general, most triangles have only left and right edges.</span></span> <span data-ttu-id="21927-126">En la ilustración siguiente se muestra un borde superior y un borde derecho.</span><span class="sxs-lookup"><span data-stu-id="21927-126">The following illustration shows a top edge and a right edge.</span></span>

![Ilustración de un cuadrado numerado que contiene dos triángulos](images/triedge.png)

<span data-ttu-id="21927-128">La Convención de llenado superior izquierda determina la acción realizada por Direct3D cuando un triángulo pasa a través del centro de un píxel.</span><span class="sxs-lookup"><span data-stu-id="21927-128">The top-left filling convention determines the action taken by Direct3D when a triangle passes through the center of a pixel.</span></span> <span data-ttu-id="21927-129">En la ilustración siguiente se muestran dos triángulos, uno en (0,0), (5, 0) y (5, 5), y el otro en (0, 5), (0, 0) y (5, 5).</span><span class="sxs-lookup"><span data-stu-id="21927-129">The following illustration shows two triangles, one at (0, 0), (5, 0), and (5, 5), and the other at (0, 5), (0, 0), and (5, 5).</span></span> <span data-ttu-id="21927-130">En este caso, el primer triángulo obtiene 15 píxeles (se muestra en negro), mientras que el segundo obtiene solo 10 píxeles (mostrados en gris) porque el borde compartido es el borde izquierdo del primer triángulo.</span><span class="sxs-lookup"><span data-stu-id="21927-130">The first triangle in this case gets 15 pixels (shown in black), whereas the second gets only 10 pixels (shown in gray) because the shared edge is the left edge of the first triangle.</span></span>

![Ilustración de un cuadrado numerado que muestra dos triángulos](images/twotris.png)

<span data-ttu-id="21927-132">Si define un rectángulo con la esquina superior izquierda en (0,5, 0,5) y la esquina inferior derecha en (2,5, 4,5), el punto central de este rectángulo está en (1,5, 2,5).</span><span class="sxs-lookup"><span data-stu-id="21927-132">If you define a rectangle with its upper-left corner at (0.5, 0.5) and its lower-right corner at (2.5, 4.5), the center point of this rectangle is at (1.5, 2.5).</span></span> <span data-ttu-id="21927-133">Cuando el rasterizador de Direct3D tessellates este rectángulo, el centro de cada píxel es inequívoca dentro de cada uno de los cuatro triángulos, y no es necesaria la Convención de llenado superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="21927-133">When the Direct3D rasterizer tessellates this rectangle, the center of each pixel is unambiguously inside each of the four triangles, and the top-left filling convention is not needed.</span></span> <span data-ttu-id="21927-134">En la ilustración siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="21927-134">The following illustration shows this.</span></span> <span data-ttu-id="21927-135">Los píxeles del rectángulo se etiquetan según el triángulo en el que Direct3D los incluye.</span><span class="sxs-lookup"><span data-stu-id="21927-135">The pixels in the rectangle are labeled according to the triangle in which Direct3D includes them.</span></span>

![Muestra un cuadrado numerado que contiene un rectángulo que se divide en cuatro triángulos.](images/noambig.png)

<span data-ttu-id="21927-137">Si mueve el rectángulo de la ilustración anterior para que la esquina superior izquierda esté en (1,0, 1,0), la esquina inferior derecha en (3,0, 5,0) y su punto central en (2,0, 3,0), Direct3D aplica la Convención de llenado superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="21927-137">If you move the rectangle in the preceding illustration so that its upper-left corner is at (1.0, 1.0), its lower-right corner at (3.0, 5.0), and its center point at (2.0, 3.0), Direct3D applies the top-left filling convention.</span></span> <span data-ttu-id="21927-138">La mayoría de los píxeles de este rectángulo ocupan el borde entre dos o más triángulos, como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="21927-138">Most pixels in this rectangle straddle the border between two or more triangles, as the following illustration shows.</span></span>

![Ilustración de un cuadrado numerado que contiene un rectángulo dividido en cuatro triángulos](images/fillrule.png)

<span data-ttu-id="21927-140">En ambos rectángulos, los mismos píxeles se ven afectados, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="21927-140">For both rectangles, the same pixels are affected, as shown in the following illustration.</span></span>

![Ilustración de los píxeles afectados por los dos cuadrados numerados anteriores](images/samepix.png)

## <a name="point-and-line-rules"></a><span data-ttu-id="21927-142">Reglas de punto y línea</span><span class="sxs-lookup"><span data-stu-id="21927-142">Point and Line Rules</span></span>

<span data-ttu-id="21927-143">Los puntos se representan igual que los sprites de punto, que se representan como quadrilaterals alineados por pantalla y, por tanto, se ajustan a las mismas reglas que la representación de polígonos.</span><span class="sxs-lookup"><span data-stu-id="21927-143">Points are rendered the same as point sprites, which are both rendered as screen-aligned quadrilaterals and thus adhere to the same rules as polygon rendering.</span></span>

<span data-ttu-id="21927-144">Las reglas de representación de líneas sin alias son exactamente iguales que las de [las líneas de GDI](../gdi/lines.md).</span><span class="sxs-lookup"><span data-stu-id="21927-144">Non-antialiased line rendering rules are exactly the same as those for [GDI lines](../gdi/lines.md).</span></span>

<span data-ttu-id="21927-145">Para obtener información sobre la representación de líneas alisadas, vea [**ID3DXLine**](id3dxline.md).</span><span class="sxs-lookup"><span data-stu-id="21927-145">For information about antialiased line rendering, see [**ID3DXLine**](id3dxline.md).</span></span>

## <a name="point-sprite-rules"></a><span data-ttu-id="21927-146">Reglas de Sprite de punto</span><span class="sxs-lookup"><span data-stu-id="21927-146">Point Sprite Rules</span></span>

<span data-ttu-id="21927-147">Los sprites de punto y los primitivos de revisión se rasterizan como si los primitivos estuviesen en primer lugar en triángulos y los triángulos resultantes se rasterizan.</span><span class="sxs-lookup"><span data-stu-id="21927-147">Point sprites and patch primitives are rasterized as if the primitives were first tessellated into triangles and the resulting triangles rasterized.</span></span> <span data-ttu-id="21927-148">Para obtener más información, vea [sprites de punto (Direct3D 9)](point-sprites.md).</span><span class="sxs-lookup"><span data-stu-id="21927-148">For more information, see [Point Sprites (Direct3D 9)](point-sprites.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21927-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21927-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21927-150">Sistemas de coordenadas y geometría</span><span class="sxs-lookup"><span data-stu-id="21927-150">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
