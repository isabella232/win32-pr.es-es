---
description: En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales, como las API de Media Foundation, DirectSound y Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de secuencia desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado.
ms.assetid: ecda0b5b-6583-43b4-a9b4-f12a95f09452
title: Consideraciones de implementación de enrutamiento de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27dc1f7e3fe56d6b421ca59f528ab1a65d2261a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000637"
---
# <a name="stream-routing-implementation-considerations"></a>Consideraciones de implementación de enrutamiento de flujo

En Windows 7, las API de plataforma de alto nivel que usan las API de audio principales, como las API de Media Foundation, DirectSound y Wave, implementan la característica de enrutamiento de flujo mediante la administración del cambio de secuencia desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Las aplicaciones multimedia que usan estas API usan el comportamiento de enrutamiento de flujo sin modificaciones en el origen. Los clientes de WASAPI directos pueden usar las notificaciones enviadas por componentes de audio principales e implementar la característica de enrutamiento de flujo.

Los clientes de WASAPI directos (aplicaciones multimedia que usan WASAPI directamente) reciben nuevas notificaciones de sesión de dispositivo y audio enviadas por componentes de audio principales. El comportamiento de la característica de enrutamiento de flujo se define en el modo en que la aplicación controla estas notificaciones.

La API de MMDevice y la sesión de audio envían notificaciones sobre los cambios de estado de dispositivo y los cambios de sesión a los clientes de WASAPI en forma de devoluciones de llamada. Para obtener estas notificaciones, el cliente debe registrar su implementación de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents). Para obtener más información, consulte [notificaciones relevantes para el enrutamiento de flujos](relevant-device-notifications-for-stream-routing.md).

En el escenario de auriculares USB descrito en [enrutamiento de transmisión](stream-routing.md), una aplicación está reproduciendo una secuencia de audio y usa MMDEVICEAPI y WASAPI para representar la secuencia en el dispositivo de representación predeterminado, **Speaker**. Cuando se cambia el dispositivo predeterminado, la aplicación recibe una notificación de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) . La aplicación también recibe notificaciones de [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) que indican que el usuario ha quitado el dispositivo de punto de conexión de audio o que el formato de secuencia ha cambiado para el dispositivo al que está conectada la sesión de audio. Después de recibir las notificaciones, la aplicación detiene el streaming al extremo del orador y vuelve a abrir la secuencia para la representación en el punto de conexión predeterminado actual, los auriculares.

![diagrama del flujo de datos para las notificaciones de dispositivo.](images/stream-routing.gif)

En respuesta a estas notificaciones, es posible que el cliente vuelva a abrir la secuencia en el nuevo dispositivo predeterminado en el nuevo formato seleccionado por el usuario.

## <a name="stream-managment"></a>Administración de flujos

En la lista siguiente se resumen los pasos que debe realizar un cliente de WASAPI para proporcionar la funcionalidad de cambio de secuencia.

1.  Espere a la notificación de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) pertinente. Si el dispositivo es el dispositivo predeterminado, se recibe la notificación [**IMMNotificationClient:: OnDefaultDeviceChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondefaultdevicechanged) .
2.  Si hay un nuevo dispositivo disponible, obtenga una referencia al punto de conexión del nuevo dispositivo. Llame a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para el nuevo dispositivo predeterminado. Si el dispositivo nuevo no es el predeterminado, puede recuperar el dispositivo mediante una llamada a [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice). Para obtener más información, consulte [obtención del punto de conexión del dispositivo para el enrutamiento de transmisiones](getting-the-default-device-endpoint-for-stream-routing.md).
3.  Espere a [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) con el valor de razón.
    > [!Note]  
    > Dado que todas estas operaciones son asincrónicas, no se puede predecir el orden en el que la aplicación recibe notificaciones de cambio de dispositivo y de desconexión de sesión. La aplicación debe implementar el control de notificaciones para recibir estas notificaciones en cualquier orden. Sin embargo, normalmente, la aplicación recibe el valor **AudioSessionDisconnect** antes de la notificación de cambio de dispositivo predeterminada.

     

4.  Evalúe el valor del motivo y determine si es necesario transferir el flujo a otro punto de conexión de audio o si es necesario reinicializar el flujo con un nuevo formato.
5.  Detenga el streaming al dispositivo predeterminado anterior si el motivo indica que el flujo se debe volver a enrutar al nuevo dispositivo predeterminado.
6.  Realizar cálculos de asignación de posición.
7.  Abra la secuencia en el nuevo dispositivo y transfiera toda la información de estado.
8.  Reanude el streaming en el nuevo dispositivo predeterminado.
9.  Controlar la salida del dispositivo predeterminado anterior.

Para que la operación de cambio de flujo parezca perfecta, debe realizarse lo más rápido posible. Esto depende del rendimiento de los componentes implicados en el reinicio de la secuencia en el nuevo dispositivo.

## <a name="position-mapping-considerations"></a>Consideraciones sobre la asignación de posiciones

Cuando la aplicación obtiene notificaciones de [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) y [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) , puede enrutar los flujos existentes al nuevo dispositivo predeterminado. Cuando una secuencia de audio existente se interrumpe y se abre en el nuevo dispositivo, la representación en el nuevo dispositivo debe comenzar en la posición en la que se detuvo la secuencia en el dispositivo antiguo. Para ello, la aplicación debe tener la última posición de dispositivo conocida, para calcular la posición de inicio en el nuevo dispositivo. Por ejemplo, esta posición se puede usar como desplazamiento Delta para la asignación de posición subsiguiente. Cuando el flujo comienza a representarse, la nueva posición del dispositivo se puede reasignar a la posición del dispositivo almacenado en memoria caché.

En los pasos siguientes se resume el proceso de realizar una transición de flujo sin problemas.

1.  Almacenar en caché la última posición del dispositivo de la secuencia en el dispositivo antiguo.
2.  Detenga el flujo en el dispositivo antiguo.
3.  Realizar cálculos de reasignación para obtener la nueva posición.
4.  Empiece a representar la secuencia en el nuevo dispositivo.
5.  Libere el flujo anterior.

Durante la transición, la aplicación debe asegurarse de que el reloj no se queda sin sincronización, lo que da lugar a secuencias de audio y vídeo que no están sincronizadas. Esto puede ocurrir si los ejemplos de vídeo continúan representando mientras la secuencia de audio se enruta al nuevo dispositivo. La aplicación debe almacenar en caché la posición del reloj para el cálculo de reasignación y asegurarse de que los ejemplos de vídeo no se representen hasta que la secuencia de audio se vuelva a abrir en el nuevo dispositivo, de modo que cuando el clip reanude la representación, se sincronicen las secuencias de audio y de vídeo. En algunos casos, en los que el tiempo de presentación para representar los fotogramas de vídeo se basa en el reloj de audio, es suficiente detener la secuencia de audio hasta que se complete la conmutación de la secuencia y no sea necesaria ninguna otra implementación de asignación de posición para la secuencia de vídeo para la sincronización de vídeo de audio.

Si durante la representación, [**IAudioRenderClient:: getBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) devuelve un error porque se pierde el dispositivo anterior, la aplicación no necesita detener la secuencia antigua porque la operación de streaming ya finalizó. Para obtener información acerca de cómo controlar este error, consulte [recuperación de un error de Invalid-Device](recovering-from-an-invalid-device-error.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de MMDevice](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> <dt>

[Enrutamiento de flujos](stream-routing.md)
</dt> </dl>

 

 



