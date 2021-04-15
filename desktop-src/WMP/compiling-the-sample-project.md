---
title: Compilar el proyecto de ejemplo
description: Compilar el proyecto de ejemplo
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player tiendas en línea, compilar proyectos de ejemplo
- tiendas en línea, compilar proyectos de ejemplo
- tipo 2 tiendas en línea, compilar proyectos de ejemplo
- Windows Media Player tiendas en línea, proyectos de ejemplo
- tiendas en línea, proyectos de ejemplo
- tipo 2 tiendas en línea, proyectos de ejemplo
- Windows Media Player tiendas en línea, Asistente para proyectos
- tiendas en línea, Asistente para proyectos
- tipo 2 tiendas en línea, Asistente para proyectos
- complementos, Asistente para proyectos
- Complementos de Windows Media Player, Asistente para proyectos
- compilar proyectos de ejemplo
- ejemplos, tipo 2 tiendas en línea
- Asistente para proyectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695369"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="3c7bc-117">Compilar el proyecto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c7bc-117">Compiling the Sample Project</span></span>

<span data-ttu-id="3c7bc-118">El asistente genera todos los archivos que necesita para compilar el proyecto de ejemplo, por lo que no debe cambiar la configuración predeterminada del proyecto.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="3c7bc-119">En Visual Studio, en el menú **compilar** , haga clic en **compilar solución** para compilar y registrar el componente com.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="3c7bc-120">De forma predeterminada, la configuración de depuración está activa.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="3c7bc-121">En Windows Vista y versiones posteriores, el proyecto no se compilará correctamente a menos que ejecute Visual Studio con un token de acceso de administrador completo.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="3c7bc-122">Haga clic con el botón derecho en el nombre o el icono de Visual Studio y haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="3c7bc-123">Antes de intentar compilar el proyecto, asegúrese de configurar el entorno de desarrollo para que apunte a las carpetas denominadas include y lib en las que instaló el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="3c7bc-124">El compilador y el vinculador deberán tener acceso a algunos de los archivos de estas carpetas.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="3c7bc-125">Si ejecutó la utilidad de registro de Visual Studio que se incluye con el SDK de Windows Vista, es probable que el entorno de desarrollo ya se haya configurado para que apunte al Windows SDK carpetas include y lib.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="3c7bc-126">De lo contrario, debe configurar manualmente el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="3c7bc-127">Para configurar manualmente Visual Studio, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="3c7bc-128">En el menú **Herramientas** , haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="3c7bc-129">Haga clic en **proyectos y soluciones** y, a continuación, haga clic en **directorios de VC + +**.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="3c7bc-130">En **Mostrar directorios para**, haga clic en **incluir** archivos o **archivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="3c7bc-131">Agregue los directorios de los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="3c7bc-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c7bc-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c7bc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7bc-133">Compilar el complemento para una tienda en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="3c7bc-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




