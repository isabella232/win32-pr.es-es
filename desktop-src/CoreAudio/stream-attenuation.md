---
description: Experiencia predeterminada de los patos
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiencia predeterminada de los patos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807549"
---
# <a name="default-ducking-experience"></a>Experiencia predeterminada de los patos

Considere un escenario en el que un usuario recibe una llamada telefónica mientras escucha música en el equipo. Durante la llamada de teléfono, el usuario desea reducir el nivel de volumen de la música mientras asiste a la llamada de teléfono y reanudar el volumen original una vez finalizada la llamada telefónica. En función de las opciones especificadas por el usuario en el panel de control **sonidos** , el sistema operativo proporciona automáticamente esta *funcionalidad a través* de la función de la pérdida de la *secuencia* o la reducción de la intensidad de una secuencia de audio.

La experiencia de atenuación predeterminada depende de las preferencias del usuario, tal y como se especifica en la opción de **sonido** del panel de control. En la pestaña **comunicaciones** , el usuario puede elegir un nivel de atenuación (el valor predeterminado es 80%), silenciar todas las secuencias que no son de comunicación o deshabilitar la experiencia de atenuación de flujo predeterminada. El sistema permite que se abran nuevas secuencias no de comunicación (excepto para nuevos sonidos del sistema) durante la sesión de comunicación, pero las nuevas secuencias no se atenúan automáticamente. Cuando se cierran todas las secuencias de comunicación, el sistema finaliza la sesión de comunicación y restaura el volumen de las secuencias que se atenuaron durante la sesión de comunicación.

Para indicar la atenuación de la secuencia visualmente, el sistema cambia la configuración del mezclador de volumen en función de las preferencias del usuario. Por ejemplo, si el usuario especifica un nivel de atenuación, el mezclador de volumen baja el control deslizante, muestra el nuevo volumen atenuado y muestra el nivel de volumen original. En la imagen siguiente se ilustra este proceso.

![diagrama del comportamiento de atenuación de secuencias predeterminado proporcionado en Windows 7](images/stream-aatenuation.jpg)

Una aplicación puede invalidar la atenuación de flujos e implementar una experiencia personalizada de pato si sabe cuándo se inicia y finaliza la sesión de comunicación. Para obtener más información, vea [proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Deshabilitación de la experiencia de patos predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento personalizado de patos](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de patos](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtención de eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



