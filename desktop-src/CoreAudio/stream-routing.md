---
description: El enrutamiento de secuencias es la capacidad de una aplicación multimedia para cambiar secuencias entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Enrutamiento de flujos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164786"
---
# <a name="stream-routing"></a>Enrutamiento de flujos

*El enrutamiento de* secuencias es la capacidad de una aplicación multimedia para cambiar secuencias entre dispositivos con una interrupción mínima en la reproducción o la sesión de captura.

Un equipo puede tener varios dispositivos de representación y captura. El sistema enumera estos dispositivos en el panel de control **Sonidos.** En esta lista, un usuario puede establecer un dispositivo para que sea el dispositivo predeterminado para cada rol: reproducción, grabación o los cuatro roles de comunicación (representación de la consola, captura de consola, representación de comunicación o captura de comunicación). La lista de dispositivos se puede modificar dinámicamente, ya que algunos de estos dispositivos pueden estar disponibles temporalmente, por ejemplo, un casco USB. Cuando hay varios dispositivos disponibles, el usuario puede cambiar el valor predeterminado a otro dispositivo. El usuario también puede cambiar el formato de un dispositivo (frecuencia de  muestreo, bits por muestra, entre otros) en la pestaña Opciones avanzadas de las propiedades del dispositivo.

Considere un escenario en el que un usuario selecciona **Altavoces** como dispositivo predeterminado para representar secuencias de audio. A continuación, el usuario conecta un casco USB, selecciona el casco como el nuevo dispositivo predeterminado y cambia la frecuencia de muestreo del dispositivo de 44,1 kHz a 48 kHz. El usuario quiere reproducir la secuencia de audio en el casco con la nueva frecuencia de muestreo con una interrupción mínima en la sesión de streaming.

En este escenario, hay dos casos que la aplicación multimedia debe controlar:

-   La secuencia debe transferirse al nuevo dispositivo predeterminado con una interrupción mínima de la reproducción.
-   El nuevo dispositivo debe reanudar la reproducción en el nuevo formato (es decir, el usuario puede cambiar más que la frecuencia de muestreo).

En Windows Vista, para admitir este escenario, la aplicación multimedia tenía que proporcionar la implementación para el enrutamiento de flujos. La aplicación era responsable de terminar las secuencias existentes y reiniciar las secuencias en el nuevo dispositivo. Si el usuario cambió el dispositivo predeterminado o su formato de combinación cambió, se cerraron todas las sesiones asociadas y la aplicación tuvo que controlar la recuperación.

En Windows 7, una aplicación puede transferir sin problemas una secuencia desde un dispositivo predeterminado existente a un nuevo punto de conexión de audio predeterminado. Los conjuntos de API de audio de alto nivel, Media Foundation, Direct Sound y WAVE API implementan la característica de enrutamiento de flujos. Las aplicaciones multimedia que usan estos conjuntos de API para reproducir o capturar una secuencia desde el dispositivo predeterminado usan la implementación predeterminada y no tendrán que modificar la aplicación. Sin embargo, si la aplicación multimedia usa MMDeviceAPI o WASAPI directamente, la aplicación debe proporcionar la implementación de enrutamiento de flujos.

> [!Note]  
> MMDeviceAPI y WASAPI son componentes de Core Audio API que una aplicación puede usar para representar o capturar una secuencia en un dispositivo. MMDeviceAPI detecta el nuevo dispositivo de punto de conexión de audio y WASAPI administra el flujo de datos de audio entre una aplicación multimedia y el dispositivo de punto de conexión de audio.

 

Para implementar la característica de enrutamiento de flujos, la aplicación debe escuchar las notificaciones enviadas por MMDeviceAPI y WASAPI cuando:

-   El usuario cambia el dispositivo predeterminado.
-   Se quita el dispositivo predeterminado existente y se agrega un nuevo dispositivo predeterminado.
-   Se cambia el formato del dispositivo.

Al controlar estas notificaciones, una aplicación puede realizar las operaciones de administración de flujos necesarias al transferir la secuencia al nuevo dispositivo predeterminado. Además, la aplicación puede representar o capturar secuencias existentes mediante el nuevo formato especificado por el usuario mientras una sesión de representación está activa.

Esta sección contiene los siguientes temas:

-   [Obtención del punto de conexión de dispositivo para el enrutamiento de flujos](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Notificaciones pertinentes para el enrutamiento de flujos](relevant-device-notifications-for-stream-routing.md)
-   [Consideraciones sobre la implementación del enrutamiento de flujos](stream-routing-implementation-considerations.md)

Los ejemplos siguientes, incluidos en el SDK de Windows, muestran cómo una aplicación puede controlar las notificaciones de enrutamiento de flujos.

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

[Acerca de MMDevice API](mmdevice-api.md)
</dt> <dt>

[Acerca de WASAPI](wasapi.md)
</dt> </dl>

 

 



