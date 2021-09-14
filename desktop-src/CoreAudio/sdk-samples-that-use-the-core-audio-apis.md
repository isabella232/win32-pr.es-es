---
description: Ejemplos de SDK que usan las API de audio principales
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Ejemplos de SDK que usan las API de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f875095579b40c6646d89e31328c148c5724c309
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164810"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a>Ejemplos de SDK que usan las API de audio principales

El SDK Windows incluye los siguientes ejemplos de código que muestran el uso de las API de audio principal. Los ejemplos siguientes se encuentran en el directorio %MSSdk% ejemplos de audio multimedia, donde \\ \\ %MSSdk% es el directorio raíz de la instalación del SDK de Windows en \\ el equipo.




| Muestra | Desascription | 
|--------|--------------|
| <a href="aecmicarray.md">AECMicArray</a> | En este ejemplo se usan las API MMDevice, WASAPI, DeviceTopology y EndpointVolume para capturar un flujo de voz de alta calidad. El ejemplo admite la cancelación de eco acústico (AEC) y el procesamiento de la matriz de micrófonos mediante el uso de AEC DMO también denominado DSP de captura de voz proporcionado por Microsoft . | 
| <a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a> | Esta aplicación de ejemplo usa las API de audio principal para capturar datos de audio de un dispositivo de entrada, especificados por el usuario y los escribe en un nombre único denominado . Archivo WAV en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos. | 
| <a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a> | Esta aplicación de ejemplo usa las API de audio principal para capturar datos de audio de un dispositivo de entrada, especificados por el usuario y los escribe en un nombre único denominado . Archivo WAV en el directorio actual. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador. | 
| <a href="duckingcapturesample.md">DuckingCaptureSample</a> | Esta aplicación de ejemplo muestra cómo abrir y cerrar flujos de comunicación y provocar eventos de achacamiento que una aplicación puede obtener para implementar la atenuación de flujos. Esta aplicación implementa un cliente de chat que usa Core Audio API para leer datos de audio de un dispositivo de comunicación y reproducirlo en el dispositivo de salida. | 
| <a href="endpointvolume.md">EndpointVolume</a> | Esta aplicación de ejemplo usa las API de audio principal para cambiar el volumen del dispositivo, especificado por el usuario. | 
| <a href="osd.md">OSD</a> | En este ejemplo se usan las API MMDevice y EndpointVolume para implementar una pantalla en pantalla que muestra los cambios de volumen en el flujo de salida que se reproduce a través del dispositivo de punto de conexión de representación de audio predeterminado. La pantalla en pantalla aparece cuando el usuario ajusta el nivel de volumen en el programa de control de volúmenes de Windows, Sndvol.exe, y desaparece después de que el nivel de volumen permanezca sin cambios durante un breve período. | 
| <a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a> | Esta aplicación de ejemplo usa core Audio APIs para representar datos de audio en un dispositivo de salida, especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos para un cliente de representación en modo exclusivo. Para una secuencia en modo exclusivo, el cliente comparte el búfer del punto de conexión con el dispositivo de audio. | 
| <a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a> | Esta aplicación de ejemplo usa core Audio APIs para representar datos de audio en un dispositivo de salida, especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo exclusivo. Para una secuencia en modo exclusivo, el cliente comparte el búfer del punto de conexión con el dispositivo de audio. | 
| <a href="rendersharedeventdriven.md">RenderSharedEventDriven</a> | Esta aplicación de ejemplo usa core Audio APIs para representar datos de audio en un dispositivo de salida, especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por eventos para un cliente de representación en modo compartido. Para una secuencia en modo compartido, el cliente comparte el búfer del punto de conexión con el motor de audio. | 
| <a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a> | Esta aplicación de ejemplo usa core Audio APIs para representar datos de audio en un dispositivo de salida, especificado por el usuario. En este ejemplo se muestra el almacenamiento en búfer controlado por temporizador para un cliente de representación en modo compartido. Para una secuencia en modo compartido, el cliente comparte el búfer del punto de conexión con el motor de audio. | 
| WinAudio | En este ejemplo se usa MMDevice API y WASAPI para reproducir y capturar secuencias de audio. La interfaz de usuario de esta aplicación de ejemplo permite a los usuarios seleccionar dispositivos de punto de conexión de audio, cambiar el nivel de volumen de la sesión de audio local y reproducir archivos .wav y la entrada de micrófono.<blockquote>[!Note]<br />Este ejemplo ha quedado en desuso Windows 7.</blockquote><br /> | 




 

Puede descargar el SDK Windows desde el sitio web del Centro de [descarga Windows SDK de Microsoft.](https://developer.microsoft.com/windows/downloads/sdk-archive/)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




