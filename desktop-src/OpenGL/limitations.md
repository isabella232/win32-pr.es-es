---
title: Limitaciones
description: Limitaciones
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL en Windows, limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775259"
---
# <a name="limitations"></a><span data-ttu-id="594b2-104">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="594b2-104">Limitations</span></span>

<span data-ttu-id="594b2-105">La implementación genérica tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="594b2-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="594b2-106">Impresión.</span><span class="sxs-lookup"><span data-stu-id="594b2-106">Printing.</span></span>

    <span data-ttu-id="594b2-107">Puede imprimir una imagen de OpenGL directamente en una impresora solo con metaarchivos.</span><span class="sxs-lookup"><span data-stu-id="594b2-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="594b2-108">Para obtener más información, consulte [Imprimir una imagen de OpenGL](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="594b2-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="594b2-109">Los gráficos de OpenGL y GDI no se pueden mezclar en una ventana de búfer doble.</span><span class="sxs-lookup"><span data-stu-id="594b2-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="594b2-110">Una aplicación puede dibujar directamente gráficos OpenGL y gráficos GDI en una ventana de un solo búfer, pero no en una ventana de búfer doble.</span><span class="sxs-lookup"><span data-stu-id="594b2-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="594b2-111">No hay paletas de colores de hardware por ventana.</span><span class="sxs-lookup"><span data-stu-id="594b2-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="594b2-112">Windows tiene una sola paleta de colores de hardware del sistema, que se aplica a toda la pantalla.</span><span class="sxs-lookup"><span data-stu-id="594b2-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="594b2-113">Una ventana de OpenGL no puede tener su propia paleta de hardware, pero puede tener su propia paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="594b2-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="594b2-114">Para ello, debe convertirse en una aplicación que tenga en cuenta la paleta.</span><span class="sxs-lookup"><span data-stu-id="594b2-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="594b2-115">Para obtener más información, vea [modos de color OpenGL y administración de la paleta de Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="594b2-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="594b2-116">No hay compatibilidad directa con el portapapeles, el intercambio dinámico de datos (DDE) o OLE.</span><span class="sxs-lookup"><span data-stu-id="594b2-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="594b2-117">Una ventana con gráficos OpenGL no es compatible directamente con estas funciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="594b2-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="594b2-118">Sin embargo, hay soluciones alternativas para usar el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="594b2-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="594b2-119">Para obtener más información, vea [copiar una imagen de OpenGL en el portapapeles](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="594b2-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="594b2-120">No se incluye la biblioteca de clases de C++ de inventor 2,0.</span><span class="sxs-lookup"><span data-stu-id="594b2-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="594b2-121">La biblioteca de clases Inventory, que se basa en OpenGL, proporciona construcciones de nivel superior para programar gráficos 3D.</span><span class="sxs-lookup"><span data-stu-id="594b2-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="594b2-122">No se incluye en la versión actual de la implementación de OpenGL para Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="594b2-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="594b2-123">No se admiten las siguientes características de formato de píxel: imágenes Stereoscopic, bitplanes alfa y búferes auxiliares.</span><span class="sxs-lookup"><span data-stu-id="594b2-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="594b2-124">Sin embargo, hay compatibilidad con varios búferes auxiliares, entre los que se incluyen: búfer de estarcido, búfer de acumulación, búfer de reserva (doble búfer), superposición y búfer de plano de proporcionaban y búfer de profundidad (eje z).</span><span class="sxs-lookup"><span data-stu-id="594b2-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




