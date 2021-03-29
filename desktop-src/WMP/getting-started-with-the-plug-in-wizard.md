---
title: Introducción con el Asistente para complementos
description: Introducción con el Asistente para complementos
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Complementos de Windows Media Player, instalación del Asistente para complementos
- complementos, Asistente para instalar complementos
- crear complementos, Asistente para instalar complementos
- Asistente para complementos de Windows Media Player, instalar
- instalación del Asistente para complementos
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994436"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="163f4-109">Introducción con el Asistente para complementos</span><span class="sxs-lookup"><span data-stu-id="163f4-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="163f4-110">Para configurar el entorno de desarrollo para crear complementos de Media Player de Windows, debe instalar los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="163f4-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="163f4-111">Microsoft Visual Studio .NET 2003 o posterior</span><span class="sxs-lookup"><span data-stu-id="163f4-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="163f4-112">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="163f4-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="163f4-113">Windows SDK, que incluye el SDK de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="163f4-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="163f4-114">Asistente para complementos de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="163f4-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="163f4-115">Instalación del asistente</span><span class="sxs-lookup"><span data-stu-id="163f4-115">Installing the Wizard</span></span>

<span data-ttu-id="163f4-116">Realice los pasos siguientes para instalar el Asistente para complementos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="163f4-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="163f4-117">Busque la carpeta en la que instaló el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="163f4-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="163f4-118">Expanda la carpeta para ver sus subcarpetas y vaya a ejemplos \\ multimedia \\ WMP \\ asistentes \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="163f4-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="163f4-119">Busque los tres archivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="163f4-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="163f4-120">wmpwiz. vsz</span><span class="sxs-lookup"><span data-stu-id="163f4-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="163f4-121">wmpwiz. vsdir</span><span class="sxs-lookup"><span data-stu-id="163f4-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="163f4-122">wmpwiz. ico</span><span class="sxs-lookup"><span data-stu-id="163f4-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="163f4-123">Con un editor de texto, como el Bloc de notas, edite el archivo wmpwiz. vsz.</span><span class="sxs-lookup"><span data-stu-id="163f4-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="163f4-124">Busque la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="163f4-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="163f4-125">Cambie `<VsWizardEngine version goes here>` a uno de los valores siguientes, en función de la versión de Visual Studio que tenga instalada.</span><span class="sxs-lookup"><span data-stu-id="163f4-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="163f4-126">Value</span><span class="sxs-lookup"><span data-stu-id="163f4-126">Value</span></span>              | <span data-ttu-id="163f4-127">Versión de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="163f4-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="163f4-128">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="163f4-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="163f4-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="163f4-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="163f4-130">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="163f4-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="163f4-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="163f4-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="163f4-132">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="163f4-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="163f4-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="163f4-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="163f4-134">Busque la línea siguiente:</span><span class="sxs-lookup"><span data-stu-id="163f4-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="163f4-135">Cambie `<path to wmpwiz directory goes here>` a la ruta de acceso donde se encuentran los archivos del asistente.</span><span class="sxs-lookup"><span data-stu-id="163f4-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="163f4-136">Por ejemplo, supongamos que tiene Visual Studio 2008 y que los archivos del asistente están aquí: C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples multimedia de los \\ asistentes de \\ \\ \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="163f4-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="163f4-137">El archivo wmpwiz. vsz tendrá el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="163f4-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="163f4-138">Busque la carpeta en la que instaló Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="163f4-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="163f4-139">Expanda la carpeta para ver sus subcarpetas y busque una carpeta denominada VCProjects.</span><span class="sxs-lookup"><span data-stu-id="163f4-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="163f4-140">Copie los tres archivos enumerados en el paso 2 en la carpeta VCProjects.</span><span class="sxs-lookup"><span data-stu-id="163f4-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="163f4-141">El asistente ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="163f4-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="163f4-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="163f4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="163f4-143">Compilar un complemento</span><span class="sxs-lookup"><span data-stu-id="163f4-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="163f4-144">Usar el Asistente para complementos con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="163f4-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




