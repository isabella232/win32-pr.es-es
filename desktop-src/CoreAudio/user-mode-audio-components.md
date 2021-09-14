---
description: User-Mode componentes de audio
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode componentes de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164778"
---
# <a name="user-mode-audio-components"></a>User-Mode componentes de audio

En Windows Vista, las API de audio principales sirven como base del subsistema de audio en modo de usuario. Las API de audio principales se implementan como una capa fina de componentes del sistema en modo de usuario que separan los clientes en modo de usuario de los controladores de audio en modo kernel y el hardware de audio. Las API de audio de nivel superior, como Direct Sound y las Windows multimedia, acceden a los dispositivos de audio a través de las API de audio principales. Además, algunas aplicaciones de audio se comunican directamente con las API de audio principales.

Las API de audio principales admiten la noción fácil de usar de un dispositivo de punto de conexión de audio. Un dispositivo de punto de conexión de audio es una abstracción de software que representa un dispositivo físico que el usuario manipula directamente. Algunos ejemplos de dispositivos de punto de conexión de audio son altavoces, auriculares y micrófonos. Para obtener más información, vea [Dispositivos de punto de conexión de audio.](audio-endpoint-devices.md)

En el diagrama siguiente se muestran las API de audio principales y su relación con los demás componentes de audio en modo de usuario Windows Vista.

![diagrama de componentes de representación de audio en modo de usuario](images/fig1.jpg)

Por motivos de simplicidad, el diagrama anterior muestra solo una ruta de acceso de datos de representación de audio al dispositivo del punto de conexión: el diagrama no muestra una ruta de acceso de datos de captura de audio. Las API de audio principales incluyen [MMDevice API,](mmdevice-api.md) [WASAPI,](wasapi.md) [DeviceTopology API](devicetopology-api.md)y [EndpointVolume API,](endpointvolume-api.md)que se implementan en los módulos del sistema en modo de usuario Audioses.dll y Mmdevapi.dll.

Como se muestra en el diagrama anterior, las API de audio principales proporcionan una base para las siguientes API de nivel superior:

-   Media Foundation
-   Windows funciones **waveXxx** y **mixerXxx** multimedia
-   DirectSound
-   Directmusic

Direct Sound, el Windows funciones de audio multimedia y Media Foundation (a través de su representador de audio de streaming o el componente SAR) se comunican directamente con las API de audio principales. DirectDirectamente se comunica con las API de audio principales indirectamente a través de Direct Sound.

Un cliente de WASAPI pasa datos a un dispositivo de punto de conexión a través de un búfer *de punto de conexión.* Los componentes de hardware y software del sistema administran el movimiento de datos desde el búfer del punto de conexión al dispositivo del punto de conexión de una manera que es en gran medida transparente para el cliente. Además, para un dispositivo de punto de conexión que se conecta a un adaptador de audio con detección de presencia de conector, el cliente puede crear un búfer de punto de conexión solo para un dispositivo de punto de conexión que esté físicamente presente. Para obtener más información sobre la detección de presencia de conectores, vea [Dispositivos de punto de conexión de audio.](audio-endpoint-devices.md)

En el diagrama anterior se muestran dos tipos de búfer de punto de conexión. Si un cliente de WASAPI abre una secuencia en modo compartido *,* el cliente escribe datos de audio en el búfer del punto de conexión y el motor de audio Windows lee los datos del búfer. En este modo, el cliente comparte el hardware de audio con otras aplicaciones que se ejecutan en otros procesos. El motor de audio mezcla las secuencias de estas aplicaciones y reproduce la combinación resultante a través del hardware. El motor de audio es un componente del sistema en modo de usuario (Audiodg.dll) que realiza todas sus operaciones de procesamiento de flujos en software. Por el contrario, si un cliente abre una secuencia en *modo exclusivo*, el cliente tiene acceso exclusivo al hardware de audio. Normalmente, solo un pequeño número de aplicaciones de "audio pro" o RTC requieren el modo exclusivo. Aunque el diagrama muestra las secuencias en modo compartido y en modo exclusivo, solo existe una de estas dos secuencias (y su búfer de punto de conexión correspondiente), dependiendo de si el cliente abre la secuencia en modo compartido o en modo exclusivo.

En modo exclusivo, el cliente puede elegir abrir la secuencia en cualquier formato de audio que admita el dispositivo de punto de conexión. En modo compartido, el cliente debe abrir la secuencia en el formato de combinación que usa actualmente el motor de audio (o un formato similar al formato de combinación). Los flujos de entrada del motor de audio y la combinación de salidas del motor están en este formato.

