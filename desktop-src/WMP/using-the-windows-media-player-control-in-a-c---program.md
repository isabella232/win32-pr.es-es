---
title: Usar el control Media Player de Windows en un programa de C++
description: Usar el control Media Player de Windows en un programa de C++
ms.assetid: 2531ac25-5e9d-462e-a06a-6f81bf4ca33d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Windows Media Player, C++
- Modelo de objetos de Windows Media Player, C++
- modelo de objetos, C++
- Windows Media Player Mobile, C++
- Control ActiveX de Windows Media Player, C++
- Control ActiveX móvil de Windows Media Player, C++
- Control ActiveX, C++
- Incrustación de programas de C++
- incrustación, programas de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02430dbdaba3bb2e8ea3ca6e46b202a289a096f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269074"
---
# <a name="using-the-windows-media-player-control-in-a-c-program"></a><span data-ttu-id="7c543-119">Usar el control Media Player de Windows en un programa de C++</span><span class="sxs-lookup"><span data-stu-id="7c543-119">Using the Windows Media Player Control in a C++ Program</span></span>

> [!Note]  
> <span data-ttu-id="7c543-120">El uso de C++ para insertar el control Media Player de Windows es compatible con Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="7c543-120">Using C++ to embed the Windows Media Player control is supported for Windows Media Player 9 Series or later.</span></span>

 

<span data-ttu-id="7c543-121">Hay varias maneras de usar el control de Media Player de Windows en un programa de C++.</span><span class="sxs-lookup"><span data-stu-id="7c543-121">There are several different ways to use the Windows Media Player control in a C++ program.</span></span> <span data-ttu-id="7c543-122">Puede crear una instancia del control en una aplicación de consola o puede incrustar el control en una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c543-122">You can create an instance of the control in a console application, or you can embed the control in a Windows application.</span></span> <span data-ttu-id="7c543-123">Además, puede implementar interfaces que le permitan ejecutar un control Embedded Player en modo remoto.</span><span class="sxs-lookup"><span data-stu-id="7c543-123">Also, you can implement interfaces that enable you to run an embedded Player control in remote mode.</span></span> <span data-ttu-id="7c543-124">Puede personalizar la interfaz de usuario de un control incrustado aplicando un archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="7c543-124">You can customize the user interface of an embedded control by applying a skin definition file.</span></span>

<span data-ttu-id="7c543-125">Esta información se describe en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c543-125">This information is described in the following topics.</span></span>



| <span data-ttu-id="7c543-126">Tema</span><span class="sxs-lookup"><span data-stu-id="7c543-126">Topic</span></span>                                                                                                                                      | <span data-ttu-id="7c543-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c543-127">Description</span></span>                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c543-128">Usar el control de Media Player de Windows en una aplicación de consola</span><span class="sxs-lookup"><span data-stu-id="7c543-128">Using the Windows Media Player Control in a Console Application</span></span>](using-the-windows-media-player-control-in-a-console-application.md)     | <span data-ttu-id="7c543-129">Describe una sencilla aplicación de consola de C++ que crea instancias del control Media Player de Windows para mostrar la versión.</span><span class="sxs-lookup"><span data-stu-id="7c543-129">Describes a simple C++ console application that instantiates the Windows Media Player control to display the version.</span></span>                                                       |
| [<span data-ttu-id="7c543-130">Hospedar el control de Media Player de Windows en una aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="7c543-130">Hosting the Windows Media Player Control in a Windows Application</span></span>](hosting-the-windows-media-player-control-in-a-windows-application.md) | <span data-ttu-id="7c543-131">Describe cómo utilizar la ventana host ActiveX ATL para incrustar el control Media Player de Windows en un programa de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c543-131">Describes how to use the ATL ActiveX host window to embed the Windows Media Player control in a Windows program.</span></span>                                                            |
| [<span data-ttu-id="7c543-132">Control remoto del Reproductor de Windows Media</span><span class="sxs-lookup"><span data-stu-id="7c543-132">Remoting the Windows Media Player Control</span></span>](remoting-the-windows-media-player-control.md)                                                 | <span data-ttu-id="7c543-133">Describe cómo incrustar el control Media Player de Windows en un programa de C++ en modo remoto, lo que permite a los usuarios desacoplar el control para cambiar al modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="7c543-133">Describes how to embed the Windows Media Player control in a C++ program in remote mode, which lets your users undock the control to switch to the full mode of the Player.</span></span> |
| [<span data-ttu-id="7c543-134">Controlar eventos en C++</span><span class="sxs-lookup"><span data-stu-id="7c543-134">Handling Events in C++</span></span>](handling-events-in-c.md)                                                                                         | <span data-ttu-id="7c543-135">Describe cómo recibir notificaciones de eventos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7c543-135">Describes how to receive event notifications from Windows Media Player.</span></span>                                                                                                     |
| [<span data-ttu-id="7c543-136">Usar máscaras con el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="7c543-136">Using Skins with the Windows Media Player Control</span></span>](using-skins-with-the-windows-media-player-control.md)                                 | <span data-ttu-id="7c543-137">Describe cómo aplicar un archivo de máscara a un control de Media Player de Windows incrustado en un programa de C++.</span><span class="sxs-lookup"><span data-stu-id="7c543-137">Describes how to apply a skin file to a Windows Media Player control embedded in a C++ program.</span></span>                                                                             |



 

> [!Note]  
> <span data-ttu-id="7c543-138">Puede incrustar el control de Windows Media Player 10 Mobile en una aplicación Windows CE.</span><span class="sxs-lookup"><span data-stu-id="7c543-138">You can embed the Windows Media Player 10 Mobile control in a Windows CE application.</span></span> <span data-ttu-id="7c543-139">Las técnicas que se usan para ello son similares a las que se usan con el control de Media Player de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c543-139">The techniques you use to do this are similar to those used with the desktop Windows Media Player control.</span></span> <span data-ttu-id="7c543-140">Sin embargo, hay diferencias entre ATL para Windows y ATL para Windows CE.</span><span class="sxs-lookup"><span data-stu-id="7c543-140">However, there are differences between ATL for Windows and ATL for Windows CE.</span></span> <span data-ttu-id="7c543-141">En esta documentación se describen las diferencias entre estas implementaciones, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="7c543-141">This documentation describes the differences between these implementations, where appropriate.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7c543-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c543-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c543-143">**Referencia del modelo de objetos para C++**</span><span class="sxs-lookup"><span data-stu-id="7c543-143">**Object Model Reference for C++**</span></span>](object-model-reference-for-c.md)
</dt> <dt>

[<span data-ttu-id="7c543-144">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="7c543-144">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




