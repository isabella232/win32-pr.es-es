---
title: Incrustar el control Media Player de Windows en un programa personalizado
description: Incrustar el control Media Player de Windows en un programa personalizado
ms.assetid: 2a5f0cd7-e3fa-4d4f-9203-bcb13362c9ab
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Windows Media Player Mobile, incrustar el control ActiveX
- incrustación, programas personalizados
- incrustación de programas personalizados
- incrustación, programas basados en Visual Basic
- Incrustación de programas basados en Visual Basic
- incrustar, usar manualmente métodos COM
- incrustación manual mediante métodos COM
- incrustación, programas de C++
- Incrustación de programas de C++
- incrustación, programas de Visual Studio
- Visual Studio, inserción de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 441678e4b8db51040e18d9d31d2af78db134f74b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075498"
---
# <a name="embedding-the-windows-media-player-control-in-a-custom-program"></a><span data-ttu-id="365f2-120">Incrustar el control Media Player de Windows en un programa personalizado</span><span class="sxs-lookup"><span data-stu-id="365f2-120">Embedding the Windows Media Player Control in a Custom Program</span></span>

<span data-ttu-id="365f2-121">Dado que el control ActiveX de Windows Media Player se basa en la tecnología del modelo de objetos componentes (COM) de Microsoft, puede incrustarlo en programas escritos con muchos lenguajes de programación diferentes.</span><span class="sxs-lookup"><span data-stu-id="365f2-121">Because the Windows Media Player ActiveX control is based on Microsoft Component Object Model (COM) technology, you can embed it in programs written with many different programming languages.</span></span> <span data-ttu-id="365f2-122">El control Media Player de Windows representa una manera fácil de agregar sofisticada funcionalidad multimedia digital a cualquier programa.</span><span class="sxs-lookup"><span data-stu-id="365f2-122">The Windows Media Player control represents an easy way to add sophisticated digital media functionality to any program.</span></span>

<span data-ttu-id="365f2-123">En Microsoft Visual Basic, puede Agregar el control al cuadro de herramientas de control, colocarlo en un formulario y ajustar las propiedades del control en la ventana Propiedades.</span><span class="sxs-lookup"><span data-stu-id="365f2-123">In Microsoft Visual Basic, you can add the control to the control toolbox, place it on a form, and adjust the control properties in the properties window.</span></span> <span data-ttu-id="365f2-124">Si desea una interfaz de usuario personalizada, puede colocar botones de comando en el formulario y agregar el código que administra el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="365f2-124">If you want a custom user interface, you can place command buttons on the form and add code that manages the Windows Media Player control.</span></span> <span data-ttu-id="365f2-125">Incrustar el control en un programa basado en Visual Basic es muy similar a insertarlo en un documento de Office y programarlo con VBA.</span><span class="sxs-lookup"><span data-stu-id="365f2-125">Embedding the control in a Visual Basic-based program is very similar to embedding it in an Office document and programming it with VBA.</span></span>

<span data-ttu-id="365f2-126">Como alternativa, puede incrustar el control manualmente mediante métodos COM para crear instancias del control y tener acceso a las interfaces COM documentadas en [Referencia del modelo de objetos para C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="365f2-126">Alternately, you can embed the control manually using COM methods to instantiate the control and access the COM interfaces documented in [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

<span data-ttu-id="365f2-127">Al incrustar el control Media Player de Windows en un programa de C++, tiene la opción de implementar interfaces COM que permiten que el control se ejecute en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="365f2-127">When you embed the Windows Media Player control in a C++ program, you have the option of implementing COM interfaces that allow the control to run in remote mode.</span></span> <span data-ttu-id="365f2-128">Esto significa que el control incrustado comparte el mismo motor de reproducción que el modo completo del reproductor y los usuarios pueden alternar entre el modo completo y el estado acoplado sin interrumpir la reproducción de medios digitales.</span><span class="sxs-lookup"><span data-stu-id="365f2-128">This means that the embedded control shares the same playback engine as the full mode of the Player, and users can switch back and forth between the full mode and the docked state without interrupting digital media playback.</span></span> <span data-ttu-id="365f2-129">También puede controlar lo que se muestra en los distintos paneles del reproductor en modo completo cuando los usuarios cambian al estado desacoplado.</span><span class="sxs-lookup"><span data-stu-id="365f2-129">You can also control what is displayed in the various panes of the full mode Player when your users switch to the undocked state.</span></span>

<span data-ttu-id="365f2-130">Con la incrustación de C++, también tiene la opción de aplicar un archivo de definición de máscara al control Embedded Player.</span><span class="sxs-lookup"><span data-stu-id="365f2-130">With C++ embedding, you also have the option of applying a skin definition file to the embedded Player control.</span></span> <span data-ttu-id="365f2-131">Se trata de una forma sencilla de crear un código de interfaz de usuario ligero que se puede mantener por separado del código de programa principal.</span><span class="sxs-lookup"><span data-stu-id="365f2-131">This is an easy way to create lightweight user interface code that you can maintain separately from your main program code.</span></span>

<span data-ttu-id="365f2-132">Microsoft Visual Studio admite la incrustación de controles ActiveX, incluido el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="365f2-132">Microsoft Visual Studio supports embedding ActiveX controls, including the Windows Media Player control.</span></span> <span data-ttu-id="365f2-133">Cuando elige hacer esto, Visual Studio crea un nuevo ensamblado de interoperabilidad alternativo (Interop) para administrar la interoperabilidad entre el .NET Framework y el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="365f2-133">When you choose to do this, Visual Studio creates a new alternate interoperability (interop) assembly to manage interoperability between the .NET Framework and the Windows Media Player control.</span></span> <span data-ttu-id="365f2-134">Visual Studio usa la herramienta de tlbimp.exe de .NET Framework para crear el ensamblado de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="365f2-134">Visual Studio uses the .NET Framework tlbimp.exe tool to create the interop assembly.</span></span> <span data-ttu-id="365f2-135">Esto significa que las firmas que se muestran al usar la característica IntelliSense en Visual Studio usan la semántica determinada por la versión actual de Tlbimp.</span><span class="sxs-lookup"><span data-stu-id="365f2-135">This means that the signatures displayed when using the IntelliSense feature in Visual Studio use semantics determined by the current version of tlbimp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="365f2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="365f2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365f2-137">**Incrustar el control Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="365f2-137">**Embedding the Windows Media Player Control**</span></span>](embedding-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="365f2-138">**Usar el control Media Player de Windows en un programa de C++**</span><span class="sxs-lookup"><span data-stu-id="365f2-138">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> <dt>

[<span data-ttu-id="365f2-139">**Usar el control de Media Player de Windows en una solución de .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="365f2-139">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="365f2-140">**Usar el control Media Player de Windows con Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="365f2-140">**Using the Windows Media Player Control with Visual Basic**</span></span>](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




