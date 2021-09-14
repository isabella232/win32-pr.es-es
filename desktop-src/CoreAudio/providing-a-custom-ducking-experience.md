---
description: Una aplicación puede no participar en la experiencia de aplazamiento predeterminada que controla el sistema y reemplazarla por una implementación personalizada.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Proporcionar un comportamiento de agachamiento personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164857"
---
# <a name="providing-a-custom-ducking-behavior"></a>Proporcionar un comportamiento de agachamiento personalizado

Una aplicación puede no participar en la [experiencia de aplazamiento](stream-attenuation.md) predeterminada que controla el sistema y reemplazarla por una implementación personalizada.

Una aplicación puede proporcionar una experiencia de agachamiento personalizada. Por ejemplo, Reproductor de Windows Media proporciona su propia experiencia de agachamiento mediante la pausa del flujo multimedia actual durante una sesión de comunicación y la reanudación de la reproducción cuando se cierra la sesión. Se incluye una aplicación multimedia de ejemplo que implementa el agachamiento con Windows ejemplos del SDK. Para obtener más información, vea [DuckingMediaPlayer](duckingmediaplayer.md). Para simular la experiencia de apertura y cierre de flujos de comunicación y la generación de eventos de afijo, consulte [DuckingCaptureSample](duckingcapturesample.md), que también se incluye con ejemplos de SDK Windows.

Una aplicación multimedia que reproduce sonidos que se atenuarán debe tener en cuenta los flujos de comunicación cuando se abren y cierran en el sistema. La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o DirectSound, que usan las API de audio principal. Un cliente WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

**Para proporcionar una experiencia de agachamiento personalizada, un cliente WASAPI debe realizar las siguientes tareas:**

1.  Regístrese para recibir eventos de agachamiento del administrador *de* agachas, un componente del sistema de audio que controla las notificaciones relacionadas con los cambios de flujo de comunicación. Para obtener más información, [consulte Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Si el cliente se registra para recibir notificaciones de agachamiento, el administrador de agachamiento deshabilita el comportamiento predeterminado proporcionado por el sistema. Si el comportamiento predeterminado está deshabilitado de forma explícita (consulte [Deshabilitación](disabling-the-ducking-experience.md)de la experiencia predeterminada de agachamiento) y el cliente no proporciona un comportamiento de sustitución, la aplicación no experimenta ningún comportamiento de achacamiento.

     

2.  Escuche las notificaciones de eventos de patito enviadas por el administrador de agachas y realice el comportamiento de agacha deseado. Para obtener más información sobre cómo implementar un comportamiento de agachamiento, vea [Consideraciones de implementación para las notificaciones de agachamiento.](handling-audio-ducking-events-from-communication-devices.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Experiencia de agachamiento predeterminada](stream-attenuation.md)
</dt> <dt>

[Deshabilitación de la experiencia de agachamiento predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de achacamiento](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtener eventos de agachamiento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



