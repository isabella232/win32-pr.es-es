---
title: Introducción con el SDK de Windows Media Player
description: Introducción con el SDK de Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, Complementos
- Windows Media Player Mobile, Complementos de la interfaz de usuario
- Complementos móviles de Windows Media Player
- complementos, interfaz de usuario
- complementos, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800626"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="9b3e5-110">Introducción con el SDK de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="9b3e5-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="9b3e5-111">Para crear el complemento, primero debe instalar Microsoft eMbedded Visual C++ 4,0 y Visual Studio 2003.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="9b3e5-112">También debe instalar el SDK de Pocket PC 2003 o el SDK de smartphone 2003, que son descargas independientes.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="9b3e5-113">Para compilar y ejecutar el proyecto, un dispositivo Pocket PC o smartphone que ejecute el sistema operativo Windows Mobile 2003 Second Edition debe estar sincronizado con el equipo de desarrollo mediante Microsoft ActiveSync® 3.7.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="9b3e5-114">Dado que los complementos de interfaz de usuario en dispositivos Windows Mobile usan el mismo modelo de complemento que las versiones de escritorio, puede usar el Asistente para complementos de Windows Media Player como punto de partida al crear un complemento de la interfaz de usuario de fondo que funcionará con Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="9b3e5-115">Para crear código de complemento de la interfaz de usuario, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9b3e5-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="9b3e5-116">Abra Visual Studio 2003 e inicie un nuevo proyecto en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="9b3e5-117">En el panel **plantillas** **, seleccione Asistente para complementos de Media Player de Windows** .</span><span class="sxs-lookup"><span data-stu-id="9b3e5-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="9b3e5-118">Asigne al proyecto el nombre NetworkPlugin y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="9b3e5-119">Seleccione **complemento** de la interfaz de usuario y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="9b3e5-120">Seleccione **fondo** y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="9b3e5-121">Haga clic en **Siguiente** para cerrar el asistente.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="9b3e5-122">Si va a supervisar eventos con el complemento, debe comprobar la **escucha de eventos** antes de finalizar el asistente, y debe leer la documentación de la interfaz **IWMPEvents** para averiguar qué eventos se admiten en Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="9b3e5-123">Ahora que ha creado el código de complemento de la interfaz de usuario, debe crear un proyecto Windows CE DLL vacío en eMbedded Visual C++ 4,0.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="9b3e5-124">Después, copie los archivos de código fuente generados por el asistente en ese nuevo proyecto para que se compilen con el compilador ARM4.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="9b3e5-125">Para crear un proyecto vacío</span><span class="sxs-lookup"><span data-stu-id="9b3e5-125">To create an empty project</span></span>

1.  <span data-ttu-id="9b3e5-126">Inicie un nuevo proyecto en el Visual C++ incrustado y, a continuación, seleccione **WCE Dynamic-Link Library** en el panel **proyectos** .</span><span class="sxs-lookup"><span data-stu-id="9b3e5-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="9b3e5-127">Asigne un nombre al proyecto y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="9b3e5-128">Asegúrese de que haya seleccionado **un proyecto Windows CE dll vacío** y, a continuación, haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="9b3e5-129">Haga clic en el elemento de menú **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="9b3e5-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="9b3e5-130">Seleccione **Agregar al proyecto** y, a continuación, haga clic en **archivos**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="9b3e5-131">Seleccione los archivos de C++ que creó con el Asistente para complementos y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9b3e5-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b3e5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b3e5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b3e5-133">**Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile**</span><span class="sxs-lookup"><span data-stu-id="9b3e5-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="9b3e5-134">**Interfaz IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="9b3e5-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




