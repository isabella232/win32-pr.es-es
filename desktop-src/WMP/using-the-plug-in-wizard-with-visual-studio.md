---
title: Usar el Asistente para complementos con Visual Studio
description: Usar el Asistente para complementos con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Complementos de Windows Media Player, Visual Studio
- complementos, Visual Studio
- crear complementos, Visual Studio
- Asistente para complementos de Windows Media Player, Visual Studio
- Asistente para complementos de Windows Media Player de Visual Studio
- Asistente para complementos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357281"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="7805b-109">Usar el Asistente para complementos con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7805b-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="7805b-110">Una vez instalados los componentes necesarios, puede crear rápidamente un complemento que sirva como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="7805b-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="7805b-111">Los siguientes pasos lo guiarán.</span><span class="sxs-lookup"><span data-stu-id="7805b-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="7805b-112">Inicie Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7805b-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="7805b-113">En el menú **archivo** , seleccione **nuevo** y haga clic en **proyecto**.</span><span class="sxs-lookup"><span data-stu-id="7805b-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="7805b-114">En **tipos de proyecto**, seleccione **proyectos de Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="7805b-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="7805b-115">En **plantillas**, seleccione **Asistente para complementos de Media Player de Windows**.</span><span class="sxs-lookup"><span data-stu-id="7805b-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="7805b-116">Escriba un nombre para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="7805b-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="7805b-117">Escriba una ubicación para el proyecto.</span><span class="sxs-lookup"><span data-stu-id="7805b-117">Enter a location for your project.</span></span> <span data-ttu-id="7805b-118">Esta es la carpeta en la que se copiarán los archivos del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7805b-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="7805b-119">Haga clic en **Aceptar** para iniciar el asistente.</span><span class="sxs-lookup"><span data-stu-id="7805b-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="7805b-120">Seleccione el tipo de complemento que desea crear.</span><span class="sxs-lookup"><span data-stu-id="7805b-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="7805b-121">Complete los demás cuadros de diálogo del asistente.</span><span class="sxs-lookup"><span data-stu-id="7805b-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="7805b-122">Use el entorno de desarrollo de Visual Studio para compilar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="7805b-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="7805b-123">En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="7805b-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="7805b-124">Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="7805b-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="7805b-125">Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7805b-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="7805b-126">El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="7805b-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="7805b-127">Si ejecutó la utilidad de registro de Visual Studio que se incluye con el Windows SDK, es probable que el entorno de desarrollo ya se haya configurado para que apunte a las carpetas include y lib de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7805b-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="7805b-128">De lo contrario, debe configurar manualmente el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="7805b-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="7805b-129">Para configurar manualmente Visual Studio, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7805b-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="7805b-130">En el menú **Herramientas** , haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="7805b-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="7805b-131">Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.</span><span class="sxs-lookup"><span data-stu-id="7805b-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="7805b-132">En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="7805b-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="7805b-133">Agregue los directorios de los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7805b-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7805b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7805b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7805b-135">Compilar un complemento</span><span class="sxs-lookup"><span data-stu-id="7805b-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




