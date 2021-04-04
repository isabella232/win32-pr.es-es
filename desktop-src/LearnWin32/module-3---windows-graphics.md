---
title: Módulo 3. Gráficos de Windows
description: En el módulo 1 de esta serie se ha mostrado cómo crear una ventana en blanco.
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075324"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="cba1e-104">Módulo 3.</span><span class="sxs-lookup"><span data-stu-id="cba1e-104">Module 3.</span></span> <span data-ttu-id="cba1e-105">Gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="cba1e-105">Windows Graphics</span></span>

<span data-ttu-id="cba1e-106">En el [módulo 1](your-first-windows-program.md) de esta serie se ha mostrado cómo crear una ventana en blanco.</span><span class="sxs-lookup"><span data-stu-id="cba1e-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="cba1e-107">El [módulo 2](module-2--using-com-in-your-windows-program.md) llevó un ligero desvío a través del modelo de objetos componentes (com), que es la base de muchas de las API modernas de Windows.</span><span class="sxs-lookup"><span data-stu-id="cba1e-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="cba1e-108">Ahora es el momento de agregar gráficos a la ventana en blanco que creamos en el módulo 1.</span><span class="sxs-lookup"><span data-stu-id="cba1e-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="cba1e-109">Este módulo se inicia con una introducción de alto nivel de la arquitectura de gráficos de Windows.</span><span class="sxs-lookup"><span data-stu-id="cba1e-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="cba1e-110">A continuación, veremos Direct2D, una potente API de gráficos que se presentó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cba1e-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cba1e-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cba1e-111">In this section</span></span>

-   [<span data-ttu-id="cba1e-112">Información general de la arquitectura de gráficos de Windows</span><span class="sxs-lookup"><span data-stu-id="cba1e-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="cba1e-113">El Administrador de ventanas de escritorio</span><span class="sxs-lookup"><span data-stu-id="cba1e-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="cba1e-114">Modo retenido frente al modo inmediato</span><span class="sxs-lookup"><span data-stu-id="cba1e-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="cba1e-115">Su primer programa de Direct2D</span><span class="sxs-lookup"><span data-stu-id="cba1e-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="cba1e-116">Destinos de representación, dispositivos y recursos</span><span class="sxs-lookup"><span data-stu-id="cba1e-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="cba1e-117">Dibujo con Direct2D</span><span class="sxs-lookup"><span data-stu-id="cba1e-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="cba1e-118">PPP y Device-Independent píxeles</span><span class="sxs-lookup"><span data-stu-id="cba1e-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="cba1e-119">Usar el color en Direct2D</span><span class="sxs-lookup"><span data-stu-id="cba1e-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="cba1e-120">Aplicación de transformaciones en Direct2D</span><span class="sxs-lookup"><span data-stu-id="cba1e-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="cba1e-121">Apéndice: transformaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="cba1e-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="cba1e-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cba1e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba1e-123">Aprender a programar para Windows en C++</span><span class="sxs-lookup"><span data-stu-id="cba1e-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 




