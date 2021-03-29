---
title: Acerca de la configuración de monitor
description: Acerca de la configuración de monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- supervisar, acerca de
- supervisión, calibración de color
- monitor, ajuste del área de visualización del monitor
- supervisar, guardar la configuración del monitor
- supervisar, restaurar la configuración de monitor
- supervisión, características de proveedor
- calibración de color
- ajustar el área de visualización del monitor
- guardar la configuración del monitor
- restaurar la configuración del monitor
- características del proveedor
- configuración del monitor, calibración de color
- supervisión de la configuración, acerca de
- configuración del monitor, ajuste del área de visualización del monitor
- supervisar la configuración, guardar la configuración del monitor
- supervisión de la configuración, restauración de la configuración de monitor
- configuración de supervisión, características de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532067"
---
# <a name="about-monitor-configuration"></a><span data-ttu-id="1e39e-120">Acerca de la configuración de monitor</span><span class="sxs-lookup"><span data-stu-id="1e39e-120">About Monitor Configuration</span></span>

<span data-ttu-id="1e39e-121">Los usos de las funciones de configuración del monitor incluyen:</span><span class="sxs-lookup"><span data-stu-id="1e39e-121">Uses for the monitor configuration functions include:</span></span>

-   <span data-ttu-id="1e39e-122">Calibración de color.</span><span class="sxs-lookup"><span data-stu-id="1e39e-122">Color calibration.</span></span> <span data-ttu-id="1e39e-123">Un monitor calibrado correctamente reproduce los colores correctamente.</span><span class="sxs-lookup"><span data-stu-id="1e39e-123">A properly calibrated monitor reproduces colors correctly.</span></span> <span data-ttu-id="1e39e-124">Normalmente, una aplicación de calibración de color muestra un patrón de prueba y tiene controles para cambiar la configuración de un monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-124">Typically, a color calibration application displays a test pattern and has controls to change a monitor setting.</span></span> <span data-ttu-id="1e39e-125">El usuario cambia la configuración hasta que se cumple una condición y repite este proceso para cada configuración del monitor hasta que se calibra el monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-125">The user changes the setting until a condition is met, and repeats this process for each monitor setting until the monitor is calibrated.</span></span>
-   <span data-ttu-id="1e39e-126">Ajuste del área de visualización del monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-126">Adjusting the monitor's display area.</span></span> <span data-ttu-id="1e39e-127">Las funciones de configuración del monitor se pueden usar para cambiar el tamaño y la posición del área de presentación de un monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-127">The monitor configuration functions can be used to change the size and position of a monitor's display area.</span></span> <span data-ttu-id="1e39e-128">Por ejemplo, cuando un monitor LCD está conectado a un equipo mediante un conector analógico, se obtiene la mejor calidad de imagen cuando hay una asignación de uno a uno entre píxeles en el búfer de fotogramas de la tarjeta gráfica y píxeles en el monitor LCD.</span><span class="sxs-lookup"><span data-stu-id="1e39e-128">For example, when an LCD monitor is connected to a computer by using an analog connector, the best image quality is obtained when there is a one-to-one mapping between pixels in the graphics card's frame buffer and pixels on the LCD monitor.</span></span>
-   <span data-ttu-id="1e39e-129">Guardar y restaurar la configuración del monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-129">Saving and restoring monitor settings.</span></span> <span data-ttu-id="1e39e-130">Algunos usuarios necesitan varios conjuntos de valores de supervisión, ya que los distintos escenarios requieren una configuración de monitor diferente.</span><span class="sxs-lookup"><span data-stu-id="1e39e-130">Some users need multiple sets of monitor settings, because different scenarios require different monitor settings.</span></span> <span data-ttu-id="1e39e-131">Por ejemplo, la configuración de supervisión que es óptima para las aplicaciones de escritorio no es óptima para ver la televisión.</span><span class="sxs-lookup"><span data-stu-id="1e39e-131">For example, monitor settings that are optimal for desktop applications are not optimal for watching television.</span></span>
-   <span data-ttu-id="1e39e-132">Usar las características de supervisión específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-132">Using vendor-specific monitor features.</span></span> <span data-ttu-id="1e39e-133">Con las funciones de configuración del monitor, los fabricantes pueden crear aplicaciones que usen las características específicas del proveedor del monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-133">Using the monitor configuration functions, manufacturers can create applications that use the vendor-specific features of the monitor.</span></span>

