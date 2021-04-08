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
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Ejemplos de SDK que usan las API de audio principales

El Windows SDK incluye los siguientes ejemplos de código que muestran el uso de las API de audio principales. Los ejemplos siguientes se encuentran en el directorio% MSSdk% \\ Samples \\ multimedia \\ audio, donde% MSSdk% es el directorio raíz de la instalación de Windows SDK en el equipo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Muestra</th>
<th>Deascription</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="aecmicarray.md">AECMicArray</a></td>
<td>En este ejemplo se usan las API MMDevice, WASAPI, DeviceTopology y EndpointVolume para capturar una secuencia de voz de alta calidad. El ejemplo de admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante AEC DMO también denominado DSP de captura de voz proporcionado por Microsoft.</td>
</tr>
<tr class="even">
<td><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada, especificado por el usuario y lo escribe en un nombre único. Archivo WAV en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en eventos.</td>
</tr>
<tr class="odd">
<td><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para capturar datos de audio de un dispositivo de entrada, especificado por el usuario y lo escribe en un nombre único. Archivo WAV en el directorio actual. Este ejemplo muestra el almacenamiento en búfer basado en temporizador.</td>
</tr>
<tr class="even">
<td><a href="duckingcapturesample.md">DuckingCaptureSample</a></td>
<td>En esta aplicación de ejemplo se muestra la apertura y el cierre de secuencias de comunicación y la causa de los eventos que una aplicación puede obtener para implementar la atenuación de la secuencia. Esta aplicación implementa un cliente de chat que usa las API de audio principales para leer los datos de audio de un dispositivo de comunicación y reproducirlos en el dispositivo de salida.</td>
</tr>
<tr class="odd">
<td><a href="endpointvolume.md">EndpointVolume</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para cambiar el volumen del dispositivo, especificado por el usuario.</td>
</tr>
<tr class="even">
<td><a href="osd.md">Feature</a></td>
<td>En este ejemplo se usan las API MMDevice y EndpointVolume para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de extremo de representación de audio predeterminado. La presentación en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volumen de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca inalterado durante un breve período de tiempo.</td>
</tr>
<tr class="odd">
<td><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo exclusivo. En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</td>
</tr>
<tr class="even">
<td><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo exclusivo. En el caso de una secuencia en modo exclusivo, el cliente comparte el búfer del extremo con el dispositivo de audio.</td>
</tr>
<tr class="odd">
<td><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en eventos para un cliente de representación en modo compartido. En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</td>
</tr>
<tr class="even">
<td><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></td>
<td>Esta aplicación de ejemplo usa las API de audio principales para representar datos de audio en un dispositivo de salida, especificado por el usuario. Este ejemplo muestra el almacenamiento en búfer basado en temporizador para un cliente de representación en modo compartido. En el caso de una secuencia en modo compartido, el cliente comparte el búfer del extremo con el motor de audio.</td>
</tr>
<tr class="odd">
<td>WinAudio</td>
<td>En este ejemplo se usa la API MMDevice y WASAPI para reproducir y capturar secuencias de audio. La interfaz de usuario de esta aplicación de ejemplo permite a los usuarios seleccionar dispositivos de punto de conexión de audio, cambiar el nivel de volumen de la sesión de audio local y reproducir los archivos. wav y la entrada del micrófono.
<blockquote>
[!Note]<br />
Este ejemplo está en desuso en Windows 7.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Puede descargar el Windows SDK desde el sitio web del [centro de descarga de Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las API de audio de Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




