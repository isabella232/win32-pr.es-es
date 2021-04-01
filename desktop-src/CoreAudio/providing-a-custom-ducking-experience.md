---
description: Una aplicación puede optar por no participar en la experiencia de carga predeterminada que controla el sistema y reemplazarla por una implementación personalizada.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Proporcionar un comportamiento personalizado de patos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153400"
---
# <a name="providing-a-custom-ducking-behavior"></a>Proporcionar un comportamiento personalizado de patos

Una aplicación puede optar por no participar en la experiencia de carga [predeterminada](stream-attenuation.md) que controla el sistema y reemplazarla por una implementación personalizada.

Una aplicación puede proporcionar una experiencia personalizada de patos. Por ejemplo, Windows Media Player proporciona su propia experiencia de pato al pausar el flujo multimedia actual durante una sesión de comunicación y reanudar la reproducción cuando se cierra la sesión. Con Windows SDK ejemplos se incluye una aplicación multimedia de ejemplo que implementa la pato. para obtener más información, vea [DuckingMediaPlayer](duckingmediaplayer.md). Para simular la experiencia de apertura y cierre de secuencias de comunicación y la generación de eventos de patos, vea [DuckingCaptureSample](duckingcapturesample.md), que también se incluye con Windows SDK ejemplos.

Una aplicación multimedia que reproduzca sonidos que se atenuarán debe ser consciente de las secuencias de comunicación, cuando se abren y cierran en el sistema. La implementación personalizada se puede proporcionar mediante MediaFoundation, DirectShow o DirectSound, que usan las API de audio principales. Un cliente de WASAPI directo también puede invalidar el control predeterminado si sabe cuándo se inicia y finaliza la sesión de comunicación.

**Para proporcionar una experiencia de patos personalizada, un cliente de WASAPI debe realizar las siguientes tareas:**

1.  Regístrese para recibir eventos de patos del *Administrador de patos*, un componente del sistema de audio que controla las notificaciones relacionadas con los cambios en el flujo de comunicación. Para obtener más información, [obtenga eventos](handling-audio-ducking-events-from-communication-devices.md)de perdedor.
    > [!Note]  
    > Si el cliente se registra para recibir notificaciones de patos, el administrador de patos deshabilita el comportamiento predeterminado proporcionado por el sistema. Si el comportamiento predeterminado está deshabilitado explícitamente (consulte [deshabilitación de la experiencia predeterminada de la](disabling-the-ducking-experience.md)misma) y el cliente no proporciona un comportamiento de sustitución, la aplicación no experimenta ningún comportamiento de perdedor.

     

2.  Escuche las notificaciones de eventos de pato enviadas por el administrador de patos y realice el comportamiento deseado. Para obtener más información sobre la implementación de un comportamiento de patos, consulte [consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Experiencia predeterminada de los patos](stream-attenuation.md)
</dt> <dt>

[Deshabilitación de la experiencia de patos predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtención de eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



