---
title: Información general para desarrolladores
description: Información general para desarrolladores
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Complementos de Windows Media Player, visualizaciones
- complementos, visualizaciones
- visualizaciones, información general para desarrolladores
- visualizaciones personalizadas, información general para desarrolladores
- visualizaciones, controles COM
- visualizaciones personalizadas, controles COM
- visualizaciones, entrada de audio
- visualizaciones personalizadas, entrada de audio
- visualizaciones, salida gráfica
- visualizaciones personalizadas, salida gráfica
- visualizaciones, herramientas de dibujo
- visualizaciones personalizadas, herramientas de dibujo
- visualizaciones, lenguaje de programación
- visualizaciones personalizadas, lenguaje de programación
- visualizaciones, Visual C++
- visualizaciones personalizadas, Visual C++
- visualizaciones, Asistente para complementos
- visualizaciones personalizadas, Asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357382"
---
# <a name="developer-overview"></a><span data-ttu-id="d53e6-122">Información general para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="d53e6-122">Developer Overview</span></span>

<span data-ttu-id="d53e6-123">Desde el punto de vista del desarrollador, las visualizaciones son programas de software que toman datos de audio proporcionados por Windows Media Player y convierten los datos en gráficos que van a la vista del usuario.</span><span class="sxs-lookup"><span data-stu-id="d53e6-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="d53e6-124">Los principales temas que un desarrollador debe comprender para crear una nueva visualización son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d53e6-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="d53e6-125">Empaquetado de visualización</span><span class="sxs-lookup"><span data-stu-id="d53e6-125">Visualization Packaging</span></span>

<span data-ttu-id="d53e6-126">Las visualizaciones son controles COM que Windows Media Player usa para convertir las ondas de onda de audio en gráficos animados en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d53e6-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="d53e6-127">Los controles COM se empaquetan como bibliotecas de vínculos dinámicos (dll) de Microsoft Windows y deben estar registrados en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="d53e6-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="d53e6-128">Cuando se ejecuta Windows Media Player, las visualizaciones personalizadas registradas se cargan y se ven de acuerdo con las instrucciones de la máscara que usa Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d53e6-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="d53e6-129">Entrada de audio</span><span class="sxs-lookup"><span data-stu-id="d53e6-129">Audio Input</span></span>

<span data-ttu-id="d53e6-130">Windows Media Player proporciona el código con instantáneas de los datos de frecuencia de audio y de forma de onda a intervalos de tiempo medidos en fracciones de segundo.</span><span class="sxs-lookup"><span data-stu-id="d53e6-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="d53e6-131">El intervalo de instantánea está determinado internamente por el Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d53e6-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="d53e6-132">Salida gráfica</span><span class="sxs-lookup"><span data-stu-id="d53e6-132">Graphical Output</span></span>

<span data-ttu-id="d53e6-133">La salida gráfica de la visualización es un contexto de dispositivo de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d53e6-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="d53e6-134">Se trata de una superficie de dibujo estándar de Windows que se puede dibujar cada vez que se proporciona una instantánea de audio.</span><span class="sxs-lookup"><span data-stu-id="d53e6-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="d53e6-135">Toda la tecnología de Windows en segundo plano se encarga de usted.</span><span class="sxs-lookup"><span data-stu-id="d53e6-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="d53e6-136">Solo tiene que dibujar en el contexto del dispositivo con los datos de audio proporcionados.</span><span class="sxs-lookup"><span data-stu-id="d53e6-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="d53e6-137">Herramientas de dibujo</span><span class="sxs-lookup"><span data-stu-id="d53e6-137">Drawing Tools</span></span>

<span data-ttu-id="d53e6-138">Puede dibujar en el contexto del dispositivo con las funciones estándar de Microsoft Windows Interfaz de dispositivo gráfico (GDI), usando lápices y pinceles para crear diseños modificados por los datos de audio que proporciona Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d53e6-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="d53e6-139">GDI proporciona un amplio conjunto de herramientas de dibujo que pueden crear muchos tipos de efectos visuales.</span><span class="sxs-lookup"><span data-stu-id="d53e6-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="d53e6-140">Lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="d53e6-140">Programming Language</span></span>

<span data-ttu-id="d53e6-141">Microsoft Visual C++ 6,0 y versiones posteriores es el único idioma admitido para crear visualizaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d53e6-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="d53e6-142">Asistente para complementos</span><span class="sxs-lookup"><span data-stu-id="d53e6-142">Plug-in Wizard</span></span>

<span data-ttu-id="d53e6-143">Windows Media Player proporciona un asistente COM que se puede Agregar a Visual C++ que generará el código subyacente necesario para la visualización.</span><span class="sxs-lookup"><span data-stu-id="d53e6-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="d53e6-144">No solo se proporcionan todos los archivos de código fuente, pero se genera una máscara de ejemplo para facilitar la prueba de la visualización.</span><span class="sxs-lookup"><span data-stu-id="d53e6-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="d53e6-145">El código generado crea una visualización similar a las barras, con dos valores preestablecidos.</span><span class="sxs-lookup"><span data-stu-id="d53e6-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="d53e6-146">Después, puede modificar el código para crear su propia visualización.</span><span class="sxs-lookup"><span data-stu-id="d53e6-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="d53e6-147">También se genera un archivo de registro para registrar la visualización de forma que Windows Media Player pueda cargarla.</span><span class="sxs-lookup"><span data-stu-id="d53e6-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="d53e6-148">En el siguiente tema se describe cómo el código de visualización procesa los datos de audio:</span><span class="sxs-lookup"><span data-stu-id="d53e6-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="d53e6-149">Flujo de control</span><span class="sxs-lookup"><span data-stu-id="d53e6-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="d53e6-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d53e6-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d53e6-151">**Acerca de las visualizaciones personalizadas**</span><span class="sxs-lookup"><span data-stu-id="d53e6-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




