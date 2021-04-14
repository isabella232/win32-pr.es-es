---
title: Superposición, proporcionaban y planos principales
description: Puede usar planos de capa de hardware (planos superpuestos y proporcionaban) en sus aplicaciones.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL en Windows, planos de capas de hardware
- planos de capa de hardware OpenGL
- planos superpuesto OpenGL
- proporcionaban de los aviones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665650"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="34ef7-107">Superposición, proporcionaban y planos principales</span><span class="sxs-lookup"><span data-stu-id="34ef7-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="34ef7-108">Puede usar planos de capa de hardware (planos superpuestos y proporcionaban) en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="34ef7-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="34ef7-109">Con Windows, los formatos de píxel describen las configuraciones de píxeles de un dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="34ef7-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="34ef7-110">Cada formato de píxel describe la profundidad y otras características de los búferes de color principales y describe los búferes adicionales (como profundidad, acumulación, estarcido y auxiliar) que usa el plano principal.</span><span class="sxs-lookup"><span data-stu-id="34ef7-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="34ef7-111">Los formatos de píxel ahora se han ampliado para incluir búferes de superposición y proporcionaban.</span><span class="sxs-lookup"><span data-stu-id="34ef7-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="34ef7-112">Los planos de capa siempre tienen un búfer de color Front-Left y también pueden incluir búferes de color frontal y derecho.</span><span class="sxs-lookup"><span data-stu-id="34ef7-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="34ef7-113">Cada plano de capa tiene un contexto de representación específico para representar en los búferes de capas.</span><span class="sxs-lookup"><span data-stu-id="34ef7-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="34ef7-114">No se pueden usar las funciones de dibujo de GDI en los planos de capas.</span><span class="sxs-lookup"><span data-stu-id="34ef7-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="34ef7-115">Una ventana administra los búferes de color de los planos de capa de forma similar al modo en que administra los búferes de color del plano principal.</span><span class="sxs-lookup"><span data-stu-id="34ef7-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="34ef7-116">Puede mostrar varias ventanas con planos superpuestos y/o proporcionaban al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="34ef7-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="34ef7-117">No puede tener ventanas de superposición de libre flotante que puedan moverse sobre cualquier ventana del plano de dibujo principal.</span><span class="sxs-lookup"><span data-stu-id="34ef7-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="34ef7-118">Además, dado que ocultaría los planos subyacentes en una ventana en todo momento, no puede usar planos emergentes de hardware que no tengan ningún color transparente.</span><span class="sxs-lookup"><span data-stu-id="34ef7-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="34ef7-119">Cada plano de capa de una ventana tiene una paleta asociada.</span><span class="sxs-lookup"><span data-stu-id="34ef7-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="34ef7-120">Puede establecer la paleta de un plano de capas de índice de color, pero la paleta de un plano de color RGBA es fija.</span><span class="sxs-lookup"><span data-stu-id="34ef7-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="34ef7-121">Debe obtener la paleta adecuada cuando una ventana está en primer plano.</span><span class="sxs-lookup"><span data-stu-id="34ef7-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="34ef7-122">Los planos de capa tienen un color o índice de píxeles transparente que permite que se muestren los planos de capas subyacentes.</span><span class="sxs-lookup"><span data-stu-id="34ef7-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="34ef7-123">Puede copiar el estado de un contexto de representación en otro contexto de representación en un plano de capas independiente.</span><span class="sxs-lookup"><span data-stu-id="34ef7-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="34ef7-124">También puede compartir listas de visualización entre los contextos de representación en diferentes planos de capas.</span><span class="sxs-lookup"><span data-stu-id="34ef7-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="34ef7-125">Las siguientes funciones se usan con planos de capas:</span><span class="sxs-lookup"><span data-stu-id="34ef7-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="34ef7-126">**wglCopyContext**</span><span class="sxs-lookup"><span data-stu-id="34ef7-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="34ef7-127">**wglCreateLayerContext**</span><span class="sxs-lookup"><span data-stu-id="34ef7-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="34ef7-128">**wglDescribeLayerPlane**</span><span class="sxs-lookup"><span data-stu-id="34ef7-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="34ef7-129">**wglGetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="34ef7-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="34ef7-130">**wglRealizeLayerPalette**</span><span class="sxs-lookup"><span data-stu-id="34ef7-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="34ef7-131">**wglSetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="34ef7-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="34ef7-132">**wglSwapLayerBuffers**</span><span class="sxs-lookup"><span data-stu-id="34ef7-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




