---
title: Uso de mensajes de ventana para administrar Waveform-Audio reproducción
description: Uso de mensajes de ventana para administrar Waveform-Audio reproducción
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- audio de forma de onda, administración de la reproducción con mensajes
- interfaz de audio de onda, administración de la reproducción con mensajes
- reproducir archivos de audio de forma de onda, administrar la reproducción con mensajes
- audio de forma de onda, mensajes
- interfaz de audio de forma de onda, mensajes
- reproducir archivos de audio de forma de onda, mensajes
- MM_WOM_CLOSE mensaje
- MM_WOM_DONE mensaje
- MM_WOM_OPEN mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31d8a88cb74953a1d38285a77b18ac25cd7495c3e29e71c5259551b5c2c3453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135890"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Uso de mensajes de ventana para administrar Waveform-Audio reproducción

Los mensajes siguientes se pueden enviar a una función de procedimiento de ventana para administrar la reproducción de audio de forma de onda.



| Message                                | Descripción                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) | Se envía cuando el dispositivo se cierra mediante la [**función waveOutClose.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)                                 |
| [**MM \_ WOM \_ DONE**](mm-wom-done.md)   | Se envía cuando el controlador de dispositivo finaliza con un bloque de datos enviado mediante la [**función waveOutWrite.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) |
| [**MM \_ WOM \_ OPEN**](mm-wom-open.md)   | Se envía cuando se abre el dispositivo mediante la [**función waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)                                   |



 

Un *parámetro wParam* *e lParam* está asociado a cada uno de estos mensajes. El *parámetro wParam* siempre especifica un identificador del dispositivo de audio de forma de onda abierto. Para el [**mensaje \_ MM WOM \_ DONE,**](mm-wom-done.md) *lParam* especifica un puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el bloque de datos completado. El *parámetro lParam* no se usa para los mensajes [**MM \_ WOM \_ CLOSE**](mm-wom-close.md) y [**MM \_ WOM \_ OPEN.**](mm-wom-open.md)

El mensaje más útil probablemente sea \_ MM WOM \_ DONE. Cuando este mensaje indica que se ha completado la reproducción de un bloque de datos, puede limpiar y liberar el bloque de datos. A menos que necesite asignar memoria o inicializar variables, probablemente no necesite procesar los mensajes MM WOM OPEN y \_ \_ MM \_ WOM \_ CLOSE.

La aplicación proporciona la función de devolución de llamada para dispositivos de salida de audio de forma de onda. Para obtener información sobre esta función de devolución de llamada, vea [**la función waveOutProc.**](/previous-versions//dd743869(v=vs.85))

 

 