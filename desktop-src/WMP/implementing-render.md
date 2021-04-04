---
title: Implementación de render
description: Implementación de render
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- visualizaciones, función RenderWindow
- visualizaciones personalizadas, función RenderWindow
- Función render, parámetros
- RenderWindow función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077321"
---
# <a name="implementing-render"></a><span data-ttu-id="f4691-111">Implementación de render</span><span class="sxs-lookup"><span data-stu-id="f4691-111">Implementing Render</span></span>

<span data-ttu-id="f4691-112">La forma más sencilla de pensar en la programación de la visualización es que está creando un controlador para un evento con hora.</span><span class="sxs-lookup"><span data-stu-id="f4691-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="f4691-113">A intervalos específicos, Windows Media Player toma una instantánea de los datos de audio que se reproducen y proporciona los datos de la instantánea a la visualización cargada actualmente.</span><span class="sxs-lookup"><span data-stu-id="f4691-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="f4691-114">Esto es similar a la programación controlada por eventos y forma parte del modelo de programación de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f4691-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="f4691-115">Escribirá código y esperará a que lo llame un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="f4691-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="f4691-116">Si el código es una implementación de la función [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para la representación en modo sin ventanas, recibe los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f4691-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="f4691-117">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="f4691-117">*TimedLevel*</span></span>

<span data-ttu-id="f4691-118">Se trata de una estructura que define los datos de audio que el código va a analizar.</span><span class="sxs-lookup"><span data-stu-id="f4691-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="f4691-119">La estructura se compone de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="f4691-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="f4691-120">La primera matriz se basa en la información de frecuencia y contiene una instantánea del espectro de audio dividida en porciones de 1024.</span><span class="sxs-lookup"><span data-stu-id="f4691-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="f4691-121">Cada celda de la matriz contiene un valor comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="f4691-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="f4691-122">La primera celda comienza en 20 Hz y en el último 22050 Hz.</span><span class="sxs-lookup"><span data-stu-id="f4691-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="f4691-123">La matriz es bidimensional para representar audio estéreo.</span><span class="sxs-lookup"><span data-stu-id="f4691-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="f4691-124">La segunda matriz se basa en la información de la forma de onda y se corresponde con la potencia de audio, donde la onda más fuerte es, cuanto mayor sea el valor.</span><span class="sxs-lookup"><span data-stu-id="f4691-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="f4691-125">La matriz de la forma de onda es una instantánea granular de los últimos 1024 segmentos de energía de audio tomados en intervalos de tiempo muy pequeños.</span><span class="sxs-lookup"><span data-stu-id="f4691-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="f4691-126">Esta matriz también es bidimensional para representar audio estéreo.</span><span class="sxs-lookup"><span data-stu-id="f4691-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="f4691-127">*CÁMARAS*</span><span class="sxs-lookup"><span data-stu-id="f4691-127">*HDC*</span></span>

<span data-ttu-id="f4691-128">Se trata de un identificador de Microsoft Windows para un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4691-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="f4691-129">Esto proporciona una manera de identificar la superficie de dibujo en Windows.</span><span class="sxs-lookup"><span data-stu-id="f4691-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="f4691-130">No es necesario crearlo, solo tiene que usarlo para llamadas específicas de funciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f4691-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="f4691-131">*RECT*</span><span class="sxs-lookup"><span data-stu-id="f4691-131">*RECT*</span></span>

<span data-ttu-id="f4691-132">Se trata de un rectángulo de Microsoft Windows que define el tamaño de una superficie de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f4691-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="f4691-133">Se trata de un rectángulo sencillo con cuatro propiedades: **izquierda**, **derecha**, **superior** e **inferior**.</span><span class="sxs-lookup"><span data-stu-id="f4691-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="f4691-134">Los valores reales son proporcionados por Windows Media Player para que pueda determinar cómo el usuario o el desarrollador de máscaras ha ajustado el tamaño de la ventana en la que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="f4691-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="f4691-135">También determina la posición en la HDC en la que se supone que se debe representar el efecto.</span><span class="sxs-lookup"><span data-stu-id="f4691-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="f4691-136">Si el código es una implementación de la función **IWMPEffects2:: RenderWindowed** para la representación en una ventana, recibe los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="f4691-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="f4691-137">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="f4691-137">*TimedLevel*</span></span>

<span data-ttu-id="f4691-138">Esta es la misma información que recibe la función de **representación** .</span><span class="sxs-lookup"><span data-stu-id="f4691-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="f4691-139">*fRequiredRender*</span><span class="sxs-lookup"><span data-stu-id="f4691-139">*fRequiredRender*</span></span>

<span data-ttu-id="f4691-140">El parámetro *fRequiredRender* le informa de que la visualización debe volver a dibujarse, por ejemplo, cuando se arrastra otra ventana sobre ella.</span><span class="sxs-lookup"><span data-stu-id="f4691-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="f4691-141">Cuando este valor es false, puede omitir el código de representación de forma segura si el elemento multimedia actual está detenido o en pausa.</span><span class="sxs-lookup"><span data-stu-id="f4691-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="f4691-142">Esto le permite evitar consumir ciclos de CPU innecesariamente.</span><span class="sxs-lookup"><span data-stu-id="f4691-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="f4691-143">El complemento de ejemplo generado por el Asistente para complementos no proporciona una implementación personalizada para **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="f4691-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="f4691-144">En su lugar, el código de complemento de ejemplo recupera el contexto de dispositivo de la ventana primaria proporcionada por Windows Media Player en [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), recupera las dimensiones de la ventana primaria como una estructura Rect y, a continuación, llama a a través de para **representar** mediante el contexto de dispositivo, el Rect y el puntero de nivel de tiempo de **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="f4691-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="f4691-145">En las secciones siguientes se proporciona más información acerca de la implementación de **Render**:</span><span class="sxs-lookup"><span data-stu-id="f4691-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="f4691-146">Usar niveles de tiempo</span><span class="sxs-lookup"><span data-stu-id="f4691-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="f4691-147">Usar contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4691-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="f4691-148">Usar rectángulos</span><span class="sxs-lookup"><span data-stu-id="f4691-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="f4691-149">Código de representación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4691-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="f4691-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4691-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4691-151">**Implementar el código**</span><span class="sxs-lookup"><span data-stu-id="f4691-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




