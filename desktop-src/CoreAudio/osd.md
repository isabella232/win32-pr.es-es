---
description: En este ejemplo se usan las API de audio principales para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Feature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080224"
---
# <a name="osd"></a><span data-ttu-id="93191-103">Feature</span><span class="sxs-lookup"><span data-stu-id="93191-103">OSD</span></span>

<span data-ttu-id="93191-104">En este ejemplo se usan las API de audio principales para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="93191-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="93191-105">La presentación en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volumen de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca inalterado durante un breve período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="93191-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="93191-106">Este tema contiene las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="93191-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="93191-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="93191-107">Description</span></span>](#description)
-   [<span data-ttu-id="93191-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93191-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="93191-109">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="93191-110">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="93191-111">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="93191-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93191-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="93191-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="93191-113">Description</span></span>

<span data-ttu-id="93191-114">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="93191-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="93191-115">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="93191-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="93191-116">API de audio [EndpointVolume](endpointvolume-api.md)</span><span class="sxs-lookup"><span data-stu-id="93191-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="93191-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93191-117">Requirements</span></span>



| <span data-ttu-id="93191-118">Producto</span><span class="sxs-lookup"><span data-stu-id="93191-118">Product</span></span>                                                        | <span data-ttu-id="93191-119">Versión</span><span class="sxs-lookup"><span data-stu-id="93191-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="93191-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="93191-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="93191-121">Windows Vista o posterior</span><span class="sxs-lookup"><span data-stu-id="93191-121">Windows Vista or later</span></span> |
| <span data-ttu-id="93191-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="93191-122">Visual Studio</span></span>                                                  | <span data-ttu-id="93191-123">2005 o posterior</span><span class="sxs-lookup"><span data-stu-id="93191-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="93191-124">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-124">Downloading the Sample</span></span>

<span data-ttu-id="93191-125">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="93191-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="93191-126">Location</span><span class="sxs-lookup"><span data-stu-id="93191-126">Location</span></span>    | <span data-ttu-id="93191-127">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="93191-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93191-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="93191-128">Windows SDK</span></span> | <span data-ttu-id="93191-129">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ OSD \\ ...</span><span class="sxs-lookup"><span data-stu-id="93191-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="93191-130">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-130">Building the Sample</span></span>

1.  <span data-ttu-id="93191-131">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo OSD.</span><span class="sxs-lookup"><span data-stu-id="93191-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="93191-132">Ejecute el comando "Start OSD. sln" en el directorio OSD para abrir el proyecto OSD en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="93191-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="93191-133">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="93191-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="93191-134">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="93191-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="93191-135">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, OSD. vcproj.</span><span class="sxs-lookup"><span data-stu-id="93191-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="93191-136">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="93191-136">Running the Sample</span></span>

1.  <span data-ttu-id="93191-137">Ejecute el archivo ejecutable OSD, OSD.exe, en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="93191-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="93191-138">Tenga en cuenta que no verá un icono de la bandeja del sistema o una ventana de la aplicación, pero puede ver el proceso en ejecución mediante TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="93191-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="93191-139">Ejecute sndvol.exe para cambiar el volumen o silenciar, o bien cambie el volumen mediante controles de teclado o un control HID.</span><span class="sxs-lookup"><span data-stu-id="93191-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="93191-140">Se muestra la interfaz de usuario OSD.</span><span class="sxs-lookup"><span data-stu-id="93191-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="93191-141">Para salir de la aplicación, ejecute TaskMgr.exe, resalte el proceso de OSD.exe y haga clic en **Finalizar proceso**.</span><span class="sxs-lookup"><span data-stu-id="93191-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93191-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93191-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93191-143">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="93191-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



