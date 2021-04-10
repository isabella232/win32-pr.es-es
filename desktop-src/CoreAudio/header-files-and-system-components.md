---
description: Archivos de encabezado y componentes del sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Archivos de encabezado y componentes del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153407"
---
# <a name="header-files-and-system-components"></a>Archivos de encabezado y componentes del sistema

En la tabla siguiente se enumeran los archivos de encabezado que contienen las definiciones de interfaz para los cuatro componentes de audio principales.



|                                              |                              |
|----------------------------------------------|------------------------------|
| Componente de audio principal                         | Archivo de encabezado                  |
| [API de MMDevice](mmdevice-api.md)             | Mmdeviceapi. h                |
| [WASAPI](wasapi.md)                         | Audioclient. h, Audiopolicy. h |
| [API de DeviceTopology](devicetopology-api.md) | Devicetopology. h             |
| [API de EndpointVolume](endpointvolume-api.md) | Endpointvolume. h             |



 

Otro archivo de encabezado, Audiosessiontypes. h, define las constantes que usa WASAPI. Estos archivos de encabezado se encuentran en el directorio% MSSdk% \\ include, donde% MSSdk% es el directorio raíz de la instalación de Windows SDK en el equipo.

Cada API de la tabla anterior consta de un conjunto de interfaces COM relacionadas. Dado que algunos aspectos del streaming de audio dependen de la baja latencia y la sincronización precisa, las implementaciones de las API MMDevice, WASAPI, DeviceTopology y EndpointVolume no usan el marco de Microsoft .NET o el entorno de ejecución administrado.

Las API de audio principales se implementan en los componentes del sistema de modo usuario Audioses.dll y Mmdevapi.dll. Las aplicaciones cliente no tienen acceso directamente a los puntos de entrada de estos archivos dll. En su lugar, los clientes llaman a la función **CoCreateInstance** o **CoCreateInstanceEx** para obtener la interfaz [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) del objeto de la clase MMDeviceEnumerator. Este objeto enumera los [dispositivos de punto de conexión de audio](audio-endpoint-devices.md) en el sistema. La interfaz de **IMMDeviceEnumerator** forma parte de la API de MMDevice. Desde esta interfaz, los clientes pueden obtener directa o indirectamente las demás interfaces de la API de MMDevice, incluida la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . **IMMDevice** representa un dispositivo de punto de conexión de audio determinado. A través de **IMMDevice**, los clientes pueden obtener directa o indirectamente las interfaces específicas del dispositivo en WASAPI, la API de DeviceTopology y la API de EndpointVolume. Para obtener más información sobre **CoCreateInstance** y **CoCreateInstanceEx**, consulte la documentación de Windows SDK. Para obtener más información sobre el acceso a las interfaces en las API de audio principales, consulte [enumeración de dispositivos de audio](enumerating-audio-devices.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las API de audio de Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



