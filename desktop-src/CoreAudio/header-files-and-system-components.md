---
description: Archivos de encabezado y componentes del sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Archivos de encabezado y componentes del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 794f7a6947b5af2756676cf7b02dc34da1da1a0ad99dc4642e8ae3db3876d360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079835"
---
# <a name="header-files-and-system-components"></a>Archivos de encabezado y componentes del sistema

En la tabla siguiente se enumeran los archivos de encabezado que contienen las definiciones de interfaz para los cuatro componentes de Core Audio.



| Componente de audio principal                         | Archivo de encabezado                  |
|----------------------------------------------|------------------------------|
| [MMDevice API](mmdevice-api.md)             | Mmdeviceapi.h                |
| [WASAPI](wasapi.md)                         | Audioclient.h, Audiopolicy.h |
| [DeviceTopology API](devicetopology-api.md) | Devicetopology.h             |
| [EndpointVolume API](endpointvolume-api.md) | Endpointvolume.h             |



 

Otro archivo de encabezado, Audiosessiontypes.h, define las constantes usadas por WASAPI. Estos archivos de encabezado se encuentran en el directorio %MSSdk% include, donde %MSSdk% es el directorio raíz de la instalación del SDK de Windows en \\ el equipo.

Cada API de la tabla anterior consta de un conjunto de interfaces COM relacionadas. Dado que algunos aspectos del streaming de audio dependen de una latencia baja y de una sincronización precisa, las implementaciones de las API MMDevice, WASAPI, DeviceTopology y EndpointVolume no usan el entorno de ejecución administrada o de microsoft .NET Framework.

Las API de audio principal se implementan en los componentes del sistema en modo de usuario Audioses.dll y Mmdevapi.dll. Las aplicaciones cliente no acceden directamente a los puntos de entrada de estos archivos DLL. En su lugar, los clientes llaman a las funciones **CoCreateInstance** o **CoCreateInstanceEx** para obtener la [**interfaz IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) del objeto de clase MMDeviceEnumerator. Este objeto enumera los dispositivos de [punto de conexión de audio](audio-endpoint-devices.md) en el sistema. La **interfaz IMMDeviceEnumerator** forma parte de MMDevice API. Desde esta interfaz, los clientes pueden obtener directa o indirectamente las demás interfaces de LA API MMDevice, incluida [**la interfaz IMMDevice.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) **IMMDevice representa** un dispositivo de punto de conexión de audio determinado. A **través de IMMDevice**, los clientes pueden obtener directa o indirectamente las interfaces específicas del dispositivo en WASAPI, DeviceTopology API y EndpointVolume API. Para obtener más información sobre **CoCreateInstance** y **CoCreateInstanceEx,** consulte la documentación Windows SDK. Para obtener más información sobre cómo acceder a las interfaces de las API de audio principales, vea [Enumerating Audio Devices](enumerating-audio-devices.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



