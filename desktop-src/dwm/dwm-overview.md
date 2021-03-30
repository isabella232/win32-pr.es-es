---
title: Administrador de ventanas de escritorio
description: La característica de composición de escritorio, introducida en Windows Vista, ha cambiado fundamentalmente el modo en que las aplicaciones muestran píxeles en la pantalla.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Administrador de ventanas de escritorio (DWM), acerca de
- DWM (Administrador de ventanas de escritorio), acerca de
- Administrador de ventanas de escritorio (DWM), composición
- DWM (Administrador de ventanas de escritorio), composición
- composición de escritorio
- composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776728"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="dcbf1-109">Administrador de ventanas de escritorio</span><span class="sxs-lookup"><span data-stu-id="dcbf1-109">Desktop Window Manager</span></span>

<span data-ttu-id="dcbf1-110">La característica de composición de escritorio, introducida en Windows Vista, ha cambiado fundamentalmente el modo en que las aplicaciones muestran píxeles en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="dcbf1-111">Cuando la composición del escritorio está habilitada, las ventanas individuales ya no se dibujan directamente en la pantalla o en el dispositivo de pantalla principal como ocurría en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="dcbf1-112">En su lugar, su dibujo se redirige a superficies fuera de la pantalla en la memoria de vídeo, que luego se representan en una imagen de escritorio y se muestran en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="dcbf1-113">La composición del escritorio se realiza mediante el Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="dcbf1-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="dcbf1-114">A través de la composición del escritorio, DWM permite efectos visuales en el escritorio, así como diversas características, como marcos de ventanas de cristal, animaciones de transición de ventanas 3D, Windows Flip y Windows Flip3D y compatibilidad con alta resolución.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="dcbf1-115">La Administrador de ventanas de escritorio se ejecuta como un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="dcbf1-116">Se puede habilitar y deshabilitar mediante el elemento del panel de control herramientas administrativas, en servicios, como Administrador de ventanas de escritorio administrador de sesión.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="dcbf1-117">Una aplicación puede controlar muchas de las características de DWM o tener acceso a ellas a través de las API de DWM.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="dcbf1-118">En la documentación siguiente se describen las características y los requisitos de las API de DWM.</span><span class="sxs-lookup"><span data-stu-id="dcbf1-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="dcbf1-119">Información general de DWM</span><span class="sxs-lookup"><span data-stu-id="dcbf1-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="dcbf1-120">Código de ejemplo de DWM</span><span class="sxs-lookup"><span data-stu-id="dcbf1-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="dcbf1-121">Referencia de DWM</span><span class="sxs-lookup"><span data-stu-id="dcbf1-121">DWM Reference</span></span>](reference.md)

 

 




