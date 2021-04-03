---
description: User-Mode componentes de audio
ms.assetid: b240b629-5bb6-4b07-95be-8ca5a14a3567
title: User-Mode componentes de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18715db2d32be3c4a70182571028acbfca411539
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907312"
---
# <a name="user-mode-audio-components"></a>User-Mode componentes de audio

En Windows Vista, las API de audio principales sirven como base del subsistema de audio de modo usuario. Las API de audio principales se implementan como una capa fina de componentes del sistema en modo de usuario que separan los clientes de modo de usuario de los controladores de audio de modo kernel y el hardware de audio. Las API de audio de nivel superior, como DirectSound y las funciones multimedia de Windows, acceden a los dispositivos de audio a través de las API de audio principales. Además, algunas aplicaciones de audio se comunican directamente con las API de audio principales.

Las API de audio principales admiten la noción fácil de utilizar de un dispositivo de punto de conexión de audio. Un dispositivo de punto de conexión de audio es una abstracción de software que representa un dispositivo físico que el usuario manipula directamente. Algunos ejemplos de dispositivos de punto de conexión de audio son los altavoces, los auriculares y los micrófonos. Para obtener más información, vea [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).

En el diagrama siguiente se muestran las API de audio principales y su relación con los demás componentes de audio de modo de usuario de Windows Vista.

![diagrama de componentes de representación de audio de modo de usuario](images/fig1.jpg)

Para simplificar, en el diagrama anterior solo se muestra una ruta de acceso de datos de representación de audio al dispositivo de extremo; el diagrama no muestra una ruta de acceso de datos de captura de audio. Las API de audio principales incluyen [MMDEVICE API](mmdevice-api.md), [WASAPI](wasapi.md), [DeviceTopology API](devicetopology-api.md)y [EndpointVolume API](endpointvolume-api.md), que se implementan en los módulos del sistema de modo usuario Audioses.dll y Mmdevapi.dll.

Como se muestra en el diagrama anterior, las API de audio principales proporcionan una base para las siguientes API de nivel superior:

-   Media Foundation
-   Funciones **waveXxx** y **mixerXxx** multimedia de Windows
-   DirectSound
-   DirectMusic

DirectSound, las funciones de audio multimedia de Windows y Media Foundation (a través de su representador de audio de streaming, o el componente SAR) se comunican directamente con las API de audio principales. DirectMusic se comunica indirectamente con las API de audio principales a través de DirectSound.

Un cliente de WASAPI pasa los datos a un dispositivo de punto de conexión a través de un *búfer de extremo*. Los componentes de software y hardware del sistema administran el movimiento de datos desde el búfer del extremo al dispositivo de extremo de una manera muy transparente para el cliente. Además, para un dispositivo de extremo que se conecta a un adaptador de audio con la detección de la presencia de conector, el cliente puede crear un búfer de extremo solo para un dispositivo de extremo que está presente físicamente. Para obtener más información sobre la detección de la presencia de tomas, consulte [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).

En el diagrama anterior se muestran dos tipos de búfer de extremo. Si un cliente de WASAPI abre una secuencia en *modo compartido*, el cliente escribe datos de audio en el búfer del extremo y el motor de audio de Windows Lee los datos del búfer. En este modo, el cliente comparte el hardware de audio con otras aplicaciones que se ejecutan en otros procesos. El motor de audio mezcla los flujos de estas aplicaciones y reproduce la combinación resultante a través del hardware. El motor de audio es un componente del sistema de modo de usuario (Audiodg.dll) que realiza todas las operaciones de procesamiento de secuencias en el software. Por el contrario, si un cliente abre una secuencia en *modo exclusivo*, el cliente tiene acceso exclusivo al hardware de audio. Normalmente, solo un pequeño número de aplicaciones de "Audio Pro" o RTC requiere el modo exclusivo. Aunque el diagrama muestra los flujos en modo compartido y en modo exclusivo, solo uno de estos dos flujos (y su búfer de extremo correspondiente) existe, dependiendo de si el cliente abre la secuencia en modo compartido o en modo exclusivo.

En el modo exclusivo, el cliente puede optar por abrir la secuencia en cualquier formato de audio que admita el dispositivo de extremo. En el modo compartido, el cliente debe abrir la secuencia en el formato de combinación que el motor de audio usa actualmente (o un formato similar al formato de combinación). Los flujos de entrada del motor de audio y la combinación de salida del motor se encuentran en este formato.

En Windows 7, se ha agregado una nueva característica denominada *modo Low-latence* para las secuencias en modo de uso compartido. En este modo, el motor de audio se ejecuta en modo de extracción, en el que hay una reducción significativa de la latencia. Esto es muy útil para las aplicaciones de comunicación que requieren una baja latencia de secuencia de audio para una transmisión por secuencias más rápida.

