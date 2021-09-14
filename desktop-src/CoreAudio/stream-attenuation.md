---
description: Experiencia de agachamiento predeterminada
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiencia de agachamiento predeterminada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164793"
---
# <a name="default-ducking-experience"></a>Experiencia de agachamiento predeterminada

Considere un escenario en el que un usuario recibe una llamada telefónica mientras escucha música en el equipo. Durante la llamada telefónica, el usuario quiere reducir el nivel de volumen de la música mientras asiste a la llamada telefónica y reanudar el volumen original una vez finalizada la llamada telefónica. En función de las opciones especificadas por el usuario en el panel  de  **control** Sonidos, el sistema operativo proporciona automáticamente esta funcionalidad a través del achacamiento o atenuación del flujo, lo que reduce la intensidad de una secuencia de audio.

La experiencia de atenuación predeterminada depende de las preferencias del usuario, como se especifica en la opción Sonido del panel **de** control. En la **pestaña** Comunicaciones, el usuario puede elegir un nivel de atenuación (el valor predeterminado es 80 %), silenciar todos los flujos que no son de comunicación o deshabilitar la experiencia de atenuación de secuencia predeterminada. El sistema permite abrir nuevas secuencias que no son de comunicación (excepto los sonidos del sistema nuevos) durante la sesión de comunicación, pero las nuevas secuencias no se atenuan automáticamente. Cuando se cierran todos los flujos de comunicación, el sistema finaliza la sesión de comunicación y restaura el volumen de las secuencias atenuadas durante la sesión de comunicación.

Para indicar visualmente la atenuación de secuencias, el sistema cambia la configuración del mezclador de volúmenes en función de las preferencias del usuario. Por ejemplo, si el usuario especifica un nivel de atenuación, el mezclador de volúmenes reduce el control deslizante, muestra el nuevo volumen atenuado y muestra el nivel de volumen original. En la imagen siguiente se muestra este proceso.

![diagrama del comportamiento de atenuación de flujo predeterminado proporcionado en Windows 7](images/stream-aatenuation.jpg)

Una aplicación puede invalidar la atenuación de flujos e implementar una experiencia de agachamiento personalizada si sabe cuándo comienza y finaliza la sesión de comunicación. Para obtener más información, [vea Proporcionar un comportamiento de agachamiento personalizado.](providing-a-custom-ducking-experience.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de un dispositivo de comunicación](using-the-communication-device.md)
</dt> <dt>

[Deshabilitación de la experiencia de agachamiento predeterminada](disabling-the-ducking-experience.md)
</dt> <dt>

[Proporcionar un comportamiento de agachamiento personalizado](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Consideraciones de implementación para las notificaciones de achacamiento](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtener eventos de agachamiento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



