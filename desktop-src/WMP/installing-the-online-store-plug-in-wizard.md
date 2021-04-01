---
title: Instalación del Asistente para complementos de tienda en línea
description: Instalación del Asistente para complementos de tienda en línea
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player tiendas en línea, Complementos
- tiendas en línea, Complementos
- tipo 1 tiendas en línea, Complementos
- Windows Media Player tiendas en línea, Asistente para complementos
- tiendas en línea, Asistente para complementos
- tipo 1 tiendas en línea, Asistente para complementos
- Windows Media Player tiendas en línea, instalar el Asistente para complementos
- tiendas en línea, Asistente para instalar complementos
- Escriba 1 tiendas en línea, Asistente para instalar complementos
- complementos, Windows Media Player tiendas en línea
- complementos, tiendas en línea
- complementos, escriba 1 tiendas en línea
- complementos, Asistente para instalar complementos
- complementos, Asistente para complementos
- Complementos de Windows Media Player, escriba 1 tiendas en línea
- Complementos de Windows Media Player, tiendas en línea
- Complementos de Windows Media Player, Windows Media Player tiendas en línea
- Complementos de Windows Media Player, instalación del Asistente para complementos
- Complementos de Windows Media Player, Asistente para complementos
- instalación del Asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075837"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="d43b5-124">Instalación del Asistente para complementos de tienda en línea</span><span class="sxs-lookup"><span data-stu-id="d43b5-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="d43b5-125">Para configurar el entorno de desarrollo para crear complementos de tienda en línea de tipo 1, debe instalar los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d43b5-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="d43b5-126">Microsoft Visual Studio 2005 o posterior</span><span class="sxs-lookup"><span data-stu-id="d43b5-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="d43b5-127">Windows Media Player 11 o posterior</span><span class="sxs-lookup"><span data-stu-id="d43b5-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="d43b5-128">Windows SDK, que incluye el SDK de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d43b5-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="d43b5-129">Asistente para complementos de tienda en línea</span><span class="sxs-lookup"><span data-stu-id="d43b5-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="d43b5-130">Instalación del asistente</span><span class="sxs-lookup"><span data-stu-id="d43b5-130">Installing the Wizard</span></span>

<span data-ttu-id="d43b5-131">Siga estos pasos para instalar el Asistente para complementos de tienda en línea en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d43b5-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="d43b5-132">Busque la carpeta en la que instaló el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d43b5-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="d43b5-133">Expanda la carpeta para ver sus subcarpetas y vaya a samples \\ multimedia \\ WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="d43b5-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="d43b5-134">Busque los tres archivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d43b5-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="d43b5-135">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="d43b5-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="d43b5-136">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="d43b5-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="d43b5-137">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="d43b5-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="d43b5-138">Con un editor de texto como el Bloc de notas, edite el archivo wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="d43b5-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="d43b5-139">Busque la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="d43b5-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="d43b5-140">Cambie `<VsWizardEngine version goes here>` a uno de los valores siguientes, en función de la versión de Visual Studio que tenga instalada.</span><span class="sxs-lookup"><span data-stu-id="d43b5-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="d43b5-141">Value</span><span class="sxs-lookup"><span data-stu-id="d43b5-141">Value</span></span>              | <span data-ttu-id="d43b5-142">Versión de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d43b5-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="d43b5-143">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="d43b5-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="d43b5-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="d43b5-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="d43b5-145">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="d43b5-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="d43b5-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="d43b5-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="d43b5-147">Busque la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="d43b5-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="d43b5-148">Cambie `<path to wmpservices directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.</span><span class="sxs-lookup"><span data-stu-id="d43b5-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="d43b5-149">Por ejemplo, supongamos que tiene Visual Studio 2008 y que los archivos del asistente están aquí: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples multimedia de los servicios de los \\ \\ \\ asistentes \\ .</span><span class="sxs-lookup"><span data-stu-id="d43b5-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="d43b5-150">El archivo wmpservices. vsz tendrá el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="d43b5-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="d43b5-151">Busque la carpeta en la que instaló Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d43b5-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="d43b5-152">Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada VCProjects.</span><span class="sxs-lookup"><span data-stu-id="d43b5-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="d43b5-153">Copie los tres archivos enumerados en el paso 2 en la carpeta VCProjects.</span><span class="sxs-lookup"><span data-stu-id="d43b5-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="d43b5-154">El asistente ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="d43b5-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d43b5-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d43b5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d43b5-156">Compilar el complemento para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="d43b5-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