En Windows 7, se ha  agregado una nueva característica denominada modo de baja demora para secuencias en modo de recurso compartido. En este modo, el motor de audio se ejecuta en modo de extracción, en el que hay una reducción significativa de la latencia. Esto es muy útil para las aplicaciones de comunicación que requieren una latencia de secuencia de audio baja para un streaming más rápido.

Las aplicaciones que administran secuencias de audio de baja latencia pueden usar el servicio Programador de clases multimedia (MMCSS) en Windows Vista para aumentar la prioridad de los subprocesos de aplicación que acceden a los búferes de punto de conexión. MMCSS permite que las aplicaciones de audio se ejecuten con prioridad alta sin denegar los recursos de CPU a las aplicaciones de prioridad inferior. MMCSS asigna una prioridad a un subproceso en función de su nombre de tarea. Por ejemplo, Windows Vista admite los nombres de tarea "Audio" y "Pro Audio" para los subprocesos que administran secuencias de audio. De forma predeterminada, la prioridad de un subproceso "Pro Audio" es mayor que la de un subproceso "Audio". Para más información sobre MMCSS, consulte la documentación Windows SDK.

Las API de audio principales admiten formatos de secuencia pcm y no PCM. Sin embargo, el motor de audio solo puede mezclar secuencias PCM. Por lo tanto, solo las secuencias en modo exclusivo pueden tener formatos que no son PCM. Para obtener más información, vea [Formatos de dispositivo.](device-formats.md)

El motor de audio se ejecuta en su propio proceso protegido, que es independiente del proceso en el que se ejecuta la aplicación. Para admitir una secuencia en modo compartido, el servicio de audio de Windows (el cuadro con la etiqueta "Servicio de audio" en el diagrama anterior) asigna un búfer de punto de conexión entre procesos al que pueden acceder tanto la aplicación como el motor de audio. Para el modo exclusivo, el búfer del punto de conexión reside en la memoria que es accesible tanto para la aplicación como para el hardware de audio.

El Windows de audio es el módulo que implementa Windows directiva de audio. La directiva de audio es un conjunto de reglas internas que el sistema aplica a las interacciones entre secuencias de audio de varias aplicaciones que comparten y compiten por el uso del mismo hardware de audio. El Windows servicio de audio implementa la directiva de audio estableciendo los parámetros de control para el motor de audio. Las tareas del servicio de audio incluyen:

-   Realizar un seguimiento de los dispositivos de audio que el usuario agrega o quita del sistema.
-   Supervisar los roles asignados a los dispositivos de audio del sistema.
-   Administrar las secuencias de audio de grupos de tareas que generan clases similares de contenido de audio (consola, multimedia y comunicaciones).
-   Controlar el nivel de volumen del flujo de salida combinado ("submezcla") para cada uno de los distintos tipos de contenido de audio.
-   Informar al motor de audio sobre los elementos de procesamiento en las rutas de acceso de datos para las secuencias de audio.

En algunas versiones de Windows, el servicio de audio Windows está deshabilitado de forma predeterminada y debe estar activado explícitamente antes de que el sistema pueda reproducir audio.

En el ejemplo que se muestra en el diagrama anterior, el dispositivo de punto de conexión es un conjunto de altavoces que están conectados al adaptador de audio. La aplicación cliente escribe datos de audio en el búfer del punto de conexión y el motor de audio controla los detalles de transporte de los datos del búfer al dispositivo del punto de conexión.

El cuadro con la etiqueta "Controlador de audio" en el diagrama anterior podría ser una combinación de componentes de controladores proporcionados por el sistema y proporcionados por el proveedor. En el caso de un adaptador de audio en un bus PCI o PCI Express, el sistema proporciona el controlador del sistema de clase de puerto (Portcls.sys), que implementa un conjunto de controladores de puerto para las distintas funciones de audio del adaptador, y el proveedor de hardware proporciona un controlador de adaptador que implementa un conjunto de controladores de miniportador para controlar las operaciones específicas del dispositivo para los controladores de puerto. En el caso de un códec y un controlador de audio de alta definición en un bus PCI o PCI Express, el sistema proporciona el controlador del adaptador (Hdaudio.sys) y no se necesita ningún controlador proporcionado por el proveedor. En el caso de un adaptador de audio en un bus USB, el sistema proporciona el controlador de sistema de clase AVStream (Ks.sys) más el controlador de audio USB (Usbaudio.sys); de nuevo, no se necesita ningún controlador proporcionado por el proveedor.

Por motivos de simplicidad, en el diagrama anterior solo se muestran secuencias de representación. Sin embargo, las API de audio principales también admiten secuencias de captura. En modo compartido, varios clientes pueden compartir la secuencia capturada desde un dispositivo de hardware de audio. En modo exclusivo, un cliente tiene acceso exclusivo a la secuencia capturada desde el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



