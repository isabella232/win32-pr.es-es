---
title: El Administrador de ventanas de escritorio
description: .
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73167b762a9952eb508f09e70f3d4183b3b7a018
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357051"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="fc4ad-103">El Administrador de ventanas de escritorio</span><span class="sxs-lookup"><span data-stu-id="fc4ad-103">The Desktop Window Manager</span></span>

<span data-ttu-id="fc4ad-104">Antes de Windows Vista, un programa de Windows dibujaría directamente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="fc4ad-105">En otras palabras, el programa escribiría directamente en el búfer de memoria que muestra la tarjeta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="fc4ad-106">Este enfoque puede producir artefactos visuales si una ventana no se vuelve a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="fc4ad-107">Por ejemplo, si el usuario arrastra una ventana sobre otra ventana y la ventana inferior no vuelve a dibujarse lo suficiente rápidamente, la ventana de nivel superior puede dejar un rastro:</span><span class="sxs-lookup"><span data-stu-id="fc4ad-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![captura de pantalla que muestra los artefactos Repaint.](images/graphics04.png)

<span data-ttu-id="fc4ad-109">El rastro se debe a que las ventanas se dibujan en la misma área de memoria.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="fc4ad-110">A medida que se arrastra la ventana de nivel superior, se debe volver a dibujar la ventana siguiente.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="fc4ad-111">Si el repintado es demasiado lento, provoca los artefactos mostrados en la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="fc4ad-112">Windows Vista ha cambiado fundamentalmente el modo en que se dibujan las ventanas, introduciendo el Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="fc4ad-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="fc4ad-113">Cuando DWM está habilitado, una ventana ya no se dibuja directamente en el búfer de pantalla.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="fc4ad-114">En su lugar, cada ventana se dibuja en un búfer de memoria fuera de la pantalla, también denominado *superficie fuera* de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="fc4ad-115">A continuación, el DWM compone estas superficies en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-115">The DWM then composites these surfaces to the screen.</span></span>

![diagrama que muestra cómo el DWM compone el escritorio.](images/graphics05.png)

<span data-ttu-id="fc4ad-117">DWM proporciona varias ventajas con respecto a la antigua arquitectura de gráficos.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="fc4ad-118">Menos mensajes Repaint.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-118">Fewer repaint messages.</span></span> <span data-ttu-id="fc4ad-119">Cuando una ventana está obstruida por otra ventana, no es necesario volver a dibujar la ventana obstruida.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="fc4ad-120">Artefactos reducidos.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-120">Reduced artifacts.</span></span> <span data-ttu-id="fc4ad-121">Anteriormente, arrastrar una ventana podía crear artefactos visuales, tal como se describe.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="fc4ad-122">Efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-122">Visual effects.</span></span> <span data-ttu-id="fc4ad-123">Dado que DWM se encarga de componer la pantalla, puede representar áreas translúcidas y borrosas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="fc4ad-124">Escalado automático para altos ppp.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="fc4ad-125">Aunque el escalado no es la manera ideal de administrar valores altos de PPP, se trata de una reserva viable para aplicaciones más antiguas que no se diseñaron para la configuración de PPP alta.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="fc4ad-126">(Volveremos a este tema más adelante, en la sección de [PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md)).</span><span class="sxs-lookup"><span data-stu-id="fc4ad-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="fc4ad-127">Vistas alternativas.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-127">Alternative views.</span></span> <span data-ttu-id="fc4ad-128">El DWM puede usar las superficies de la ocultación de varias formas interesantes.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="fc4ad-129">Por ejemplo, el DWM es la tecnología que subyace a Windows Flip 3D, las miniaturas y las transiciones animadas.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="fc4ad-130">Sin embargo, tenga en cuenta que no se garantiza que el DWM esté habilitado.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="fc4ad-131">Es posible que la tarjeta gráfica no admita los requisitos del sistema DWM y que los usuarios puedan deshabilitar DWM a través del panel de control **propiedades del sistema** .</span><span class="sxs-lookup"><span data-stu-id="fc4ad-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="fc4ad-132">Esto significa que el programa no debe basarse en el comportamiento de repintado de DWM.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="fc4ad-133">Pruebe el programa con DWM deshabilitado para asegurarse de que se vuelve a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="fc4ad-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="fc4ad-134">Siguientes</span><span class="sxs-lookup"><span data-stu-id="fc4ad-134">Next</span></span>

[<span data-ttu-id="fc4ad-135">Modo retenido frente al modo inmediato</span><span class="sxs-lookup"><span data-stu-id="fc4ad-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




