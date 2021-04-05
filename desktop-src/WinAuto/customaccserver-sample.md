---
title: Ejemplo de CustomAccServer
description: .
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c047bde41bdf4a486e14ce6f293113a41ae9e285
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420363"
---
# <a name="customaccserver-sample"></a><span data-ttu-id="f58c4-103">Ejemplo de CustomAccServer</span><span class="sxs-lookup"><span data-stu-id="f58c4-103">CustomAccServer Sample</span></span>

<span data-ttu-id="f58c4-104">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="f58c4-104">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f58c4-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="f58c4-105">Description</span></span>](#description)
-   [<span data-ttu-id="f58c4-106">Descargar información</span><span class="sxs-lookup"><span data-stu-id="f58c4-106">Download Information</span></span>](#download-information)
-   [<span data-ttu-id="f58c4-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="f58c4-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="f58c4-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f58c4-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f58c4-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f58c4-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="f58c4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f58c4-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="f58c4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f58c4-111">Description</span></span>

<span data-ttu-id="f58c4-112">Este ejemplo muestra cómo implementar un servidor de Microsoft Active Accessibility para un control personalizado simple.</span><span class="sxs-lookup"><span data-stu-id="f58c4-112">This sample shows how to implement a Microsoft Active Accessibility server for a simple custom control.</span></span> <span data-ttu-id="f58c4-113">El objeto accesible para el control está compuesto del elemento raíz (un cuadro de lista) y sus elementos secundarios (los elementos de lista).</span><span class="sxs-lookup"><span data-stu-id="f58c4-113">The accessible object for the control consists of the root element (a list box) and its children (the list items.)</span></span>

## <a name="download-information"></a><span data-ttu-id="f58c4-114">Descargar información</span><span class="sxs-lookup"><span data-stu-id="f58c4-114">Download Information</span></span>

<span data-ttu-id="f58c4-115">El ejemplo CustomAccServer se instala como parte del [Kit de desarrollo de software (SDK) de Microsoft Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) y está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="f58c4-115">The CustomAccServer sample is installed as part of the [Microsoft Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="f58c4-116">Location</span><span class="sxs-lookup"><span data-stu-id="f58c4-116">Location</span></span>    | <span data-ttu-id="f58c4-117">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="f58c4-117">Path/URL</span></span>                                                                           |
|-------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f58c4-118">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f58c4-118">Windows SDK</span></span> | <span data-ttu-id="f58c4-119">% Archivos de programa% \\ Microsoft SDK \\ Windows número de \\ \[ versión \] \\ ejemplos \\ WinUI \\ MSAA</span><span class="sxs-lookup"><span data-stu-id="f58c4-119">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\msaa</span></span> |



 

## <a name="minimum-requirements"></a><span data-ttu-id="f58c4-120">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="f58c4-120">Minimum Requirements</span></span>



| <span data-ttu-id="f58c4-121">Producto</span><span class="sxs-lookup"><span data-stu-id="f58c4-121">Product</span></span>          | <span data-ttu-id="f58c4-122">Versión</span><span class="sxs-lookup"><span data-stu-id="f58c4-122">Version</span></span>                         |
|------------------|---------------------------------|
| <span data-ttu-id="f58c4-123">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f58c4-123">Operating System</span></span> | <span data-ttu-id="f58c4-124">Windows XP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f58c4-124">Windows XP, Windows Server 2003</span></span> |
| <span data-ttu-id="f58c4-125">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f58c4-125">Windows SDK</span></span>      | <span data-ttu-id="f58c4-126">7.0</span><span class="sxs-lookup"><span data-stu-id="f58c4-126">7.0</span></span>                             |
| <span data-ttu-id="f58c4-127">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f58c4-127">Visual Studio</span></span>    | <span data-ttu-id="f58c4-128">2008</span><span class="sxs-lookup"><span data-stu-id="f58c4-128">2008</span></span>                            |



 

## <a name="building-the-sample"></a><span data-ttu-id="f58c4-129">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f58c4-129">Building the Sample</span></span>

<span data-ttu-id="f58c4-130">Para compilar el ejemplo con Visual Studio 2008:</span><span class="sxs-lookup"><span data-stu-id="f58c4-130">To build the sample using Visual Studio 2008:</span></span>

1.  <span data-ttu-id="f58c4-131">Ejecute la herramienta de configuración del kit de desarrollo de software (SDK) de Microsoft Windows que se proporciona con el SDK para agregar directorios de inclusión de SDK a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f58c4-131">Run the Microsoft Windows Software Development Kit (SDK) Configuration Tool provided with the SDK to add SDK include directories to Visual Studio.</span></span>
2.  <span data-ttu-id="f58c4-132">Abra el explorador de Windows y navegue hasta el directorio del proyecto.</span><span class="sxs-lookup"><span data-stu-id="f58c4-132">Open Windows Explorer and navigate to the project directory.</span></span>
3.  <span data-ttu-id="f58c4-133">Haga doble clic en el icono del archivo. sln (solución) para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f58c4-133">Double-click the icon for the .sln (solution) file to open the project in Visual Studio.</span></span>
4.  <span data-ttu-id="f58c4-134">En el menú **compilar** , seleccione **compilar solución** para compilar la solución.</span><span class="sxs-lookup"><span data-stu-id="f58c4-134">On the **Build** menu, select **Build Solution** to build the solution.</span></span> <span data-ttu-id="f58c4-135">La aplicación se compilará en el \\ Directorio de depuración o \\ versión predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f58c4-135">The application will be built in the default \\Debug or \\Release directory.</span></span>

<span data-ttu-id="f58c4-136">Para generar el ejemplo desde la línea de comandos, vea crear ejemplos en las notas de la versión de Windows SDK en la siguiente ubicación:% archivos de programa% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ReleaseNotes.htm</span><span class="sxs-lookup"><span data-stu-id="f58c4-136">To build the sample from the command line, see Building Samples in the Windows SDK release notes at the following location: %Program Files%\\Microsoft SDKs\\Windows\\v7.0\\ReleaseNotes.htm</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f58c4-137">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="f58c4-137">Running the Sample</span></span>

<span data-ttu-id="f58c4-138">Para ejecutar el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f58c4-138">To run the sample:</span></span>

1.  <span data-ttu-id="f58c4-139">Navegue hasta el directorio que contiene el nuevo ejecutable, mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f58c4-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f58c4-140">Escriba AccServer.exe en la línea de comandos o haga doble clic en el icono de AccServer.exe para iniciarlo desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="f58c4-140">Type AccServer.exe at the command line, or double-click the icon for AccServer.exe to launch it from Windows Explorer.</span></span>

<span data-ttu-id="f58c4-141">Para ejecutar desde Visual Studio, presione F5 o haga clic en **iniciar depuración** en el menú **depurar** .</span><span class="sxs-lookup"><span data-stu-id="f58c4-141">To run from Visual Studio, press F5 or click **Start Debugging** from the **Debug** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f58c4-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f58c4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f58c4-143">Muestras</span><span class="sxs-lookup"><span data-stu-id="f58c4-143">Samples</span></span>](samples.md)
</dt> </dl>

 

 




