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
# <a name="about-the-windows-core-audio-apis"></a>Acerca de las API de audio de Windows Core

En esta documentación se proporciona información sobre las API de audio principales para la familia de sistemas operativos Microsoft Windows.

Las API de audio principales se introdujeron en Windows Vista. Se trata de un nuevo conjunto de componentes de audio de modo de usuario que proporciona a las aplicaciones cliente capacidades de audio mejoradas. Entre estas funcionalidades se incluyen las siguientes:

-   Transmisión por secuencias de audio de baja latencia y resistente a problemas.
-   Confiabilidad mejorada (muchas funciones de audio se han pasado del modo kernel al modo de usuario).
-   Seguridad mejorada (el procesamiento del contenido de audio protegido se realiza en un proceso seguro y con privilegios reducidos).
-   Asignación de roles en todo el sistema (consola, multimedia y comunicaciones) en dispositivos de audio individuales.
-   Abstracción de software de los dispositivos de punto de conexión de audio (por ejemplo, altavoces, auriculares y micrófonos) que el usuario manipula directamente.

Las API de audio principales se han mejorado en Windows 7. Para obtener más información acerca de las mejoras y las nuevas características agregadas, consulte [novedades de las API de audio principales en Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

En esta documentación se describen las API de audio principales. Estas API sirven como base para las siguientes API de nivel superior:

-   DirectSound
-   DirectMusic
-   Funciones **waveXxx** y **mixerXxx** multimedia de Windows
-   Media Foundation

Estas API de nivel superior usan las API de audio principales para compartir el acceso a los dispositivos de audio. Media Foundation es nuevo en Windows Vista, mientras que las funciones DirectSound, DirectMusic y **waveXxx** y **mixerXxx** se admiten en Windows 98, Windows Millennium Edition y en Windows 2000 y versiones posteriores.

La mayoría de las aplicaciones de audio se comunican con las API de nivel superior en lugar de comunicarse directamente con las API de audio principales. Algunos ejemplos de aplicaciones que usan API de nivel superior son:

-   Instancias de Media Player
-   Reproductores de DVD
-   Juegos
-   Aplicaciones empresariales, como Microsoft Office PowerPoint, que reproducen archivos de sonido

Normalmente, estas aplicaciones se comunican con las API de DirectSound o Media Foundation.

Es posible que la comunicación directa con las API de audio principales no sea adecuada para muchas aplicaciones de audio de uso general. Por ejemplo, las API de audio principales requieren secuencias de audio para usar los formatos de datos nativos de un dispositivo de audio. Sin embargo, es posible que los desarrolladores de software de terceros que desarrollan los siguientes tipos de productos necesiten las funcionalidades especiales de las API de audio principales:

-   Aplicaciones de audio profesional ("audio de Pro")
-   Aplicaciones RTC (comunicación en tiempo real)
-   API de audio de terceros

Una aplicación de "audio de Pro" o RTC puede necesitar acceso directo a las características de bajo nivel de las API de audio principales para lograr una latencia mínima al obtener acceso exclusivo al hardware de audio. Una API de audio de terceros podría requerir acceso directo a las API de audio principales para implementar un conjunto de características que es posible que no sean totalmente compatibles con ninguna de las API de audio de alto nivel que se suministran con Windows.

Una aplicación que usa una API de audio heredada para reproducir o grabar audio podría requerir funcionalidades adicionales que no son compatibles con la API de audio heredada, pero que son compatibles con las API de audio principales. En muchos casos, la aplicación puede acceder a estas funcionalidades directamente a través de las API de audio principales, que se pueden usar junto con la API de audio heredada.

Las API de audio principales son:

-   [API de dispositivo multimedia (MMDevice)](mmdevice-api.md). Los clientes usan esta API para enumerar los dispositivos de punto de conexión de audio en el sistema.
-   [API de sesión de audio de Windows (WASAPI)](wasapi.md). Los clientes usan esta API para crear y administrar secuencias de audio hacia y desde dispositivos de punto de conexión de audio.
-   [API de DeviceTopology](devicetopology-api.md). Los clientes usan esta API para acceder directamente a las características topológicas (por ejemplo, controles de volumen y multiplexores) que se encuentran a lo largo de las rutas de acceso de datos dentro de los dispositivos de hardware de los adaptadores de audio.
-   [API de EndpointVolume](endpointvolume-api.md). Los clientes usan esta API para acceder directamente a los controles de volumen en los dispositivos de punto de conexión de audio. Esta API la usan principalmente las aplicaciones que administran secuencias de audio en modo exclusivo.

Estas API admiten la noción fácil de utilizar de un dispositivo de punto de conexión, que se describe en [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).

Microsoft no planea que las API de audio principales que se describen aquí estén disponibles para su uso con versiones anteriores de Windows, incluidas Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 y Windows 98.

Esta información general contiene los siguientes temas.



| **Tema.**                                                                                      | **Descripción**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Novedades de las API de audio principales en Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Resume las nuevas características y las mejoras de las API de audio principales                   |
| [Archivos de encabezado y componentes del sistema](header-files-and-system-components.md)                   | Describe los archivos de encabezado y los componentes del sistema para las API de audio principales.                 |
| [Ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md)       | Enumera los ejemplos de la Windows SDK que usan las API de audio principales.                        |




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de audio principales](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



