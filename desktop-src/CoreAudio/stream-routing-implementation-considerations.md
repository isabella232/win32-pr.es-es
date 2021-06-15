---
description: Obtenga información sobre las consideraciones de implementación para el enrutamiento de flujos. Las API implementan el enrutamiento de flujos controlando el cambio de secuencia a un nuevo punto de conexión de audio predeterminado.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Consideraciones sobre la implementación del enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd753fe027c92ffac9f5a41cea589b600d7f26
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068041"
---
# <a name="stream-routing-implementation-considerations"></a>Consideraciones sobre la implementación del enrutamiento de flujos

En Windows 7, las API de plataforma de alto nivel que usan las API de audio principal, como las API de Media Foundation, Direct Sound y Wave, implementan la característica de enrutamiento de flujos controlando el cambio de flujo de un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API usan el comportamiento de enrutamiento de flujos sin modificaciones en el origen. Los clientes WASAPI directos pueden usar las notificaciones enviadas por los componentes de Core Audio e implementar la característica de enrutamiento de secuencias.

Los clientes WASAPI directos (aplicaciones multimedia que usan WASAPI directamente) reciben nuevas notificaciones de sesión de audio y dispositivo enviadas por los componentes de Audio principal. El comportamiento de la característica de enrutamiento de flujos se define mediante la forma en que la aplicación controla estas notificaciones.

MMDevice API y la sesión de audio envían notificaciones sobre los cambios de estado del dispositivo y los cambios de sesión a los clientes WASAPI en forma de devoluciones de llamada. Para obtener estas notificaciones, el cliente debe registrar su implementación de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Para obtener más información, vea [Notificaciones pertinentes para el enrutamiento de secuencias.](relevant-device-notifications-for-stream-routing.md)

En el escenario de casco USB descrito en [Stream Routing](stream-routing.md), una aplicación reproduce una secuencia de audio y usa MMDeviceAPI y WASAPI para representar la secuencia en el dispositivo de representación predeterminado, **Speaker**. Cuando se cambia el dispositivo predeterminado, la aplicación recibe una [**notificación IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) La aplicación también recibe notificaciones [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) que indican que el usuario quitó el dispositivo de punto de conexión de audio o que el formato de secuencia cambió para el dispositivo al que está conectada la sesión de audio. Tras recibir las notificaciones, la aplicación deja de transmitir al punto de conexión del hablante y vuelve a abrir la secuencia para representarla en el punto de conexión predeterminado actual, el casco.

![diagrama de flujo de datos para notificaciones de dispositivos.](images/stream-routing.gif)

En respuesta a estas notificaciones, el cliente podría volver a abrir la secuencia en el nuevo dispositivo predeterminado con el nuevo formato seleccionado por el usuario.

## <a name="stream-managment"></a>Stream Managment

En la lista siguiente se resumen los pasos que debe realizar un cliente WASAPI para proporcionar la funcionalidad de conmutación de flujo.

1.  Espere a la notificación [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) pertinente. Si el dispositivo es el predeterminado, se recibe la notificación [**IMMNotificationClient::OnDefaultDeviceChanged.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged)
2.  Si hay un nuevo dispositivo disponible, obtenga una referencia al punto de conexión del nuevo dispositivo. Llame [**a IMMDeviceEnumerator::GetDefaultAudioEndpoint para**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) el nuevo dispositivo predeterminado. Si el nuevo dispositivo no es el predeterminado, puede recuperarlo llamando a [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Para obtener más información, vea [Getting the Device Endpoint for Stream Routing](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Espere a [**IAudioSessionEvents::OnSessionDisconnected con**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) el valor de motivo.
    > [!Note]  
    > Dado que todas estas operaciones son asócronas, no se puede predecir el orden en el que la aplicación recibe notificaciones de cambio de dispositivo y de desconexión de sesión. La aplicación debe implementar el control de notificaciones para recibir estas notificaciones en cualquier orden. Sin embargo, normalmente, la aplicación recibe el **valor AudioSessionDisconnect** antes de la notificación de cambio de dispositivo predeterminada.

     

4.  Evalúe el valor de motivo y determine si la secuencia debe transferirse a otro punto de conexión de audio o si la secuencia debe reinicializarse con un nuevo formato.
5.  Detenga el streaming al dispositivo predeterminado anterior si el motivo indica que la secuencia se debe volver a enrutar al nuevo dispositivo predeterminado.
6.  Realizar cálculos de asignación de posición.
7.  Abra la secuencia en el nuevo dispositivo y transfiera toda la información de estado.
8.  Reanude el streaming en el nuevo dispositivo predeterminado.
9.  Controlar la salida del dispositivo predeterminado anterior.

Para que la operación de conmutación de flujo parezca perfecta, debe realizarse lo más rápido posible. Esto depende del rendimiento de los componentes implicados en la nueva iniciación de la secuencia en el nuevo dispositivo.

## <a name="position-mapping-considerations"></a>Consideraciones sobre la asignación de posiciones

Cuando la aplicación obtiene [**notificaciones IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) [**e IAudioSessionEvents,**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) puede enrutar las secuencias existentes al nuevo dispositivo predeterminado. Cuando una secuencia de audio existente se interrumpe y se abre en el nuevo dispositivo, la representación en el nuevo dispositivo debe comenzar en la posición en la que se detuvo la secuencia en el dispositivo antiguo. Para ello, la aplicación debe tener la última posición conocida del dispositivo para calcular la posición inicial en el nuevo dispositivo. Por ejemplo, esta posición se puede usar como desplazamiento delta para la asignación de posición posterior. Cuando la secuencia comienza a representarse, la nueva posición del dispositivo se puede volver a colocar en la posición del dispositivo almacenado en caché.

En los pasos siguientes se resume el proceso de realizar una transición de flujo sin problemas.

1.  Almacenar en caché la última posición del dispositivo de la secuencia en el dispositivo antiguo.
2.  Detenga la secuencia en el dispositivo antiguo.
3.  Realice cálculos de remapping para obtener la nueva posición.
4.  Comience a representar la secuencia en el nuevo dispositivo.
5.  Libere la secuencia anterior.

Durante la transición, la aplicación debe asegurarse de que el reloj no salga de la sincronización, lo que da lugar a secuencias de audio y vídeo no sincronizadas. Esto puede ocurrir si los ejemplos de vídeo se siguen representando mientras la secuencia de audio se enruta al nuevo dispositivo. La aplicación debe almacenar en caché la posición del reloj para el cálculo de remapping y asegurarse de que los ejemplos de vídeo no se representen hasta que la secuencia de audio se vuelva a abrir en el nuevo dispositivo, de modo que cuando el clip reanude la representación, se sincronicen las secuencias de audio y vídeo. En algunos casos, cuando el tiempo de presentación para representar los fotogramas de vídeo se basa en el reloj de audio, es suficiente detener la secuencia de audio hasta que se complete el cambio de secuencia y no sea necesaria ninguna otra implementación de asignación de posición para la secuencia de vídeo para la sincronización de vídeo de audio.

Si durante la representación, [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) devuelve un error porque se pierde el dispositivo antiguo, la aplicación no necesita detener la secuencia anterior porque la operación de streaming ya ha finalizado. Para obtener información sobre cómo controlar este error, vea [Recuperación de un Invalid-Device error](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de MMDevice API](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



