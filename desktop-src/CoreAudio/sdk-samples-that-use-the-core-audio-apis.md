---
description: Ejemplos de SDK que usan las API de audio principales
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Ejemplos de SDK que usan las API de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000640"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="f1c82-103">Ejemplos de SDK que usan las API de audio principales</span><span class="sxs-lookup"><span data-stu-id="f1c82-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="f1c82-104">El Windows SDK incluye los siguientes ejemplos de código que muestran el uso de las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="f1c82-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="f1c82-105">Los ejemplos siguientes se encuentran en el directorio% MSSdk% \\ Samples \\ multimedia \\ audio, donde% MSSdk% es el directorio raíz de la instalación de Windows SDK en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f1c82-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1c82-106">Muestra</span><span class="sxs-lookup"><span data-stu-id="f1c82-106">Sample</span></span></th>
<th><span data-ttu-id="f1c82-107">Deascription</span><span class="sxs-lookup"><span data-stu-id="f1c82-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f1c82-108"><a href="aecmicarray.md">AECMicArray</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="f1c82-109">En este ejemplo se usan las API MMDevice, WASAPI, DeviceTopology y EndpointVolume para capturar una secuencia de voz de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="f1c82-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="f1c82-110">El ejemplo de admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO también denominado DSP de captura de voz proporcionado por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1c82-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1c82-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-112">Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada, especificado por el usuario y lo escribe en un nombre único. Archivo WAV en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="f1c82-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="f1c82-113">Este ejemplo muestra el almacenamiento en búfer basado en eventos.</span><span class="sxs-lookup"><span data-stu-id="f1c82-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1c82-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-115">Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada, especificado por el usuario y lo escribe en un nombre único. Archivo WAV en el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="f1c82-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="f1c82-116">Este ejemplo muestra el almacenamiento en búfer basado en temporizador.</span><span class="sxs-lookup"><span data-stu-id="f1c82-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1c82-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="f1c82-118">En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1c82-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="f1c82-119">Esta aplicación implementa un cliente de chat que usa las API de audio principales para leer los datos de audio de un dispositivo de comunicación y reproducirlos en el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="f1c82-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1c82-120"><a href="endpointvolume.md">EndpointVolume</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="f1c82-121">Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c82-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1c82-122"><a href="osd.md">Feature</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="f1c82-123">En este ejemplo se usan las API MMDevice y EndpointVolume para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f1c82-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="f1c82-124">La presentación en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volumen de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca inalterado durante un breve período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f1c82-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1c82-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-126">Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c82-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="f1c82-127">Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c82-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="f1c82-128">En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f1c82-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1c82-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-130">Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c82-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="f1c82-131">Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f1c82-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="f1c82-132">En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="f1c82-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1c82-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-134">Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c82-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="f1c82-135">Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="f1c82-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="f1c82-136">En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="f1c82-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1c82-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="f1c82-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="f1c82-138">Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1c82-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="f1c82-139">Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="f1c82-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="f1c82-140">En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</span><span class="sxs-lookup"><span data-stu-id="f1c82-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1c82-141">WinAudio</span><span class="sxs-lookup"><span data-stu-id="f1c82-141">WinAudio</span></span></td>
<td><span data-ttu-id="f1c82-142">En este ejemplo se usa la API MMDevice y WASAPI para reproducir y capturar secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="f1c82-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="f1c82-143">La interfaz de usuario de esta aplicación de ejemplo permite a los usuarios seleccionar dispositivos de punto de conexión de audio, cambiar el nivel de volumen de la sesión de audio local y reproducir los archivos. wav y la entrada del micrófono.</span><span class="sxs-lookup"><span data-stu-id="f1c82-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="f1c82-144">Este ejemplo está en desuso en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f1c82-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f1c82-145">Puede descargar el Windows SDK desde el sitio web del [centro de descarga de Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .</span><span class="sxs-lookup"><span data-stu-id="f1c82-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1c82-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c82-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c82-147">Acerca de las API de audio de Windows Core</span><span class="sxs-lookup"><span data-stu-id="f1c82-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




