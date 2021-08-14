---
title: Recepción de Running-Status mensajes
description: Recepción de Running-Status mensajes
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Interfaz digital instrumentable (MIDI), estado de ejecución
- MIDI (Interfaz digital instrumentable), estado de ejecución
- grabación de audio MIDI, estado de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4d782e1e25c718ddd177d1d9baf471d0715d70680b65920052e85d6fffc551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371350"
---
# <a name="receiving-running-status-messages"></a>Recepción de Running-Status mensajes

La *especificación Standard MIDI Files 1.0* permite usar el estado de ejecución cuando un mensaje tiene el mismo byte de estado que el mensaje anterior.  Cuando se usa el estado de ejecución, se puede omitir el byte de estado de los mensajes posteriores. Todos los controladores de dispositivos de entrada DE LÍNEA son necesarios para expandir los mensajes que usan el estado de ejecución en mensajes completos, de modo que siempre reciba mensajes COMPLETOs de UN controlador de dispositivo de entrada DE LÍNEA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




