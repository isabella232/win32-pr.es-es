---
title: Ejemplo customAccServer
description: Ejemplo customAccServer
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088013"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="f20e5-103">Ejemplo customAccServer</span><span class="sxs-lookup"><span data-stu-id="f20e5-103">CustomAccServer Sample</span></span>

<span data-ttu-id="f20e5-104">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f20e5-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f20e5-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="f20e5-105">Description</span></span>](#description)
-   [<span data-ttu-id="f20e5-106">Descargar información</span><span class="sxs-lookup"><span data-stu-id="f20e5-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="f20e5-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="f20e5-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="f20e5-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f20e5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f20e5-109">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="f20e5-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f20e5-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f20e5-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f20e5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f20e5-111">Description</span></span>

<span data-ttu-id="f20e5-112">En este ejemplo se muestra cómo implementar un servidor Microsoft Active Accessibility para un control personalizado simple.</span><span class="sxs-lookup"><span data-stu-id="f20e5-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="f20e5-113">El objeto accesible para el control consta del elemento raíz (un cuadro de lista) y sus elementos secundarios (los elementos de lista).</span><span class="sxs-lookup"><span data-stu-id="f20e5-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="f20e5-114">Descargar información</span><span class="sxs-lookup"><span data-stu-id="f20e5-114">Download Information</span></span>

<span data-ttu-id="f20e5-115">El ejemplo CustomAccServer se instala como parte de [Microsoft Kit de desarrollo de software de Windows (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) y está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="f20e5-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="f20e5-116">Location</span><span class="sxs-lookup"><span data-stu-id="f20e5-116">Location</span></span>    | <span data-ttu-id="f20e5-117">Ruta de acceso o dirección URL</span><span class="sxs-lookup"><span data-stu-id="f20e5-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f20e5-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f20e5-118">Windows SDK</span></span> | <span data-ttu-id="f20e5-119">%Program Files% \\ Microsoft SDKs \\ Windows version number Samples \\ \[ \] \\ \\ winui \\ msaa</span><span class="sxs-lookup"><span data-stu-id="f20e5-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="f20e5-120">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="f20e5-120">Minimum Requirements</span></span>



| <span data-ttu-id="f20e5-121">Producto</span><span class="sxs-lookup"><span data-stu-id="f20e5-121">Product</span></span>          | <span data-ttu-id="f20e5-122">Versión</span><span class="sxs-lookup"><span data-stu-id="f20e5-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="f20e5-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f20e5-123">Operating System</span></span> | <span data-ttu-id="f20e5-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f20e5-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="f20e5-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f20e5-125">Windows SDK</span></span>      | <span data-ttu-id="f20e5-126">7.0</span><span class="sxs-lookup"><span data-stu-id="f20e5-126">7.0</span></span>                             |
| <span data-ttu-id="f20e5-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f20e5-127">Visual Studio</span></span>    | <span data-ttu-id="f20e5-128">2008</span><span class="sxs-lookup"><span data-stu-id="f20e5-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="f20e5-129">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f20e5-129">Building the Sample</span></span>

<span data-ttu-id="f20e5-130">Para compilar el ejemplo mediante Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="f20e5-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="f20e5-131">Ejecute la herramienta de configuración de Microsoft Kit de desarrollo de software de Windows (SDK) proporcionada con el SDK para agregar directorios de incluyen del SDK a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f20e5-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="f20e5-132">Abra Explorador de Windows y vaya al directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f20e5-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="f20e5-133">Haga doble clic en el icono del archivo .sln (solución) para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f20e5-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="f20e5-134">En el **menú Compilar,** seleccione **Compilar solución** para compilar la solución.</span><span class="sxs-lookup"><span data-stu-id="f20e5-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="f20e5-135">La aplicación se compilará en el directorio \\ debug o \\ release predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f20e5-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="f20e5-136">Para compilar el ejemplo desde la línea de comandos, vea Compilar ejemplos en las notas de la versión de Windows SDK en la siguiente ubicación: %Archivos de programa% Sdk \\ de Microsoft para Windows \\ \\ v7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="f20e5-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f20e5-137">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f20e5-137">Running the Sample</span></span>

<span data-ttu-id="f20e5-138">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f20e5-138">To run the sample:</span></span>

1.  <span data-ttu-id="f20e5-139">Vaya al directorio que contiene el nuevo ejecutable mediante el símbolo del sistema o Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20e5-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f20e5-140">Escriba AccServer.exe en la línea de comandos o haga doble clic en el icono AccServer.exe para iniciarlo desde Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f20e5-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="f20e5-141">Para ejecutar desde Visual Studio, presione F5 o haga clic **en Iniciar depuración** en el **menú** Depurar.</span><span class="sxs-lookup"><span data-stu-id="f20e5-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f20e5-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f20e5-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20e5-143">Muestras</span><span class="sxs-lookup"><span data-stu-id="f20e5-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




