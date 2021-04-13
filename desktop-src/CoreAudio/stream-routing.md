---
description: El enrutamiento de flujos es la capacidad de una aplicación multimedia para cambiar de flujo entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496349"
---
# <a name="stream-routing"></a>Enrutamiento de flujos

El *enrutamiento de flujos* es la capacidad de una aplicación multimedia para cambiar de flujo entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.

Un equipo puede tener varios dispositivos de representación y captura. El sistema muestra estos dispositivos en el panel de control **sonidos** . En esta lista, un usuario puede establecer que un dispositivo sea el dispositivo predeterminado para cada rol: reproducción, grabación o los cuatro roles de comunicaciones (representación de la consola, captura de la consola, representación de la comunicación o captura de comunicación). La lista de dispositivos se puede modificar de forma dinámica, ya que algunos de estos dispositivos pueden estar disponibles temporalmente, por ejemplo, un casco USB. Cuando hay varios dispositivos disponibles, el usuario puede cambiar el valor predeterminado a otro dispositivo. El usuario también puede cambiar el formato de un dispositivo (velocidad de muestreo, bits por muestra, etc.) en la pestaña **Opciones avanzadas** de las propiedades del dispositivo.

Considere un escenario en el que un usuario selecciona los **oradores** como el dispositivo predeterminado para representar secuencias de audio. Después, el usuario conecta un auricular USB, selecciona el casco como nuevo dispositivo predeterminado y cambia la velocidad de muestra del dispositivo de 44,1 kHz a 48 kHz. El usuario desea reproducir la secuencia de audio del casco con la nueva velocidad de muestra con una interrupción mínima en la sesión de streaming.

En este escenario, hay dos casos en los que la aplicación multimedia debe controlar:

-   La secuencia se debe transferir al nuevo dispositivo predeterminado con una interrupción mínima para la reproducción.
-   El nuevo dispositivo debe reanudar la reproducción en el nuevo formato (es decir, el usuario puede cambiar más de la frecuencia de muestreo).

En Windows Vista, para admitir este escenario, la aplicación multimedia tenía que proporcionar la implementación para el enrutamiento de flujo. La aplicación era responsable de terminar los flujos existentes y reiniciar las secuencias en el nuevo dispositivo. Si el usuario cambió el dispositivo predeterminado o su formato de combinación cambió, se cerrarán todas las sesiones asociadas y la aplicación tenía que administrar la recuperación.

En Windows 7, una aplicación puede transferir sin problemas un flujo desde un dispositivo predeterminado existente a un nuevo punto de conexión de audio predeterminado. Los conjuntos de API de audio de alto nivel como Media Foundation, DirectSound y las API de WAVE implementan la característica de enrutamiento de flujo. Las aplicaciones multimedia que usan estos conjuntos de API para reproducir o capturar una secuencia desde el dispositivo predeterminado usan la implementación predeterminada y no tendrán que modificar la aplicación. Sin embargo, si la aplicación multimedia usa MMDeviceAPI o WASAPI directamente, la aplicación debe proporcionar la implementación de enrutamiento de flujo.

> [!Note]  
> MMDeviceAPI y WASAPI son componentes principales de la API de audio que una aplicación puede usar para representar o capturar un flujo en un dispositivo. El MMDeviceAPI detecta el nuevo dispositivo de punto de conexión de audio y WASAPI administra el flujo de datos de audio entre una aplicación multimedia y el dispositivo de punto de conexión de audio.

 

Para implementar la característica de enrutamiento de flujo, la aplicación debe escuchar las notificaciones enviadas por MMDeviceAPI y WASAPI cuando:

-   El usuario cambia el dispositivo predeterminado.
-   Se quita el dispositivo predeterminado existente y se agrega un nuevo dispositivo predeterminado.
-   Se cambia el formato del dispositivo.

Al controlar estas notificaciones, una aplicación puede realizar las operaciones necesarias de administración de transmisiones mientras se transfiere el flujo al nuevo dispositivo predeterminado. Además, la aplicación puede representar o capturar las secuencias existentes utilizando el nuevo formato especificado por el usuario mientras una sesión de representación está activa.

Esta sección contiene los siguientes temas:

-   [Obtención del punto de conexión del dispositivo para el enrutamiento de flujo](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notificaciones relevantes para el enrutamiento de flujos](relevant-device-notifications-for-stream-routing.md)
-   [Consideraciones de implementación de enrutamiento de flujo](stream-routing-implementation-considerations.md)

En los siguientes ejemplos, incluidos en el Windows SDK, se muestra cómo una aplicación puede controlar las notificaciones de enrutamiento de flujo.

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de flujos](stream-management.md)
</dt> <dt>

[Acerca de la API de MMDevice](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> </dl>

 

 



