---
title: Uso de mensajes de ventana para administrar Waveform-Audio grabación
description: Uso de mensajes de ventana para administrar Waveform-Audio grabación
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio de forma de onda, administración de la grabación con mensajes
- interfaz de audio de onda, administración de la grabación con mensajes
- grabación de audio de forma de onda, administración de la grabación con mensajes
- audio de forma de onda, mensajes
- interfaz de audio de forma de onda, mensajes
- grabación de audio de forma de onda, mensajes
- MM_WIM_CLOSE mensaje
- MM_WIM_DATA mensaje
- MM_WIM_OPEN mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135657"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Uso de mensajes de ventana para administrar Waveform-Audio grabación

Los mensajes siguientes se pueden enviar a una función de procedimiento de ventana para administrar la grabación de audio de forma de onda.



| Message                                | Descripción                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WIM \_ CLOSE**](mm-wim-close.md) | Se envía cuando el dispositivo se cierra mediante la [**función waveInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)                                     |
| [**MM \_ WIM \_ DATA**](mm-wim-data.md)   | Se envía cuando el controlador de dispositivo finaliza con un búfer enviado mediante la [**función waveInAddBuffer.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) |
| [**MM \_ WIM \_ OPEN**](mm-wim-open.md)   | Se envía cuando se abre el dispositivo mediante la [**función waveInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)                                       |



 

El *parámetro lParam* de [**MM \_ WIM \_ DATA**](mm-wim-data.md) especifica un puntero a una [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer. Es posible que este búfer no se llene completamente con datos de audio de forma de onda; La grabación puede detenerse antes de que se llene el búfer. Use el **miembro dwBytesRecorded de** la estructura **WAVEHDR** para determinar la cantidad de datos válidos presentes en el búfer.

El mensaje más útil es probablemente [**MM \_ WIM \_ DATA**](mm-wim-data.md). Cuando la aplicación termine de usar el bloque de datos enviado por el controlador de dispositivo, puede limpiar y liberar el bloque de datos. A menos que necesite asignar memoria o inicializar variables, probablemente no necesite usar los mensajes [**\_ MM WIM \_ OPEN**](mm-wim-open.md) y [**MM \_ WIM \_ CLOSE.**](mm-wim-close.md)

La aplicación proporciona la función de devolución de llamada para dispositivos de entrada de audio de forma de onda. Para obtener información sobre esta función de devolución de llamada, vea [**la función waveInProc.**](/previous-versions//dd743849(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 