<span data-ttu-id="1e39e-134">Las funciones de configuración del monitor se dividen en funciones de alto nivel y bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e39e-134">The monitor configuration functions are divided into high-level and low-level functions.</span></span> <span data-ttu-id="1e39e-135">Las funciones de alto nivel son más fáciles de usar que las funciones de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e39e-135">The high-level functions are easier to use than the low-level functions.</span></span> <span data-ttu-id="1e39e-136">Para usar las funciones de alto nivel, no es necesario saber nada sobre la interfaz de comandos del canal de datos de pantalla (DDC/CI).</span><span class="sxs-lookup"><span data-stu-id="1e39e-136">To use the high-level functions, you do not need to know anything about the Display Data Channel Command Interface (DDC/CI).</span></span> <span data-ttu-id="1e39e-137">Sin embargo, las funciones de alto nivel no proporcionan acceso a las características específicas del proveedor del monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-137">However, the high-level functions do not give you access to vendor-specific features of the monitor.</span></span>

<span data-ttu-id="1e39e-138">Las funciones de bajo nivel son un contenedor fino en torno a los comandos DDC/CI.</span><span class="sxs-lookup"><span data-stu-id="1e39e-138">The low-level functions are a thin wrapper around the DDC/CI commands.</span></span> <span data-ttu-id="1e39e-139">Para usar las funciones de bajo nivel, debe estar familiarizado con el estándar DDC/CI y también con el estándar del conjunto de comandos de control de monitor de VESA (MCCS).</span><span class="sxs-lookup"><span data-stu-id="1e39e-139">To use the low-level functions, you must be familiar with the DDC/CI standard and also with the VESA Monitor Control Command Set (MCCS) standard.</span></span> <span data-ttu-id="1e39e-140">Por lo general, debe usar las funciones de alto nivel a menos que necesite usar características que solo están disponibles en las funciones de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="1e39e-140">Generally, you should use the high-level functions unless you need to use features that are available only in the low-level functions.</span></span>

<span data-ttu-id="1e39e-141">Las funciones de configuración del monitor de alto nivel están diseñadas para que una aplicación no pueda poner un monitor en un estado inutilizable.</span><span class="sxs-lookup"><span data-stu-id="1e39e-141">The high-level monitor configuration functions are designed so that an application cannot put a monitor into an unusable state.</span></span> <span data-ttu-id="1e39e-142">Las funciones de bajo nivel se pueden usar para enviar códigos VCP al monitor.</span><span class="sxs-lookup"><span data-stu-id="1e39e-142">The low-level functions can be used to send VCP codes to the monitor.</span></span> <span data-ttu-id="1e39e-143">Sin embargo, tenga en cuenta que algunos códigos VCP pueden deshabilitar la funcionalidad importante o poner el monitor en un estado en el que el usuario no pueda ver la imagen de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1e39e-143">However, be aware that some VCP codes can disable important functionality or put the monitor into a state where the user cannot see the display image.</span></span> <span data-ttu-id="1e39e-144">Para obtener más información, consulte el estándar del conjunto de comandos de control de monitor de VESA (MCCS).</span><span class="sxs-lookup"><span data-stu-id="1e39e-144">For more information, see the VESA Monitor Control Command Set (MCCS) standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e39e-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e39e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e39e-146">Configuración de monitor</span><span class="sxs-lookup"><span data-stu-id="1e39e-146">Monitor Configuration</span></span>](monitor-configuration.md)
</dt> </dl>

 

 




