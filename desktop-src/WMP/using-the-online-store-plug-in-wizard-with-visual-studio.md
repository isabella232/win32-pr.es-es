---
title: Usar el Asistente para complementos de la tienda en línea con Visual Studio
description: Usar el Asistente para complementos de la tienda en línea con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, Asistente para complementos
- tiendas en línea, Asistente para complementos
- tipo 1 tiendas en línea, Asistente para complementos
- Windows Media Player tiendas en línea, Visual Studio
- tiendas en línea, Visual Studio
- tipo 1 tiendas en línea, Visual Studio
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, Visual Studio
- complementos, Asistente para complementos
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Windows Media Player, Visual Studio
- Complementos de Windows Media Player, Asistente para complementos
- Asistente para tiendas en línea de Visual Studio, Windows Media Player
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704575"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="a58c4-124">Usar el Asistente para complementos de la tienda en línea con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a58c4-124">Using the Online Store Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="a58c4-125">Una vez instalados los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="a58c4-125">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="a58c4-126">Los pasos siguientes le guiarán:</span><span class="sxs-lookup"><span data-stu-id="a58c4-126">The following steps will guide you:</span></span>

1.  <span data-ttu-id="a58c4-127">Inicie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a58c4-127">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="a58c4-128">En el menú **archivo** , seleccione **nuevo** y haga clic en **proyecto**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-128">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="a58c4-129">En **tipos de proyecto**, haga clic en **proyectos de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-129">In **Project Types**, click **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="a58c4-130">En **plantillas**, haga clic en el **asistente de Windows Media Player tiendas en línea**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-130">In **Templates**, click **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="a58c4-131">Escriba un nombre para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a58c4-131">Enter a name for your project.</span></span>
6.  <span data-ttu-id="a58c4-132">Escriba una ubicación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a58c4-132">Enter a location for your project.</span></span> <span data-ttu-id="a58c4-133">Esta es la carpeta en la que se copiarán los archivos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a58c4-133">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="a58c4-134">Haga clic en **Aceptar** para iniciar el asistente.</span><span class="sxs-lookup"><span data-stu-id="a58c4-134">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="a58c4-135">Seleccione **tipo 1 (integración profunda)** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-135">Select **Type 1 (Deep integration)**, and click **Next**.</span></span>
9.  <span data-ttu-id="a58c4-136">Escriba un nombre descriptivo y un distribuidor de contenido.</span><span class="sxs-lookup"><span data-stu-id="a58c4-136">Enter a friendly name and a content distributor.</span></span> <span data-ttu-id="a58c4-137">Haga clic en **Finalizar**</span><span class="sxs-lookup"><span data-stu-id="a58c4-137">Click **Finish**.</span></span>
10. <span data-ttu-id="a58c4-138">Use el entorno de desarrollo de Visual Studio para compilar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="a58c4-138">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="a58c4-139">En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="a58c4-139">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="a58c4-140">Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-140">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="a58c4-141">Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a58c4-141">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="a58c4-142">El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="a58c4-142">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="a58c4-143">Si ejecutó la utilidad de registro de Visual Studio que se incluye con el Windows SDK, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y lib de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a58c4-143">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="a58c4-144">De lo contrario, debe configurar manualmente el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a58c4-144">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="a58c4-145">Para configurar manualmente Visual Studio, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="a58c4-145">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="a58c4-146">En el menú **herramientas** , haga clic en opciones.</span><span class="sxs-lookup"><span data-stu-id="a58c4-146">On the **Tools** menu, click Options.</span></span>
2.  <span data-ttu-id="a58c4-147">Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-147">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="a58c4-148">En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="a58c4-148">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="a58c4-149">Agregue los directorios de los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a58c4-149">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a58c4-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a58c4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a58c4-151">Compilar el complemento para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="a58c4-151">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




