---
title: Paletas y el administrador de paletas
description: El administrador de paletas de Windows, que forma parte de GDI, se centra específicamente en los adaptadores de pantalla de 8 bits con una paleta de hardware de 256 entradas de color.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL en Windows, administrador de paletas
- OpenGL en Windows, paletas de hardware
- Administrador de paletas OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665649"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="ae75c-107">Paletas y el administrador de paletas</span><span class="sxs-lookup"><span data-stu-id="ae75c-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="ae75c-108">El administrador de paletas de Windows, que forma parte de GDI, se centra específicamente en los adaptadores de pantalla de 8 bits con una *paleta de hardware* de 256 entradas de color.</span><span class="sxs-lookup"><span data-stu-id="ae75c-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="ae75c-109">Los píxeles de la pantalla se almacenan como un índice de 8 bits en la paleta de hardware.</span><span class="sxs-lookup"><span data-stu-id="ae75c-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="ae75c-110">Cada entrada de la paleta de hardware suele definir un color de 24 bits (8 en rojo, verde y azul).</span><span class="sxs-lookup"><span data-stu-id="ae75c-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="ae75c-111">El administrador de paletas mantiene una *paleta del sistema* que es una copia de la paleta de hardware.</span><span class="sxs-lookup"><span data-stu-id="ae75c-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="ae75c-112">La paleta del sistema se divide en dos secciones: 20 colores reservados y los colores 236 restantes, que se pueden establecer mediante el administrador de paletas.</span><span class="sxs-lookup"><span data-stu-id="ae75c-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="ae75c-113">Una *paleta lógica* de 20 colores predeterminada se selecciona y se lleva a cabo en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae75c-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="ae75c-114">Puede crear y usar una nueva paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="ae75c-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="ae75c-115">Para cambiar la paleta del sistema, seleccione y observe la paleta lógica que creó.</span><span class="sxs-lookup"><span data-stu-id="ae75c-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="ae75c-116">Probablemente creará una paleta lógica para especificar los colores que desea que se muestren en la aplicación de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="ae75c-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="ae75c-117">Con ciertas llamadas GDI, puede reemplazar temporalmente la mayoría de la paleta del sistema por una paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="ae75c-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="ae75c-118">Con una paleta lógica, puede definir colores de píxeles para la GDI mediante el modo RGBA o el modo de índice de color.</span><span class="sxs-lookup"><span data-stu-id="ae75c-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="ae75c-119">El tamaño máximo de una paleta lógica es de 256 colores para dispositivos de 8 bits y 4.096 colores en un dispositivo de color verdadero (16, 24 y 32 bits).</span><span class="sxs-lookup"><span data-stu-id="ae75c-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="ae75c-120">Para obtener más información sobre los modos RGBA y índice de color, consulte [modo RGBA y administración](rgba-mode-and-windows-palette-management.md) de la paleta de Windows y [modos de color OpenGL y administración de paletas de Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="ae75c-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




