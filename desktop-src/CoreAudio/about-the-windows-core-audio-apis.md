---
description: Acerca de las API de audio de Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Acerca de las API de audio de Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907513"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="523bd-103">Acerca de las API de audio de Windows Core</span><span class="sxs-lookup"><span data-stu-id="523bd-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="523bd-104">En esta documentación se proporciona información sobre las API de audio principales para la familia de sistemas operativos Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="523bd-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="523bd-105">Las API de audio principales se introdujeron en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="523bd-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="523bd-106">Se trata de un nuevo conjunto de componentes de audio de modo de usuario que proporciona a las aplicaciones cliente capacidades de audio mejoradas.</span><span class="sxs-lookup"><span data-stu-id="523bd-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="523bd-107">Entre estas funcionalidades se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="523bd-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="523bd-108">Transmisión por secuencias de audio de baja latencia y resistente a problemas.</span><span class="sxs-lookup"><span data-stu-id="523bd-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="523bd-109">Confiabilidad mejorada (muchas funciones de audio se han pasado del modo kernel al modo de usuario).</span><span class="sxs-lookup"><span data-stu-id="523bd-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="523bd-110">Seguridad mejorada (el procesamiento del contenido de audio protegido se realiza en un proceso seguro y con privilegios reducidos).</span><span class="sxs-lookup"><span data-stu-id="523bd-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="523bd-111">Asignación de roles en todo el sistema (consola, multimedia y comunicaciones) en dispositivos de audio individuales.</span><span class="sxs-lookup"><span data-stu-id="523bd-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="523bd-112">Abstracción de software de los dispositivos de punto de conexión de audio (por ejemplo, altavoces, auriculares y micrófonos) que el usuario manipula directamente.</span><span class="sxs-lookup"><span data-stu-id="523bd-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="523bd-113">Las API de audio principales se han mejorado en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="523bd-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="523bd-114">Para obtener más información acerca de las mejoras y las nuevas características agregadas, consulte [novedades de las API de audio principales en Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="523bd-115">En esta documentación se describen las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="523bd-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="523bd-116">Estas API sirven como base para las siguientes API de nivel superior:</span><span class="sxs-lookup"><span data-stu-id="523bd-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="523bd-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="523bd-117">DirectSound</span></span>
-   <span data-ttu-id="523bd-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="523bd-118">DirectMusic</span></span>
-   <span data-ttu-id="523bd-119">Funciones **waveXxx** y **mixerXxx** multimedia de Windows</span><span class="sxs-lookup"><span data-stu-id="523bd-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="523bd-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="523bd-120">Media Foundation</span></span>

<span data-ttu-id="523bd-121">Estas API de nivel superior usan las API de audio principales para compartir el acceso a los dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="523bd-122">Media Foundation es nuevo en Windows Vista, mientras que las funciones DirectSound, DirectMusic y **waveXxx** y **mixerXxx** se admiten en Windows 98, Windows Millennium Edition y en Windows 2000 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="523bd-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="523bd-123">La mayoría de las aplicaciones de audio se comunican con las API de nivel superior en lugar de comunicarse directamente con las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="523bd-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="523bd-124">Algunos ejemplos de aplicaciones que usan API de nivel superior son:</span><span class="sxs-lookup"><span data-stu-id="523bd-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="523bd-125">Instancias de Media Player</span><span class="sxs-lookup"><span data-stu-id="523bd-125">Media players</span></span>
-   <span data-ttu-id="523bd-126">Reproductores de DVD</span><span class="sxs-lookup"><span data-stu-id="523bd-126">DVD players</span></span>
-   <span data-ttu-id="523bd-127">Juegos</span><span class="sxs-lookup"><span data-stu-id="523bd-127">Games</span></span>
-   <span data-ttu-id="523bd-128">Aplicaciones empresariales, como Microsoft Office PowerPoint, que reproducen archivos de sonido</span><span class="sxs-lookup"><span data-stu-id="523bd-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="523bd-129">Normalmente, estas aplicaciones se comunican con las API de DirectSound o Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="523bd-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="523bd-130">Es posible que la comunicación directa con las API de audio principales no sea adecuada para muchas aplicaciones de audio de uso general.</span><span class="sxs-lookup"><span data-stu-id="523bd-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="523bd-131">Por ejemplo, las API de audio principales requieren secuencias de audio para usar los formatos de datos nativos de un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="523bd-132">Sin embargo, es posible que los desarrolladores de software de terceros que desarrollan los siguientes tipos de productos necesiten las funcionalidades especiales de las API de audio principales:</span><span class="sxs-lookup"><span data-stu-id="523bd-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="523bd-133">Aplicaciones de audio profesional ("audio de Pro")</span><span class="sxs-lookup"><span data-stu-id="523bd-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="523bd-134">Aplicaciones RTC (comunicación en tiempo real)</span><span class="sxs-lookup"><span data-stu-id="523bd-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="523bd-135">API de audio de terceros</span><span class="sxs-lookup"><span data-stu-id="523bd-135">Third-party audio APIs</span></span>

<span data-ttu-id="523bd-136">Una aplicación de "audio de Pro" o RTC puede necesitar acceso directo a las características de bajo nivel de las API de audio principales para lograr una latencia mínima al obtener acceso exclusivo al hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="523bd-137">Una API de audio de terceros podría requerir acceso directo a las API de audio principales para implementar un conjunto de características que es posible que no sean totalmente compatibles con ninguna de las API de audio de alto nivel que se suministran con Windows.</span><span class="sxs-lookup"><span data-stu-id="523bd-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="523bd-138">Una aplicación que usa una API de audio heredada para reproducir o grabar audio podría requerir funcionalidades adicionales que no son compatibles con la API de audio heredada, pero que son compatibles con las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="523bd-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="523bd-139">En muchos casos, la aplicación puede acceder a estas funcionalidades directamente a través de las API de audio principales, que se pueden usar junto con la API de audio heredada.</span><span class="sxs-lookup"><span data-stu-id="523bd-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="523bd-140">Las API de audio principales son:</span><span class="sxs-lookup"><span data-stu-id="523bd-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="523bd-141">[API de dispositivo multimedia (MMDevice)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="523bd-142">Los clientes usan esta API para enumerar los dispositivos de punto de conexión de audio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="523bd-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="523bd-143">[API de sesión de audio de Windows (WASAPI)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="523bd-144">Los clientes usan esta API para crear y administrar secuencias de audio hacia y desde dispositivos de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="523bd-145">[API de DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="523bd-146">Los clientes usan esta API para acceder directamente a las características topológicas (por ejemplo, controles de volumen y multiplexores) que se encuentran a lo largo de las rutas de acceso de datos dentro de los dispositivos de hardware de los adaptadores de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="523bd-147">[API de EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="523bd-148">Los clientes usan esta API para acceder directamente a los controles de volumen en los dispositivos de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="523bd-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="523bd-149">Esta API la usan principalmente las aplicaciones que administran secuencias de audio en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="523bd-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="523bd-150">Estas API admiten la noción fácil de utilizar de un dispositivo de punto de conexión, que se describe en [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="523bd-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="523bd-151">Microsoft no planea que las API de audio principales que se describen aquí estén disponibles para su uso con versiones anteriores de Windows, incluidas Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 y Windows 98.</span><span class="sxs-lookup"><span data-stu-id="523bd-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="523bd-152">Esta información general contiene los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="523bd-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="523bd-153">**Tema.**</span><span class="sxs-lookup"><span data-stu-id="523bd-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="523bd-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="523bd-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="523bd-155">Novedades de las API de audio principales en Windows 7</span><span class="sxs-lookup"><span data-stu-id="523bd-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="523bd-156">Resume las nuevas características y las mejoras de las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="523bd-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="523bd-157">Archivos de encabezado y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="523bd-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="523bd-158">Describe los archivos de encabezado y los componentes del sistema para las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="523bd-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="523bd-159">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="523bd-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="523bd-160">Enumera los ejemplos de la Windows SDK que usan las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="523bd-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="523bd-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="523bd-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="523bd-162">API de audio principales</span><span class="sxs-lookup"><span data-stu-id="523bd-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



