---
title: El Administrador de ventanas de escritorio
description: El Administrador de ventanas de escritorio
ms.assetid: 79250d49-dad5-46c6-892d-b92dac14b417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fca8550134ba0c1cdafe0bd5c349061ef900a9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103903"
---
# <a name="the-desktop-window-manager"></a><span data-ttu-id="e12b9-103">El Administrador de ventanas de escritorio</span><span class="sxs-lookup"><span data-stu-id="e12b9-103">The Desktop Window Manager</span></span>

<span data-ttu-id="e12b9-104">Antes de Windows Vista, un programa de Windows se dibujaba directamente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e12b9-104">Before Windows Vista, a Windows program would draw directly to the screen.</span></span> <span data-ttu-id="e12b9-105">En otras palabras, el programa escribiría directamente en el búfer de memoria que muestra la tarjeta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e12b9-105">In other words, the program would write directly to the memory buffer shown by the video card.</span></span> <span data-ttu-id="e12b9-106">Este enfoque puede provocar artefactos visuales si una ventana no se vuelve a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="e12b9-106">This approach can cause visual artifacts if a window does not repaint itself correctly.</span></span> <span data-ttu-id="e12b9-107">Por ejemplo, si el usuario arrastra una ventana sobre otra ventana y la ventana debajo no se vuelve a dibujar lo suficientemente rápido, la ventana de nivel superior puede dejar un final:</span><span class="sxs-lookup"><span data-stu-id="e12b9-107">For example, if the user drags one window over another window, and the window underneath does not repaint itself quickly enough, the top-most window can leave a trail:</span></span>

![captura de pantalla que muestra cómo volver a dibujar artefactos.](images/graphics04.png)

<span data-ttu-id="e12b9-109">El final se debe a que ambas ventanas pintan en la misma área de memoria.</span><span class="sxs-lookup"><span data-stu-id="e12b9-109">The trail is caused because both windows paint to the same area of memory.</span></span> <span data-ttu-id="e12b9-110">A medida que se arrastra la ventana de nivel superior, se debe volver a dibujar la ventana debajo de ella.</span><span class="sxs-lookup"><span data-stu-id="e12b9-110">As the top-most window is dragged, the window below it must be repainted.</span></span> <span data-ttu-id="e12b9-111">Si el repintado es demasiado lento, provoca los artefactos mostrados en la imagen anterior.</span><span class="sxs-lookup"><span data-stu-id="e12b9-111">If the repainting is too slow, it causes the artifacts shown in the previous image.</span></span>

<span data-ttu-id="e12b9-112">Windows Vista cambió fundamentalmente la forma en que se dibujan las ventanas, al introducir Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="e12b9-112">Windows Vista fundamentally changed how windows are drawn, by introducing the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="e12b9-113">Cuando dwm está habilitado, una ventana ya no se dibuja directamente en el búfer de presentación.</span><span class="sxs-lookup"><span data-stu-id="e12b9-113">When the DWM is enabled, a window no longer draws directly to the display buffer.</span></span> <span data-ttu-id="e12b9-114">En su lugar, cada ventana se dibuja en un búfer de memoria fuera de pantalla, también denominado *superficie fuera de pantalla*.</span><span class="sxs-lookup"><span data-stu-id="e12b9-114">Instead, each window draws to an offscreen memory buffer, also called an *offscreen surface*.</span></span> <span data-ttu-id="e12b9-115">A continuación, el DWM compone estas superficies en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e12b9-115">The DWM then composites these surfaces to the screen.</span></span>

![diagrama que muestra cómo el dwm compone el escritorio.](images/graphics05.png)

<span data-ttu-id="e12b9-117">DWM proporciona varias ventajas con respecto a la arquitectura de gráficos antigua.</span><span class="sxs-lookup"><span data-stu-id="e12b9-117">The DWM provides several advantages over the old graphics architecture.</span></span>

