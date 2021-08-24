---
description: Experiencia de afición predeterminada
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiencia de afición predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec323bdaf01a7bba0821a9dee2c349239b3a53660334d2ac57edbf71287f396d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695025"
---
# <a name="default-ducking-experience"></a>Experiencia de afición predeterminada

Considere un escenario en el que un usuario recibe una llamada telefónica mientras escucha música en el equipo. Durante la llamada telefónica, el usuario quiere reducir el nivel de volumen de la música mientras asiste a la llamada de teléfono y reanudar el volumen original una vez finalizada la llamada telefónica. En función de las opciones especificadas por el usuario en el panel  de  **control** Sonidos, el sistema operativo proporciona automáticamente esta funcionalidad a través de la atenuación de secuencias o de agresiones, lo que reduce la intensidad de una secuencia de audio.

La experiencia de atenuación predeterminada depende de la preferencia del usuario, como se especifica en la opción Sonido del panel **de** control. En la **pestaña** Comunicaciones, el usuario puede elegir un nivel de atenuación (el valor predeterminado es 80%), silenciar todos los flujos que no son de comunicación o deshabilitar la experiencia de atenuación de secuencia predeterminada. El sistema permite abrir nuevas secuencias que no son de comunicación (excepto los sonidos del sistema nuevos) durante la sesión de comunicación, pero las nuevas secuencias no se atenuan automáticamente. Cuando se cierran todos los flujos de comunicación, el sistema finaliza la sesión de comunicación y restaura el volumen de las secuencias que se atenuaron durante la sesión de comunicación.

Para indicar visualmente la atenuación de secuencias, el sistema cambia la configuración del mezclador de volumen en función de las preferencias del usuario. Por ejemplo, si el usuario especifica un nivel de atenuación, el mezclador de volumen reduce el control deslizante, muestra el nuevo volumen atenuado y muestra el nivel de volumen original. En la imagen siguiente se muestra este proceso.

![diagrama del comportamiento de atenuación de flujo predeterminado proporcionado en Windows 7](images/stream-aatenuation.jpg)

Una aplicación puede invalidar la atenuación de secuencias e implementar una experiencia de afijo personalizada si sabe cuándo se inicia y finaliza la sesión de comunicación. Para obtener más información, vea [Proporcionar un comportamiento de afijo personalizado.](providing-a-custom-ducking-experience.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Deshabilitación de la experiencia de afición predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento de afijo personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para notificaciones de afijo](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtención de eventos de afición](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



