---
description: Acerca de Windows Core Audio API
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Acerca de Windows Core Audio API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165166"
---
# <a name="about-the-windows-core-audio-apis"></a>Acerca de Windows Core Audio API

En esta documentación se proporciona información sobre core audio API para la familia Windows de sistemas operativos de Microsoft.

Las API de audio principales se introdujeron en Windows Vista. Se trata de un nuevo conjunto de componentes de audio en modo de usuario que proporciona a las aplicaciones cliente funcionalidades de audio mejoradas. Estas funcionalidades incluyen lo siguiente:

-   Streaming de audio de baja latencia y resistente a problemas.
-   Confiabilidad mejorada (muchas funciones de audio han pasado del modo kernel al modo de usuario).
-   Seguridad mejorada (el procesamiento del contenido de audio protegido tiene lugar en un proceso seguro con menos privilegios).
-   Asignación de roles específicos de todo el sistema (consola, multimedia y comunicaciones) a dispositivos de audio individuales.
-   Abstracción de software de los dispositivos de punto de conexión de audio (por ejemplo, altavoces, cascos y micrófonos) que el usuario manipula directamente.

Las API de audio principales se han mejorado en Windows 7. Para obtener más información sobre las mejoras y las nuevas características agregadas, vea Novedades de las API de audio principales [en Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

En esta documentación se describen las API de audio principales. Estas API sirven como base para las siguientes API de nivel superior:

-   DirectSound
-   Directmusic
-   Windows funciones **waveXxx** y **mixerXxx** multimedia
-   Media Foundation

Estas API de nivel superior usan las API de audio principal para compartir el acceso a los dispositivos de audio. Media Foundation es una novedad de Windows Vista, mientras que DirectSound, DirectXxx y las funciones **waveXxx** y **mixerXxx** se admiten en Windows 98, Windows Millennium Edition y en Windows 2000 y versiones posteriores.

La mayoría de las aplicaciones de audio se comunican con las API de nivel superior en lugar de comunicarse directamente con las API de audio principal. Algunos ejemplos de aplicaciones que usan API de nivel superior son:

-   Instancias de Media Player
-   Reproductores de DVD
-   Juegos
-   Aplicaciones empresariales, como Microsoft Office PowerPoint, que reproducen archivos de sonido

Normalmente, estas aplicaciones se comunican con DirectSound o Media Foundation API.

Es posible que la comunicación directa con las API de audio principal no sea adecuada para muchas aplicaciones de audio de uso general. Por ejemplo, las API de audio principal requieren secuencias de audio para usar los formatos de datos nativos de un dispositivo de audio. Sin embargo, los desarrolladores de software de terceros que desarrollan los siguientes tipos de productos pueden requerir las funcionalidades especiales de las API de audio principales:

-   Professional de audio ("audio pro")
-   Aplicaciones de comunicación en tiempo real (RTC)
-   API de audio de terceros

Una aplicación de "audio pro" o RTC podría necesitar acceso directo a las características de bajo nivel de las API de audio principal para lograr una latencia mínima al obtener acceso exclusivo al hardware de audio. Una API de audio de terceros podría requerir acceso directo a core Audio API para implementar un conjunto de características que podrían no ser totalmente compatibles con ninguna API de audio de alto nivel que se suministra con Windows.

Una aplicación que usa una API de audio heredada para reproducir o grabar audio puede requerir funcionalidades adicionales que no son compatibles con la API de audio heredada, pero que son compatibles con las API de audio principal. En muchos casos, la aplicación puede acceder a estas funcionalidades directamente a través de las API de audio principal, que se pueden usar junto con la API de audio heredada.

Las API de audio principales son:

-   [API de dispositivo multimedia (MMDevice).](mmdevice-api.md) Los clientes usan esta API para enumerar los dispositivos de punto de conexión de audio en el sistema.
-   [Windows Audio Session API (WASAPI).](wasapi.md) Los clientes usan esta API para crear y administrar secuencias de audio hacia y desde dispositivos de punto de conexión de audio.
-   [DeviceTopology API](devicetopology-api.md). Los clientes usan esta API para acceder directamente a las características topológicas (por ejemplo, controles de volumen y multiplexores) que se encuentran a lo largo de las rutas de acceso de datos dentro de dispositivos de hardware en adaptadores de audio.
-   [EndpointVolume API](endpointvolume-api.md). Los clientes usan esta API para acceder directamente a los controles de volumen en dispositivos de punto de conexión de audio. Esta API la usan principalmente las aplicaciones que administran secuencias de audio en modo exclusivo.

Estas API admiten la noción fácil de usar de un dispositivo de punto de conexión, que se describe en [Dispositivos](audio-endpoint-devices.md)de punto de conexión de audio .

Microsoft no planea que las API de audio principales que se describen aquí estén disponibles para su uso con versiones anteriores de Windows, como Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 y Windows 98.

Esta información general contiene los temas siguientes.



| **Tema.**                                                                                      | **Descripción**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Novedades de las API de audio principales en Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Resume las nuevas características y las mejoras de las API de audio principal.                   |
| [Archivos de encabezado y componentes del sistema](header-files-and-system-components.md)                   | Describe los archivos de encabezado y los componentes del sistema para core Audio API.                 |
| [Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)       | Enumera los ejemplos del SDK Windows que usan core audio API.                        |




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de audio principal](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



