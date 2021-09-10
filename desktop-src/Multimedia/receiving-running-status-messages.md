---
title: Recepción de Running-Status mensajes
description: Recepción de Running-Status mensajes
ms.assetid: 4f2e8e41-89f6-45e3-ae16-47b856f0e63e
keywords:
- Interfaz digital instrumentable (MIDI), estado de ejecución
- MIDI (Interfaz digital instrumenta de música), estado de ejecución
- grabación de audio MIDI, estado de ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4d12a19f525a6fa673747063774bf4507d65b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370921"
---
# <a name="receiving-running-status-messages"></a>Recepción de Running-Status mensajes

La *especificación Standard MIDI Files 1.0* permite usar el estado de ejecución cuando un mensaje tiene el mismo byte de estado que el mensaje anterior.  Cuando se usa el estado de ejecución, se puede omitir el byte de estado de los mensajes posteriores. Todos los controladores de dispositivos de entrada DE LÍNEA son necesarios para expandir los mensajes que usan el estado de ejecución en mensajes completos, de modo que siempre reciba mensajes COMPLETOs de UN CONTROLADOR DE DISPOSITIVO DE ENTRADA DE LÍNEA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 