Las aplicaciones que administran secuencias de audio de baja latencia pueden usar el servicio Programador de clases multimedia (MMCSS) en Windows Vista para aumentar la prioridad de los subprocesos de aplicación que acceden a los búferes de extremo. MMCSS permite que las aplicaciones de audio se ejecuten con alta prioridad sin denegar recursos de CPU a las aplicaciones de menor prioridad. MMCSS asigna una prioridad a un subproceso en función del nombre de la tarea. Por ejemplo, Windows Vista admite los nombres de tarea "audio" y "Audio Pro" para los subprocesos que administran secuencias de audio. De forma predeterminada, la prioridad de un subproceso de "audio de Pro" es mayor que la de un subproceso de "audio". Para obtener más información acerca de MMCSS, consulte la documentación de Windows SDK.

Las API de audio principales admiten formatos de secuencias PCM y no PCM. Sin embargo, el motor de audio solo puede mezclar flujos PCM. Por lo tanto, solo los flujos de modo exclusivo pueden tener formatos que no sean PCM. Para obtener más información, vea [formatos de dispositivo](device-formats.md).

El motor de audio se ejecuta en su propio proceso protegido, que es independiente del proceso en el que se ejecuta la aplicación. Para admitir una secuencia en modo compartido, el servicio audio de Windows (el cuadro con la etiqueta "servicio de audio" en el diagrama anterior) asigna un búfer de extremo entre procesos que es accesible tanto para la aplicación como para el motor de audio. En el modo exclusivo, el búfer del extremo reside en la memoria que es accesible tanto para la aplicación como para el hardware de audio.

El servicio audio de Windows es el módulo que implementa la Directiva de audio de Windows. La Directiva de audio es un conjunto de reglas internas que el sistema aplica a las interacciones entre flujos de audio de varias aplicaciones que comparten y compiten por el uso del mismo hardware de audio. El servicio audio de Windows implementa la Directiva de audio mediante el establecimiento de los parámetros de control del motor de audio. Entre las tareas del servicio de audio se incluyen las siguientes:

-   Seguimiento de los dispositivos de audio que el usuario agrega o quita del sistema.
-   La supervisión de los roles que se asignan a los dispositivos de audio en el sistema.
-   Administrar secuencias de audio de grupos de tareas que generan clases similares de contenido de audio (consola, multimedia y comunicaciones).
-   Controlar el nivel de volumen del flujo de salida combinado ("submezcla") para cada uno de los distintos tipos de contenido de audio.
-   Informar al motor de audio sobre los elementos de procesamiento en las rutas de acceso de datos para las secuencias de audio.

En algunas versiones de Windows, el servicio audio de Windows está deshabilitado de forma predeterminada y se debe activar explícitamente antes de que el sistema pueda reproducir audio.

En el ejemplo que se muestra en el diagrama anterior, el dispositivo de extremo es un conjunto de oradores que están conectados al adaptador de audio. La aplicación cliente escribe datos de audio en el búfer del extremo y el motor de audio controla los detalles de transporte de los datos del búfer al dispositivo de extremo.

El cuadro con la etiqueta "controlador de audio" en el diagrama anterior puede ser una combinación de componentes de controladores proporcionados por el sistema y proporcionados por el proveedor. En el caso de un adaptador de audio en un bus PCI o PCI Express, el sistema suministra el controlador del sistema de clase de puerto (Portcls.sys), que implementa un conjunto de controladores de puerto para las distintas funciones de audio del adaptador, y el proveedor de hardware proporciona un controlador de adaptador que implementa un conjunto de controladores de minipuerto para controlar las operaciones específicas del dispositivo para los controladores de puerto. En el caso de un controlador y un códec de audio de alta definición en un bus PCI o PCI Express, el sistema suministra el controlador del adaptador (Hdaudio.sys) y no se necesita ningún controlador proporcionado por el proveedor. En el caso de un adaptador de audio en un bus USB, el sistema suministra el controlador del sistema de clase AVStream (Ks.sys) más el controlador de audio USB (Usbaudio.sys); de nuevo, no se necesita ningún controlador proporcionado por el proveedor.

Para simplificar, el diagrama anterior muestra solo las secuencias de representación. Sin embargo, las API de audio principales también admiten secuencias de captura. En el modo compartido, varios clientes pueden compartir el flujo capturado desde un dispositivo de hardware de audio. En el modo exclusivo, un cliente tiene acceso exclusivo al flujo capturado desde el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación](programming-guide.md)
</dt> </dl>

 

 