-   <span data-ttu-id="e12b9-118">Menos mensajes de repintado.</span><span class="sxs-lookup"><span data-stu-id="e12b9-118">Fewer repaint messages.</span></span> <span data-ttu-id="e12b9-119">Cuando una ventana está obstruida por otra ventana, no es necesario volver a dibujarla.</span><span class="sxs-lookup"><span data-stu-id="e12b9-119">When a window is obstructed by another window, the obstructed window does not need to repaint itself.</span></span>
-   <span data-ttu-id="e12b9-120">Artefactos reducidos.</span><span class="sxs-lookup"><span data-stu-id="e12b9-120">Reduced artifacts.</span></span> <span data-ttu-id="e12b9-121">Anteriormente, arrastrar una ventana podía crear artefactos visuales, como se describe.</span><span class="sxs-lookup"><span data-stu-id="e12b9-121">Previously, dragging a window could create visual artifacts, as described.</span></span>
-   <span data-ttu-id="e12b9-122">Efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="e12b9-122">Visual effects.</span></span> <span data-ttu-id="e12b9-123">Dado que dwm se encarga de componer la pantalla, puede representar áreas translúcidas y desenfoque de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e12b9-123">Because the DWM is in charge of compositing the screen, it can render translucent and blurred areas of the window.</span></span>
-   <span data-ttu-id="e12b9-124">Escalado automático para valores altos de PPP.</span><span class="sxs-lookup"><span data-stu-id="e12b9-124">Automatic scaling for high DPI.</span></span> <span data-ttu-id="e12b9-125">Aunque el escalado no es la manera ideal de controlar valores altos de PPP, es una reserva viable para las aplicaciones anteriores que no se diseñaron para la configuración de valores altos de PPP.</span><span class="sxs-lookup"><span data-stu-id="e12b9-125">Although scaling is not the ideal way to handle high DPI, it is a viable fallback for older applications that were not designed for high DPI settings.</span></span> <span data-ttu-id="e12b9-126">(Volveremos a este tema más adelante, en la sección [PPP y Device-Independent píxeles).](dpi-and-device-independent-pixels.md)</span><span class="sxs-lookup"><span data-stu-id="e12b9-126">(We will return to this topic later, in the section [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).)</span></span>
-   <span data-ttu-id="e12b9-127">Vistas alternativas.</span><span class="sxs-lookup"><span data-stu-id="e12b9-127">Alternative views.</span></span> <span data-ttu-id="e12b9-128">DwM puede usar las superficies fuera de la pantalla de varias maneras interesantes.</span><span class="sxs-lookup"><span data-stu-id="e12b9-128">The DWM can use the offscreen surfaces in various interesting ways.</span></span> <span data-ttu-id="e12b9-129">Por ejemplo, DWM es la tecnología detrás de Windows Flip 3D, miniaturas y transiciones animadas.</span><span class="sxs-lookup"><span data-stu-id="e12b9-129">For example, the DWM is the technology behind Windows Flip 3D, thumbnails, and animated transitions.</span></span>

<span data-ttu-id="e12b9-130">Sin embargo, tenga en cuenta que no se garantiza que el DWM esté habilitado.</span><span class="sxs-lookup"><span data-stu-id="e12b9-130">Note, however, that the DWM is not guaranteed to be enabled.</span></span> <span data-ttu-id="e12b9-131">Es posible que la tarjeta gráfica no admita los requisitos del sistema DWM y que los usuarios puedan deshabilitarlo mediante el panel de control **Propiedades** del sistema.</span><span class="sxs-lookup"><span data-stu-id="e12b9-131">The graphics card might not support the DWM system requirements, and users can disable the DWM through the **System Properties** control panel.</span></span> <span data-ttu-id="e12b9-132">Esto significa que el programa no debe basarse en el comportamiento de volver a dibujar del DWM.</span><span class="sxs-lookup"><span data-stu-id="e12b9-132">That means your program should not rely on the repainting behavior of the DWM.</span></span> <span data-ttu-id="e12b9-133">Pruebe el programa con DWM deshabilitado para asegurarse de que se vuelve a dibujar correctamente.</span><span class="sxs-lookup"><span data-stu-id="e12b9-133">Test your program with DWM disabled to make sure that it repaints correctly.</span></span>

## <a name="next"></a><span data-ttu-id="e12b9-134">Siguientes</span><span class="sxs-lookup"><span data-stu-id="e12b9-134">Next</span></span>

[<span data-ttu-id="e12b9-135">Modo retenido frente al modo inmediato</span><span class="sxs-lookup"><span data-stu-id="e12b9-135">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)

 

 




