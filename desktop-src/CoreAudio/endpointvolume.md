---
description: Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, según lo especificado por el usuario.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496372"
---
# <a name="endpointvolume"></a><span data-ttu-id="03616-103">EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="03616-103">EndpointVolume</span></span>

<span data-ttu-id="03616-104">Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, según lo especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="03616-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="03616-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="03616-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="03616-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="03616-106">Description</span></span>](#description)
-   [<span data-ttu-id="03616-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03616-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="03616-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="03616-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="03616-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="03616-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03616-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="03616-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="03616-112">Description</span></span>

<span data-ttu-id="03616-113">En este ejemplo se muestran las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="03616-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="03616-114">[MMDEVICE API](mmdevice-api.md) para la enumeración y selección de dispositivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="03616-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="03616-115">[ENDPOINTVOLUME API](endpointvolume-api.md) para controlar los niveles de volumen del punto de conexión del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03616-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="03616-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03616-116">Requirements</span></span>



| <span data-ttu-id="03616-117">Producto</span><span class="sxs-lookup"><span data-stu-id="03616-117">Product</span></span>                                                        | <span data-ttu-id="03616-118">Versión</span><span class="sxs-lookup"><span data-stu-id="03616-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="03616-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="03616-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="03616-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03616-120">Windows 7</span></span> |
| <span data-ttu-id="03616-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="03616-121">Visual Studio</span></span>                                                  | <span data-ttu-id="03616-122">2008</span><span class="sxs-lookup"><span data-stu-id="03616-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="03616-123">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-123">Downloading the Sample</span></span>

<span data-ttu-id="03616-124">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="03616-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="03616-125">Location</span><span class="sxs-lookup"><span data-stu-id="03616-125">Location</span></span>    | <span data-ttu-id="03616-126">Ruta de acceso/URL</span><span class="sxs-lookup"><span data-stu-id="03616-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03616-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="03616-127">Windows SDK</span></span> | <span data-ttu-id="03616-128">\\Archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ multimedia \\ audio \\ EndpointVolume \\ ...</span><span class="sxs-lookup"><span data-stu-id="03616-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="03616-129">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-129">Building the Sample</span></span>

<span data-ttu-id="03616-130">Para compilar el ejemplo x, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="03616-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="03616-131">Para compilar el ejemplo EndpointVolumeChanger, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="03616-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="03616-132">Abra el shell de CMD para el Windows SDK y cambie al directorio de ejemplo EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="03616-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="03616-133">Ejecute el comando `start EndpointVolumeChanger.sln` en el directorio EndpointVolume para abrir el proyecto EndpointVolumeChanger en la ventana de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="03616-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="03616-134">En la ventana, seleccione la configuración de la solución de **depuración** o **versión** , seleccione el menú **compilar** en la barra de menús y seleccione la opción **compilar** .</span><span class="sxs-lookup"><span data-stu-id="03616-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="03616-135">Si no abre Visual Studio desde el shell de CMD para el SDK, Visual Studio no tendrá acceso al entorno de compilación del SDK.</span><span class="sxs-lookup"><span data-stu-id="03616-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="03616-136">En ese caso, el ejemplo no se compilará a menos que establezca explícitamente la variable de entorno MSSdk, que se usa en el archivo de proyecto, WASAPIEndpointVolume. vcproj.</span><span class="sxs-lookup"><span data-stu-id="03616-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="03616-137">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="03616-137">Running the Sample</span></span>

<span data-ttu-id="03616-138">Si compila la aplicación de demostración correctamente, se genera un archivo ejecutable EndpointVolumeChanger.exe.</span><span class="sxs-lookup"><span data-stu-id="03616-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="03616-139">Para ejecutarlo, escriba `EndpointVolumeChanger` en una ventana de comandos seguida de los argumentos obligatorios u opcionales.</span><span class="sxs-lookup"><span data-stu-id="03616-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="03616-140">En el ejemplo siguiente se muestra cómo alternar el valor de silenciar en el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03616-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="03616-141">En la tabla siguiente se muestran los argumentos.</span><span class="sxs-lookup"><span data-stu-id="03616-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="03616-142">Argumento</span><span class="sxs-lookup"><span data-stu-id="03616-142">Argument</span></span>        | <span data-ttu-id="03616-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="03616-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="03616-144">-?</span><span class="sxs-lookup"><span data-stu-id="03616-144">-?</span></span>              | <span data-ttu-id="03616-145">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="03616-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="03616-146">-H</span><span class="sxs-lookup"><span data-stu-id="03616-146">-h</span></span>              | <span data-ttu-id="03616-147">Muestra la ayuda.</span><span class="sxs-lookup"><span data-stu-id="03616-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="03616-148">Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="03616-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="03616-149">.</span><span class="sxs-lookup"><span data-stu-id="03616-149">.</span></span> |
| <span data-ttu-id="03616-150">-arriba</span><span class="sxs-lookup"><span data-stu-id="03616-150">-up</span></span>             | <span data-ttu-id="03616-151">Incrementa el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="03616-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="03616-152">Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="03616-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="03616-153">-abajo</span><span class="sxs-lookup"><span data-stu-id="03616-153">-down</span></span>           | <span data-ttu-id="03616-154">Disminuye el nivel de volumen en el dispositivo de punto de conexión de audio en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="03616-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="03616-155">-v</span><span class="sxs-lookup"><span data-stu-id="03616-155">-v</span></span>              | <span data-ttu-id="03616-156">Establece el nivel de volumen maestro en el dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="03616-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="03616-157">-consola</span><span class="sxs-lookup"><span data-stu-id="03616-157">-console</span></span>        | <span data-ttu-id="03616-158">Use el dispositivo de consola predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03616-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="03616-159">-comunicaciones</span><span class="sxs-lookup"><span data-stu-id="03616-159">-communications</span></span> | <span data-ttu-id="03616-160">Use el dispositivo de comunicación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03616-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="03616-161">-multimedia</span><span class="sxs-lookup"><span data-stu-id="03616-161">-multimedia</span></span>     | <span data-ttu-id="03616-162">Use el dispositivo multimedia predeterminado.</span><span class="sxs-lookup"><span data-stu-id="03616-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="03616-163">-punto de conexión</span><span class="sxs-lookup"><span data-stu-id="03616-163">-endpoint</span></span>       | <span data-ttu-id="03616-164">Use el identificador de extremo especificado en el valor del modificador.</span><span class="sxs-lookup"><span data-stu-id="03616-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="03616-165">Si la aplicación se ejecuta sin argumentos, enumera los dispositivos disponibles y solicita al usuario que seleccione un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03616-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="03616-166">Una vez que el usuario especifica el dispositivo, la aplicación muestra la configuración actual del volumen del punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="03616-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="03616-167">El volumen se puede controlar mediante los modificadores descritos en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="03616-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="03616-168">Para obtener más información sobre el control de los niveles de volumen de los dispositivos de punto de conexión de audio, consulte [ENDPOINTVOLUME API](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="03616-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03616-169">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03616-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03616-170">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="03616-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



