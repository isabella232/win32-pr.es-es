---
title: Flujo de control
description: Flujo de control
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualizaciones, flujo de programa
- visualizaciones personalizadas, flujo de programa
- visualizaciones, flujo de control
- visualizaciones personalizadas, flujo de control
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- visualizaciones, función RenderWindow
- visualizaciones personalizadas, función RenderWindow
- Función render, flujo de programa de visualización
- RenderWindow función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993988"
---
# <a name="flow-of-control"></a><span data-ttu-id="80820-115">Flujo de control</span><span class="sxs-lookup"><span data-stu-id="80820-115">Flow of Control</span></span>

<span data-ttu-id="80820-116">Los datos de audio entran en Windows Media Player continuamente a través de un archivo o una secuencia.</span><span class="sxs-lookup"><span data-stu-id="80820-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="80820-117">Esos datos se pasan a la visualización.</span><span class="sxs-lookup"><span data-stu-id="80820-117">That data is passed to your visualization.</span></span> <span data-ttu-id="80820-118">Dibuja en una superficie definida y pasa esa superficie de nuevo a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="80820-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="80820-119">Este intercambio se produce varias veces al segundo y, al usuario, el resultado es una animación agradable que se mueve en el tiempo a la música.</span><span class="sxs-lookup"><span data-stu-id="80820-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="80820-120">Esta es la secuencia específica del flujo del programa de visualización:</span><span class="sxs-lookup"><span data-stu-id="80820-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="80820-121">En un intervalo de tiempo, Windows Media Player toma una instantánea del audio que se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="80820-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="80820-122">Windows Media Player proporciona los datos de esa instantánea a la visualización a través de la función **Render** y la función **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="80820-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="80820-123">Debe escribir código que se ejecutará cuando se llame a **Render** y **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="80820-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="80820-124">El código dibuja mediante el uso de un contexto de dispositivo definido por Windows Media Player cuando se representa sin ventana, o bien mediante una ventana que se crea cuando se representa en la ventana.</span><span class="sxs-lookup"><span data-stu-id="80820-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="80820-125">En una región especificada por la máscara actual, Windows Media Player muestra lo que dibujó el código.</span><span class="sxs-lookup"><span data-stu-id="80820-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="80820-126">Este proceso se repite varias veces por segundo, lo que crea animaciones gráficas que se transtimen a la música.</span><span class="sxs-lookup"><span data-stu-id="80820-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="80820-127">Cuando la música deja de reproducirse, la visualización se detiene.</span><span class="sxs-lookup"><span data-stu-id="80820-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80820-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80820-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80820-129">**Información general para desarrolladores**</span><span class="sxs-lookup"><span data-stu-id="80820-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




